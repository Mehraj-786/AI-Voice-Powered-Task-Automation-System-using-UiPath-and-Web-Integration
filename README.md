# AI-Voice-Powered-Task-Automation-System-using-UiPath-and-Web-Integration
An AI-powered voice automation system integrating web, AI, and UiPath. It enables users—especially the visually impaired—to execute tasks via voice commands, with AI classifying intents and UiPath automating actions, providing real-time voice and visual success feedback.
This project is an AI-integrated voice automation system designed to help users — including those with visual impairments — interact with a web application through natural voice commands.
The system connects a frontend interface, a Node.js backend, and UiPath automation workflows to execute real-world tasks such as booking a cab, ordering food, or fetching institutional data.

When a user opens the web app, it immediately provides voice-based guidance:

“Press any key to start recording your request”

“Press any key to stop recording”


Once the user’s voice input is processed, the AI (powered by a backend classifier) determines the task type, provider, and payload from the input JSON, such as:

{
  "taskType": "order_food",
  "provider": "Zomato",
  "payload": { "food_item": "pizza" }
}

The system then triggers a corresponding UiPath workflow (for example, to automate an order process).
After successful task execution, the application gives both visual and voice feedback:

> “✅ Task has been successfully completed!”



This makes automation more accessible, intelligent, and user-friendly.


---

⚙ Tech Stack

Layer	Technology Used	Description

🎨 Frontend	React + TypeScript (index.tsx)	Provides voice-based UI and real-time status updates
🧠 Backend	Node.js + Express (index.js)	Handles API requests, task classification, and communication with UiPath
🤖 Automation	UiPath Studio / Robot	Executes the workflow (e.g., booking, data retrieval, or processing)
🔉 Speech Handling	Web Speech API / Voice Synthesizer	Converts speech to text and text to speech for accessibility
🌐 Communication	HTTP (POST/GET APIs)	Sends structured task requests and receives responses
🔒 Hosting Option	Local / Ngrok / Cloudflare Tunnel	Enables web-to-desktop connectivity without Orchestrator



---

🚀 Features

🗣 Voice-Based Interaction: Users can operate the system entirely through voice commands.

🤝 AI-Driven Intent Extraction: The backend classifies requests into structured JSON (taskType, provider, payload).

⚡ UiPath Workflow Integration: Automates real tasks like booking, verification, or data retrieval.

🧩 Dynamic Payload Handling: Payload structure adapts automatically to the user’s request.

🔊 Audio Feedback: Provides real-time voice guidance and confirmation messages.

🌍 Accessibility Support: Designed with visually impaired users in mind.

💻 Local or Hybrid Hosting: Works locally or online (via Ngrok tunnel or Orchestrator).



---

🎯 Objectives

To integrate AI, Voice Interaction, and RPA into a unified automation platform.

To make automation accessible to visually impaired users through speech guidance.

To enable dynamic task execution without manual workflow selection.

To demonstrate the potential of hybrid AI + RPA systems for real-world applications.



---

📈 Expected Outcomes

A functional web-based AI assistant capable of triggering UiPath automations.

Seamless data flow between frontend, backend, and UiPath workflows.

Real-time voice and visual feedback for user confirmation.

Demonstration of a scalable model for accessible automation systems.

A working prototype showing end-to-end integration between web apps and RPA bots.



---

🧠 System Architecture

Flow:

User (Voice Input)
      ↓
Frontend (Speech to Text)
      ↓
Backend (AI/LLM-based Intent Extraction)
      ↓
UiPath Workflow Trigger
      ↓
Task Execution
      ↓
Backend Response → Frontend
      ↓
Voice + Visual Output: “Task Completed Successfully”


---

🧰 Setup Instructions

1️⃣ Clone Repository

git clone https://github.com/<yourusername>/AI-Voice-Automation.git
cd AI-Voice-Automation

2️⃣ Install Dependencies

npm install

3️⃣ Start Backend Server

node index.js

4️⃣ Start Frontend

If using React:

npm start

5️⃣ Run UiPath Workflow

Open UiPath Studio → Publish your workflow (e.g., BookCab.xaml).

Ensure UiRobot.exe is installed (default path: C:\Program Files (x86)\UiPath\Studio\UiRobot.exe).


6️⃣ Configure Backend Trigger

Edit your index.js:

exec(
  "C:\\Program Files (x86)\\UiPath\\Studio\\UiRobot.exe" execute --file "C:\\Users\\YourName\\Documents\\UiPath\\BookCab\\Main.xaml"
);

7️⃣ Test Integration

Run your app → Speak your command → Observe workflow execution → See confirmation on screen + hear success voice.


---

🔒 Hosting Options

Option	Description

🏠 Local	Run backend and UiPath on the same machine
☁ Ngrok Tunnel	Expose backend endpoint to the web
🧭 Cloudflare Tunnel	Secure, free alternative to Ngrok
🧠 UiPath Orchestrator	(Optional) Cloud-level workflow management



---

💡 Future Enhancements

Add multi-language voice support.

Integrate Gemini API or GPT for better task understanding.

Add database for user history and task logs.

Implement user authentication for secure automation triggers.

Build mobile version for voice-based RPA tasking.



---

📚 Domains Covered

AI / ML — intent classification, voice processing

Web & Mobile Development — full-stack web interface

Sustainable Tech — accessibility for visually impaired users

Automation / RPA — UiPath workflow execution



---
