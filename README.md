# LAB-5
tanggal 12 agustus 2025 
# Mengkoneksikan mikrotik ke internet  
A. konfigurasi mikrotik ke internet dengan IP dynamic
  
![y](TOPOLOGIdym.PNG)

          pasangkan pengkabelan LAN sesui topologi 
          ether1-WAN (untuk koneksi ke Internet), dan
          ether2-LAN (untuk koneksi ke PC Klien)

![y](LAB.PNG)

      onfigurasi DHCP Client ether1-WAN agar dapat IP dari ISP/internet:
      IP>DHCP client
      klik +
      masukan interface=ether1-WAN  
      klik, Apply   
      lalu OK  

![y](LAB1.PNG)

      cek tab status untuk melihat IP yang di dapatkan ether1-WAN  

![](LAB2.PNG)

      melakukan pengujian koneksi mikrotik ke internet lewat terminal:  

![Y](LAB3.PNG)

     Melakukan seting IP pada interface ether2-LAN::  
     IP>AddreS  
     klik +   
     masukan interface, address seperti di gambar.  
     apply lalu OK. 
     
![Y](LAB4.PNG) 

    Lakukan konfigurasi NAT, agar PC Klien dapat terkoneksi Internet melewati Mikrotik:  
    IP>Firewall>NAT  
    klik +  
    isi tab general dan action: lihat seperti di gambar  

![Y](LAB5.PNG)

![Y](LAB5.1.PNG)


    Lalu konfigurasi DHCP server:  
    IP>DHCP Server  
    pilih DHCP setup   
    pilih ether2-LAN   
    klik next hingga selesai  

![Y](LAB7.PNG)

    yang terakhir konfigursi DNS:  
    IP>DNS   
    masukan server=8.8.8.8 (ip google)  
    klik Applay lalu OK.

![Y](labdns.PNG)



