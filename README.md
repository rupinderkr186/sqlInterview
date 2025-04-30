# Sql(Structured Query Language) Interview Questions & Answers
## 1) What is normalization?  
Normalization is a database design technique to remove redunadant data.
## 2) How to implement normalization?
Normalization is implemented by splitting tables in two, one with reference data(master table) and other with transaction data.

![image](https://github.com/user-attachments/assets/7b106a42-1960-4306-accb-b515347946b9)

In the above table country name like India, IND is redunadant and we can split this in **2 tables: one as mst_country and other as tblCustomer**. Now we can use country Id from mst_country in tblCustomer to reference countries.

![normalization](https://github.com/user-attachments/assets/35be3393-1bc3-4c18-8f99-773f2e87a81b)

## 3) What is denormalization?  
Denormalization is a database technique to <ins>improve search performance.</ins> In denormalization we merge table so that we need to fetch from less tables and thus increase search performance.In denormalization tables have duplicate data.
![image](https://github.com/user-attachments/assets/e152c83c-e922-46a1-a4ef-da6b10ca6635)

## 4) Explain OLTP vs OLAP?
**OLTP** : Online Transaction Processing.Normalization avoids redundancy and we follow normalization design(1st, 2nd and 3rd normal forms).  
**OLAP** : Online Analytical Processing. Denormalization improves search performance and we follow denormalization design.

![image](https://github.com/user-attachments/assets/7349491a-6afe-4ead-93d9-b8c814acaab6)

## 5) Explain 1st, 2nd and 3rd normal form?
**1st normal form** : A table is in first normal form when the columns have <ins>Atomic values</ins>. It should not have <ins>repeating groups</ins>. If the table is not in 1st normal form, it can have <ins>insert, update and delete anamolies</ins>.  
![image](https://github.com/user-attachments/assets/a8665269-4f00-4b50-b13b-a0900649135a)

**2nd Normal form** : First normal form should be satisfied. All non-key columns should be <ins>fully dependent on the Primary key</ins>. 
![image](https://github.com/user-attachments/assets/30db4906-d1c3-4ca1-8fb4-72844c412e56)

**3rd Normal** : All 1st and 2nd normal form should be satisfied. No <ins>transient</ins> dependency should be present.
![image](https://github.com/user-attachments/assets/df9a947a-eacd-4f67-9a84-cfe813cb2712)

**Acronym: APT**
![image](https://github.com/user-attachments/assets/e8ce1d0e-d956-428f-a0c1-76121a52e827)

## 6) Primary Key vs Unique key ?
Remember the 2 Ns.  
**1st N NULLS** : Unique can have NULLS , but primary key can not have NULLS.  
**2nd N Numbers** : Many unique keys but ony ONE Primary key.  
Both keys dont allow duplicates in tables.
![image](https://github.com/user-attachments/assets/a7b71a19-e7cb-4d09-83c5-bf525873db2d)

## 7) Differentiate between Char vs Varchar ?
Char is Fixed length while varchar is variable length.
![image](https://github.com/user-attachments/assets/cc2df0c2-33d8-49cd-b946-3e270fa0b677)
