# jenkins local installation
1. Install docker compose
2. copy/clone the code to your own repo
3. Make sure you have a jenkins_home directory
4. run $docker-compose up -d
5. Go to localhost:8080 and Configure jenkins first admin user
   The password is located at your volume ($PWD/jenkins_home/secrets)
   Alternatively go into the container in the path shown in the config panel (localhost:8080)
   $docker exec -ti jenkins bash (not working in windows :(... )
6. Install recommended plugins
7. Start writtin your first jobs
