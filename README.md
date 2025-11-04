# Banking-Customer-segmentation-Using-Gradio-Interface-
This case requires to develop a customer segmentation to define marketing strategy. The dataset has about 8951 credit card holders information for last 6 months(Dataset obtained from https://www.kaggle.com/datasets/arjunbhasin2013/ccdata).


The project begins by importing the necessary Python libraries such as pandas, numpy, matplotlib, seaborn, scikit-learn, and gradio for data handling, visualization, modeling, and creating a simple user interface.


In the data preprocessing stage, the dataset containing customer information—such as spending habits, transaction history, credit usage, and income—is loaded using pandas. Non-numeric columns and missing values are handled carefully to ensure that the clustering model receives clean numerical input. The numeric features are then standardized using StandardScaler, which ensures that each feature contributes equally to the clustering algorithm, avoiding dominance by attributes with larger numeric ranges.


Once the data is prepared, the K-Means clustering algorithm from scikit-learn is applied to group customers into distinct clusters based on their similarities. The number of clusters is often chosen either through experimentation or methods like the Elbow Method. In your final working version, the model successfully divided the dataset into seven clusters, indicating seven unique groups of customers with different financial behaviors and characteristics.


Cluster	Customers	Possible interpretation 
0	- Moderate spenders — average usage(These customers maintain a balanced level of credit card usage. They make regular purchases and repayments but do not show extreme spending or saving behavior. They represent stable, average users who are reliable but not highly profitable.)


1	- Low-usage or inactive customers(This group rarely uses their credit cards or keeps very low transaction volumes. They might prefer cash or other payment methods.)


2	- Consistent spenders, low credit risk(These customers show steady, predictable spending patterns and pay their balances on time. They are financially disciplined and have low default risk.)


3 - Balanced users — steady transactions(These users maintain a good mix of spending, repayment, and credit utilization. They are neither too conservative nor too aggressive, reflecting a financially healthy and dependable customer segment.)


4 - High-value or loyal customers(This is one of the most profitable segments. These customers use their cards frequently, maintain high balances, and often take advantage of premium services.)


5 - Very active / premium cardholders(These are top-tier customers with very high spending and transaction activity. They may use multiple banking services, including loans and investments. They contribute significantly to the bank’s revenue.)


6 - Outliers — unusual or elite customers(A very small group showing unusual spending or repayment patterns. They might represent either extremely wealthy individuals or atypical users.)




Finally, the project integrates a Gradio interface to make the model interactive and user-friendly. Through the interface, users can upload a CSV file of customer data, and the model automatically performs segmentation and displays the number of clusters and customer distribution within each.
