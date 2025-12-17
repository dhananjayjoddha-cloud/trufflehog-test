# print("Hello Secure World")

# AWS_ACCESS_KEY_ID = "AKIA123456789TESTKEY"
# AWS_SECRET_ACCESS_KEY = "wJalrXUtnFEMI/K7MDENG/bPxRfiCYTESTKEY"

# API_ENDPOINT = "https://api.example.com/v1/data"

# print("AWS Key:", AWS_ACCESS_KEY_ID)
# print("API Endpoint:", API_ENDPOINT)


import os

print("Hello Secure World")

# Load secrets securely from environment variables
AWS_ACCESS_KEY_ID = os.getenv("AWS_ACCESS_KEY_ID")
AWS_SECRET_ACCESS_KEY = os.getenv("AWS_SECRET_ACCESS_KEY")
NGROK_API_KEY = os.getenv("NGROK_API_KEY")

API_ENDPOINT = "https://api.example.com/v1/data"

# Safety checks
if not NGROK_API_KEY:
    raise RuntimeError("NGROK_API_KEY is not set")

print("AWS Key loaded:", bool(AWS_ACCESS_KEY_ID))
print("ngrok API Key loaded:", bool(NGROK_API_KEY))
print("API Endpoint:", API_ENDPOINT)
