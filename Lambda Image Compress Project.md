# Project : Image Compress Using Lambda Function with S3 Event Trigger

***Create a Layer***
![307](https://github.com/user-attachments/assets/51773a28-83f9-43fb-a268-f297e423df29)
![308](https://github.com/user-attachments/assets/5ec10ca1-3785-4a08-8be2-e921d1aefedc)

## Execute these commands:
```
mkdir -p lambda-layer/python/lib/python3.12/site-packages
```
```
pip install requests numpy -t lambda-layer/python/lib/python3.12/site-packages
```
```
cd lambda-layer/
```
```
zip -r python.zip python/
```
```
ls
```

***Create a Bucket***
![309](https://github.com/user-attachments/assets/2a995598-81bf-41b4-95f9-08a555c615c2)

***Create input & output object folder***
![312](https://github.com/user-attachments/assets/b9dd1ae6-73be-4068-92a5-b0c3702a963d)

***Create a IAM Role***
![313](https://github.com/user-attachments/assets/4b4e2703-da26-4826-8d4d-fe69d233e15a)

***Create a Function***
![314](https://github.com/user-attachments/assets/c6f49cba-cb15-49d4-88f4-58baa821ba49)
![315](https://github.com/user-attachments/assets/7de0358a-fe24-4fd8-b648-459b28a16e50)

***Add a Layer**
![316](https://github.com/user-attachments/assets/ed59dbeb-9003-4d3a-be67-1173ebaf6b20)
![317](https://github.com/user-attachments/assets/4f8f98c5-a82e-4460-be4d-035fc78287de)

***Write a python code for image compression and deploy then create event for test*** 
![319](https://github.com/user-attachments/assets/6ff74af6-06dc-48b7-940d-063e3bc6f42e)

## Lambda Function Code
**Here's the complete Lambda function code:**

```
import boto3
import os
from PIL import Image
import io
import urllib.parse

# Initialize the S3 client
s3 = boto3.client('s3')

# Get environment variables for output prefix and compression quality
output_prefix = os.environ.get('OUTPUT_PREFIX', 'output/')
quality = int(os.environ.get('QUALITY', 75))  # Compression quality (0-100)

def lambda_handler(event, context):
    # Process each file upload event individually
    for record in event['Records']:
        # Extract bucket name and object key (file path)
        bucket = record['s3']['bucket']['name']
        key = urllib.parse.unquote_plus(record['s3']['object']['key'])

        # Only process supported image types
        if not key.lower().endswith(('.jpg', '.jpeg', '.png')):
            print(f"Incorrect image format: {key}")
            return {
                'statusCode': 400,
                'body': 'Incorrect image format'
            }

        try:
            # Download the image file from S3
            response = s3.get_object(Bucket=bucket, Key=key)
            image_data = response['Body'].read()

            # Open the image using Pillow
            img = Image.open(io.BytesIO(image_data))

            # Prepare an in-memory buffer to hold the compressed image
            compressed_io = io.BytesIO()

            # Save the image to buffer with compression (JPEG format)
            img.save(compressed_io, format='JPEG', optimize=True, quality=quality)
            compressed_io.seek(0)  # Reset buffer pointer to the beginning

            # Build the output file key (path), changing folder and file name
            output_key = key.replace("input/", output_prefix, 1).rsplit('.', 1)[0] + "_compressed.jpg"

            # Upload the compressed image back to S3 in the output/ directory
            s3.put_object(
                Bucket=bucket,
                Key=output_key,
                Body=compressed_io,
                ContentType='image/jpeg'
            )

            print(f"Compressed image saved to: {output_key}")
            return {
                'statusCode': 200,
                'body': f'Successfully compressed and saved to {output_key}'
            }

        except Exception as e:
            print(f"Error processing image {key}: {str(e)}")
            return {
                'statusCode': 500,
                'body': f'Error processing image: {str(e)}'
            }
```

***Go to Confifuration Section and encrease Timeout***
![320](https://github.com/user-attachments/assets/fde383b7-7266-4036-9508-290122f3fd3d)
![321](https://github.com/user-attachments/assets/508ca45f-ab9f-4b19-98fa-be77e3f833d9)

***Add Environment Variables for code***
![322](https://github.com/user-attachments/assets/10a784d5-0c92-48a7-9421-31d4b07c34de)
![323](https://github.com/user-attachments/assets/b3415068-4dcc-4fea-aeb4-af4a9460cb0f)

***Add Trigger : S3 Bucket***
![326](https://github.com/user-attachments/assets/e021535b-0ccb-4f26-aedc-085f0350b0f0)

***Upload a image in input folder***
![331](https://github.com/user-attachments/assets/0ab7042d-c44b-42fe-bed1-b43bca64bc52)

***See the Compress image in output folder***
![333](https://github.com/user-attachments/assets/d2a95550-f507-4a29-b8b9-6232c33c0a9d)
