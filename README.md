# AMP-API
Introduction to AMP-API


**After following this guide, you will be able to:**

- Understand how Cisco AMP helps investigate endpoints and store event data.
- Learn how to use the AMP API for tasks like authentication, basic management, searching, and event handling.
- See how AMP works with other security tools and how APIs help in typical workflows.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
**AMP APIs: Authentication**

There are two ways to authenticate when using the Cisco AMP for Endpoints APIs. First, you need to get a client ID from the Cisco AMP console. Once you have the client ID, you can authenticate using one of these methods:

1. **URL authentication**: Use this format:  
   `https://<your_client_id>:<your_api_key>@<api_endpoint>`

2. **Basic HTTP authentication (Base64)**: Use this method to encode your client ID and API key in Base64.

To start using the API, follow these simple steps:

1. Go to the **Accounts** menu and choose **API Credentials**.
2. Click **+ New API Credentials**.
3. Enter a unique name for your application.
4. Select the access level: **Read-only** or **Read & Write**.
5. Click **Create**.
6. Copy the **API Client ID** and **API Key**, and keep them for your API calls.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**AMP APIs: Use Case & Example**

Once you're authenticated, you can now use the API to get information from Cisco AMP for Endpoints. Here are some examples:

Query for detailed endpoint (computer) information:

API call: GET

URL: https://api.amp.cisco.com/v1/computers

Query for general event information. There will be a limit of 10 results returned (limit=10):

API call: GET

URL: https://api.amp.cisco.com/v1/events?limit=10

Query for only three (limit=3) currently known sections of application information that are blocking a file, starting at the second position (offset=2):

API call: GET

URL: https://api.amp.cisco.com/v1/file_lists/application_blocking?limit=3&offset=2

Query for three of the configured policies (limit), starting at the second position (offset):

API call: GET

URL: https://api.amp.cisco.com/v1/policies?limit=3&offset=2



----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**References:**

Cisco Systems, Inc., Overview of the Cisco AMP for Endpoints API, [https://www.cisco.com/c/en/us/support/docs/security/amp-endpoints/201121-Overview-of-the-Cisco-AMP-for-Endpoints.html.](https://www.cisco.com/c/en/us/support/docs/security/amp-endpoints/201121-Overview-of-the-Cisco-AMP-for-Endpoints.html)

Cisco Systems, Inc., Cisco AMP for Endpoints API, [https://api-docs.amp.cisco.com/api_resources?api_host=api.amp.cisco.com&api_version=v1.](https://api-docs.amp.cisco.com/api_resources?api_host=api.amp.cisco.com&api_version=v1)

DevNet API Docs, Cisco Advanced Malware Protection (AMP) for Endpoints API: [https://developer.cisco.com/amp-for-endpoints/.](https://developer.cisco.com/amp-for-endpoints/)

DevNet Learning Labs:

https://developer.cisco.com/learning/modules/ampforendpoints/intro-to-cisco-amp/step/1.

https://developer.cisco.com/learning/modules/ampforendpoints/intro-into-amp-apis/step/1.

More Use Cases and details may be found at: [https://www.cisco.com/c/en/us/products/security/amp-for-endpoints/case-study-listing.html.](https://www.cisco.com/c/en/us/products/security/amp-for-endpoints/case-study-listing.html)

Cisco Systems, Inc., Additional AMP Everywhere Integrations, [https://www.cisco.com/c/en/us/products/security/advanced-malware-protection/index.html#~integrations.](https://www.cisco.com/c/en/us/products/security/advanced-malware-protection/index.html#~integrations)
