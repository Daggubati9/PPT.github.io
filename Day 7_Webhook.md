## ✅ 1. Webhook in CX using BigQuery API

A webhook in Dialogflow CX is used to connect the chatbot to external services. In our case, we use it to connect to BigQuery to fetch or insert data based on user inputs.

Example Use Case:

"If a user asks: 'What is today’s sales total?', the webhook will trigger a Python function, run a query in BigQuery, and send back the result."

Key Flow:

User sends input → CX detects intent → webhook triggered → Python code runs BigQuery query → result sent back to CX

## ✅ 2. Webhook Components

A webhook is like a messenger. CX sends a request in JSON, and our backend receives it, processes it, and sends back a reply.

| Component          | Explanation                                                  |
| ------------------ | ------------------------------------------------------------ |
| **URL**            | Endpoint where Dialogflow sends request (your webhook URL)   |
| **Request Body**   | JSON sent by Dialogflow (includes session, parameters, etc.) |
| **Response Body**  | JSON sent back by webhook (includes fulfillment message)     |
| **Authentication** | Can secure your webhook using headers/token if needed        |

## ✅ 3. Webhook Session Info

Session info carries conversation context. It helps us track user data like their name, choices, or previous responses across multiple turns.

  "sessionInfo": {
    "session": "projects/your-project/locations/global/agents/.../sessions/abc123",
    "parameters": {
      "username": "John",
      "user_id": "1234"
    }
  }

We can read session info in our webhook to personalize the response or use parameters in queries.

## ✅ 4. Delete the Intent (in CX)

To delete an intent in Dialogflow CX, go to the Intents tab, select the intent, and click Delete. You can also delete it via the CX API.

Steps:

  Open Dialogflow CX Agent.
  
  Click Intents.
  
  Select the intent.
  
  Click Delete.

Optional (API):

You can use REST API or gcloud CLI:

  gcloud dialogflow cx intents delete INTENT_ID --agent=AGENT_ID --location=global
  
## ✅ 5. Parameter Values

Parameters are values extracted from user input. For example, if the user says 'Book a table for 3 people', Dialogflow will extract the number 3 as a parameter.

Custom (your own entities)

  Built-in (like @sys.date, @sys.number, etc.)

How to use in webhook:

  "parameters": {
    "people_count": 3,
    "date": "2025-05-20"
  }
  
"In the webhook, we read these parameters to write queries or build a response."

