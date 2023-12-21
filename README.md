# HealthGuide
Uses ChatGPT API to get customised health advise based on a healthGuide questionnaire.

# Steps to Run
Create a Virtual Environment in python with virtualenv 'python -m venv venv'

'Set-ExecutionPolicy RemoteSigned -Scope CurrentUser'

Activate venv with '.\venv\Scripts\Activate'

Install requirements with 'pip install -r requirements.txt'

Run the app with 'python app.py'

Run the app when the terminal is closed 'nohup python app.py &'

Remember ChatGPT API is a paid service. If you get rate limiting errors it could be that your API key is not linked to a paid subscription. You can create a subscription at: https://platform.openai.com/account/billing/overview

# Nginx commands
#Nginx configuration file for editing
sudo vi /etc/nginx/sites-enabled/default

#nginx configuration
server { listen 80; # server_name 34.239.195.167;

location /healthguide {
    proxy_pass http://127.0.0.1:5000/;
}
#Test the Nginx configuration for syntax errors
sudo nginx -t

#Restart Nginx to apply the changes
sudo service nginx restart
