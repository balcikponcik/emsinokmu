# 💘 Emsi Ok mu? Nok mu?

Aşk, arkadaşlık, iş yeri, akrabalar, futbol, spor ve siyaset üzerine **2000 kaotik soru** içeren, rastgele kart çekilen bir parti oyunu.
Tek bir HTML dosyasıdır; kurulum, sunucu ya da kütüphane gerektirmez.

## Nasıl oynanır?

1. **Kart çek** düğmesine bas. Deste karışır ve kartlar rastgele, tek tek gelir.
2. Soruyu yüksek sesle oku. Herkes aynı anda **"OK!"** ya da **"NOK!"** desin.
3. Çoğunluğun kararını gir. Azınlıkta kalan kendini savunur. 😄
4. Deste bitince masanın OK/NOK karnesi çıkar.

**Kontroller**

| Hareket | OK | NOK | Atla |
|---|---|---|---|
| Düğme | OK | NOK | Atla |
| Kaydırma (telefon) | Sağa | Sola | — |
| Klavye | → | ← | Boşluk |

**🚩 RED FLAG** düğmesine (ya da klavyede **R** tuşuna) basınca ekran kırmızı siren ışıklarıyla yanar ve siren sesi çalar. Sayaç, oyunda kaç red flag yakalandığını tutar.

**💚 GREEN FLAG** düğmesine (ya da klavyede **G** tuşuna) basınca ekran yeşil ışınlar ve uçuşan kalplerle kutlama moduna geçer, neşeli bir melodi çalar. Onun da ayrı bir sayacı vardır.

## Kategoriler

| Kategori | Kart |
|---|---|
| 💘 Flört ve Tanışma | 75 |
| 📱 Telefon ve Sosyal Medya | 70 |
| 😤 Kıskançlık ve Sınırlar | 65 |
| 💸 Para ve Sorumluluk | 57 |
| 👨‍👩‍👧 Aile ve Çevre | 50 |
| 💍 Ciddi İlişki ve Evlilik | 60 |
| 🛋️ Günlük İlişki Kaosu | 83 |
| 🔥 Ayrılık ve Barışma | 55 |
| 🎲 Tamamen Kaos | 35 |
| 🤝 Arkadaşlık | 160 |
| 💼 İş Yeri | 150 |
| 🧓 Akrabalar | 140 |
| ⚽ Futbol | 396 |
| 🏅 Spor | 135 |
| 🗳️ Siyaset ve Toplum | 178 |
| 🏙️ Şehir ve Gündelik Hayat | 147 |
| 🍽️ Yeme-İçme ve Tatil | 144 |
| **Toplam** | **2000** |

Üstteki **Kategoriler** menüsünü açıp sadece istediğin kategorileri oynatabilirsin.

### 😏 Ahmet'in Çapkınlık Dosyası

Yaklaşık her 20 kartta bir sarı renkli **ÖZEL** kart gelir. Bu kartlarda Ahmet'in çapkınlığıyla ilgili 70 soru vardır. Hepsi çıktıktan sonra yeniden karıştırılıp gelmeye devam eder.
Bu kartlar 2000'lik desteye sayılmaz, ama verilen oylar skora eklenir.

## GitHub Pages ile yayınlama

1. GitHub'da yeni bir repo aç (örneğin `emsi-ok-mu-nok-mu`).
2. Bu klasördeki dosyaları (`index.html`, `README.md`, `.nojekyll`) repoya yükle:
   ```bash
   git init
   git add .
   git commit -m "Emsi Ok mu? Nok mu? ilk sürüm"
   git branch -M main
   git remote add origin https://github.com/KULLANICI_ADIN/emsi-ok-mu-nok-mu.git
   git push -u origin main
   ```
   Komut satırı kullanmak istemezsen GitHub sayfasında **Add file → Upload files** ile dosyaları sürükleyip bırakabilirsin.
3. Repoda **Settings → Pages** bölümüne gir.
4. **Source** kısmında `Deploy from a branch`, branch olarak `main`, klasör olarak `/ (root)` seç ve **Save**'e bas.
5. Bir iki dakika sonra oyun şu adreste açılır:
   `https://KULLANICI_ADIN.github.io/emsi-ok-mu-nok-mu/`

Linki arkadaşlarına at, herkes telefondan oynayabilir.

## Soru eklemek ya da değiştirmek

Bütün sorular `index.html` içindeki `CATS` (normal kartlar) ve `SPECIAL` (Ahmet kartları) dizilerindedir.
Yeni soru eklemek için ilgili kategorinin `items` listesine tırnak içinde bir satır daha eklemen yeterli:

```js
{ id: "kaos", name: "🎲 Tamamen Kaos", items: [
  "Sevgiliye yapay zekâya aşk mektubu yazdırmak",
  "Senin yeni sorun buraya",
  ...
]}
```

Özel kartların hangi sıklıkla geleceğini `nextGap` satırından ayarlayabilirsin (şu an 18–22 kartta bir).
