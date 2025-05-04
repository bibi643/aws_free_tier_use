# Remote SSH from visual studio code

# Goal

The goal here is to connect to an EC2 instance using a ssh connexion from Visual Studio Code.


# Process

## AWS
- Launch instance in AWS
- Download the .pem key
- Give a name to the instance in AWS **Important**

## Local Terminal

- Choose the instance in AWS and click on connect button.
- In the Tab **SSH Client** copy the example line

```shell
ssh -i "key_name.pem" ubuntu@X.X.X.X
# Replace the X.X.X.X by the IP public of the instance in AWS.
``
