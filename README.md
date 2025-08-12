
# AI-Powered Healthcare Assistant

## Deploy
- [Live Demo](https://gen-ai-mech-hackathon.vercel.app/) *(replace with your own deployment link)*

## Overview
This project is an AI-powered healthcare web application designed to provide **real-time disease detection** and **personalized preventive care**.  
It uses machine learning models to diagnose diseases such as **asthma, cancer, diabetes, and stroke**, and offers a chatbot powered by a fine-tuned LLM for follow-up consultations.

If a disease is detected, the user receives preventive measures along with interactive guidance from the chatbot.

## Key Features
- 🩺 **Real-time disease detection** using trained ML models  
- 💡 **Personalized preventive measures** for detected diseases  
- 🤖 **LLM-powered chatbot** for further consultation  
- 🔐 **Secure authentication** (sign-up & sign-in)  
- 🖥 **User-friendly interface** with clear navigation  

---

## How It Works
1. User signs up or logs in.  
2. Navigates to the **Diagnosis** page.  
3. Fills out a form with required medical information.  
4. The ML model predicts if the user has any of the listed diseases.  
5. If positive, preventive measures are shown.  
6. The user can chat with the AI doctor for more guidance.

---

## Unique Approach
This project combines **diagnosis** and **recommendation**:
- **Diagnosis:** Uses disease-specific ML models to analyze user-provided data.
- **Recommendation:** Generates a detailed report including causes, symptoms, prescription suggestions, and lifestyle changes.
- **AI Chatbot:** A fine-tuned medical LLM for general health-related queries.

---

## Demo Video
[Watch Here](https://youtu.be/jwQfrptToTA)

---

## Workflow
![Workflow](/image/explain.png)

---

## Screenshots

### Sign-Up Page
![Sign Up](/image/1.png)

### Home Page
![Home](/image/2.png)

### Diagnosis Page
![Diagnosis](/image/3.png)

### Form Page
![Form](/image/4.png)
![Form Page 2](/image/6.png)
![Form Page 3](/image/7.png)

### Chat Page
![Chat](/image/5.png)

---

## Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
````

### 2. Run the Frontend

```bash
cd frontend
npm install
npm run dev
```

### 3. Run the Backend

```bash
cd backend
python -m venv env
source env/bin/activate  # Mac/Linux
env\Scripts\activate     # Windows
pip install -r requirements.txt
cd genaimechbackend
python manage.py runserver
```

### 4. Configure `.env`

Create `.env` in `backend/genaimechbackend/genaimechbackend/`:

```env
HOST=
PROJECT_NAME=
DB_USERNAME=
PASSWORD=
SECRET_KEY=
```

### 5. Access the App

Visit [http://localhost:3000](http://localhost:3000) in your browser.

---

## Model & Fine-Tuning

* **Base model:** [Intel/Mistral-7B-v0.1-int4-inc](https://huggingface.co/Intel/Mistral-7B-v0.1-int4-inc)
* **Fine-tuning dataset:** [Mental Health Conversational Dataset](https://huggingface.co/datasets/heliosbrahma/mental_health_conversational_dataset)
* Run fine-tuning:

```bash
python medical_finetune.py --bf16 True --use_ipex True --max_seq_length 512
```

---

## Datasets Used

* [Diabetes Dataset](https://www.kaggle.com/datasets/akshaydattatraykhare/diabetes-dataset)
* [Asthma Dataset](https://www.kaggle.com/datasets/deepayanthakur/asthma-disease-prediction)
* [Stroke Dataset](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset)
* [Lung Cancer Dataset](https://www.kaggle.com/datasets/mysarahmadbhat/lung-cancer)

---

## Author

Developed by **\[Your Name]**
GitHub: [your-username](https://github.com/your-username)
Email: [your-email@example.com](mailto:your-email@example.com)
