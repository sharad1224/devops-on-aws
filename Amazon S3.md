
# Amazon S3 (Simple Storage Service)

## Definition
Amazon S3 is an object storage service that offers industry-leading scalability, data availability, security, and performance.

## Key Features
- Durable and highly available object storage  
- Fine-grained access controls using IAM policies and bucket policies  
- Event notifications and triggers  
- Versioning and lifecycle policies  
- Server-side and client-side encryption  

## Use Cases
- Backup and restore  
- Data archiving  
- Static website hosting  
- Application data storage  

## Key Components / Concepts
- **Bucket**: A container for storing objects  
- **Object**: Files stored in buckets  
- **ACLs and Policies**: Define access to buckets and objects  
- **S3 Storage Classes**: Standard, Intelligent-Tiering, Glacier, etc.  

## Architecture Diagram
![s3](https://github.com/user-attachments/assets/76490b3f-a82e-4af0-bdf8-8a54ca9dd403)


## Best Practices
- Enable versioning to protect against accidental deletion  
- Use lifecycle policies to manage object transitions  
- Apply encryption for sensitive data  
- Set up bucket policies and IAM roles for security  

## Pricing Model
- Pay only for what you use: storage, requests, data transfer  
- Different storage classes have different pricing  
- Data transfer costs apply for outbound data  

## Exam Tips
- Know the storage classes and use cases  
- Understand S3 access control mechanisms  
- Be familiar with data consistency models and encryption options  

## Quick Recap
- S3 provides secure, durable, scalable object storage  
- Choose appropriate storage class based on use case  
- Secure buckets using IAM policies and encryption


## Simple S3 Bucket creation 

![102](https://github.com/user-attachments/assets/ced077c7-0363-4af8-8a01-160ed7cf75c3)
![103](https://github.com/user-attachments/assets/c307f20e-1de0-4232-b828-f17a20e07485)
![104](https://github.com/user-attachments/assets/3d9f85b7-e381-4d04-a22d-63860117721d)
![105](https://github.com/user-attachments/assets/8bca7465-141f-4ff6-9c23-5c7efb40bb63)
![107](https://github.com/user-attachments/assets/98c7803c-e36c-4be4-b11f-5b4b055cbb26)
![108](https://github.com/user-attachments/assets/322d1a99-0a19-4615-9ab7-37e02a3ce85d)
![109](https://github.com/user-attachments/assets/9a327599-e639-4cee-a452-91a15e63fc03)
![110](https://github.com/user-attachments/assets/f3fac5be-a514-4e27-856a-37aa18074618)
![112](https://github.com/user-attachments/assets/e9458f1d-062e-4cdd-b415-763e22021996)
![113](https://github.com/user-attachments/assets/7c410ac7-1e7c-4e9d-99f8-8b5595083ba5)
![114](https://github.com/user-attachments/assets/7dac783e-326c-4dbd-b592-95968d2a0e83)
![115](https://github.com/user-attachments/assets/37466f0f-8fa9-4af5-be6d-50706ed1d019)
![116](https://github.com/user-attachments/assets/63da62d3-fa31-4b5d-8fb9-494cd4554382)
![119](https://github.com/user-attachments/assets/1fa69f46-cd1c-40cc-afa8-984ccac0aba2)
![121](https://github.com/user-attachments/assets/a4893fe2-4d2f-4883-b4d8-98de69eb908d)
![122](https://github.com/user-attachments/assets/74eeb6ce-d29a-4dc8-aa75-017ec4079e2a)
![123](https://github.com/user-attachments/assets/7ca82ca8-f555-42bd-82cd-90b25fb90e1a)


## Simple static website hosting

![125](https://github.com/user-attachments/assets/55f45c14-8774-4735-abd7-e4419394437e)
![129](https://github.com/user-attachments/assets/dcde9a04-472b-42c3-b667-ffc9a01b558b)
![130](https://github.com/user-attachments/assets/c8845efa-f2fb-4156-9d79-de2e43078847)
![132](https://github.com/user-attachments/assets/e73a806f-3e16-4262-8866-6159d25de9d0)
![133](https://github.com/user-attachments/assets/0a6c98f1-7b24-44c3-b230-dc2fcc751b32)


## Show error page if website url wrong

![136](https://github.com/user-attachments/assets/52b7ddf6-33ee-4707-a1eb-f91ad2ae1e4c)
![137](https://github.com/user-attachments/assets/281ad8c0-ffbc-4db4-8e28-7b9b6a720920)
![138](https://github.com/user-attachments/assets/d9d4f21c-b86b-4a11-b5f3-8ae254fa723e)
![139](https://github.com/user-attachments/assets/4f85ecad-540d-4c3e-b11e-1d959d488499)
![141](https://github.com/user-attachments/assets/00d1b9ed-501f-4dbd-95a3-988eac57f1f1)



## Bucket Versioning

***1. Creating the Bucket with Versioning Disabled***

![149](https://github.com/user-attachments/assets/f5dda1dd-e3ae-49ad-94b7-2269e975945b)



***2. Uploading the First Version of the File***

![150](https://github.com/user-attachments/assets/fe57f99e-ba17-4e0a-b8d6-4846543bcfe2)



***3. Re-uploading and Overwriting the File without Versioning***

![151](https://github.com/user-attachments/assets/e9fd28b3-11bf-438e-82f1-b5f2c9da67c2)
![152](https://github.com/user-attachments/assets/b4ef8d76-e51f-45c6-8209-f2d0463f3fc8)



***4. Enabling Bucket Versioning***

![153](https://github.com/user-attachments/assets/01a36c3f-5fc8-4d9d-ae97-344b13d72dea)
![154](https://github.com/user-attachments/assets/fbc6c541-916a-4ce9-9426-27e623020ab0)



***5. Adding Additional Versions***

![155](https://github.com/user-attachments/assets/54ab359b-f195-4ba5-b921-86e0daed3dab)
![156](https://github.com/user-attachments/assets/11070d74-2917-4f27-92e9-0d8280f3f56c)

**update version**
![157](https://github.com/user-attachments/assets/89a19c1c-256f-4d9c-aba3-ecc40122eed4)
![158](https://github.com/user-attachments/assets/29366cf3-c17d-4ff8-9e2c-4bae6abbca4e)


***6. If delete latest version file***

![159](https://github.com/user-attachments/assets/5486fc62-5117-4e99-8f98-126c1d59f732)
![160](https://github.com/user-attachments/assets/56d1082e-34c8-4d9d-8efc-c2389c508b8d)
![161](https://github.com/user-attachments/assets/46360eca-a7b5-4fee-8eb2-11f86d22149b)


***7. Recover deleted file***

![162](https://github.com/user-attachments/assets/ab32f551-99d3-4ecc-b1cc-91da7059a976)
![163](https://github.com/user-attachments/assets/23be6c9b-161a-43d7-98d8-e852fe82e542)
![164](https://github.com/user-attachments/assets/f00ed184-f20b-4730-80f1-3366d63b7207)


***8. Now delete a latest version***

![165](https://github.com/user-attachments/assets/096ce8c3-fb94-449f-a731-7484c1111870)
![166](https://github.com/user-attachments/assets/6de05227-c023-4098-af53-3b1f6696c15d)
![167](https://github.com/user-attachments/assets/6c4c8a7f-db38-4638-a7c6-52255a87bad2)



***9. Suspending Bucket Versioning***

![168](https://github.com/user-attachments/assets/7e0a262c-bf55-4b9b-b6ba-3ae64d200b38)





