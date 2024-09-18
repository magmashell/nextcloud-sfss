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

# Step 2: Install GitHub Integration Apps on Nextcloud
- update enable to Github Integration Apps the following Sociallogin Side Menu would appear
<img width="322" alt="image" src="https://github.com/user-attachments/assets/f1c2824b-8ac3-4dde-9fc2-c98bf959ed6d">

- On Sociallogin App, input the GitHub Client ID and Secrets to enable the oauth integration
<img width="639" alt="image" src="https://github.com/user-attachments/assets/7f234f0d-7304-4186-b499-051e55c8a4f1">




