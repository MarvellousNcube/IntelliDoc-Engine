{\rtf1\ansi\ansicpg1252\cocoartf2821
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fswiss\fcharset0 Helvetica;}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
\paperw11900\paperh16840\margl1440\margr1440\vieww11520\viewh8400\viewkind0
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f0\fs24 \cf0 # \uc0\u55358 \u56800  IntelliDoc Engine\
\
**Automating Document Understanding Using AWS**\
\
## \uc0\u55357 \u56524  Problem Statement\
\
Businesses in healthcare, finance, and compliance handle a massive volume of complex documents. Manual processing is inefficient, costly, and error-prone. Traditional OCR fails to understand context and lacks intelligent insights.\
\
---\
\
## \uc0\u55357 \u56960  Solution Overview\
\
The **IntelliDoc Engine** is a serverless, cloud-native pipeline that:\
- Extracts structured data from documents using Amazon Textract\
- Converts data to semantic embeddings with Amazon SageMaker\
- Enables search and question answering via Amazon OpenSearch\
- Tracks metadata in Amazon DynamoDB\
- Evolves with user feedback using an MLOps pipeline\
\
---\
\
## \uc0\u55358 \u56816  Tech Stack\
\
| Service           | Purpose                              |\
|------------------|--------------------------------------|\
| **S3**           | Document intake (uploads)            |\
| **Lambda**       | Event triggers and orchestration     |\
| **Textract**     | OCR + layout extraction              |\
| **SageMaker**    | NLP + Embeddings generation          |\
| **OpenSearch**   | Fast semantic search & similarity    |\
| **DynamoDB**     | Metadata tracking                    |\
| **IAM**          | Secure role and access management    |\
\
---\
\
## \uc0\u55357 \u56577  Architecture Flow\
\
1. **Upload Document to S3**\
   - Triggers Lambda to start processing.\
\
2. **Trigger Textract via Lambda**\
   - Start text and form extraction.\
\
3. **Check Textract Job Status**\
   - Polls for job completion and retrieves text.\
\
4. **Generate Embeddings with SageMaker**\
   - Sends extracted text to a hosted NLP model (e.g., BERT).\
\
5. **Store Embeddings in OpenSearch**\
   - Enables smart, contextual question answering.\
\
6. **Track Metadata in DynamoDB**\
   - For lifecycle tracking and user attribution.\
\
7. **User Q&A**\
   - User inputs a question; embeddings compared; relevant text and answer returned.\
\
8. **MLOps (Planned)**\
   - Collects feedback to retrain models and auto-deploy improvements.\
\
---\
\
## \uc0\u55357 \u56481  Features\
\
- Serverless and event-driven\
- Semantic document search\
- Real-time Q&A interface\
- Scalable pipeline for various domains (finance, healthcare, compliance)\
- Built-in metadata and version tracking\
\
---\
\
## \uc0\u55357 \u56568  Screenshots\
\
> _Add screenshots of your S3 config, Lambda flows, SageMaker endpoint, OpenSearch console, and DynamoDB entries here._\
\
---\
\
## \uc0\u55357 \u56592  IAM & Security Best Practices\
\
- Least privilege IAM roles\
- Role chaining between services (Lambda to Textract, SageMaker, OpenSearch)\
- VPC setup with NAT Gateway and Elastic IPs for secure internet access\
\
---\
\
## \uc0\u55357 \u56999  Key Challenges & Learnings\
\
| Challenge | How I Solved It |\
|----------|------------------|\
| IAM Role Confusion | Researched IAM policies and created custom roles for service access |\
| OpenSearch Validation | Fixed IAM role ARN formatting for fine-grained access |\
| Textract Async Handling | Created polling Lambda to manage job results |\
| SageMaker Endpoint | Deployed pre-trained sentence-transformer with proper IAM and networking |\
| VPC Connectivity | Debugged EC2 connectivity and allocated Elastic IP |\
\
---\
\
## \uc0\u55358 \u56810  Future Improvements\
\
- Add feedback loop for model retraining (MLOps)\
- UI for document uploads and Q&A\
- Multi-language document support\
- Enhanced access logs and monitoring with CloudWatch\
\
---\
\
## \uc0\u55357 \u56514  Project Setup (How to Run It)\
\
1. Create an S3 bucket and enable versioning.\
2. Set up IAM roles for Lambda, Textract, SageMaker, and OpenSearch.\
3. Deploy the Lambda functions and link triggers from S3.\
4. Create SageMaker endpoint with sentence-transformer.\
5. Set up OpenSearch domain and index mappings.\
6. Use API Gateway or CLI to query documents via Lambda functions.\
7. Monitor and log using CloudWatch.\
\
---\
\
## \uc0\u55357 \u56556  Contact\
\
Built with \uc0\u55357 \u56507  by Marvellous T Ncube\
\uc0\u55357 \u56551  Marvncube@hotmail.com \
\uc0\u55357 \u56599  [GitHub]https://github.com/marvellousncube  \'95 [LinkedIn]{\field{\*\fldinst{HYPERLINK "https://www.linkedin.com/in/marvellous-ncube-77a825255/"}}{\fldrslt https://www.linkedin.com/in/marvellous-ncube-77a825255/}}\
\
}