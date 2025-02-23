# 🚀 RAG Backend Assignment (Ringg.Ai)

## 📌 Overview  
This project is a **Retrieval-Augmented Generation (RAG) backend system** built using **Node.js, Express, and Weaviate**. It enables **document ingestion, storage, and querying** via a **vector database** with an intuitive React-based frontend.  

---

## 🏗️ System Architecture & Workflow  

### 🔹 Components:
1. **Backend (Node.js, Express, Weaviate)**  
   - Handles file uploads, text extraction, and chunk storage in Weaviate.  
   - Processes queries and retrieves relevant document chunks.  

2. **Frontend (React)**  
   - Allows users to upload documents and query stored data.  
   - Supports **PDF, DOCX, TXT uploads** but not JSON.  
   - **Live Deployment:** [RAG Frontend](https://rag-bakend-assignment-deploy-1-77cf.onrender.com)  

3. **Weaviate (Vector Search Engine)**  
   - Stores document embeddings for efficient retrieval.  

---

## ⚙️ Features  

✅ **File Upload & Processing**  
- Uploads **PDF, DOCX, TXT** via UI or API.  
- Extracts text, splits it into chunks, generates embeddings, and stores them.  

✅ **Vector-Based Search**  
- Queries stored text chunks using **NearVector search**.  
- Filters results by document ID.  

✅ **JSON Data Handling**  
- Supports **mathematical & statistical operations** (sum, avg, variance, etc.).  
- JSON objects stored dynamically in Weaviate.  

✅ **Scalable API Endpoints**  
- RESTful API for **file upload, querying, and JSON statistics**.  

✅ **Bulk Testing (Python Scripts)**  
- Automated **text & JSON file uploads** for testing.  
- Query testing with stored document IDs.  

---

## 🔥 API Endpoints  

### 📂 **File Upload**
- **URL:** `/api/files/upload`  
- **Method:** `POST`  
- **Body:** `multipart/form-data` with `document`  
- **Response:** `{ message: 'File processed successfully', documentId, fileName, extractedText }`  

### 🔍 **Search Query (Text)**
- **URL:** `/api/search/search`  
- **Method:** `POST`  
- **Body:** `{ query: "your search query" }`  
- **Response:** Array of relevant document snippets.  

### 📊 **JSON Statistics (Computations)**
- **URL:** `/api/json/json_stats`  
- **Method:** `GET`  
- **Query Params:** `document_id, field, operation`  
- **Supported Operations:** `max, min, sum, average, variance, std_dev, count_above, count_below, group_by`  

### 📥 **JSON Upload**
- **URL:** `/api/json/json_upload`  
- **Method:** `POST`  
- **Body:** `multipart/form-data` with `document`  
- **Response:** `{ message: 'JSON Uploaded successfully', json_global_id, fileName }`  

---

## 🛠️ Running the Project Locally  

### 📌 **1. Clone the Repository**
```sh
git clone https://github.com/shubham212001/RAG_backend_repo
cd RAG_backend_repo
```

### ⚙️ **2. Backend Setup**
```sh
cd backend
npm install
```
Create a `.env` file:
```env
PORT=4000
REACT_APP_WCD_URL=<your-weaviate-url>
REACT_APP_WCD_API_KEY=<your-weaviate-api-key>
REACT_APP_OPENAI_KEY=<your-openai-api-key>
```
Start the backend:
```sh
npm start
```

### 💻 **3. Frontend Setup**
```sh
cd frontend
npm install
```
Modify `frontend/src/App.js`:
```js
const url = "http://localhost:4000";
```
Start the frontend:
```sh
npm start
```
Access UI at: [http://localhost:3000](http://localhost:3000)  

---

## 🔬 **API Testing with Python Scripts**  

### 📌 **1. Bulk Upload & Query (Text Data)**
```sh
python APItesting/Text/textFilesUpload.py
python APItesting/Text/textQueries.py
```

### 📌 **2. Bulk Upload & Query (JSON Data)**
```sh
python APItesting/Json/JsonUpload.py
python APItesting/Json/JsonGetStats.py
```

---

## 🚀 **Potential Improvements**
🔹 Implement **caching** to speed up retrieval.  
🔹 Add **unit & integration tests** for stability.  
🔹 Improve **error handling & scalability**.  

---

## 📞 **Contact**
**Shubham Sharma**  
📧 Email: [shubham.sharma200121@gmail.com](mailto:shubham.sharma200121@gmail.com)  
🔗 GitHub: [shubham212001](https://github.com/shubham212001)  

---

⭐ **If you found this helpful, drop a ⭐ on the repo!**  

