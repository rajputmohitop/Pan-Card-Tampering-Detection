# Pan Card Tampering Detection

A Flask-based web application that detects tampering in Pan Card images using image processing and structural similarity analysis.

## Features
- Upload Pan Card images for tampering detection
- Automatic comparison with reference image
- Visual highlighting of differences
- Similarity score and Real/Fake classification
- Sample images included for testing

## Prerequisites
- Python 3.7 or higher
- pip (Python package manager)

## Installation Steps

### Option 1: Using Virtual Environment (Recommended for Windows/Mac/Linux)
```bash
# Step 1: Clone or download the project
git clone <repository-url>
cd Pan\ Card\ Tampering\ Detection

# Step 2: Create virtual environment
python -m venv .venv

# Step 3: Activate virtual environment
# On Windows:
.\.venv\Scripts\activate
# On Mac/Linux:
source .venv/bin/activate

# Step 4: Install dependencies
pip install -r requirements.txt

# Step 5: Run the application
python app.py
```

### Option 2: Using Conda
```bash
# Step 1: Clone or download the project
git clone <repository-url>
cd Pan\ Card\ Tampering\ Detection

# Step 2: Create conda environment
conda create -n pan-card-detection python=3.9

# Step 3: Activate environment
conda activate pan-card-detection

# Step 4: Install dependencies
pip install -r requirements.txt

# Step 5: Run the application
python app.py
```

## Running the Application

Once started, the application will be available at:
```
http://127.0.0.1:5000/
```

1. Open your browser and navigate to the URL above
2. Click "BROWSE" to upload a Pan Card image
3. Click "CHECK" to analyze the image
4. View the results showing similarity score and Real/Fake classification

## Testing
Sample Pan Card images for testing are available in the `sample_data/` folder:
- `original.jpg` - Original Pan Card image
- `tampered.jpg` - Tampered Pan Card image for testing

## Project Structure
```
├── app.py                          # Main Flask application entry point
├── config.py                       # Configuration settings
├── requirements.txt                # Python dependencies
├── app/
│   ├── __init__.py                # Flask app initialization
│   ├── views.py                   # Flask routes and logic
│   └── static/
│       ├── uploads/               # User uploaded images
│       ├── original/              # Reference Pan Card image
│       ├── generated/             # Generated comparison images
│       ├── css/                   # Stylesheets
│       └── js/                    # JavaScript files
└── sample_data/                   # Sample images for testing
```

## Dependencies
All required Python packages are listed in `requirements.txt` and will be installed automatically during setup.

## Notes
- This is a development server. For production deployment, use a production WSGI server like Gunicorn
- The application creates necessary directories automatically on first run
- Make sure to have at least 500MB free space for dependencies
