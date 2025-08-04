🚀 FastAPI ML API

এই প্রজেক্টটি একটি FastAPI ভিত্তিক RESTful API যা একটি মেশিন লার্নিং মডেল (যেমন: model.pkl) ব্যবহার করে প্রেডিকশন রিটার্ন করে।

📁 প্রলনী স্ট্রাকচার

fastApi/
├── app.py # FastAPI main application
├── model.pkl # Trained ML model
├── requirements.txt # Python dependencies
├── myenv/ # (Optional) Virtual environment
└── README.md # Project documentation

✅ Requirements

Python 3.10+ (Recommended)

pip

(Optional) virtualenv or venv

⚙️ Installation

# 1. create virtual enviroment

python -m venv myenv
source myenv/Scripts/activate # Windows

# or

source myenv/bin/activate # Mac/Linux

# 2. nedded packages

pip install -r requirements.txt

📦 Requirements.txt (example)

fastapi
uvicorn
scikit-learn==1.6.1
numpy
pandas

🚀 রানের নির্দেশনা

uvicorn app:app --reload

এটি http://127.0.0.1:8000 তে API চালু করবে।

📬 API Endpoints

🔹 POST /predict

মডেল থেকে প্রেডিকশন পাওয়ার জন্য এই এন্ডপয়েন্ট ব্যবহার করো।

✅ Request (JSON):

{
"age": 35,
"weight": 100,
"height": 1.72,
"income_lpa": 10,
"smoker": true,
"city": "Gurgaon",
"occupation": "government_job"
}

✅ Response (JSON):

{
"predicted_catagory": "Medium"
}

⚠️ Common Issues

❗ Pickle/Model Version Error:

InconsistentVersionWarning বা Can't get attribute error এড়াতে, মডেলটি যেই Scikit-learn ভার্শনে ট্রেইন করা হয়েছিলো সেই ভার্শন ইনস্টল করো:

pip install scikit-learn==1.6.1

📚 Swagger & Redoc Docs

Swagger UI: http://127.0.0.1:8000/docs

ReDoc: http://127.0.0.1:8000/redoc

✍️ Author

Mohammad Maruf

Email: mohammadmarufgazi@gmail.com

GitHub: your-github

📄 License :
This project is licensed under the MIT License.
