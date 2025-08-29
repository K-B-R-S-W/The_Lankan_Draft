# 🏏 The Lankan Draft

<div align="center">

![Cricket](https://img.shields.io/badge/Cricket-🏏-green?style=for-the-badge)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-🤖-blue?style=for-the-badge)
![Python](https://img.shields.io/badge/Python-3.8%2B-brightgreen?style=for-the-badge&logo=python)
![Flask](https://img.shields.io/badge/Flask-2.3.3-red?style=for-the-badge&logo=flask)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

**A sophisticated machine learning-based web application to analyze player performance and assist in selecting the optimal Sri Lankan cricket squad across T20, ODI, and Test formats.**

[🚀 Demo](#-demo) • [📋 Features](#-features) • [⚡ Quick Start](#-quick-start) • [🔧 Installation](#-installation) • [📖 Usage](#-usage)

</div>

---

## 🌟 Overview

The **The Lankan Draft** leverages advanced machine learning algorithms to revolutionize cricket team selection. By analyzing comprehensive player statistics across multiple formats, our system provides data-driven insights for optimal team composition.

### 🎯 What Makes This Special?

- **🔬 ML-Powered Analysis**: Uses Random Forest algorithms to predict player performance
- **🏆 Multi-Format Support**: Covers T20, ODI, and Test cricket formats
- **📊 Comprehensive Data**: Analyzes batting, bowling, and overall player statistics
- **🌐 Modern Web Interface**: Clean, responsive UI with dark/light mode toggle
- **⚡ Real-Time Predictions**: Instant team selection based on current form
- **🏗️ Modular Architecture**: Well-organized codebase with separated prediction logic
- **📈 Updated Player Database**: Latest Sri Lankan cricket player statistics

---

## 🛠 Tech Stack

### Backend
- **🐍 Python 3.8+** - Core programming language
- **🌐 Flask 2.3.3** - Web framework for API development
- **🔗 Flask-CORS** - Cross-origin resource sharing
- **🤖 Scikit-learn** - Machine learning algorithms
- **📊 Pandas** - Data manipulation and analysis
- **🔢 NumPy** - Numerical computing

### Frontend
- **🎨 HTML5 & CSS3** - Modern web standards
- **⚡ JavaScript (ES6+)** - Interactive functionality
- **📱 Responsive Design** - Mobile-first approach

### Data & ML
- **📈 Random Forest Classifier** - Player performance prediction
- **💾 CSV Data Storage** - Player statistics database
- **🎯 Joblib Models** - Serialized ML models for deployment

---

## 📋 Features

### 🎯 Core Features
- ✅ **Smart Player Selection** - AI-driven team composition
- ✅ **Multi-Format Analysis** - T20, ODI, and Test match optimization
- ✅ **Performance Metrics** - Comprehensive batting & bowling statistics
- ✅ **Real-Time API** - RESTful endpoints for team predictions
- ✅ **Interactive Dashboard** - User-friendly web interface

### 🔮 Advanced Features
- 🎨 **Dark/Light Theme** - Customizable UI experience
- 📱 **Mobile Responsive** - Works seamlessly on all devices
- ⚡ **Fast Predictions** - Sub-second response times
- 📊 **Data Visualization** - Player performance insights
- 🔄 **Dynamic Updates** - Easy player database management

---

## 🚀 Quick Start

### Prerequisites
- Python 3.9 or higher
- pip package manager

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/yourusername/The_Lankan_Draft.git
cd The_Lankan_Draft
```

### 2️⃣ Install Dependencies
```bash
# Install core requirements
pip install -r requirements.txt

# Or minimal setup
pip install -r requirements-core.txt
```

### 3️⃣ Run the Application
```bash
# Navigate to Backend directory
cd Backend

# Start the Flask server
python App.py
```

### 4️⃣ Access the Application
- **API Endpoint**: `http://localhost:5000`
- **Health Check**: `http://localhost:5000/health`
- **Web Interface**: Open `Frontend/index.html` in your browser

---

## 🔧 Installation

### 🐍 Virtual Environment Setup (Recommended)
```bash
# Create virtual environment
python -m venv cricket_env

# Activate environment
# Windows:
cricket_env\Scripts\activate
# macOS/Linux:
source cricket_env/bin/activate

# Install dependencies
pip install -r requirements.txt
```

### 🔧 Conda Environment Setup (Alternative)
```bash
# Create conda environment
conda create -n cricket_env python=3.9

# Activate environment
conda activate cricket_env

# Install dependencies
pip install -r requirements.txt
```

### 📦 Package Installation
```bash
# Core packages
pip install Flask==2.3.3 Flask-CORS==4.0.0
pip install pandas==2.1.4 numpy==1.24.3
pip install scikit-learn==1.3.2 joblib==1.3.2

# Development packages (optional)
pip install jupyter matplotlib seaborn
```

---

## 📖 Usage

### 🌐 API Endpoints

#### Health Check
```http
GET /health
```
**Response:**
```json
{
    "status": "ok"
}
```

#### Team Prediction
```http
GET /predict/<format>
```
**Formats:** `test`, `odi`, `t20`

**Example Response:**
```json
{
    "success": true,
    "match_type": "ODI",
    "team": [
        {
            "playerId": "1",
            "name": "Charith Asalanka",
            "role": "Batting Allrounder",
            "age": "28y 18d",
            "batting_style": "Left hand Bat",
            "bowling_style": "Right arm Offbreak",
            "category": "Allrounder"
        }
    ],
    "total_players": 11,
    "batters": 6,
    "bowlers": 5
}
```

### 🖥 Web Interface

1. **Home Page**: Select cricket format (T20/ODI/Test)
2. **Team Display**: View selected players with detailed statistics
3. **Player Cards**: Interactive cards showing player information
4. **Theme Toggle**: Switch between dark and light modes

---

## 📊 Project Structure

```
The_Lankan_Draft/
├── 📁 Backend/
│   ├── 🐍 App.py                 # Flask API server
│   ├── 📁 prediction_scripts/    # Team selection logic
│   │   ├── 🏏 ODI_main.py       
│   │   ├── 🏏 T20_main.py       
│   │   └── 🏏 Test_main.py      
│   ├── 📊 Data/
│   │   ├── players.csv          # Player database
│   │   ├── ODI_bat.csv          # ODI batting statistics
│   │   ├── ODI_ball.csv         # ODI bowling statistics
│   │   ├── T20_Bat.csv          # T20 batting statistics
│   │   ├── T20_Ball.csv         # T20 bowling statistics
│   │   ├── Test_Bat.csv         # Test batting statistics
│   │   └── Test_Ball.csv        # Test bowling statistics
│   └── 🤖 Models/
│       ├── bat_model_odi.pkl    # ODI batting model
│       ├── bowl_model_odi.pkl   # ODI bowling model
│       ├── bat_model_t20.pkl    # T20 batting model
│       ├── bowl_model_t20.pkl   # T20 bowling model
│       ├── bat_model_test.pkl   # Test batting model
│       └── bowl_model_Test.pkl  # Test bowling model
├── 🌐 Frontend/
│   ├── 🏠 index.html           # Main landing page
│   ├── 🏏 odi.html             
│   ├── 🏏 t20.html             
│   ├── 🏏 test.html            
│   ├── 🖼️ bg.jpg               
│   └── 🎨 logo.png             
├── 📓 Model_Training_scripts/
│   ├── ODI_train.ipynb         # ODI model training
│   ├── T20_train.ipynb         # T20 model training
│   └── testTrain.ipynb         # Test model training
├── 📋 requirements.txt          # Full dependencies
├── 📋 requirements-core.txt     # Core dependencies
└── 📖 README.md                
```

---

## 🧠 Machine Learning Pipeline

### 📈 Data Processing
1. **Data Collection**: Player statistics from various cricket databases
2. **Feature Engineering**: Batting average, strike rate, bowling economy, etc.
3. **Data Cleaning**: Handle missing values and outliers
4. **Normalization**: Standardize numerical features

### 🤖 Model Training
1. **Random Forest Classifier**: Separate models for batting and bowling
2. **Feature Selection**: Identify key performance indicators
3. **Model Validation**: Cross-validation and performance metrics
4. **Hyperparameter Tuning**: Optimize model parameters

### 🎯 Prediction Logic
1. **Batting Selection**: Top 6 players based on batting performance
2. **Bowling Selection**: Top 5 bowlers (excluding selected batters)
3. **Team Balance**: Ensure diverse playing roles and styles
4. **Final Team**: 11 players optimized for the selected format

---

## 🔮 Future Enhancements

- 📊 **Advanced Analytics**: Player comparison and trend analysis
- 🌍 **Multi-Team Support**: Extend to other cricket teams
- 📱 **Mobile App**: Native iOS/Android applications
- 🔄 **Real-Time Updates**: Live match data integration
- 🎯 **Match Simulation**: Predict match outcomes
- 📈 **Performance Tracking**: Historical performance analysis

---

## 🤝 Contributing

We welcome contributions! Here's how you can help:

1. **🍴 Fork the Repository**
2. **🌿 Create a Feature Branch**
   ```bash
   git checkout -b 
   ```
3. **✍️ Commit Your Changes**
   ```bash
   git commit -m 
   ```
4. **📤 Push to Branch**
   ```bash
   git push origin 
   ```
5. **🔄 Open a Pull Request**

### 📝 Contribution Guidelines
- Follow Python PEP 8 style guidelines
- Add tests for new features
- Update documentation as needed
- Ensure backward compatibility

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- **Sri Lanka Cricket Board** - For inspiring this project
- **Cricket Statistics Community** - For valuable data insights
- **Open Source Contributors** - For the amazing tools and libraries
- **ML Community** - For algorithms and best practices

---

## 📮 Support

**📧 Email:** [k.b.ravindusankalpaac@gmail.com](mailto:k.b.ravindusankalpaac@gmail.com)  
**🐞 Bug Reports:** [GitHub Issues](https://github.com/K-B-R-S-W/The_Lankan_Draft/issues)  
**📚 Documentation:** [Project Wiki](https://github.com/K-B-R-S-W/The_Lankan_Draft/wiki)  
**💭 Discussions:** [GitHub Discussions](https://github.com/K-B-R-S-W/The_Lankan_Draft/discussions)  

---

## ⭐ Support This Project
If you find this project helpful, please give it a **⭐ star** on GitHub — it motivates me to keep improving! 🚀