Merhaba! bu geliştirmeye açık Türkçe PHP stil rehberidir. Dilediğiniz gibi katkıda bulunabilirsiniz.

# php-stil-rehberi-tr
Herkese açık php stil rehberi

## Genel
1. Tab yerine 4 boşluk kullanılacak
2. Shortag <? **kullanılmayacak** onun yerine **<?php** kullanılacak
3. Php dosyası bitiminde ?> ile tag **kapatılmayacak**

## Laravel

### Model
1. Model isimleri tekil olacak. Örn. User
2. İlişkiler ilişkinin tipine göre çoğul veya tekil isimlendirilecek. Örn. HasMany: user*s*, hasOne: user

### Route

Route'lar restful tasarlanacak.

Route'lar çoğul olacak. Örn. /users/

Nested Route'lar ilişki tipine göre çoğul veya tekil isimlendirilecek. Örn. hasMany: users/1/customer**s** , hasOne: customers/2/user

Çok kelimeli Route'lar tire "-" ile ayrılacak. Örn. /hello-world/

### Controller

Controller isimleri Tekil olacak ve sonunda Controller yazacak. Örn. UserController
