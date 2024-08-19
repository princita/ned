# Run the script and import data

![image](https://github.com/princit/DataMiningBusinessIntelligence/assets/29123911/6ab98f33-6a08-40a4-b933-3aef76d03de2)

# Create a quick measure
![image](https://github.com/princit/DataMiningBusinessIntelligence/assets/29123911/431d0fc1-cacb-40db-af68-562c0c3579aa)


![image](https://github.com/princit/DataMiningBusinessIntelligence/assets/29123911/c6a1e182-f93c-40e3-ae92-a90a23d9410b)

# Quick measure example


![image](https://github.com/princit/DataMiningBusinessIntelligence/assets/29123911/368e029c-19f9-40f6-b19c-d05f3c3dac8a)


![image](https://github.com/princit/DataMiningBusinessIntelligence/assets/29123911/acd4d9b5-7f65-4d2b-9ec4-64935b04502d)

![image](https://github.com/princit/DataMiningBusinessIntelligence/assets/29123911/a1f62e0e-2d36-442c-997f-5f6f59dd5049)

# Learn DAX by using quick measures

![image](https://github.com/princit/DataMiningBusinessIntelligence/assets/29123911/8ec84f66-8f32-4387-8a8f-a8c1692595b5)

# Logical functions

![image](https://github.com/princit/DataMiningBusinessIntelligence/assets/29123911/8fc08a35-9ebb-42a3-b3cc-ec21c7a79b2c)
# IF
<code>
Price Group =
IF(
    'Product'[List Price] < 500,
    "Low",
    IF(
        'Product'[List Price] < 1500,
        "Medium",
        "High"
    )
)

</code>
<code>
= IF(SUM('InternetSales_USD'[SalesAmount_USD]) >200000, TRUE(), false())
</code>

# OR
<code>
IF(   OR(   CALCULATE(SUM('ResellerSales_USD'[SalesAmount_USD]), 'ProductSubcategory'[ProductSubcategoryName]="Touring Bikes") > 1000000  
         ,   CALCULATE(SUM('ResellerSales_USD'[SalesAmount_USD]), 'DateTime'[CalendarYear]=2007) > 2500000  
         )  
   , "Circle of Excellence"  
   , ""  
   )
</code>

# Tranform 
![image](https://github.com/princit/DataMiningBusinessIntelligence/assets/29123911/f6ab15c4-e6e9-4e59-b443-5aaf8900e525)

# Run Python Script 
![image](https://github.com/princit/DataMiningBusinessIntelligence/assets/29123911/fd6ee9dc-0f33-4a91-b2d1-724ac08af73a)
# Create a Python visual in Power BI Desktop

<code>
import matplotlib.pyplot as plt 
dataset.plot(kind='scatter', x='Age', y='Weight', color='red')
plt.show()
</code>

<code>
import matplotlib.pyplot as plt 
dataset.plot(kind='scatter', x='Age', y='Weight', color='red')
plt.show()
</code>

![image](https://github.com/princit/DataMiningBusinessIntelligence/assets/29123911/2a9af6a2-20fa-4a08-a2b9-d959da2928ea)

<code>
import matplotlib.pyplot as plt 
ax = plt.gca() 
dataset.plot(kind='line',x='Fname',y='Children',ax=ax) 
dataset.plot(kind='line',x='Fname',y='Pets', color='red', ax=ax) 
plt.show()
</code>

![image](https://github.com/princit/DataMiningBusinessIntelligence/assets/29123911/62fa85fd-fcbd-4f2f-80ba-8e2e1eb8307d)

<code>
import matplotlib.pyplot as plt 
dataset.plot(kind='bar',x='Fname',y='Age') 
plt.show()
</code>

![image](https://github.com/princit/DataMiningBusinessIntelligence/assets/29123911/996bd8d1-44ba-431e-b15a-5b88c08f46e9)

