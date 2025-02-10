# Cloud Computing

## **Enumerate S3 Buckets using lazys3**

**You can search the S3 buckets of specific company.** To do so, type **ruby lazys3.rb [Company]**

## **Enumerate S3 Buckets using S3Scanner**

In the S3Scanner folder, type **pip3 install -r requirements.txt** and press **Enter** to install the required dependencies.

![{576884B6-3E98-468E-BBDD-1F05C1FB1985}.png](Cloud%20Computing/576884B6-3E98-468E-BBDD-1F05C1FB1985.png)

## S3 bucket enumeration tools

**S3Inspector** (https://github.com) 

**s3-buckets-bruteforcer** (https://github.com)

**Mass3** (https://github.com) 

**Bucket Finder** (https://digi.ninja) 

**s3recon** (https://github.com)

## **Exploit Open S3 Buckets using AWS CLI**

```bash
 **pip3 install awscli**
```

we need to configure AWS CLI. To configure AWS CLI in the terminal window, type **aws configure** and press **Enter**.

It will ask for the following details:

- AWS Access Key ID
- AWS Secret Access Key
- Default region name
- Default output format

![{5444B317-9BC4-4F3A-9346-36EABE923226}.png](Cloud%20Computing/5444B317-9BC4-4F3A-9346-36EABE923226.png)

![{1EFFD6BD-D53B-4756-84C6-63C386E00DD4}.png](Cloud%20Computing/1EFFD6BD-D53B-4756-84C6-63C386E00DD4.png)

![{0B33D039-AF00-4D5E-BCA9-7467816E9675}.png](Cloud%20Computing/0B33D039-AF00-4D5E-BCA9-7467816E9675.png)

## **Escalate IAM User Privileges by Exploiting Misconfigured User Policy**

![{14BC0F04-B74E-435C-8AE0-5759CAD3BC7B}.png](Cloud%20Computing/d97f0626-a030-477b-91ba-c074c70fdc3a.png)

![{61FECC11-0CA2-4E38-90A9-C56AF0E6871C}.png](Cloud%20Computing/d10d7f5a-4d2c-4a6a-90d8-68d75b4d22ad.png)

![{8FDBB3A1-92DA-4BDE-BF15-A48612CCE3A4}.png](Cloud%20Computing/8FDBB3A1-92DA-4BDE-BF15-A48612CCE3A4.png)

![{02EE2EF0-F7B5-486A-BD7D-2B67A3087CAB}.png](Cloud%20Computing/02EE2EF0-F7B5-486A-BD7D-2B67A3087CAB.png)

![{AFEDFFD6-5661-4884-8C8C-70F03ABB41AE}.png](Cloud%20Computing/AFEDFFD6-5661-4884-8C8C-70F03ABB41AE.png)

![{F73D263F-B39D-4E80-A15C-2A5070EF6BA7}.png](Cloud%20Computing/F73D263F-B39D-4E80-A15C-2A5070EF6BA7.png)

Similarly, you can use various commands to obtain complete information about the AWS environment such as the list of S3 buckets, user policies, role policies, and group policies, as well as to create a new user.

- List of S3 buckets: **aws s3api list-buckets --query "Buckets[].Name"**
- User Policies: **aws iam list-user-policies**
- Role Policies: **aws iam list-role-policies**
- Group policies: **aws iam list-group-policies**
- Create user: **aws iam create-user**