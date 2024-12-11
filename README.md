# Translating Burkina

## Project Overview
This application is a language translator for underrepresented African languages, such as **Tawellemmet** and **Bambara**. It uses a **Flask API backend** powered by PyTorch models, a **React.js frontend**, and **Docker** for seamless deployment.

---

## File Structure (Supports Additional Languages)
```
translator-app/
├── backend/                   # Backend API & Model Training
│   ├── app.py                 # Flask API
│   ├── train.py               # Model training
│   ├── Dockerfile             # Docker backend configuration
│   ├── data/                  # Dataset corpus files
│   │   ├── tawellemmet-en/    # Tawellemmet-English corpus
│   │   │   ├── source.txt     # Tawellemmet sentences
│   │   │   └── target.txt     # English translations
│   │   ├── bambara-en/        # Bambara-English corpus
│   │   │   ├── source.txt     # Bambara sentences
│   │   │   └── target.txt     # English translations
│   │   ├── [new-language]/    # Additional languages can be added here
│   │   │   ├── source.txt     # Source sentences for new language
│   │   │   └── target.txt     # Corresponding English translations
│   └── requirements.txt       # Backend dependencies
│
├── frontend/                  # React.js frontend
│   ├── src/                
│   │   ├── App.js             # Main React app file
│   │   ├── index.js           # React entry point
│   │   └── App.css            # CSS styles
│   ├── public/
│   │   └── index.html         # Frontend HTML entry
│   └── Dockerfile             # Docker frontend configuration
│
├── models/                    # Trained models storage
│   └── tawellemmet-en/        # Tawellemmet model folder
│   └── bambara-en/            # Bambara model folder
│   └── [new-language]/        # Placeholder for additional language models
│
├── docker-compose.yml         # Docker Compose for multi-service setup
└── README.md                  # Project documentation
```

---

## Setup Instructions

### **1. Clone the Repository**
```bash
git clone https://github.com/your-repo/translator-app.git
cd translator-app
```

---

### **2. Backend Setup**
1. **Install Dependencies:**
   ```bash
   cd backend
   pip install -r requirements.txt
   ```

2. **Run Flask API:**
   ```bash
   python app.py
   ```

---

### **3. Frontend Setup**
1. **Install Dependencies:**
   ```bash
   cd frontend
   npm install
   ```

2. **Start React App:**
   ```bash
   npm start
   ```

---

### **4. Docker Deployment**
1. **Build and Start the Application:**
   ```bash
   docker-compose up --build
   ```

2. **Access the Application:**
   - **Frontend:** [http://localhost:3000](http://localhost:3000)
   - **Backend API:** [http://localhost:5000](http://localhost:5000)

---

## Usage
1. Enter text into the **translation text box** on the React frontend.
2. Select the desired **language pair**.
3. Click the **Translate** button.
4. View the **translated text result** below.

---

## Troubleshooting
- **Port Conflicts:** Ensure ports `5000` and `3000` are not used by other services.
- **Model Not Loading:** Ensure models are stored in `models/` after training.
- **Dataset Missing:** Verify `backend/data/` contains proper `source.txt` and `target.txt` files.

---

## Contributing
1. Fork the repository.
2. Create a feature branch (`git checkout -b feature-name`).
3. Commit changes (`git commit -m "Add feature"`).
4. Push the branch (`git push origin feature-name`).
5. Open a pull request.

---

## License
This project is licensed under the **GNU General Public License (GPL)**. See the `LICENSE` file for more details.
