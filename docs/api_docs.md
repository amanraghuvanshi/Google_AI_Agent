### API Documentation

**Base URL**: `https://api.agentic-ai.com`

---

### **Endpoints**

1. **Chatbot Configuration**

   * **POST** `/api/v1/chatbot/config`

     * **Description**: Create or update chatbot configurations.
     * **Request Body**:

       ```json
       {
         "name": "Support Bot",
         "intents": ["greeting", "faq", "escalation"],
         "platform": "dialogflow"
       }
       ```
     * **Response**:

       ```json
       {
         "status": "success",
         "message": "Configuration saved successfully."
       }
       ```

2. **User Query Handling**

   * **POST** `/api/v1/chatbot/query`

     * **Description**: Processes user queries through the AI chatbot.
     * **Request Body**:

       ```json
       {
         "userId": "12345",
         "query": "What is the refund policy?"
       }
       ```
     * **Response**:

       ```json
       {
         "response": "Our refund policy is...",
         "sentiment": "neutral"
       }
       ```

3. **AI Model Deployment**

   * **POST** `/api/v1/models/deploy`

     * **Description**: Deploys a trained model to Vertex AI.
     * **Request Body**:

       ```json
       {
         "modelName": "support_model_v1",
         "dataPath": "gs://bucket-name/data.csv"
       }
       ```
     * **Response**:

       ```json
       {
         "status": "success",
         "deploymentUrl": "https://vertex-ai/models/support_model_v1"
       }
       ```

4. **Ticket Management**

   * **GET** `/api/v1/tickets`

     * **Description**: Retrieves all tickets associated with a user.
     * **Response**:

       ```json
       [
         {
           "ticketId": "001",
           "status": "open",
           "description": "Unable to access account."
         }
       ]
       ```
