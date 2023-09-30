import pandas as pd
import matplotlib.pyplot as plt
data = pd.read_csv(r'C:\Users\Praful J\Desktop\Prodigy\Task 5\archive (1)\df.csv')

display(data)
Million Plus Cities	Cause category	Cause Subcategory	Outcome of Incident	Numbers
0	Agra	Traffic Control	Flashing Signal	Greviously Injured	0.0
1	Agra	Traffic Control	Flashing Signal	Minor Injury	0.0
2	Agra	Traffic Control	Flashing Signal	Persons Killed	0.0
3	Agra	Traffic Control	Flashing Signal	Total Injured	0.0
4	Agra	Traffic Control	Flashing Signal	Total number of Accidents	0.0
...	...	...	...	...	...
9545	Vizaq	Weather	Sunny/Clear	Greviously Injured	561.0
9546	Vizaq	Weather	Sunny/Clear	Minor Injury	252.0
9547	Vizaq	Weather	Sunny/Clear	Persons Killed	176.0
9548	Vizaq	Weather	Sunny/Clear	Total number of Accidents	1207.0
9549	Vizaq	Weather	Sunny/Clear	Total Injured	813.0
9550 rows × 5 columns

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
