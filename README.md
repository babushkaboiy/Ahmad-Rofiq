# Coffee Vending Machine – ESP32 + QRIS

Proyek ini mengendalikan mesin penjualan kopi otomatis menggunakan ESP32. Sistem menggantikan pembayaran koin dengan QRIS dan mengontrol tombol rasa melalui rangkaian relay.

![C](https://img.shields.io/badge/Language-C-blue?logo=c&logoColor=white)
![C++](https://img.shields.io/badge/Language-C++-00599C?logo=cplusplus&logoColor=white)
![ESP32](https://img.shields.io/badge/ESP32-Microcontroller-black?logo=espressif&logoColor=white)
![TFT LCD](https://img.shields.io/badge/TFT%20LCD-Display-blueviolet)
![Relay](https://img.shields.io/badge/Relay-Module-orange)
![Midtrans API](https://img.shields.io/badge/Midtrans-API%20Payment-brightgreen)

## Fitur
- Pembayaran QRIS terhubung ke API Midtrans.
- Pembacaan pulsa coin acceptor untuk mode uji.
- Kontrol tombol rasa dengan relay low-trigger.
- Tampilan menu pada TFT 3.5".
- Pembacaan data waktu, suhu, dan kapasitas gelas.

## Perangkat
- ESP32.
- Layar TFT 3.5".
- Relay 5V + transistor S9013 + resistor 1kΩ.
- Coin acceptor vending machine.
- Modul step-down 12V ke 5V.

## Struktur Kode
- Inisialisasi WiFi dan API QRIS.
- Generate QR dan tampilkan di TFT.
- Polling status pembayaran.
- Eksekusi tombol rasa via relay jika pembayaran selesai.
- Interrupt pembacaan pulsa koin untuk debugging.

## Instalasi
1. Kloning repository.
2. Pasang library: WiFi, HTTPClient, TFT_eSPI, ArduinoJson, NTPClient.
3. Sesuaikan konfigurasi Midtrans dan pin ESP32.
4. Upload ke board.

## Lisensi
Proyek bebas dimodifikasi sesuai kebutuhan.
