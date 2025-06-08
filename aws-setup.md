## S3 Bucket

### Create S3
- AWS Console
- S3 Bucket
- Create Bucket
- Enter name
- Save changes

### Modify S3
#### Properties
- `Edit static website hosting` > `Enable`
- Enter `index document` name
- `save changes`
- copy static website endpoint
#### Permissions
- `Edit Block public access`
- Eeselect
- Save changes 
- Confirm
#### Bucket Policy
- Edit
- ```
  {
    "Version": "2012-10-17",
    "Statement": [
    	{
        	"Sid": "PublicReadGetObject",
        	"Effect": "Allow",
        	"Principal": "*",
        	"Action": [
            	"s3:GetObject"
        	],
        	"Resource": [
                "arn:aws:s3:::Bucket-Name/*"
        	]
    	}
    ]
  }
- Replace "Bucket-Name" with actual s3 name
- Save changes
### Upload to S3
- Objects
- Add files
- Add HTML and other files if necisarry
- Open aws s3 bucket website link
