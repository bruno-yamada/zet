# AWS IAM - assume role in the same account

Managing access through roles instead of groups allow easier isolation of responsabilities and freedom to change around the multiples roles freelyo

eg. 
- as admin you can assume the role of a developer to check the permissions it has
- you can assign a developer tech lead both the roles of `developer` and `billing` if needed

one drawback is that you need to hop between roles according to what you need to do


## Role Creation

Through the UI
- Create the role for "Another AWS Account" but use the account-id of the same account

Through the CLI/TF
- Make sure the trust policy allows principal of the account itself:
```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "",
      "Effect": "Allow",
      "Action": "sts:AssumeRole",
      "Principal": {
        "AWS": "arn:aws-us-gov:iam::ACCOUNT_ID:root"
      }
    }
  ]
}
```

> tags: iam; aws; 

> uid: 20210817174756Z

> links: 

