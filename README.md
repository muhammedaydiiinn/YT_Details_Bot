# YouTube Detay Verisi Çekme Botu

Bu bot, YouTube API'sini kullanarak YouTube videolarının detaylarını çekmek için tasarlanmıştır. Aşağıda, botu kurmak ve çalıştırmak için gereken adımlar yer almaktadır.

## Gereksinimler

- Python 3.x
- YouTube Data API v3
- Aşağıdaki Python kütüphaneleri:
  - `google-api-python-client`
  - `pandas`

## Kurulum Adımları

### 1. Reponun Klonlanması

İlk olarak, projeyi kendi makinenize klonlayın:

```bash
git clone https://github.com/muhammedaydiiinn/YT_Details_Bot.git
cd YT_Details_Bot
```

### 2. Sanal Ortamın (myenv) Aktifleştirilmesi

Projede kullanılan bağımlılıkları yönetmek için sanal bir ortam kullanıyoruz. GitHub'a yüklenen `myenv` sanal ortamını aktif hale getirin:

- Windows için:
  ```bash
  myenv\Scripts\activate
  ```
- MacOS/Linux için:
  ```bash
  source myenv/bin/activate
  ```

### 3. Gerekli Kütüphanelerin Kurulması

Eğer sanal ortamınız aktif değilse ya da bağımlılıkları yeniden yüklemek istiyorsanız, `requirements.txt` dosyasını kullanarak gerekli Python kütüphanelerini şu komutla kurabilirsiniz:

```bash
pip install -r requirements.txt
```

### 4. API Anahtarının Ayarlanması

YouTube Data API v3 anahtarını almanız gerekmektedir. [Buradan](https://console.developers.google.com/) YouTube API anahtarını alabilirsiniz. API anahtarını aldıktan sonra, `info.txt` dosyasının ilk satırına API anahtarınızı yapıştırın.

```text
YOUR_YOUTUBE_API_KEY
https://www.youtube.com/watch?v=EXAMPLE_VIDEO_ID_1
https://www.youtube.com/watch?v=EXAMPLE_VIDEO_ID_2
```

- **İlk satır**: YouTube API anahtarınız.
- **Diğer satırlar**: Verisini çekeceğiniz YouTube videolarının linkleri.

### 5. Botun Çalıştırılması

Botu çalıştırmak için aşağıdaki komutu kullanabilirsiniz:

```bash
python main.py
```

Bu komut, `info.txt` dosyasındaki videoların detaylarını çekecek ve bir word dosyasına kaydedecektir.

### 6. Sonuçların İncelenmesi

Bot çalıştırıldıktan sonra, çekilen veriler bir word dosyasında depolanacaktır. Bu dosyayı inceleyerek video detaylarını görüntüleyebilirsiniz.
