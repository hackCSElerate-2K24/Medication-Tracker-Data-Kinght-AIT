# Data Kinght-AIT
MedicationExpirationTracker



Project Description



Our project helps users keep track of medication expiry dates by scanning labels using a camera. By utilizing Optical Character Recognition (OCR), it extracts key details such as the medication name, expiry date, and dosage from the label images. The extracted data is then stored in a database, allowing users to easily access and monitor their medications. This solution aims to prevent the use of expired medications, improving safety and ensuring that medications are consumed within their recommended timeframes.


Installation


To set up the Medication Expiration Tracker project locally, follow these detailed steps:

1. System Requirements


    Operating System: Windows, macOS, or Linux.

    Python Version: 3.7 or higher.
   
    Package Manager: pip for installing dependencies.
   
    Database: SQLite


   
3. Clone the Repository

4. 
    First, clone the project repository from GitHub (or your project's source).
    git clone https://github.com/jnanasahana/medication-expiration-tracker.git
    cd medication-expiration-tracker
5. Set up a Virtual Environment (Optional but recommended)

6. 
    It's best to set up a virtual environment to manage dependencies for the project.

    bash
      python3 -m venv venv

   
    Activate the virtual environment:

    On Windows:

   bash
   
       venv\Scripts\activate
   
    On macOS/Linux:
   
    bash
   
        source venv/bin/activate
   
 8. Install Dependencies

 9. 
     Install the necessary Python packages by running:
    
     bash
    
       pip install -r requirements.txt
    
    The requirements.txt file contains all the dependencies needed for the project. Key libraries may include:
    
    OpenCV: For image processing and scanning.
    
    Pillow: For image manipulation.
    
    Tesseract OCR: For optical character recognition (OCR).
    
    Flask/Django: If the project uses a web framework.
    
    SQLite/MySQL: For database management.
    
    For OCR, you may need to install Tesseract separately:

    Windows: Download Tesseract from here.
    
    macOS:
    
    bash
    
      brew install tesseract
    
    Linux:
    
    bash
    
      sudo apt install tesseract-ocr
    
11. Configure Database (Optional)
12. 
    The project uses SQLite by default, but you can configure it to use another database (like MySQL or 
    PostgreSQL) by modifying the database configuration file (config.py or equivalent).
    
    SQLite: The database file is typically stored locally as database.db.
    
14. Configure Environment Variables (if needed)
15. 
    Some projects may require environment variables for secret keys or API credentials (e.g., for OCR 
    services or database connections).

    Create a .env file in the project root directory and add any necessary environment variables. Example:
  javascript

     DATABASE_URI=sqlite:///database.db
    
     OCR_ENGINE_PATH=/path/to/tesseract
    
17. Run Migrations (for databases)
18. 
    If your project includes database migrations (e.g., using Flask-Migrate or Django migrations), run 
    the migrations to set up the database schema.

   For Flask:
   
   bash
   
      flask db upgrade
      
   For Django:
   
   bash
   
      python manage.py migrate
      
11. Run the Application
12. 
    Start the application locally. Depending on your project setup, you may run it with a web framework 
    like Flask or Django:

   For Flask:
   
   bash
   
      flask run
      
   For Django:
   
   bash
   
      python manage.py runserver
      
  By default, this will run the application on http://localhost:5000 for Flask or http://localhost:8000 
  for Django.

11. Test the OCR Functionality
12. 
    After the server is running, you can test the OCR feature by uploading images of medication labels 
    through the app's interface. Make sure that the Tesseract OCR engine is correctly set up.
    
    Check the logs if there are issues with the OCR or image processing functionality.
    
    Ensure the medication data (name, expiry date, and dosage) is extracted correctly from the image and 
    saved in the database.
    
14. Optional: Frontend Setup
15. 
     If the project includes a frontend (e.g., React or Angular), you may need to install additional 
     dependencies and run the frontend server:
    
    Navigate to the frontend directory (if applicable) and run:
    
    bash
    
       npm install
    
       npm start
    
17. Access the Application
18. 
     Once the application is running, open your browser and go to http://localhost:5000 (or the 
     appropriate port) to interact with the Medication Expiration Tracker.
    
   Troubleshooting Tips:
   
      Missing dependencies: Make sure all libraries listed in requirements.txt are installed.
      
      OCR issues: Ensure Tesseract is installed correctly and the path is set in the environment 
       variables.
      Database connection errors: Check your database configuration and ensure it's running correctly.
