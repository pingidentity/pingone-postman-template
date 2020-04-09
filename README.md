The Postman collections use variables in the request URLs to specify UUIDs for PingOne resources within your organization. If you create a PingOne environment in Postman, and then apply that environment to the collection, you can define common variables once and apply the values to many requests. For more information about setting up Postman environments, see the following topic in the Postman documentation: Environments in Postman.

For example, a request URL from the users Postman collection that returns data about a specific user contains variables for the environment ID and the user ID:

GET {{apiPath}}/environments/{{envID}}/users/{{userID}}

To run this request, you must define a value for the {{apiPath}} variable with the regional domain associated with your organization. Options are: https://api.pingone.com/v1 for environments the North America region, https://api.pingone.eu/v1 for environments in the European Union region, and https://api.pingone.asia/v1 for environments in the Asia-Pacific region.

In addition, you must define values for the {{envID}} and {{userID}} variables with the UUIDs for your environment and the specific user resource whose data you want to return. Almost every request in PingOne requires an environment ID, and if you are working primarily in one environment and with one user for testing purposes, then setting values for these variables in a Postman environment will save time.

In addition, every request to PingOne Management API endpoints requires an access token to authenticate the request. The Authorization type for the endpoints in the Postman collections is configured to Bearer Token and the value of the token is set as the variable {{accessToken}}. You can create an access token variable in the Postman environment and set its value to your current valid token.

For authorization requests, you must define a value for the {{authPath}} variable, which specifies the domain associated with the authorization server. If you are not using a custom domain name, the value should be set to https://auth.pingone.com, https://auth.pingone.eu, and https://auth.pingone.asia, depending on your region. If you have set a custom domain, for example acme.com, and you use auth.acme.com as your authentication server domain, the value of this Postman variable should be set to https://auth.acme.com.


To use this file properly:

1. Download the template.

2. Change the values as they match up to your PingOne environment.

3. Open your Postman applications.

4. Click the "Import" button and choose "Import File".

5. Select this template file and upload it in!
