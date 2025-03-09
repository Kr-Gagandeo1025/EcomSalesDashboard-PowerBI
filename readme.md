
# **Azure, SQL and PowerBI - Powered Sales Dashboard** 🚀

## **📌 Project Overview**

This project is a **Power BI dashboard** connected to an  **Azure SQL Database** , providing real-time sales analytics. It also includes a **web-based sales management system.**

🔹 **Features:**

* Real-time sales insights via **Power BI Dashboard** 📊
* **Web-based interface** for managing sales records 🖥️
* Hosted **Azure SQL Database** for data storage ⚡
* **Automated data updates** using Azure Logic Apps 🔄

---

## **🎯 Use Cases**

* **Business Intelligence:** Track revenue, top-selling products, and trends.
* **Sales Management:** Easily add/update sales records in Azure SQL.
* **Data Analytics:** Leverage Power BI for advanced sales insights.
* **Cloud-Based Hosting:** Securely manage sales data using Azure.

---

## **🔧 How to Set Up the Azure SQL Database**

### **Step 1: Create an Azure SQL Database**

1. Go to  **[Azure Portal](https://portal.azure.com/)** .
2. Navigate to **SQL Databases** → Click  **Create** .
3. Choose a **resource group** and enter a **database name** (e.g., `SalesDB`).
4. Select **Server** → Click  **Create New Server** .
   * Server Name: `your-server-name`
   * Location: Choose nearest region
   * Authentication: SQL Authentication
5. Choose **Basic Pricing Tier** (or Free Tier if available) → Click  **Review & Create** .

### **Step 2: Configure Firewall & Connect to Database**

1. Go to  **Azure SQL Database → Networking** .
2. Enable "Allow Azure services and resources to access this server".
3. Copy the **server name** (`your-server.database.windows.net`).
4. Connect via **Azure Data Studio** or  **SSMS** .

### **Step 3: Create the Sales Table**

Run this SQL query to create the table:

```sql
CREATE TABLE SalesData (
    SaleID INT IDENTITY(1,1) PRIMARY KEY,
    ProductName VARCHAR(255),
    Category VARCHAR(100),
    SaleDate DATE,
    QuantitySold INT,
    Revenue DECIMAL(10,2)
);
```

### **Step 4: Insert Sample Data**

```sql
INSERT INTO SalesData (ProductName, Category, SaleDate, QuantitySold, Revenue)
VALUES ('Laptop', 'Electronics', '2024-03-01', 5, 5000.00);
```

---

## **📊 How to View the Power BI Dashboard**

1. Open  **Power BI Desktop** .
2. Click **File → Open** → Select the provided `.pbix` file.
3. Power BI will ask for database credentials.
4. Enter:
   * **Server:** `your-server.database.windows.net`
   * **Database:** `SalesDB`
   * **Authentication:** SQL Server Authentication
5. Click **Load Data** → Your dashboard is now connected! 🚀

---

## **📸 Project Screenshots**
![Screenshot 2025-03-09 141857](https://github.com/user-attachments/assets/f3f2384c-5821-4811-aa9d-b780c3094cbf)


---

## **🌐 Live Link

You can view the `index.html` for the html code.

link : [View Deployment](https://kr-gagandeo1025.github.io/EcomSalesDashboard-PowerBI/)

---

## **📬 Contact**

For any issues, feel free to open an **issue** or reach out on [kumargagandeo9@gmail.com](mailto:kumargagandeo9@gmail.com "Mail") .
