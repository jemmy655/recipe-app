Add the following lines to `ES_HOME`/repository/conf/security/sso-idp-config.xml

    <ServiceProvider>
            <Issuer>recipe-app</Issuer>
            <AssertionConsumerService>https://localhost:9443/recipe-app/acs</AssertionConsumerService>
            <SignResponse>true</SignResponse>
            <CustomLoginPage>/recipe-app/controllers/login.jag</CustomLoginPage>
    </ServiceProvider>
   


How to run
----------
Clone the project into `ES_HOME`/repository/deployment/server/jaggeryapps/


Creating a sample dish
-----------------------
onec the application is started enter the following url 
https://localhost:9443/recipe-app/asts/dish/create_dish?resources=RECIPE_URL

here the RECIPE_URL is pointing to a recipe deployed in a server 

for example if you are useing the python Http server and the recipe name is sf_gss
the url : https://localhost:9443/recipe-app/asts/dish/create_dish?resources=http://localhost:8000/sf_gss/
