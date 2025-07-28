EasyStudy is an intelligent assistant that allows users to upload a PDF, ask questions based on its content, and get accurate responses instantly. It combines the power of LangChain, FAISS vector stores, and a local LLM (via Ollama) to create a seamless question-answering experience.

🚀 Features
📄 Upload any academic or research PDF

🔍 Ask questions based on the document’s content

💡 Instant and context-aware answers

💾 FAISS-powered local vector store for efficient retrieval

🧠 Uses Ollama for local inference (LLaMA3 model)

📦 Tech Stack
Frontend: Streamlit

LLM: Ollama (llama3.2)

Embeddings: HuggingFace (all-MiniLM-L6-v2)

Vector Store: FAISS

Framework: LangChain

🖥️ Setup Instructions
1. Clone the Repository
bash
Copy
Edit
git clone https://github.com/your-username/EasyStudy.git
cd EasyStudy
2. Create Virtual Environment (Optional)
bash
Copy
Edit
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
3. Install Dependencies
bash
Copy
Edit
pip install -r requirements.txt
4. Install and Run Ollama (for LLaMA3.2)
Make sure Ollama is installed and running:

bash
Copy
Edit
ollama run llama3
✅ Tip: You must have llama3.2 available locally. You can pull it by running ollama pull llama3.

🧠 Run the App
bash
Copy
Edit
streamlit run app.py
Then, open http://localhost:8501 in your browser.

📁 File Structure
bash
Copy
Edit
EasyStudy/
│
├── app.py                # Main Streamlit app
├── requirements.txt      # Python dependencies
├── uploaded/             # Folder for uploaded PDFs
├── faiss_index/          # Vector store created for each session
└── README.md             # You're reading it
✍️ How It Works
Upload a PDF file.

The text is extracted and split into chunks.

Text chunks are embedded using a HuggingFace model.

FAISS stores these embeddings locally.

You can now ask questions — the app retrieves relevant chunks and passes them to the LLaMA model for answers.

🔒 Note
This app runs completely offline (no OpenAI key needed).

Ensure you have enough memory for LLaMA3 to run locally via Ollama.


