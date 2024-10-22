
# Naukri Resume Auto-Updater

This is a simple Selenium-based automation script designed to automatically upload your resume on [Naukri](https://www.naukri.com), ensuring that your profile remains up-to-date. Keeping your resume refreshed on job portals like Naukri can significantly improve your visibility to potential employers.

## Features
- Automates the process of logging in to Naukri.
- Uploads a new version of your resume.
- Designed to handle common website interactions such as closing pop-ups.
- Logs the status of each operation for easy monitoring.
- Built with Python and Selenium WebDriver.

## Prerequisites

Before you begin, ensure you have the following installed on your machine:

- [Python 3.6+](https://www.python.org/downloads/)
- [Google Chrome](https://www.google.com/chrome/)
- [ChromeDriver](https://chromedriver.chromium.org/downloads) *(optional, the script will handle it if not installed manually)*

You will also need to create a free account on [Naukri.com](https://www.naukri.com) if you don't have one yet.

## Installation

### 1. Clone the repository
Start by cloning this repository to your local machine using:

```bash
git clone https://github.com/yourusername/naukri-resume-updater.git
cd naukri-resume-updater
```

### 2. Set up a virtual environment (optional but recommended)
To avoid conflicts between dependencies, create and activate a virtual environment:

```bash
# For Windows
python -m venv venv
venv\Scripts\activate

# For macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

### 3. Install required dependencies
Once the virtual environment is set up, install the required packages using the `requirements.txt` file:

```bash
pip install -r requirements.txt
```

### 4. Set up your environment variables
The script uses environment variables for your Naukri credentials. Create a `.env` file in the project directory and add the following:

```bash
# .env file
USERNAME=your_naukri_username
PASSWORD=your_naukri_password
```

Ensure that this file is in the same folder as `run.py`.

### 5. Add your resume
Place your resume in the `resume/` folder, and make sure it's named `Resume.pdf`. You can modify the file path inside the script if needed.

## Running the Script

### Step 1: Start the script

Run the script by executing the following command:

```bash
python run.py
```

The script will:
- Log in to Naukri with your provided credentials.
- Navigate to the resume update section.
- Upload the `Resume.pdf` file located in the `resume/` folder.
- Log the operation status.

### Step 2: Monitor the process
- The script will print logs to the console, informing you of each step being taken.
- If there are any issues during the process (such as incorrect login details or failure to upload the resume), the error messages will be logged.

## Project Structure

```bash
naukri-resume-updater/
├── resume/              # Folder containing your resume (e.g., Resume.pdf)
├── .env                 # File containing Naukri username and password
├── requirements.txt     # Python dependencies
├── README.md            # Project instructions
├── run.py               # Main script for automating the resume update process
└── ...
```

## Troubleshooting

1. **ChromeDriver Issues**: If the script fails to find the Chrome browser, ensure that you have Chrome installed, and ChromeDriver is either installed or automatically handled by `webdriver_manager`.
2. **Environment Variable Errors**: Double-check the `.env` file to ensure your credentials are correct.
3. **Selenium WebDriver Timeout**: Sometimes, Naukri's site may take longer to load. You can adjust the timeout values in `run.py` to wait longer for specific elements to appear.
4. **Resume Not Uploading**: Ensure that your resume is saved as `Resume.pdf` in the `resume/` folder.

## Compatibility

This project has been tested on:
- Windows 10/11
- macOS Sequoia

Make sure you have the correct Python and Chrome versions installed.

## Contributions

Feel free to open issues or submit pull requests for improvements, bug fixes, or new features!

## License

This project is open-source and available under the [MIT License](https://opensource.org/licenses/MIT).
