# Jarkom-Modul-1-F06-2023

Kelompok F06:
- Arkana Bilal Imani / 5025211034
- Azhar Abiyu

# No. 1
### Soal
User melakukan berbagai aktivitas dengan menggunakan protokol FTP. Salah satunya adalah mengunggah suatu file.  
a. Berapakah sequence number (raw) pada packet yang menunjukkan aktivitas tersebut?

b. Berapakah acknowledge number (raw) pada packet yang menunjukkan aktivitas tersebut? 

c. Berapakah sequence number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?

d. Berapakah acknowledge number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?

### Penyelesaian
Untuk mengetahui packet yang dikirim/diterima menggunakan FTP bisa menggunakan display filter `ftp`  
![](images/1a.png)  
Namun untuk mendapatkan packet yang secara spesifik hanya bisa dikirim dengan FTP, dapat menggunakan display filter `ftp contains "STOR"` karena command STOR hanya bisa dilakukan melalui FTP  
![](images/1b.png)  
Setelah packet didapatkan, tinggal dilihat sequence number (raw) dan acknowledgement number (raw) dengan membuka section Transmission Control Protocol seperti berikut:  
![](images/1c.png)  
Untuk mendapatkan packet response, display filter yang digunakan adalah `ftp contains "zip"` karena command STOR digunakan untuk upload file zip.  
![](images/1d.png)  
Perolehan flag:  
  
Kendala: tidak ada.
