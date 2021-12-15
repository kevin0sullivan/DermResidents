# DermResidents
Analysis of Dermatological Residents' Efficacy Progression Against 10+ Year Attendings using Python.
Implementation of Numpy and Matplotlib.

DataConstruction manipulates a json file exported from Google Sheets and organizes the data structure into a dictionary.  It additionally takes in an existing dictionary of each resident mapped to their start date. The resulting dictionary maps each resident to a subbdictionary of diagnostic cases, for which the date is the number of days since the resident's start date and the diagnostics success or failure is represented as a boolean.

Analysis makes in the DataConstruction's nested dictionary as well as a desired time interval to break up the length of the residency.  This allows for any possible dt analyisis to identify growth on the scale of a weekly, to a quarterly, to an annual basis.  Analysis constructs another dictionary mapping each resident to a subdictionary mapping each unit time segment to the resident's diagnostic success represented as a tuple (num_successes, num_total).
