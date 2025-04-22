# Moodify Project Structure

## AudioWAV  
Folder with train-test samples

## Code  
Folder with all the code

## file_organization.txt  
Descriptions of all the files present in the project

## Presentation_HAL 9000.pptx.pdf  
Presentation used to explain the project

## Project Final Report - HAL9000.docx.pdf  
Report on ideas and outcomes of the project

## README.pdf  
Document detailing how to run the project in different modes

---

### ./AudioWAV  
Folder inside which all the samples are present

### ./Code  
Folder where all the code resides  
- **App/** - Folder for the web app  
- **moodify-method_1.ipynb** - Code for method 1 without data augmentation  
- **moodify-method_2.ipynb** - Code for method 2 with data augmentation  
- **requirements.txt** - pip file for installing all necessary libraries

---

### ./Code/App  
- **app.py** - Code with streamlit for web app  
- **best_model.h5** - File used for storing model data of the best model  
- **label_encoder.pkl** - Label encoder used to stream serialized data structure bytes to disk  
- **scaler.pkl** - pickle file for scaling the data
