# 📊 Adventure Works Sales Data and Product Categories - Power BI Report

This Power BI report utilizes **AdventureWorks Sales Data** and **Product Categories** to provide business insights by creating relationships, adding calculated columns, and transforming data to empower business decision-making.

## ✅ Tasks Completed

### 📥 Data Import
- Connected to **AdventureWorks Sales Data.xlsx** and imported the following tables:
  - **DimCurrency**
  - **DimCustomer**
  - **DimDate**
  - **DimProduct**
  - **DimPromotion**
  - **DimSalesTerritory**
  - **FactInternetSales**
  
### 🔗 Data Relationships
- Created relationships between `FactInternetSales` and `DimDate`:
  - `OrderDateKey` to `DateKey` (Many to One)
  - `DueDateKey` to `DateKey`
  - `ShipDateKey` to `DateKey`
- Created relationships between product tables:
  - `DimProductSubcategory [CategoryKey]` to `DimProductCategory [CategoryKey]` (Many to One)
  - `DimProduct [ProductSubcategoryKey]` to `DimProductSubcategory [SubcategoryKey]` (Many to One)

### 🧹 Data Transformation
- **Calculated Columns**:
  - `IncomeStatus`: Classified `YearlyIncome` into four categories (Lower, Middle, Higher, Very High)
  - `DaysSinceFirstPurchase`: Calculated days since a customer’s first purchase
  - `FullName`: Concatenated `FirstName` and `LastName`
  - `MaleFemale`: Converted `Gender` values to Male/Female
  - `Relationship`: Converted `MaritalStatus` values to Married/Single
  - `MainCategory`: Retrieved the category name from `DimProductCategory`
  - `PromotionLengthDays`: Calculated the difference between `StartDate` and `EndDate`
  - `Profit`: Calculated the profit in `FactInternetSales` as the difference between `UnitPrice` and `ProductStandardCost`

## 📁 File

- `Adventure_Works_Sales_Data_and_Product_Categories.pbix`: Power BI report file

## 💻 How to Use

1. Open the `.pbix` file in **Power BI Desktop**.
2. Explore the data relationships, calculated columns, and reports.
