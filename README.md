# HackerEarth_RestaurantBillAmount_NLP_Model
**NLP model that process an invoice or receipt in PDF format and output the total amount mentioned in it.**
***
Download the dataset [here](https://www.hackerearth.com/challenges/competitive/hackerearth-deep-learning-challenge-emotion-detection-tom-jerry-cartoon/)
***
**Steps in the notebook:**
 1. Loading the data into colab notebook.
 2. Convert the pdf into images using pdf2image.
 3. Change the resolution of the images to 400 dpi.
 4. Extract the text from images with custom config having pattern like *TotalTOTALAmountCashTLDue$0123456789* using pytesseract.image_to_string
 5. Merge the text in a list and split using new line to fetch lines having **total, amount, cash, tl, total due** words.
 6. Searching the float values from the above lines and storing the highest float amount in a list and appending 0 for non recognizable amounts with pattern *\d+\.\d+*
 7. Reiterating the list in step 6 with different patterns viz. *'\d+\. +\d+'* and *'\d+ +\.\d'* and *'\d+ +\. +\d'* to research the zero entries got in step 6.
 8. Write the results in a csv file.
 ***
 **Observation**: Accuracy of the model obtained 36.54%
***
To check out my notebook, please click [here](https://github.com/Qadir92/HackerEarth_RestaurantBillAmount_NLP_Model/blob/main/Restaurant_Bill.ipynb)
