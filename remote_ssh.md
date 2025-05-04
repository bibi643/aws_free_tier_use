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
```
_Note_: If not working you have to change the permission with the following line.
In the terminal, go to the folder where the .pem is.

```shell
chmod 400 key_name.pem
```

## VSCode

First, install the extension **Remote SSH**.

On the bottom left corner click on ><
- Connect to host
- Configure SSH Hosts
- Choose the one with your user_name/.ssh/config

```shell
Host name_EC2 # This is the name you gave to the instance in AWS
  Hostname xxxx # This is the public ID adress
  User ubuntu # Because we choose an Ubuntu Instance
  IdentityFile path_pem_key/key_name.pem # This is the path of the key.pem you created in AWS.
```

- Click on >< again
- Connect to Hosts
- Choose Host

To check if it is working, **open a terminal in VSCode** and you see the name of the instance.


