# Recording-and-predicting-school-progress
import csv
from datetime import date 
import matplotlib.pyplot as plt
hours=float(input("how many hours you stady per day"))
if hours>5:
        print("will done")    
else:
     print("good but you can do better")
with open("study_file", "a",) as file:
   file.write(str(hours)+"\n")         
hours_list = []
with open("study_file", "r") as file:
    for line in file:
        hours_list.append(float(line.strip()))
        average = sum(hours_list) / len(hours_list)
        if average>10:
             print("too much work its bad for your healt and ou wont emprove correctly")
        elif average>6:
             print("very good iu are amproving")
        elif average>3:
          print("nice but you can do better")
        else:
             print("you are not emproving")
