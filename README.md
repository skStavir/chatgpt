# youtube link 
https://youtu.be/Vq7Lf5pI024?si=ythZ0mB4XGO3gXZO

#github link 
https://github.com/CarlosIUSalazar/HealthGPT/tree/master

# Steps to Run
python -m venv venv

Set-ExecutionPolicy RemoteSigned -Scope CurrentUser

.\venv\Scripts\Activate

pip install Flask==2.1.2 requests==2.26.0 openai==0.10.2 python-dotenv==0.19.1

pip install Werkzeug==2.0.0

python app.py
