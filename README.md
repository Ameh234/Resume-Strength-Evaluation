

```markdown
# Resume Strength Evaluation

A Flask-based web application that analyzes resumes against job-specific keywords and provides optimization feedback.

## Features
- Scores resumes on a 0-100 scale
- Identifies missing industry-specific keywords
- Checks for essential resume sections (Experience, Education, Skills)
- Supports Data Science and Marketing job targets

## Prerequisites
- Python 3.7+
- pip package manager

## Installation

1. Clone the repository:
```bash
git clone https://github.com/Ameh234/Resume-Strength-Evaluation.git
cd resume-optimizer
```

2. Create and activate a virtual environment (recommended):
```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

## Setup

1. Create required directories:
```bash
mkdir -p model data/industry_keywords static
```

2. Add keyword files:
```bash
echo -e "python\nmachine learning\ndata analysis" > data/industry_keywords/data_science.txt
echo -e "seo\ngoogle ads\nsocial media" > data/industry_keywords/marketing.txt
```

3. Train the model:
```bash
python train_model.py
```

## Usage

1. Start the Flask development server:
```bash
python app.py
```

2. Access the application at:
```
http://localhost:5000
```

3. In the web interface:
   - Select a job target
   - Paste your resume text
   - Click "Analyze Resume"

## Project Structure
```
resume-optimizer/
├── app.py                # Main application
├── train_model.py        # Model training script
├── requirements.txt      # Dependencies
├── templates/
│   ├── index.html        # Input form
│   └── result.html       # Results page
├── model/                # Saved models
├── data/
│   └── industry_keywords/ # Job-specific keywords
└── static/               # Static files
```

## Limitations
- Currently uses a small training dataset
- Only supports plain text input (no file upload)
- Limited to Data Science and Marketing roles




