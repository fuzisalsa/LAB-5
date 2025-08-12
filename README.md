# LAB-5
tanggal 12 agustus 2025 
# Mengkoneksikan mikrotik ke internet  
A. konfigurasi mikrotik ke internet dengan IP dynamic
  
![y](TOPOLOGIdym.PNG)

        1.pasangkan pengkabelan LAN sesui topologi 
          ether1-WAN (untuk koneksi ke Internet), dan
          ether2-LAN (untuk koneksi ke PC Klien)

![y](LAB.PNG)

      2.Konfigurasi DHCP Client ether1-WAN agar dapat IP dari ISP/internet:
        IP>DHCP client
        klik +
        masukan interface=ether1-WAN  
        klik, Apply   
        lalu OK  

![y](LAB1.PNG)

      cek tab status untuk melihat IP yang di dapatkan ether1-WAN  

![](LAB2.PNG)

      3.melakukan pengujian koneksi mikrotik ke internet lewat terminal:  

![Y](LAB3.PNG)

      4.Melakukan seting IP pada interface ether2-LAN::  
        IP>AddreS  
        klik +   
        masukan interface, address seperti di gambar.  
        apply lalu OK. 
     
![Y](LAB4.PNG) 

     5.Lakukan konfigurasi NAT, agar PC Klien dapat terkoneksi Internet melewati Mikrotik:  
       IP>Firewall>NAT  
       klik +  
       isi tab general dan action: lihat seperti di gambar  
       Apply lalu ok.

![Y](LAB5.PNG)

![Y](LAB5.1.PNG)


    6.Lalu konfigurasi DHCP server:  
      IP>DHCP Server  
      pilih DHCP setup   
      pilih ether2-LAN   
      klik next hingga selesai  

![Y](LAB7.PNG)

   7. yang terakhir konfigursi DNS:  
      IP>DNS   
      masukan server=8.8.8.8 (ip google)  
      klik Applay lalu OK.

![Y](labdns.PNG)

  8.Jika sudah, setting IP di windows Control Panel,  
    ubah jadi DHCP/Obtain Auto.  
    Sekarang Client bisa terhubung ke internet

B. konfigurasi mikrotik ke internet dengan IP dynamic

1.Langkah-langkahnya nya sama seperti tahap sebelumnya, cuman yang ini tidak membutuhkan DHCP Server  
2.Jika sudah, di setting IP windows di Control Panel, masukan IP secara manual, 
  masukan IP yang masih 1 network IP 192.168.10.2 karna IP gatewaynya 192.168.10.1  
  SubMask 255.255.255.0 karna /24 dan DNS nya isi 8.8.8.8
3.Sekarang Client bisa terhubung ke Internet

# Kesimpulan
Dynamic routing yaitu konfigurasi yang clientnya mendapat IP secara otomatis.  
Sedangkan Static Routing adalah konfigurasi yang harus di seting satu-satu termasuk clinetnya.
Maka dari itu dynamic routing cocok untuk jaringan berskala besar karna tidak perlu setting IP satu-satu.  
Sedangkan Static Routing tidak cocok untuk jaringan berskala besar.



