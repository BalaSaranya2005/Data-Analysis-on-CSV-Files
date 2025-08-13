import pandas as pd
import matplotlib.pyplot as plt

# 1️⃣ Load the CSV file
# Replace 'sales_data.csv' with your actual CSV file name
df = pd.read_csv("sales_data.csv")

# 2️⃣ Display the first few rows
print("📊 First 5 rows of the dataset:")
print(df.head(), "\n")

# 3️⃣ Basic info about the dataset
print("ℹ️ Dataset Info:")
print(df.info(), "\n")

# 4️⃣ Group sales by product and calculate total sales
product_sales = df.groupby("Product")["Sales"].sum().reset_index()
print("💰 Total Sales by Product:")
print(product_sales, "\n")

# 5️⃣ Group sales by region and calculate total sales
region_sales = df.groupby("Region")["Sales"].sum().reset_index()
print("🌍 Total Sales by Region:")
print(region_sales, "\n")

# 6️⃣ Plot: Sales by Product
plt.figure(figsize=(8, 5))
plt.bar(product_sales["Product"], product_sales["Sales"], color="skyblue")
plt.title("Total Sales by Product")
plt.xlabel("Product")
plt.ylabel("Sales")
plt.xticks(rotation=45)
plt.tight_layout()
plt.savefig("sales_by_product.png")
plt.show()

# 7️⃣ Plot: Sales by Region
plt.figure(figsize=(8, 5))
plt.bar(region_sales["Region"], region_sales["Sales"], color="lightgreen")
plt.title("Total Sales by Region")
plt.xlabel("Region")
plt.ylabel("Sales")
plt.xticks(rotation=45)
plt.tight_layout()
plt.savefig("sales_by_region.png")
plt.show()
