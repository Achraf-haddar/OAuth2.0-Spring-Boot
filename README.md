# Spring boot OAuth2 Social Login with GitHub and Google

A sample project that shows the implementation of OAuth2.0 login using Github and Google as an authorization server

### OAuth2.0 flow (How things really work in action)
![Diagram](./diagram/oauth2.0-diagram.PNG?raw=true "OAuth 2.0 Flow Diagram")

### Steps to create a gitHub application
* Go to [GitHub developer portal](https://github.com/settings/developers)
* Create a new application and provide the required information (supposing the application server port is 8080)
    * Set the homepage URL to http://localhost:8080  
    * Authorization callback URL to http://localhost:8080/login/oauth2/code/github.

### Steps to create a google OAuth application
* Go to Google Cloud Console.
* Create a new project by clicking on the project dropdown in the top bar and selecting "New Project".
* Enter a name for your project and click on "Create". 
* Once the project is created, select it from the project dropdown.  
* In the left sidebar, navigate to "APIs & Services" > "Credentials". 
* Click on "Create Credentials" and choose "OAuth client ID". 
* Select the application type based on your use case (e.g., Web application). 
* Set the authorized redirect URIs. Assuming your application server runs on port 8080, enter:
  * Authorized JavaScript origins: http://localhost:8080
  * Authorized redirect URIs: http://localhost:8080/auth/google/callback
* Click on "Create" to generate the OAuth client ID and client secret. 

### Steps to create a gitHub application
* Go to [GitHub developer portal](https://github.com/settings/developers)
* Create a new application and provide the required information (supposing the application server port is 8080)
  * Set the homepage URL to http://localhost:8080
  * Authorization callback URL to http://localhost:8080/login/oauth2/code/github.


### Update the `application.properties` file
After creating a new application, you need to add the client ID and the client secret to `application.properties` file

### Start the application and enjoy your Social-login