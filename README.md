# sqlInterview
## 1) What is normalization?  
Normalization is a database design technique to remove redunadant data.
Normalization is implemented by splitting tables in two, one with reference data(master table) and other with transaction data.

![image](https://github.com/user-attachments/assets/7b106a42-1960-4306-accb-b515347946b9)

In the above table country name like India, IND is redunadant and we can split this in **2 tables: one as mst_country and other as tblCustomer**. Now we can use country Id from mst_country in tblCustomer to reference countries.

![normalization](https://github.com/user-attachments/assets/35be3393-1bc3-4c18-8f99-773f2e87a81b)

## 2) What is denormalization?  
Denormalization is a database technique to <ins>improve search performance.</ins>
![image](https://github.com/user-attachments/assets/e152c83c-e922-46a1-a4ef-da6b10ca6635)
