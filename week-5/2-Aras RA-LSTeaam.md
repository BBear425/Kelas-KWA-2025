# - Login Support Team
Log in with the support team's original user credentials without applying SQL Injection or any other bypass.

# - Link
https://juice-shop.herokuapp.com/#/

# - Cara

## Step
1. Download file incident-support.kbdx dan cari kode password
2. Gunakan KeePass2John untuk di crack dengan John The Ripper
3. Gagal ketika menggunakan wordlist rockyou.txt
4. Ketika melihat main.js ketemu
   ''' changePassword() {
              localStorage.getItem('email') ?.match(/support@.*/) &&
              !this.newPasswordControl.value.match(
                /(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?=.*[@$!%*?&])[A-Za-z\d@$!%*?&]{12,30}/
              ) &&
              console.error(
                'Parola echipei de asistență nu respectă politica corporativă pentru conturile privilegiate! Vă rugăm să schimbați parola în consecință!'
              )'''
5. Jika ditranslasi memiliki arti "The support team password does not comply with the corporate policy for privileged accounts! Please change your password accordingly!"
6. Regex memiliki makna ini:
  - Mengandung huruf kecil
  - Mengandung huruf besar
  - Mengandung angka
  - Mengandung simbol khusus (@$!%*?&)
  - Panjangnya antara 12 dan 30 karakter
  - Hanya terdiri dari karakter yang diizinkan (A-Za-z\d@$!%*?&)
7. Di bruteforce ketemu Support2022!
8. Buka file kbdx dengan KeePass2 dengan password tersebut
9. Ketemu aakun dengan support@juice-sh.op dengan password J6aVjTg0pRs@?5l!Zkq2AYnCE@RF$P

Gambar
## <img width="2302" height="1275" alt="VirtualBox_kali-linux-2024 4-virtualbox-amd64_07_10_2025_14_11_34" src="https://github.com/user-attachments/assets/7b51bde1-e73b-44e2-863f-469d39604f9b" />
<img width="2302" height="1275" alt="VirtualBox_kali-linux-2024 4-virtualbox-amd64_07_10_2025_14_28_10" src="https://github.com/user-attachments/assets/eb485e87-7059-43e0-90e4-262c48fa5d30" />
<img width="2302" height="1275" alt="VirtualBox_kali-linux-2024 4-virtualbox-amd64_07_10_2025_14_43_03" src="https://github.com/user-attachments/assets/59d3d436-0d98-447b-8441-ab7630e046b6" />
<img width="2302" height="1275" alt="VirtualBox_kali-linux-2024 4-virtualbox-amd64_07_10_2025_14_42_43" src="https://github.com/user-attachments/assets/4460402b-eac6-4c64-9641-f173c9204e6e" />
<img width="2302" height="1275" alt="VirtualBox_kali-linux-2024 4-virtualbox-amd64_07_10_2025_14_33_07" src="https://github.com/user-attachments/assets/e8ddbc24-af31-472b-89eb-0880fc022a0f" />
<img width="2302" height="1275" alt="VirtualBox_kali-linux-2024 4-virtualbox-amd64_07_10_2025_22_00_28" src="https://github.com/user-attachments/assets/6a5857d8-9c07-44c8-b8f8-eabd1a3a22bd" />
<img width="2302" height="1275" alt="VirtualBox_kali-linux-2024 4-virtualbox-amd64_08_10_2025_09_50_11" src="https://github.com/user-attachments/assets/b6b4caf6-5f8c-4c97-9819-004591b11b69" />
<img width="2302" height="1275" alt="VirtualBox_kali-linux-2024 4-virtualbox-amd64_08_10_2025_09_51_25" src="https://github.com/user-attachments/assets/78e949f8-fde9-4db2-8273-c98df3db8da9" />

## Berhasil

