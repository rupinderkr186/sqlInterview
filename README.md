# Part 1- Sql(Structured Query Language) Interview Questions & Answers
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

## 8)Differentiate between Char vs NChar ?
If you want to just store english characters then use Char , For multilingual language (Non-English) use NChar.
![image](https://github.com/user-attachments/assets/9175941f-9c18-4306-a8af-eae912d36daa)

## 9) Whats the size of Char vs NChar ?
Char 1 Character = 1 byte , For NChar 1 Character = 2 bytes.  
Here **n** stands for unicode like nchar, nvarchar etc all can store unicode characters and takes 2 bytes for one character

## 10) What is the use of Index ?
Indexes increases search performance. Without index data is searched sequentially and for example if we have numbers 1 to 100 and want to search 52, it will go one by one starting from number 1 and going all the way to 52 and this will take time to search.

## 11) How does index make search faster?
Search becomes faster because of Balance tree structure. Internally it creates Node and Leaf nodes to reach to the data quick.
![image](https://github.com/user-attachments/assets/6ae599b3-7e93-4acb-b6a6-c4b94194ea70)

## 12) Clustered vs Non-Clustered index
In <ins>Clustered index</ins> leaf node will point to <ins>actual data</ins>. While in case of <ins>non-clustered index</ins> leaf node <ins>takes help of clustered index</ins>
![image](https://github.com/user-attachments/assets/8a8b3a2a-0326-4cf0-ba1d-9b9a0c42ceef)

## 13) Function vs Stored Procedures
<ins>Function</ins> returns Computed Scalar values. You cannot make permanent changes (insert, update, delete) inside function.  
<ins>Stored procedure</ins> is a mini-programs which can do anything , make changes , backup database.

![image](https://github.com/user-attachments/assets/5da094af-62cd-423b-8a79-a307c913be5c)

## 14) What are triggers and why do you need it ?
Triggers are logics which can be executed when events like insert, update, delete etc happens.
![image](https://github.com/user-attachments/assets/e366bb38-9ada-4747-b9a7-86dd289dde66)

## 15) What are types of triggers ?
There are two types After trigger and Instead OF trigger.
![image](https://github.com/user-attachments/assets/89640dfb-ca11-4660-9dc6-955e15efc40e)

## 16) Differentiate between After trigger vs Instead Of ?
<ins>After trigger</ins> : After event has happened logic is executed.
<ins>Instead Of trigger</ins>: Instead of the event the logic is executed.

## 17) What is need of Identity ?
Identity helps to define auto-incremented column.
![image](https://github.com/user-attachments/assets/4a5e8eed-e8e6-4f03-9209-f889c34def9b)

## 18) Explain transactions and how to implement it ?
Transaction treats series of activity as one single unit. Either everything is successful and or everything rollbacks.
![image](https://github.com/user-attachments/assets/e874569d-0c61-4393-a793-e2db5300c3fc)

## 19) What are inner joins ?
Inner join selects <ins>matching records</ins> from both tables.
![image](https://github.com/user-attachments/assets/bcdcbbf3-5556-4427-acda-24dbf553fb34)

## 20) Explain Left join ?
All data from left table selected and only matching records from right table.
![image](https://github.com/user-attachments/assets/cd57aa7d-4a94-41dc-a76a-575c01ccd1b5)

## 21) Explain Right join ?
All data from right table selected and only matching records from left table.
![image](https://github.com/user-attachments/assets/b415e895-ee9c-456c-9bb5-fad87180c31f)

## 22) Explain Full outer joins ?
All matching and unmatching records from both left and right table are selected.
![image](https://github.com/user-attachments/assets/27f9ef71-f25e-49fe-98b4-59a73e608d87)

## 23) Explain Cross joins ?
Cross join is cartesian. Every record of one table is joined with other table records.
![image](https://github.com/user-attachments/assets/08c92e5a-0cc2-469f-ab34-56e05149ef62)

# Part 2-Sql(Structured Query Language) Interview Questions & Answers
## 24) Why do we need UNION ?
Union combines two result sets.  
  
select [ProductId], [ProductName] from [LearnSql].[dbo].[mst_Products]  
union  
select [ProductId], [ProductName] from [LearnSql].[dbo].[mst_ExpiredProducts]

![image](https://github.com/user-attachments/assets/81a2a173-c9c7-4e78-8377-4628d3da8616)

## 25) Differentiate between Union vs Union All ?
<ins>Union</ins> combines result sets and <ins>excludes duplicates</ins> while <ins>Union all</ins> also combines result set but <ins>includes duplicates</ins>.  

select [ProductId],[ProductName] from [LearnSql].[dbo].[mst_Products]  
union all  
select [ProductId],[ProductName] from [LearnSql].[dbo].[mst_ExpiredProducts]

![image](https://github.com/user-attachments/assets/80a3b351-7976-4142-986a-4d4ed452812e)

## 26) can we have unequal columns in Union?
No.  

select[ProductName] from [LearnSql].[dbo].[mst_Products]  
union all  
select [ProductId],[ProductName] from [LearnSql].[dbo].[mst_ExpiredProducts]

![image](https://github.com/user-attachments/assets/64f18106-763c-4c05-b70a-7f48e44a6737)

## 27) Can column have different data types in Union ?
No.  

select [ProductName],[ProductId] from [LearnSql].[dbo].[mst_Products]  
union all  
select [ProductId],[ProductName] from [LearnSql].[dbo].[mst_ExpiredProducts]  

![image](https://github.com/user-attachments/assets/84968336-d1d1-4fb1-8110-4921b92ed38d)

## 28) Which Aggregate function have you used ?
Sum,Avg,Max, Min and Count.  

select sum([CustomerAmount]),  
Avg([CustomerAmount]) ,  
min([CustomerAmount]),  
max([CustomerAmount]),  
Count(*)  
from [dbo].[txn_Customer]  

![image](https://github.com/user-attachments/assets/9ad181a1-38df-4abe-bc8d-b8287c6002c1)

## 29) When to use Group by ?
It helps to convert rows in to summary rows using common values.  

select [ProductName],sum([CustomerAmount]) from [dbo].[txn_Customer]  
group by [ProductName]

![image](https://github.com/user-attachments/assets/750ceba9-9913-4961-938a-0877b52a0816)

## 30) Can we select column which is not part of group by ?
No. In a group by you can only select columns which are present in groupby.  

select[CustomerName],[ProductName],sum([CustomerAmount]) from [dbo].[txn_Customer]  
group by [ProductName]

![image](https://github.com/user-attachments/assets/fa718293-eaac-40ad-a00a-680a57d4bacb)

## 31) What is having clause ?
Having clause helps to filter group by data.  

select [ProductName],sum([CustomerAmount]) from [dbo].[txn_Customer]  
group by [ProductName]  
having [ProductName]='shoes'  

![image](https://github.com/user-attachments/assets/01adec43-cc4a-4adf-a509-1969d20a20ae)

## 32) Having clause vs Where clause
![image](https://github.com/user-attachments/assets/a717edef-b813-4b02-9d26-d83c83afbd3a)

![image](https://github.com/user-attachments/assets/76228fb0-0c3d-4614-aa8e-1864baa79c70)

## 33) How can we sort records ?
Sorting is done by using order by clause.  

select * from [dbo].[txn_Customer] **order by** [CustomerAmount] **desc / asc**

![image](https://github.com/user-attachments/assets/e93f0104-dc11-4d09-9e50-0ac542621382)

## 34) What’s the default sort ?
Ascending.

## 35) How can we remove duplicates ?
By using Distinct keyword.  

select **distinct** [ProductName] from [dbo].[txn_Customer]

![image](https://github.com/user-attachments/assets/2685c4d8-8da3-4647-92ad-31da4d41c57c)

## 36) Select the first top X records ?
By using the top keyword.  

select **top 2** * from [dbo].[txn_Customer]
![image](https://github.com/user-attachments/assets/078a905f-1314-4eb0-ba63-0fe114365f50)

## 37) How to handle NULLS ?
By using ISNULL function.
![image](https://github.com/user-attachments/assets/0fd0f5db-168b-492b-8b9f-0f5c68802fa0)
