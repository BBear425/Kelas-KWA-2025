# - Lab: SQL injection vulnerability in WHERE clause allowing retrieval of hidden data
 This lab contains a SQL injection vulnerability in the product category filter. When the user selects a category, the application carries out a SQL query like the following:
'''sql
SELECT * FROM products WHERE category = 'Gifts' AND released = 1
'''
To solve the lab, perform a SQL injection attack that causes the application to display one or more unreleased products. 

# - Link
https://portswigger.net/web-security/sql-injection/lab-retrieve-hidden-data

# - Cara

## Step
1. Intercept link kategori
2. Masukkan "'+OR+1=1--" pada kategori

## Gambar
<img width="2304" height="1276" alt="VirtualBox_kali-linux-2024 4-virtualbox-amd64_17_09_2025_09_40_02" src="https://github.com/user-attachments/assets/5260beb6-6c32-4633-84d9-f9b3bc5a0744" />
<img width="2304" height="1276" alt="VirtualBox_kali-linux-2024 4-virtualbox-amd64_17_09_2025_09_40_44" src="https://github.com/user-attachments/assets/43dd44d6-2476-43c7-9f26-77b014d677f7" />

## Berhasil


