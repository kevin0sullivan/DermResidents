# DermResidents
Analysis of Dermatological Residents' Efficacy Progression Against 10+ Year Attendings using Python.
This project contains implementation of Numpy and Matplotlib.

DataConstruction manipulates a json file exported from Google Sheets and organizes the data structure into a dictionary.  It additionally takes in an existing dictionary of each resident mapped to their start date. The resulting dictionary maps each resident to a subbdictionary of diagnostic cases, for which time is represented as the number of days since the resident's start date and the diagnostic success or failure is represented as a boolean.

Analysis takes in the DataConstruction's nested dictionary as well as a desired time interval to break up the length of the residencies into equal portions.  This allows for any possible dt analyisis to identify growth on weekly, to quarterly, to annual scales.  Analysis constructs another dictionary mapping each resident to a subdictionary mapping each unit time segment to the resident's diagnostic success represented as a tuple (num_successes, num_total).