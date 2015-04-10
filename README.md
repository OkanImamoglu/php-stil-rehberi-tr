Merhaba! bu geliştirmeye açık Türkçe PHP stil rehberidir. Dilediğiniz gibi katkıda bulunabilirsiniz.

# php-stil-rehberi-tr
Herkese açık php stil rehberi

## Genel
1. Tab yerine 4 boşluk kullanılacak
2. Shortag <? **kullanılmayacak** onun yerine **<?php** kullanılacak
3. Php dosyası bitiminde ?> ile tag **kapatılmayacak**

## Laravel

### Model
1. Model isimleri tekil olacak. Örn. User
2. İlişkiler ilişkinin tipine göre çoğul veya tekil isimlendirilecek. Örn. HasMany: user*s*, hasOne: user

### Route

1. Route'lar restful tasarlanacak.

2. Route'lar çoğul olacak. Örn. /users/

3. Nested Route'lar ilişki tipine göre çoğul veya tekil isimlendirilecek. Örn. hasMany: users/1/customer**s** , hasOne: customers/2/user

4. Çok kelimeli Route'lar tire "-" ile ayrılacak. Örn. /hello-world/

#### Restful Servisler

1. İlişkili tablolar _embed={tabloAdi} sorgusuyla çağırılacak. Örn. /customers/1?**_embed=user**
2. Birden fazla alan isteniyorsa virgül(,) ile ayrılacak. Örn. /customers/1?**_embed=user,detail**
3. Birebir eşlenik sorgular {alan}={deger} ile çağrılacak. Örn. /customers?**user_id=1**
4. Like sorguları {alan}=%{deger}% şeklinde çağırılacak. Örn. /customers?**name=%can%**
5. Sayfalama _page={sayfa} şeklinde çağrılacak. Örn. /customers?**_page=1**
6. Limit _limit={deger} şeklinde çağırılacak Örn. /customers?**_limit=25**
7. Fulltext arama sorgular _q={deger} şeklinde çağrılacak. Örn. /customers?**_q=can**

### Controller

Controller isimleri Tekil olacak ve sonunda Controller yazacak. Örn. UserController

### Migration

1. **Tablo Yaratma** create_**{{ $tabloAdi }}**_table

2. **Tablo Silme** delete_**{{ $tabloAdi }}**_table

3. **Sütun Ekleme** add_**{{ $sutunAdi}}**_column_to_**{{ $tabloAdi }}**_table

## Veritabanı
### Tablo İsimleri
Tablo isimleri çoğul ve anlamlı olmalıdır (users, posts vs...)
### İlişkili Tablolar
Bir foreign key ilişkiyi tuttuğu tablonun tekil adından türetilmelidir.

users, ve posts tablolarında foreign key posts tablosunda user_id şeklinde tutulmalıdır.

## Git

Her commit sadece kendisi ile ilgili yapılan işlemleri açıklayacak. Bir özellik tamamlandığı zaman commit edilecek. Birden fazla özellikle birlikte commit edilmeyecek. Açıklamalar ne yapıldığını tam olarak açıklayacak fakat 50 karakterden uzun olmayacak. İlk hafler büyük olacak ve yapılan işlemi açıklayacak örn. Eklendi, Güncellendi, Silindi, Düzeltildi gibi.

##### Örnekler

**Initial Commit**

**Added:** carousel.js for carousel feature on homepage

**Updated:** carousel.js for fixing dancing bug

**Deleted:** carousel.js beacuse it become unnecessary after adding bootstrap 

Standart olarak git-flow takip edilecek.

http://danielkummer.github.io/git-flow-cheatsheet/
TR: http://danielkummer.github.io/git-flow-cheatsheet/index.tr_TR.html
