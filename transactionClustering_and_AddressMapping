from sklearn.cluster import DBSCAN
import numpy as np

def cluster_transactions(transactions):
    features = np.array([[tx['timestamp'], tx['value']] for tx in transactions])
    
    clustering = DBSCAN(eps=0.5, min_samples=2).fit(features)
    
    for i, tx in enumerate(transactions):
        tx['cluster'] = clustering.labels_[i]
    
    return transactions

clustered_transactions = cluster_transactions(cleaned_transactions)
print(clustered_transactions)
