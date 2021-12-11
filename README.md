# tek-up-aws


# Work to be done

Read the code in the "main.py" file and then push it to a remote repository in your GitLab account.
Implement the architecture below knowing that you must :

- Configure your security groups properly
    - Give the value "2" for the capacities: minimum, maximum and desired of the Auto Scaling Group
    - Specify the following configurations for the Auto Scaling Group Lunch Template:
       o Amazon machine image (AMI): Amazon Linux 2 (HVM)
       o Instance type: t2.micro
       o Key pair (login): an existing key pair
       o IAM instance profile : LabInstanceProfile
       o User data:

```bash
#!/bin/bash
yum update -y
yum -y install git
pip3 install fastapi[all] boto3 pydantic
git clone https://gitlab_ci_token: your_access_token
@gitlab.com/your_username/your_project.git cd your_project
/usr/local/bin/uvicorn main:app --host 0.0.0.0 --port 8000
```

Once the various components of the architecture are created, check the EC2 Dashboard for the launch of two
instances and then copy the DNS name of your Load Balancer into the browser to display the message "Hello
World!"
Add **/docs** to your URL to display the functions offered by your API. Run the
write to disk function as follows:
```json
{
    "path": "/home/ec2-user",
    "file_name": "my_file.txt",
    "content": "Hello!"
}
```
Then test the read function from the disc to display the contents of the file you created. Repeat the test
of the read function. What do you find? Explain.
Propose a solution using the existing functions.
