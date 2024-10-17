# EX8-Implementation of Hierarchical Clustering using linkage methods
## DATE:
## AIM:
To implement Hierarchical Clustering using single and complete linkage method

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Compute the distance matrix between all data points.

2.Identify the two closest cluster and merge them.

3.Update the distance matrix to reflect the new cluster.

4.Repeat steps 2 and 3 until only one cluster remains.

## Program:
```
/*
Program to implement Hierarchical Clustering using single and complete linkage method
Developed by:K.TAMIL MARUDHU
RegisterNumber:2305001033  
*/
```
```
Program to implement Hierarchical Clustering using single and complete linkage method
Developed by: Madhu Mitha V
RegisterNumber: 2305002013
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt 
from scipy.cluster.hierarchy import dendrogram, linkage, fcluster 
from sklearn.preprocessing import StandardScaler
df=pd.read_csv("/content/Hclus_EX8.csv")
df.head()
X=df[['StudentID','Marks']].values
X
Z=linkage(X,method='complete')
plt.figure(figsize=(5,2))
plt.title("Dentogram for Student Segmentation")
labels=range(1,len(df)+1)
dendrogram(Z,labels=labels)
plt.xlabel("Student ID")
plt.ylabel("Marks")
plt.show()
max_clusters=2
clusters=fcluster(Z,max_clusters,criterion='maxclust')
clusters
plt.figure(figsize=(5,2))
plt.scatter(X[:,0],X[:,1],c=clusters,cmap='rainbow',s=100)
plt.title("Student Segmented (Hierarchical Clustering)")
plt.xlabel("Student ID")
plt.ylabel("Marks")
plt.show()
Z=linkage(X,method='single')
plt.figure(figsize=(5,2))
plt.title("Dentogram for Student Segmentation")
labels=range(1,len(df)+1)
dendrogram(Z,labels=labels)
plt.xlabel("Student ID")
plt.ylabel("Marks")
plt.show()
max_clusters=2
clusters=fcluster(Z,max_clusters,criterion='maxclust')
clusters
plt.figure(figsize=(5,2))
plt.scatter(X[:,0],X[:,1],c=clusters,cmap='rainbow',s=100)
plt.title("Student Segmented (Hierarchical Clustering)")
plt.xlabel("Student ID")
plt.ylabel("Marks")
plt.show()
```

## Output:
![Screenshot 2024-10-17 110212](https://github.com/user-attachments/assets/09eaeb0b-63a9-488e-a078-5c6be8d524c7)
![Screenshot 2024-10-17 110222](https://github.com/user-attachments/assets/cdb25b7f-b36d-496e-b8ff-1c568116bc7e)
![Screenshot 2024-10-17 110232](https://github.com/user-attachments/assets/672591bf-9393-400f-a37b-e6b448eb4d1f)
![Screenshot 2024-10-17 110251](https://github.com/user-attachments/assets/1865002d-148b-48ba-adf9-db74b0a4a1f2)
![Screenshot 2024-10-17 110304](https://github.com/user-attachments/assets/dac4e0a2-2944-42ef-89f9-62d81ae11273)
![Screenshot 2024-10-17 110312](https://github.com/user-attachments/assets/ea314984-4ce3-4f47-a052-fe8468aa62f8)
![Screenshot 2024-10-17 110321](https://github.com/user-attachments/assets/79df47d5-db7c-48db-ad58-0b2b834584b1)
![Screenshot 2024-10-17 110329](https://github.com/user-attachments/assets/a3e86c4d-103d-481f-9056-940b5c50d645)
## Result:
Thus the implementation of Hierarchical Clustering using single and complete linkage method in python programming and verified successfully.
