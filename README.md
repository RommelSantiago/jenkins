# jenkins local installation
This is a way to install docker locally. The advantage is that you can recreate the container whenever you need.
Note: These directions were tested in a windows machine

1. Install docker compose
2. copy/clone the code to your own repo
3. Make sure you have a jenkins_home directory
4. run $docker-compose up -d
5. Go to localhost:8080 and Configure jenkins first admin user
   The password is located at your volume ($PWD/jenkins_home/secrets)
   Alternatively go into the container in the path shown in the config panel (localhost:8080)
   $docker exec -ti jenkins bash 
   in windows run $ winpty docker exec -ti jenkins bash
6. Install recommended plugins
7. Start writtin your first jobs

To stop/start the service run:
$ docker-compose start/stop

To delete the service run:
$ docker-compose down

## AWS integration
To get the AWS CLI, get into the container and run:
```
# curl -o awscliv2.zip https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip
#  unzip -o awscliv2.zip
#  ./aws/install
```
Note the prompt indicates root user as indicated in yml file.