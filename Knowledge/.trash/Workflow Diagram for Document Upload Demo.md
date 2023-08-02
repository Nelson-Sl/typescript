```mermaid
sequenceDiagram
	participant User
	participant Valuer-Web
	participant Valuer-BFF
	participant Valuer-API
	participant Temp-Bucket
	participant S3-Bucket
	User->>Valuer-Web:Choose Upload Files
	Valuer-Web->>Valuer-BFF:getPreSignUrl()
	Valuer-BFF->>Temp-Bucket:Get Presigned URL
	Temp-Bucket-->>Valuer-BFF:Presigned URL
	Valuer-BFF-->>Valuer-Web:Presigned URL
	Valuer-Web->>Temp-Bucket:Upload S3 Files to Temp Bucket
	Valuer-Web-->>User:Success Message
	User->>Valuer-Web:Click Submit Button
	Valuer-Web->>Valuer-API:Send POST request to /move
	Valuer-API->>Temp-Bucket:Copy uploaded files to S3
	Temp-Bucket-->>S3-Bucket:uploaded files
	Valuer-API->>Temp-Bucket:Delete uploaded files
```
Further Works After Spike: 
1. The infras have only test environment and no pipeline has built yet, a new ticket will be created for this if needed
2. In this demo we assumed that we will upload a file per operation, should further support multiple files upload in further development

