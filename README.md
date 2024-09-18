# Testing deployment of nextcloud as secure file storage system.
# Objective:
- using nextcloud client to allow end user to store, retrieve, list and delete their files on local file system.
- Integrate with Github OAuth for user authentication.

# Test of concept with deploying of 2 docker instance, refer to docker-compose.yml.
- nextcloud-svr
- nextcloud-db

Note: Please update the parameters before running the docker compose file:
- MYSQL_ROOT_PASSWORD: <<rootpassword>>
- MYSQL_DATABASE: <<nextcloud_db_name>>
- MYSQL_USER: <<nextcloud_sql_user>>
- MYSQL_PASSWORD: <<sql_userpassword>>

``` docker compose up -d```

# Setting up Github Oauth with Nextcloud 
# Step 1: Create a GitHub OAuth App
- Got to https://github.com/settings/developers
- Generate a Client ID and Client Secrets for the application
- Update the Homepage URL to NextCloud Frontend
- Authorization Call URL https://<nextcloud_frontend>:8080/apps/sociallogin/oauth/GitHub

<img width="602" alt="image" src="https://github.com/user-attachments/assets/75fd944c-e56b-4018-9654-3ac86c8d0854">



