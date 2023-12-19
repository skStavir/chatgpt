# HealthGPT
Uses ChatGPT API to get customised health advise based on a health questionnaire.

# Steps to Run
1. Create a Virtual Environment in python with virtualenv `python -m venv venv`
2.  `Set-ExecutionPolicy RemoteSigned -Scope CurrentUser`
3. Activate venv with '.\venv\Scripts\Activate' 
4. Install requirements with `pip install -r requirements.txt`
5. Run the app with `python app.py`

Remember ChatGPT API is a paid service. If you get rate limiting errors it could be that your API key is not linked to a paid subscription.
You can create a subscription at: https://platform.openai.com/account/billing/overview

# nginx commands
sudo vi /etc/nginx/sites-enabled/default

sudo nginx -t

sudo service nginx restart

# nginx configuration
server {
    listen 80;
    # server_name 34.239.195.167;

    location /healthguide {
        proxy_pass http://127.0.0.1:5000/;
    }

