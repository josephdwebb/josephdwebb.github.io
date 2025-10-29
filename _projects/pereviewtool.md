---
layout: project
title: 'PE Review Tool'
caption: A user-friendly desktop application for manually reviewing and validating AI predictions for pulmonary embolism detection.
description: >
  Development and implementation of an intuitive software solution for medical professionals to validate AI-driven PE detection in radiology reports.
date: '01-10-2025'
image:
  path: https://i.imgur.com/vX18Q6t.png
  srcset:
    1920w: https://i.imgur.com/vX18Q6t.png
    960w:  https://i.imgur.com/vX18Q6t.png
    480w:  https://i.imgur.com/vX18Q6t.png
links:
  - title: GitHub
    url: https://github.com/josephdwebb/PE-Review-Tool
sitemap: false
---

Introducing **PE Review Tool**, a desktop application designed to support medical professionals in their critical work of reviewing and validating AI predictions for pulmonary embolism (PE) detection in radiology reports. This tool bridges the gap between automated AI analysis and human expertise, providing a streamlined interface that allows clinicians to efficiently review medical reports alongside predictions from multiple machine learning models including SVM, LLM, and Regex-based systems.

The PE Review Tool simplifies the validation workflow by presenting full medical report text with PE-related keywords intelligently highlighted, enabling rapid identification of relevant clinical information. Reviewers can systematically document their findings including PE presence, anatomical location, acuity, laterality, and burden assessments. With built-in progress tracking, keyboard shortcuts for efficient navigation, and automatic saving functionality, this tool empowers medical professionals to maintain high-quality validation datasets while minimizing repetitive tasks.

## Installation
If you would like to use the `PE Review Tool` yourself, please refer to the following steps regarding installation and setup.

### Step 1: System Requirements

Ensure your system meets the following requirements:
- **Operating System**: Windows 10+, macOS 10.14+, or Linux
- **Python**: Version 3.8 or higher
- **RAM**: 4GB minimum (8GB recommended)
- **Required Libraries**: pandas, tkinter (included with Python)

### Step 2: Downloading the Project

1. Visit [PE Review Tool](https://github.com/josephdwebb/PE-Review-Tool) on GitHub.
2. Clone the repository to your local machine using Git or GitHub Desktop.
3. Alternatively, download the repository as a ZIP file and extract it to your desired location.

### Step 3: Preparing Your Data

1. Prepare your CSV data file containing the medical reports and AI predictions.
2. Open the `config.ini` file in the project directory.
3. Update the filename parameter to match your CSV data file name.

### Step 4: Running Setup

1. Navigate to the project directory on your local machine.
2. **For Windows**: Double-click `setup.bat` to run the setup script.
3. **For Mac/Linux**: Run `setup.sh` from the terminal to install dependencies.

This step will ensure all necessary Python packages are installed and configured properly.

### Step 5: Launching the Application

1. **For Windows**: Double-click `run.bat` to launch the PE Review Tool.
2. **For Mac/Linux**: Execute `run.sh` from the terminal to start the application.

The application window will open, displaying the first report ready for review.

## Using PE Review Tool
The PE Review Tool provides an intuitive interface with the following key features:

### Review Interface

| Feature | Description |
|---------|-------------|
| Report Display | Full medical report text with PE-related keywords highlighted in yellow |
| AI Predictions | Shows predictions from multiple models (SVM, LLM, Regex) |
| Review Form | Record PE presence, location, acuity, laterality, and burden |
| Progress Bar | Visual indication of review completion percentage |
{:.scroll-table-small}

### Navigation Controls

The application supports efficient navigation through keyboard shortcuts:
- **Next Report**: Move to the next report in sequence
- **Previous Report**: Return to the previous report
- **Skip to Unreviewed**: Jump to the next unreviewed report
- **Go to Report**: Navigate directly to a specific report number

### Auto-Save Functionality

All reviews are automatically saved back to the CSV file, ensuring no data loss during the validation process. Progress statistics are continuously updated to track completion status.

**Example Workflow**:
1. Review the displayed medical report and highlighted keywords
2. Examine AI model predictions for comparison
3. Complete the review form with your clinical assessment
4. Navigate to the next report using keyboard shortcuts or buttons
5. Monitor progress through the visual progress bar

## Help
For technical support, bug reports, or feature requests, please visit the [GitHub Issues Page](https://github.com/josephdwebb/PE-Review-Tool/issues). You can also contact Joseph at josephwebb4@hotmail.com for additional assistance or feedback.

For more information and updates, please visit the [GitHub Page](https://github.com/josephdwebb/PE-Review-Tool) and feel free to contribute to the project.
