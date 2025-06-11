# Lambda Function

## S3 Trigger

***Go to Lambda Service***
![261](https://github.com/user-attachments/assets/e7b0fb66-0c49-418c-81b7-b36b9bc365d7)

***Create a Fuction***
![262](https://github.com/user-attachments/assets/13246008-762b-4764-a52c-e3afa9a00fea)
![263](https://github.com/user-attachments/assets/bda80f65-ac2e-45d6-b8c2-b5a8d971c92b)

***Create a Role for Lambda***
![265](https://github.com/user-attachments/assets/205b94dd-ed90-41c9-8a80-b731df734ef5)
![266](https://github.com/user-attachments/assets/24bb9a8e-d118-4173-9666-32c16457536a)
![267](https://github.com/user-attachments/assets/1336d944-cdec-42c6-931d-e5eb981f105f)
![268](https://github.com/user-attachments/assets/84b7d69c-c490-487b-8929-f2fb6cbacb68)
![269](https://github.com/user-attachments/assets/1bdbb8c9-37dc-4387-b4d4-223241c6fec8)
![271](https://github.com/user-attachments/assets/038d8024-2823-49a7-b51d-d97614402ab8)

***Select a Role***
![272](https://github.com/user-attachments/assets/db5cd9b9-5228-4279-a29e-26af3ae873c6)

***Go to Code Section***
![273](https://github.com/user-attachments/assets/a07e50ee-5b3f-4e5c-93d0-a481e50b4132)

***Type a Code and Deploy, after create a event test the code & See the Output***
![274](https://github.com/user-attachments/assets/5f08ea6a-4f19-4c30-82b4-fd1244c2d8c0)

***Add S3 Trigeer***
![275](https://github.com/user-attachments/assets/82f8d9da-e67e-4fef-b6ae-3492136a14b8)
![276](https://github.com/user-attachments/assets/aa7872b1-b480-4d96-8a00-f70be7fd95c3)
![278](https://github.com/user-attachments/assets/22bcacd9-cb8a-4ec3-a430-f6999c6c9991)
![279](https://github.com/user-attachments/assets/d9babccb-6d94-4d3a-8d5f-d94f6404018d)

***Type a Code For S3 object Trigger & Deploy***
![280](https://github.com/user-attachments/assets/f2b2d321-37af-43bc-be3c-e8254d8141d5)

****Upload one object in Bucket & Go CloudWatch Logs***
![281](https://github.com/user-attachments/assets/4509aacf-3aec-4ca7-89ca-b112da80ab34)

***Select Logs***
![282](https://github.com/user-attachments/assets/dac715e9-9f15-4836-96ef-682edffc69ad)

***See The Logs for uploaded object***
![283](https://github.com/user-attachments/assets/a397c9ff-de64-4932-bfe1-c173441c797b)


## Print the text data in logs to my .txt object

***edit the code***
![285](https://github.com/user-attachments/assets/ffe59626-f528-4f61-aae7-20070879024a)

**Code**
```
import json
import boto3

def lambda_handler(event, context):
    s3 = boto3.client("s3")
    print(event)

    if event:
        file_obj = event['Records'][0]
        bucket_name = str(file_obj['s3']['bucket']['name'])
        filename = str(file_obj['s3']['object']['key'])
        
        print('Filename: ' + filename)

        file_object = s3.get_object(Bucket=bucket_name, Key=filename)
        file_content = file_object['Body'].read().decode('utf-8')

        print(file_content)

        print("sharadpatelwdn@gmail.com")

    # TODO implement    
    return {
        'statusCode': 200,
        'body': json.dumps('Hello from Lambda!')
    }
```

 ***clear the logs & upload the .txt object***
![286](https://github.com/user-attachments/assets/20c8d038-4986-4fe8-b95a-a0a3084e6ebf)

***see the text data own object in logs**
![287](https://github.com/user-attachments/assets/ced21e89-b6a0-4169-8aa9-86554b7f0d53)
