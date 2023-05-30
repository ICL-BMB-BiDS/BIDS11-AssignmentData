# Assignment_Data
All materials for the assignment can be found here:
- BIDS_assignment_training_data.xlsx
- BIDS_assignment_variable_names.xlsx
- BIDS_assignment_test_data.xlsx
- BIDS_assignment_test_data_predictionsubmissionformat.xlsx

1. Use BIDS_assignment_training_data.xlsx to train your models.
2. Use BIDS_assignment_variable_names.xlsx to find out more about the important variables.
3. Apply your model on BIDS_assignment_test_data.xlsx.
4. Add your test set predictions in BIDS_assignment_test_data_predictionsubmissionformat.xlsx.

If your CID is 01234567 and you are submitting for formative feedback:

5. Save this file as BIDS_2023_01234567_test_predictions_formative.xlsx

If submitting for summative assessment of the coursework:

6. Save this file as BIDS_2023_01234567_test_predictions_coursework.xlsx

Instructions of how to receive formative feedback are provided in BIDS 11 (and re-iterated in BIDS 12).

Here is some example code how you can do this:
```
# change this to the location of the submission file (in folder of assignment data)
Y_pred_format = pd.read_excel('BIDS_assignment_test_data_predictionsubmissionformat.xlsx')
# change this variable (y_pred_test) to whatever you named the predicted class of the assignment test data
Y_pred_format.Predicted_CancerType = y_pred_test # note this was changed from Predicted_group to Predicted_CancerType
# change this to YOUR CID number
CID = '1234567'
# change this for the type of submission (formative or summative)
tp = 'formative'

# do not change anything below
filename1 = 'BIDS_2023_' # do not change this
filename2 = '_test_predictions_' # do not change this
filename3 = '.xlsx' # do not change this
filename = filename1+CID+filename2+tp+filename3 # do not change this
# save the predictions in the format you need to email me (is saved in the folder of the notebook)
Y_pred_format.to_excel(filename)
```
