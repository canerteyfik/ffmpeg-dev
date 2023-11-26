# ffmpeg-dev

Bu reponun amacı ffmpegin kurulumundan başlayarak geliştirme süreci boyunca bir kaynak sağlamaktır.
Süreç boyunca windows işletim sitemi kullanılacaktır.

# ADIM 1 FFMPEG KURULUMU

1- ffmpegin kurulumu için vcpkg (https://vcpkg.io/en/) aracından faydalanılacaktır.
vckpkg C/C++ dilleri için açık kaynaklı bir paket yöneticisidir.

2-CMD üzerinden vcpkg'yi kurmak için 
"git clone https://github.com/Microsoft/vcpkg.git" komutunu çalıştırın

3- cd vcpkg

4- bootstrap-vcpkg.bat adımlarından sonra vcpkg kurulumları bitti şimdi ffmpegin kurulumuna devam edeceğiz.

5- vcpkg install ffmpeg:x64-windows komutu ile ihtiyacımız olan .dll .lib .h dosyaları oluşacaktır

6- mevcut_dizin\vcpkg\installed\x64-windows yolunun altında ffmpeg için gerekli olan dosylar oluştu.

# NOT Kurulum yapacağımız klasör yolunda Türkçe karakterler ve boşluk karakterleri hata vermektedir. Vcpkg ile çalışırken buna dikkat edin. 

# ADIM 2 FFMPEG VISUAL STUDIO AYARLARI

1- Header dosyalarını ve .lib dosyalarını proje ayarlarından dahil etmeliyiz.

![include](https://github.com/canerteyfik/ffmpeg-dev/assets/74292890/ea870f32-4cda-4c11-bbc9-6518a440fba3)

![lib](https://github.com/canerteyfik/ffmpeg-dev/assets/74292890/eca6851a-bf4d-4110-8259-f999f0ce99fb)

![lib_2](https://github.com/canerteyfik/ffmpeg-dev/assets/74292890/0b8a157f-8e33-44e1-8d29-5bc7afdc4342)

avcodec.lib
avdevice.lib
avfilter.lib
avformat.lib
avutil.lib
pkgconf.lib
swresample.lib
swscale.lib

2-Son olarak mevcut_dizin\vcpkg\installed\x64-windows\debug\bin yolunda bulunan .dll dosyalarını projemizde bulunan exe ile aynı yere koyalım.

3-mevcut_dizin\vcpkg\installed\x64-windows yolunun altındaki herhangi bir örnekle bağımlılıkları test edelim.








