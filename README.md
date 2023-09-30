import pandas as pd
import matplotlib.pyplot as plt
data = pd.read_csv(r'C:\Users\Praful J\Desktop\Prodigy\Task 5\archive (1)\df.csv')

display(data)


data_sorted = data.sort_values(by="Numbers", ascending=False)

cities = data_sorted["Million Plus Cities"]
total_cases = data_sorted["Numbers"]

plt.figure(figsize=(14, 6))  
plt.bar(cities, total_cases, color='skyblue', width=0.8)  
plt.xlabel("City")
plt.ylabel("Total Number of Cases")
plt.title("Total Cases by City (Descending Order)")
plt.xticks(rotation=45)  
plt.tight_layout()

plt.show()

data_sorted = data.sort_values(by="Numbers", ascending=False)

cause_categories = data_sorted["Cause category"]
total_cases = data_sorted["Numbers"]

plt.figure(figsize=(14, 6))  
bars = plt.bar(cause_categories, total_cases, color='skyblue', width=0.8) 
plt.xlabel("Cause Category")
plt.ylabel("Total Number of Cases")
plt.title("Total Cases by Cause Category (Descending Order)")
plt.xticks(rotation=45) 


plt.show()

 
data_sorted = data.sort_values(by="Numbers", ascending=False)

cause_subcategories = data_sorted["Cause Subcategory"]
total_cases = data_sorted["Numbers"]

plt.figure(figsize=(14, 8))  
plt.barh(cause_subcategories, total_cases, color='skyblue')
plt.ylabel("Cause Subcategory")
plt.xlabel("Total Number of Cases")
plt.title("Total Cases by Cause Subcategory (Descending Order)")
plt.tight_layout()

plt.show()

data_sorted = data.sort_values(by="Numbers", ascending=False)

outcomes = data_sorted["Outcome of Incident"]
total_cases = data_sorted["Numbers"]

plt.figure(figsize=(14, 6))  
plt.bar(outcomes, total_cases, color='skyblue', width=0.8)  
plt.xlabel("Outcome of Incident")
plt.ylabel("Total Number of Cases")
plt.title("Total Cases by Outcome of Incident (Descending Order)")
plt.xticks(rotation=45)  
plt.tight_layout()

plt.show()
