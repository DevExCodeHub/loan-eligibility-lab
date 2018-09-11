# Predict Loan Eligibility with SPSS Modeler in Watson Studio

## Login to IBM Cloud and Create Watson Studio Service
1. Register in [IBM Cloud](https://ibm.biz/BdYmuL).
2. Go to **Catalog**.
3. Search for `watson studio`.
4. Click on the service and then **Create**.
5. On the service page, click on **Get Started**.

## Create New Project
1. Scrol down the page and click on **(+) New project icon**.
2. Name your project 'Predict loan eligibility'.
3. Click **Create**.
4. In your project page, nagivate to the Assests tab, drag the [data set](https://github.com/DevExCodeHub/Loan_eligibility_lab/blob/master/Data/train.csv) file and drop it in the Load sidebar.

## Create SPSS Model
1. On the same Assets page, scroll down to the Modeler flows.
2. Click the **(+)** New flow icon.
3. Under the 'New' tab, name your modeler 'Predictive model'.
4. Click **Create**.

## Build The Model
1. Import the Data by dragging **Data Asset** node from Import palette.
<img width="149" alt="11" src="https://user-images.githubusercontent.com/37486654/45348582-bed3e300-b5b7-11e8-9884-d0aa2982a318.PNG">
2. Configures  variables  type using **Type** node from Field Operations palette.
3. Split  the data for training with 80% and testing with 20% sets using **Partition** node from Field Operations palette.
4. Drag the Bayes Net node from the **Modeling** Palette.
5. Make sure each node is linked to the previous node then run the model.
