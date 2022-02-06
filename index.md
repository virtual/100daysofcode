# #100DaysOfCode Round 5

## R5 Day 6: 2022-02-06 Sunday

AWS Cert: Understanding AWS Core Services

- Content and Network Delivery Services
  - Amazon VPC and Direct Connect
  - Amazon Route 53 (DNS)
  - Elastic Load Balancing
  - Amazon CloudFront (CDN) and API Gateway
  - AWS Global Accelerator
- File Storage Services
  - Amazon S3 
  - Glacier and Glacier Deep Archive
  - Elastic Block Store (single EC2)
  - Elastic File System (Linux, multi EC2)
  - Data Transfer with AWS Snowball, Snowmobile

[Email: learn and test DMARC (Domain-based Message Authentication, Reporting & Conformance)](https://www.learndmarc.com/)

## R5 Day 5: 2022-02-05 Saturday

AWS Cert: Understanding AWS Core Services

Compute services:

- Amazon EC2 (Elastic Compute Cloud)
- AWS Elastic Beanstalk
- AWS Lambda

Methods of interacting:

- AWS Console
- AWS CLI (see setup below, use IAM user)
- AWS SDK

### AWS CLI

Setting up AWS CLI, download CLI v2

```sh
aws configure --profile ps
AWS Access Key ID [None]: KEY_ID
AWS Secret Access Key [None]: SECRET_KEY
Default region name [None]: us-west-2
Default output format [None]: json
```

Example, list all S3 buckets:

```sh
aws s3 ls --profile ps
```

## R5 Day 4: 2022-02-04 Friday

- Pluralsight skills:
  - CSS: 238; need to work on at-rules, transitions, animations
  - Python: 199
- Codewars: [Greed is Good](https://www.codewars.com/kata/5270d0d18625160ada0000e4/train/python)

## R5 Day 3: 2022-02-03 Thursday

AWS Cert: Fundamental Cloud Concepts

- Understanding Cloud Economics: TCO calc, pricing calc
- Supporting AWS Infrastructure: basic, developer, business, enterprise

## R5 Day 2: 2022-02-02 Wednesday

AWS Cert: Fundamental Cloud Concepts

- Cloud Computing
  - Traditional Data Centers
  - Benefits of Cloud Computing
  - Types of Cloud Computing
- AWS Global Infrastructure	
  - AWS Regions 
  - Availability Zones
  - AWS Edge Locations


## R5 Day 1: 2022-02-01 Tuesday

- Digging into Pluralsight's [AWS Cloud Practitioner cert](https://app.pluralsight.com/explore/certifications/topics/aws) (doing notes in a guide), setup account
- Need to also look into taking the skill assessment for CSS (and SCSS if available?) and see what gaps I have! 

Learned that this SCSS syntax works for compiling font styles: (thanks LauraBoemo!)

```scss
.myclass {
  font: { 
    family: $theme-font-regular; 
    size: 16px; 
    weight: 300; 
  }
}
```

## 🧧 Round 5 begins 🧧

Ideas for Round 5 starting February 1, 2022

- CSS Animations / Move Things With CSS
 (Jhey)
- Built out [Distant Life app](https://github.com/virtual/distantlife)
  - Word images
  - Word lists
  - Limit abilities to pet levels
  - Create "worlds"
  - Add another language
- [Javascript30](https://github.com/virtual/javascript30)
- [Codewars](https://www.codewars.com/dashboard) (6kyu, 172)
- [Javascript design patterns (MVC)](https://classroom.udacity.com/courses/ud989)
- [Redo Libworx in Python](https://github.com/virtual/libworx)
- [App Ideas Collection from florinpop17](https://github.com/florinpop17/app-ideas)
- [freeCodeCamp](https://www.freecodecamp.org)
  - [Complete Information Security](https://www.freecodecamp.org/learn/information-security/)
- Play with Storybook or a similar platform for UI
- AWS Cloud Practitioner
- Advanced SCSS
- Make my 100daysofcode nav mobile friendly
