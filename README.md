# 🌟 Auvive – Live Well, Gift Well  

> **⚠️ Note:** Due to Fashion Quarterly's privacy policy, the source code for this project cannot be made publicly available. However, a demonstration video is included below to showcase the project's functionality and features.

**Auvive** is an AI-powered web app that helps users find the perfect **gift or restaurant** through natural conversation.  
It asks smart, personalised questions, learns from preferences, and delivers curated recommendations — with direct links to buy or book.  

---

## 🎬 Demo Video

📹 **[Watch Demo Video](auvive-demo-video.MOV)**  
*Click the link above to view or download the demonstration video.*

**Presenter:** Yurara Ito

---

## 🧠 Core Features  

### 💬 Conversational AI  

🔹Users chat naturally with the assistant to express needs, occasions, or moods.  
🔹AI model (OpenAI / AWS Bedrock integrated) understands context and returns personalised recommendations.  

### 🎁 Gift Recommendations  

🔹Suggests products based on recipient type, occasion, and budget.  
🔹Direct links to partner stores or placeholder shopping sites.  

### 🍽️ Restaurant Finder  

🔹Curated dining options tailored to user preferences, location, and event type.  
🔹Includes cuisine filters, location preferences, and special-occasion suggestions.  

### 🔐 Authentication & Authorization

🔹Google OAuth sign-in & email account registration via AWS Cognito.  
🔹Secure user profile persisted in DynamoDB.  
🔹Integrates with Google calendar & easy event creation page.  
🔹Supports guest (unsigned) mode with temporary sessions.  

### 💾 Chat History & Session Management  

🔹Signed-in users can access their complete chat history.  
🔹Guests maintain temporary sessions in localStorage.   

---

## 🛠️ Tech Stack
- **Frontend:** React, TypeScript, html, Tailwind CSS  
- **Backend:**  Lambda (Python), Flask (Python)  
- **Database:** AWS DynamoDB    
- **Authentication:** AWS Cognito & Google OAuth  
- **Storage:** AWS S3    
- **AI Integration:** AWS Bedrock - Claude Haiku 3.0    
- **Hosting:** AWS Amplify (frontend), API Gateway (backend)    
- **Monitoring & Logs:** AWS CloudWatch  

### 🧰 AWS Configuration  

&nbsp;***Amplify*** → hosts the React frontend; connected directly to the GitHub main branch for auto-deployment.   
&nbsp;***Elastic Beanstalk***  → runs the Flask app for authentication, integrated behind API Gateway.   
&nbsp;***Lambda*** → stateless chat processor calling AI API and DynamoDB.   
&nbsp;***API Gateway*** → exposes endpoints for Authentication Flask (EB) and Chatbot Lambda.  
&nbsp;***DynamoDB Tables*** → Persists items catalog, user data, chat sessions and chat messages.  
&nbsp;***IAM Roles*** → minimal access policies for Lambda, EB, and Amplify.    
&nbsp;***CloudWatch*** → logging, metrics, and throttling alerts to control costs.  

---

## 🧪 Development Setup

### Guide 
```bash
pip install -r requirements.txt
npm install
npm run dev:all
```

### 🧑‍💻 Development Notes
The project maintains Separate **DEV** and **PROD** environments for EB and Amplify.✔️    
API Gateway **CORS** is properly configured in both, and the frontend automatically detects the user’s authentication state.✔️   

---

## 🌐 Live Application  

Visit our app:  Please contact Yurara for access.

📩 lylac.bsn@gmail.com

---

## 👥 Team 

**Team 8 — AIvengers**  
Team Lead / Full Stack Developer: Yurara Ito  
Backend Developer: Rachel Yuan   
Frontend Developer: Chloe Lee  
Project Assistant: Annabelle Ding      
Project Assistant: Helen Man        
Project Assistant: Yule Zhan     

---

## 🎯 Value Proposition
Auvive reduces **decision fatigue**, ensures users **never miss special occasions**, and makes shopping and dining a **simple, enjoyable, and personalised experience**.  

---

## 🚀 Elevator Pitch
*Auvive is your AI concierge for gifting and dining — helping you live well and gift well by turning decision fatigue into effortless, personalised recommendations.*  
