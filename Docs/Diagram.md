## Udagram Infrastructure

![Architecture](Diagram.png)

### AWS
#### RDS Postgres
The application server uses AWS RDS Postgres as database for storing and retrieving information.

Database URI: `postgre://postgres:password@database-2.ciz8eu7yteol.us-east-1.rds.amazonaws.com/udagram`

#### Elastic Beanstalk
The application server is deployed on AWS Elastic Beanstalk service. The application is build, archived and uploaded
to and S3 bucket from where Elastic Beanstalk extracts and runs the application on an endpoint.

EB URL: `http://udagrams-api-dev.eba-qtiqc9m6.us-east-1.elasticbeanstalk.com/`

#### S3 Bucket
The frontend application is deployed using AWS S3 Bucket. The bundled assets are uploaded to an S3 bucket and that
bucket is made publicly readable.

Bucket URL: `http://udagram-sheta.s3-website-us-east-1.amazonaws.com/`

End users can access the application from the Bucket URL.
