import requests
import json

# Set up your API endpoint and API key
API_ENDPOINT = 'https://api.insurtech.com/motor-insurance'
API_KEY = 'your_api_key_here'

# Define the payload for the API request
payload = {
    'policy_number': '12345',
    'vehicle_make': 'Toyota',
    'vehicle_model': 'Camry',
    'vehicle_year': '2019',
    'driver_age': 35,
    'driver_gender': 'male',
    'driver_marital_status': 'married',
    'coverage_type': 'comprehensive'
}

# Convert the payload to JSON format
payload_json = json.dumps(payload)

# Set up the headers for the API request
headers = {
    'Content-Type': 'application/json',
    'Authorization': 'Bearer ' + API_KEY
}

# Make the API request
response = requests.post(API_ENDPOINT, data=payload_json, headers=headers)

# Check the response status code
if response.status_code == 200:
    # If the response is successful, parse the JSON response
    response_data = json.loads(response.text)
    # Do something with the response data
else:
    # If the response is unsuccessful, handle the error
    print('Error: ' + str(response.status_code))
import requests
import json

# Set up your API endpoint and API key
API_ENDPOINT = 'https://api.insurtech.com/motor-insurance'
API_KEY = 'your_api_key_here'

# Define the payload for the API request
payload = {
    'policy_number': '12345',
    'vehicle_make': 'Toyota',
    'vehicle_model': 'Camry',
    'vehicle_year': '2019',
    'driver_age': 35,
    'driver_gender': 'male',
    'driver_marital_status': 'married',
    'coverage_type': 'comprehensive'
}

# Convert the payload to JSON format
payload_json = json.dumps(payload)

# Set up the headers for the API request
headers = {
    'Content-Type': 'application/json',
    'Authorization': 'Bearer ' + API_KEY
}

# Make the API request
response = requests.post(API_ENDPOINT, data=payload_json, headers=headers)

# Check the response status code
if response.status_code == 200:
    # If the response is successful, parse the JSON response
    response_data = json.loads(response.text)
    # Do something with the response data
else:
    # If the response is unsuccessful, handle the error
    print('Error: ' + str(response.status_code))
