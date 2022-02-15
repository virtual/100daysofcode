# #100DaysOfCode Round 5

## All projects:

- DistantLife
  - Day 12: Update database connections to use sqlite3
  - Day 14: Updated python server & updated code on production to use sqlite3
- Python Testing
  - Day 13: Unit Testing
- AWS Cloud Practitioner Certification
  - Fundamental Cloud Concepts ✓
    - Day 01: Account setup 
    - Day 02: Cloud Computing, AWS Global Infrastructure	 
    - Day 03: Understanding Cloud Economics, Supporting AWS Infrastructure ✓
  - Understanding AWS Core Services ✓
    - Day 05: Interacting with AWS, Compute Services
    - Day 06: Content and Network Delivery Services, File Storage Services, Database Services and Utilities, App Integration Services
    - Day 07: Management and Governance Services ✓
  - Introduction to Security and Architecture on AWS ✓
    - Day 08: AWS Architecture Core Concepts 
    - Day 09: AWS Identities and User Management
    - Day 10: Data Architecture on AWS
    - Day 11: Disaster Recovery on AWS, Architecting Applications on Amazon EC2 ✓
- Codewars
  - Day 04: Greed is Good (Python) ✓

## R5 Day 14: 2022-02-14 Monday

Updated python server & updated code on production to use sqlite3 

```sh
sudo apt-get update
sudo apt-get upgrade
cd /var/www/distantlife.com/html
sudo systemctl stop distantlife
git pull
sudo systemctl start distantlife
```


## R5 Day 13: 2022-02-13 Sunday

- [Unit Testing on Python](https://app.pluralsight.com/library/courses/using-unit-testing-python/table-of-contents)
- [Possible flask blog platform](https://github.com/gouthambs/Flask-Blogging) - but a bit too much restructuring, newness for me atm

### Unit Testing

A unit test __doesn't__ use:
- the filesystem
- a database
- the network

[Phonebook tests repo](https://github.com/virtual/python-testing)

## R5 Day 12: 2022-02-12 Saturday

DistantLife: change use of `cs50` library to `sqlite3` for database queries

Was:

```py
from cs50 import SQL

db = SQL("sqlite:///distantlife.db")
```

Now:

```py
import sqlite3

con = sqlite3.connect("distantlife.db")
con.row_factory = sqlite3.Row # includes column name in return dictionary
db = con.cursor()
```

Updated:

```py
@app.route("/pets")
@login_required
def pets():
    """Lists all of user's pets"""
    
-   # previously using cs50 db query
-   # pets_owned = db.execute("SELECT pets.id, pet_types.imgsrc, pet_types.pet_type, pets.created, pets.exp, pets.name, users.active_pet_id FROM owners JOIN pets ON pets.id = owners.pet_id JOIN pet_types ON pets.type = pet_types.id JOIN users ON users.id = owners.owner_id WHERE owner_id = ?", session_get_int("user_id"))
-   # [{'id': 15, 'imgsrc': '/pets/034-jackalope.png', 'pet_type': 'Jackalope', 'created': '2021-12-05 18:04:39', 'exp': 0, 'name': 'Unnamed Pet', 'active_pet_id': 15}]    
    
+   # now, updated using .fetchall and rows magic (above)
+   # also required trailing " , " in list of params
+   pets_owned = db.execute("SELECT pets.id, pet_types.imgsrc, pet_types.pet_type, pets.created, pets.exp, pets.name, users.active_pet_id FROM owners JOIN pets ON pets.id = owners.pet_id JOIN pet_types ON pets.type = pet_types.id JOIN users ON users.id = owners.owner_id WHERE owner_id = ?", (session_get_int("user_id"), )).fetchall()
+   # https://itheo.tech/get-column-names-from-sqlite-with-python
+   # print(dict(pets_owned[0]))
+   # {'id': 15, 'imgsrc': '/pets/034-jackalope.png', 'pet_type': 'Jackalope', 'created': '2021-12-05 18:04:39', 'exp': 0, 'name': 'Unnamed Pet', 'active_pet_id': 15}
    return render_template("list.html", pets_owned=pets_owned)
```

After every UPDATE, INSERT, and DELETE you also need to commit in order to ensure the execution moves from the journal to the database.

Example of updating a row, checking if there was an update with `rowcount` and committing the update

```py
updateqry = db.execute(
    "UPDATE pets SET exp = ? WHERE id = ?", (exp, active_pet_id))
con.commit()
if (updateqry.rowcount > 0):
    session.get("active_pet")["exp"] = exp
    return exp
else:
    return 0
```
 
## R5 Day 11: 2022-02-11 Friday

AWS Cert: Introduction to Security and Architecture on AWS

- Disaster Recovery on AWS
- Architecting Applications on Amazon EC2

## R5 Day 10: 2022-02-10 Thursday

AWS Cert: Introduction to Security and Architecture on AWS

-  Data Architecture on AWS


## R5 Day 9: 2022-02-09 Wednesday

AWS Cert: Introduction to Security and Architecture on AWS

- AWS Identities and User Management

## R5 Day 8: 2022-02-08 Tuesday

AWS Cert: Introduction to Security and Architecture on AWS

- AWS Architecture Core Concepts 

## R5 Day 7: 2022-02-07 Monday

AWS Cert: Understanding AWS Core Services

- Management and Governance Services
  - AWS CloudTrail
  - Amazon CloudWatch and AWS Config
  - AWS Systems Manager
  - AWS CloudFormation
  - AWS OpsWorks
  - AWS Organizations and Control Tower


## R5 Day 6: 2022-02-06 Sunday

AWS Cert: Understanding AWS Core Services

- Content and Network Delivery Services
  - Amazon VPC and Direct Connect
  - Amazon Route 53 (DNS)
  - Elastic Load Balancing
  - Amazon CloudFront (CDN) and API Gateway
  - AWS Global Accelerator
- Database Services and Utilities
  - RDS
  - DynamoDB
  - Elasticache
  - Redshift 
- File Storage Services
  - Amazon S3 
  - Glacier and Glacier Deep Archive
  - Elastic Block Store (single EC2)
  - Elastic File System (Linux, multi EC2)
  - Data Transfer with AWS Snowball, Snowmobile
- App Integration Services
  - AWS Messaging Services
  - AWS Step Functions

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
  - Add test suite for queries
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
