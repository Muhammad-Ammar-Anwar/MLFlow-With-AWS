# MLFLOW On AWS

### Setup:

1. Login to AWS console.
2. Create IAM user with AdministratorAccess
3. Export the credentials in your AWS CLI by running "aws configure"
4. Create a s3 bucket
5. Create EC2 machine (Ubuntu) & add Security groups 5000 port

Run the following command on EC2 machine
```bash
sudo apt update
```

```bash
sudo apt install python3-pip
```

```bash
sudo apt install pipenv
```
```bash
sudo apt install virtualenv
```
```bash
mkdir mlflow
```
```bash
cd mlflow
```
```bash
pipenv install mlflow
```
```bash
pipenv install awscli
```
```bash
pipenv install boto3
```
```bash
pipenv shell
```

## Then set aws credentials
```bash
aws configure
```
#Finally
```bash
mlflow server -h 0.0.0.0 --default-artifact-root s3://mlflow-tracking13
```
### open Public IPv4 DNS to the port 5000

### set uri in your local terminal and in your code 
```bash
export MLFLOW_TRACKING_URI=http://ec2-98-93-98-242.compute-1.amazonaws.com:5000/
```
