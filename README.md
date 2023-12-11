# CLCM 3504 PROJECT - TechCo Company website

This Project uses **Terraform** to Provision Infrastructure Resources and **GitHub Actions** to Deploy
the code on those resources.

- Refer to _.github/workflows/deploy-to-ec2.yml_ for CI/CD pipeline.

### GitHub Actions Secrets List

```
EC2_SSH_KEY
HOST_DNS
USERNAME
TARGET_DIR
RDS_USERNAME
RDS_PASSWORD
RDS_ENDPOINT
RDS_DATABASE
```

### Required prerequisites to run this project

- Terraform Installation
- AWS CLI configured (**Make sure AWS Account is accessible through CLI**)

- **Provision Infrastructure**

  ```
  git clone https://github.com/shaik-rehan-uddin/CLCM3102-PROJECT.git
  cd CLCM3102-PROJECT

  cd terraform-code
  terraform init
  terraform apply --auto-approve
  ```

- Update _HOST_DNS_ & _RDS_ENDPOINT_ in you Actions Secrets based on the Newly Provisioned Infrastructure
- Run the GitHub Actions Pipeline to deploy the code to new Infrastructure
