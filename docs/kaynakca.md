# Power Logger Mini Yazılım klavuzu 

> **Hazırlayan:** Oğuzhan ESEN  
> **Proje Adı:** STM32WL Nucleo Carrier Board  
> **Tarih:** 22 ekim 2025  
> **Versiyon:** v1.0

---


## 1. Giriş

Power Logger Mini porjesinde şu özelliklerin olması planlanmıştır.
- Akım ve voltaj bilgisinin edinilmesi (INA219,226,228).
- Oled ekran üzerinden gösterilmesi.
- Verileri sd karta kaydetmesi.
- Buton ile kayıt kontrolünün yapılması.
- Kaydın yapılırken tarih saat bilgisinin alınması.
- Hidrolink Test Boarda uyumlu olması.

Bu özellikleri karşılayabilmesi için komponet seçimi ve kaynakları verilmiştir.

### 1.1 Akım Voltaj bilgisinin karşılanması  için:
Bu bilginin karşılanması amacıyla INA219 , INA226 denenmiştir. INA226 bir ölçüde uygun oldugu görülmiş ama 16bit çözünürlük yerine 20 bit çözünürlüğün daha iyi olacagı
öngörüldüğü için INA228 kullanılmasına karar verilmiştir.
![ına226](/images/image.png)

[INA228](https://www.ozdisan.com/p/diger-guc-yonetimi-entegreleri-281/texas-ina228aqdgsrq1-1086895)
[Arduino libi](https://github.com/RobTillaart/INA228)
[Sematik ve tasarım dosyaları](https://github.com/adafruit/Adafruit-INA228-PCB)


### 1.2 OLED Ekran:
Biglerin gösterimi için i2c ile çalışan oled ekran seçilmiştir.
![alt text](/images/image-1.png)

[Kullanılan ekranın datasheet'i](https://www.ozdisan.com/api/pdf/product/assets/WEA012864DLPP3N00003.pdf)

[Test için kullandığım git linki](https://github.com/RobertoBenjami/stm32_ssd1306_i2c_dma_hal/tree/master/Drivers)

### 1.3 SD Card:
SD kartta modülü kullanılmıştır ve sd karta kayıt spi üzerinden yapılmaktadır.
![alt text](/image-2.png)
[SD kart için kullanılan kaynak](https://youtu.be/PBIm8BCnbyQ)
[SD kart için kullanılan git linki](https://github.com/PRTechTalk/STM32/tree/main/SD_Card_SPI_FatFs)


