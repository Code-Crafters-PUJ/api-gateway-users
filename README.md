# api-gateway-admin

To modify a specific endpoint in the Krakend configuration, follow these steps:

1. Locate the Configuration File:
Find and open the Krakend configuration file (typically named krakend.json or similar).

2. Identify the Endpoint to Modify:
Locate the section of the configuration file that corresponds to the endpoint you want to modify. Each endpoint is defined within the endpoints array.

3. Update the Endpoint Configuration:
Within the endpoint's configuration block, you can modify various parameters:

endpoint: Change the path where the endpoint will be accessible.
backend: Modify the backend server's details such as host and port.
host: Update the URL of the backend server.
url_pattern: Adjust the specific URL pattern on the backend server.
disable_tls_verify: Toggle TLS verification (if necessary).
Ensure to make the necessary changes according to your requirements.

4. Save the Configuration File:
After making the modifications, save the changes to the configuration file.

5. Restart Krakend:
If Krakend is already running, restart it to apply the changes. You can typically restart Krakend by stopping and starting the service or by using a command provided by your system's service manager.

EXAMPLE:
```JSON
{
  "endpoint": "/santiprueba",
  "backend": {
    "host": [
      "http://example.com:8080"
    ],
    "url_pattern": "/new/endpoint",
    "disable_tls_verify": false
  },
  "method": "POST"
}
```
