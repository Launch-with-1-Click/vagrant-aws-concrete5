# Vagarnt AWS Concrete5

[http://megumi-cloud.com/](http://megumi-cloud.com/)

## Getting Started

### 1. Install VirtualBox.

 * https://www.virtualbox.org/

### 2. Install Vagrant.

 * http://www.vagrantup.com/

### 3. Install the vagrant plugins.

```
$ vagrant plugin install vagrant-aws
```

### 6. Set shell environment variables to .bash_profile like below.

You should create IAM user for the Vagrant.

```
# https://console.aws.amazon.com/iam/home#home
export AWS_ACCESS_KEY="your aws access key"
export AWS_SECRET_ACCESS_KEY="your aws secret key"

# https://console.aws.amazon.com/ec2/v2/home#KeyPairs:
export AWS_EC2_KEYPAIR="your key pairs"
export AWS_EC2_KEYPAIR_PATH="/path/to/.ssh/id_rsa"
```

Reload environment variables.

```
$ source .bash_profile
```

### 5. Clone the repository into a local directory.

```
$ git clone git@github.com:Launch-with-1-Click/vagrant-aws-concrete5.git
```

### 6. Change into a new directory.

```
$ cd vagrant-aws-concrete5
```

### 7. Start a Vagrant environment.

```
$ vagrant up --provider=aws
```

## Sample IAM policy

```
{
  "Statement": [
    {
      "Sid": "xxxxxxxxxxxxx",
      "Action": [
        "ec2:*"
      ],
      "Effect": "Allow",
      "Resource": [
        "*"
      ]
    }
  ]
}
```
