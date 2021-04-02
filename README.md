# CLONE SMS-PORTAL
    git clone https://github.com/gannza/sms-portal.git
    
# cd sms-portal
      composer require twilio/sdk 

# The next step is to update the .env file with our Twilio credentials. So open up .env located at the root of the project directory and add these values:

    TWILIO_SID="INSERT YOUR TWILIO SID HERE"
    TWILIO_AUTH_TOKEN="INSERT YOUR TWILIO TOKEN HERE"
    TWILIO_NUMBER="INSERT YOUR TWILIO NUMBER IN [E.164] FORMAT"

# create a new database:

    mysql> create database sms_portal;
    mysql> exit;

# Let’s proceed to change our database configuration accordingly in the .env file at the root of our project folder.

    DB_DATABASE=sms_portal
    DB_USERNAME=root
    DB_PASSWORD=

# We now have our migration file ready to be migrated. We can simply do that by running the following in our terminal:
    
    php artisan migrate
