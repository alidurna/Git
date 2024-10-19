# Git Kullanma Kılavuzu

## 1. Git Kurulumu

### macOS:

Terminal'i aç ve Homebrew kullanarak Git'i yüklemek için şu komutu çalıştır:

```bash
brew install git
```

_Bu komut, Homebrew paket yöneticisi aracılığıyla Git'i yükler._

### Linux:

Terminal'i aç ve şu komutları kullanarak Git'i yükleyebilirsin:

```bash
sudo apt update
sudo apt install git
```

_Bu komut, APT paket yöneticisini kullanarak Git'i yükler ve sistemini günceller._

### Windows:

[Git resmi sitesinden](https://git-scm.com/download/win) Git'i indirip kurulum talimatlarını takip et.
_Windows kullanıcıları için, indirme ve kurulum süreci adım adım açıklanmıştır._

Kurulumdan sonra, terminal veya komut istemcisinde şu komutla versiyonunu kontrol edebilirsin:

```bash
git --version
```

_Yüklemenin başarılı olduğunu doğrulamak için Git versiyonunu kontrol et._

## 2. Git Temel Komutları

### Kullanıcı Bilgilerini Ayarlama:

İlk kez Git kullanıyorsan, kendine ait kullanıcı adı ve e-posta bilgilerini ayarlamalısın:

```bash
git config --global user.name "SeninAdın"
git config --global user.email "seninemailin@example.com"
```

_Bu bilgiler, yaptığın commitlerde yazar olarak kullanılacaktır._

## 3. Yeni Bir Depo Oluşturma

Projeni başlatmak için şu komutu kullanarak yeni bir Git deposu oluşturabilirsin:

```bash
git init
```

_Bu komut, bulunduğun dizini bir Git deposuna dönüştürerek, sürüm kontrolü yapmanı sağlar._

## 4. Depoyu GitHub'a Bağlama

GitHub'da yeni bir depo oluşturduktan sonra, projeyi GitHub'a push etmek için şu komutları kullanabilirsin:

1. GitHub'daki depoyu yerel projen ile bağla:

   ```bash
   git remote add origin https://github.com/kullaniciadi/depo-adi.git
   ```

   _Bu komut, yerel deponu GitHub'daki uzaktan bir depoya bağlar._

2. Dosyaları commit et ve GitHub'a gönder:
   ```bash
   git add .
   git commit -m "İlk commit"
   git push -u origin master
   ```
   _`git add .` komutu ile tüm değişiklikleri sahneye alırsın, `git commit` ile bu değişiklikleri kaydedersin ve `git push` ile de uzaktaki depoya gönderirsin._

## 5. Var Olan Bir Depoyu Klonlama

GitHub üzerindeki bir projeyi bilgisayarına çekmek için şu komutu kullanabilirsin:

```bash
git clone https://github.com/kullaniciadi/proje-adi.git
```

_Bu komut, belirtilen depoyu yerel bilgisayarına indirir ve çalıştırmaya hazır hale getirir._

## 6. Değişiklik Yapma ve Commit Etme

Projende değişiklik yaptıktan sonra bu değişiklikleri kaydedip Git'e göndermek için aşağıdaki adımları takip etmelisin:

1. Tüm dosyaları ekle:

   ```bash
   git add .
   ```

   _Bu komut, tüm değişiklikleri Git'in takip etmesi için sahneye alır._

2. Değişiklikleri commit et:

   ```bash
   git commit -m "Yaptığın değişikliğin açıklaması"
   ```

   _Yaptığın değişikliklerin ne olduğunu açıklamak için açıklayıcı bir mesaj yazmalısın._

3. Değişiklikleri GitHub'a push et:
   ```bash
   git push origin branch-adi
   ```
   _Bu komut, değişikliklerini uzaktaki depoya gönderir._

## 7. Branch Oluşturma ve Birleştirme

Yeni bir özellik geliştirmeye başlamadan önce yeni bir branch oluştur:

```bash
git checkout -b yeni-branch-adi
```

_Bu komut, yeni bir branch oluşturur ve bu branch'e geçiş yapar._

Branch'i tamamladıktan sonra ana branch ile birleştirmek için:

```bash
git checkout master
git merge yeni-branch-adi
```

_Bu komutlar, ana branch'e geri dönüp, oluşturduğun yeni branch'i ana branch ile birleştirir._

## 8. Değişiklikleri Geri Alma

Eğer yaptığın bir commit'i geri almak istersen:

```bash
git revert commit_hash
```

_Bu komut, belirtilen commit'i geri alır ve yeni bir commit oluşturur._

Eğer değişiklikleri tamamen silmek istiyorsan:

```bash
git reset --hard HEAD~1
```

_Bu komut, son commit'i geri alır ve dosyalarını en son commit'ten bir önceki hale getirir._

## 9. Güncel Değişiklikleri Çekme

Uzaktan depodaki güncellemeleri yerel deponla senkronize etmek için:

```bash
git pull origin master
```

_Bu komut, uzaktaki depodan en son değişiklikleri çeker ve yerel deponla birleştirir._

## 10. Yardım Alma

Git ile ilgili yardım almak için aşağıdaki komutu kullanabilirsin:

```bash
git help
```

_Bu komut, Git'in kullanımına dair bilgiler ve komutlar hakkında yardım almanı sağlar._

## Sonuç

Git, projelerini etkili bir şekilde yönetmeni sağlayan güçlü bir versiyon kontrol sistemidir. Bu kılavuz, Git ile çalışma sürecine başlamak için temel adımları içermektedir.
