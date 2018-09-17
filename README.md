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
<p align="center"><img width="149" alt="11" src="https://user-images.githubusercontent.com/37486654/45348582-bed3e300-b5b7-11e8-9884-d0aa2982a318.PNG">
  
 >Double click the node or right click to open it. Choose **Change Data Asset** to select the data asset that was uploaded to the Watson Studio then press OK and Save.
 
 <p align="center"><img width="200" alt="11" src="https://user-images.githubusercontent.com/37486654/45630471-6a41d380-baa1-11e8-87cc-c5e3d73696d8.png">
  


2. Configures  variables  type using **Type** node from Field Operations palette.
<p align="center"><img width="149" alt="11" src="https://user-images.githubusercontent.com/37486654/45349630-7d910280-b5ba-11e8-8465-b13448bfcaf6.png">
  
 >Double click the node or right click to open it. Choose **Configure Types** to read the metadata then change the `Role` drop down menu of **[Loan_Status]** from input to output. Also change the Role drop down menu of **[LoanID]** from none to Record ID. 

<p align="center"><img width="300" alt="11" src="https://user-images.githubusercontent.com/37486654/45630472-6a41d380-baa1-11e8-9699-915869462ffd.png">
  
<p align="center"><img width="300" alt="12" src="https://user-images.githubusercontent.com/37486654/45630475-6ada6a00-baa1-11e8-8670-cf8ad84e71cc.png"> 

3. Split  the data for training with 80% and testing with 20% sets using **Partition** node from Field Operations palette.
<p align="center"><img width="149" alt="11" src="https://user-images.githubusercontent.com/37486654/45349644-87b30100-b5ba-11e8-917f-57205a0cf9e9.png">

>Double click the node or right click to open it. Change the ratio in the **Training Partition** to 80% and **Testing Partition** to 20%.

<p align="center"><img width="149" alt="11" src="https://user-images.githubusercontent.com/37486654/45630476-6ada6a00-baa1-11e8-8e9e-6a735805338d.png">


4. Drag the Bayes Net node from the **Modeling** Palette.
<p align="center"><img width="149" alt="11" src="https://user-images.githubusercontent.com/37486654/45349655-8d104b80-b5ba-11e8-8f6c-4fd644a12ba8.png">

5. Make sure each node is linked to the previous node then run the model.
<p align="center"><img width="485" alt="ff" src="https://user-images.githubusercontent.com/37486654/45350098-b4b3e380-b5bb-11e8-97a5-0b815e4205e4.PNG">
 
 ***
 
<p align="center"><img src="https://user-images.githubusercontent.com/37486654/45630477-6b730080-baa1-11e8-841d-aad942e74f00.png">


