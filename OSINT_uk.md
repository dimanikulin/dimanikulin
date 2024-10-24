# Headline

TBD

# Alternative headline

TBD

# Table of contents

- [Tags](./OSINT_uk.md#tags)
- [Definitions, Acronyms, Abbreviations](./OSINT_uk.md#definitions-acronyms-abbreviations)
- [Overview](./OSINT_uk.md#overview)
- [Introduction](./OSINT_uk.md#introduction)
- [References](./OSINT_uk.md#references)

# Tags

TBD

# Definitions, Acronyms, Abbreviations

| # | Abbreviation or Acronym | Definition     |
| - | ------------------------|:--------------:|
| 1 |

# Overview

TBD

or ---

# Introduction

<https://www.youtube.com/live/8sC8x79iyP8>

Розвідка соціальних мереж (SOCMINT) - це різновид розвідки з відкритим кодом (OSINT), яка стосується збору та аналізу даних з веб-сайтів соціальних мереж. Вона охоплює всі соціальні медіа-платформи, а не лише соціальні мережі.

З чого починати загальний пошук акаунту людини в соцмережах?

Почніть із широкого пошуку, якщо ви не визначилися з конкретною платформою.
Пошук за іменем користувача - найшвидший спосіб для більшості соціальних мережах, за умови, що цільова особа постійно використовує одне й те саме ім'я користувача.
Крім того, ім'я користувача може виявити ім'я/прізвище, яке відрізняється від того, що вказано на сторінці в соціальній мережі.
Це створює додаткові критерії для пошуку.
Просто введіть ім'я користувача в Namechk.com (<https://namechk.com/>) або Instantusername.com (<https://instantusername.com/#/>) і проскануйте сотні веб-сайтів за лічені хвилини.

Якщо вам потрібна більш розширена функціональність - скористайтеся локально встановленим інструментом Maigret (<https://github.com/soxoj/maigret>), щоб налаштувати процес пошуку і створити HTML-звіти.
Використовуйте Wayback Machine (<https://web.archive.org/>), щоб отримати доступ до історичних даних знайдених вами сторінок у соціальних мережах.
Не всі вони архівуються, особливо менш популярні, але спробувати варто.

оно должно быть уникальным, Иванов или Джон даст мало результатов

- іменем користувача

WhatsMyName (<https://whatsmyname.app/>) by name
Namecheckup (<https://namecheckup.com/>) domain names cjec
Sherlock (<https://github.com/sherlock-project/sherlock>) Hunt down social media accounts by username across 400+ social networks

- електронну пошту
- домен
- хеш
- номер телефону
- зображення тощо

Зворотний пошук за зображеннями дуже корисний, коли цільовий акаунт завантажив унікальне зображення профілю або інші фотографії.
Для цього добре підходять Google (<https://images.google.com/>) і TinEye (<https://tineye.com/>), хоча, можливо, вам доведеться переглянути багато зображень, які не відповідають цільовому.

EXIF-дані зображення містять цінну інформацію, але веб-сайти зазвичай її видаляють.
Перевірте, чи доступні вони за допомогою Viewexifdata.com (<https://www.viewexifdata.com/>).

Функція "Забули пароль" - зручний інструмент для перевірки того, чи зареєструвалася цільова особа на сайті.
Однак перевіряти кожен сайт по черзі нудно, і Python-інструмент Holehe (<https://github.com/megadose/holehe>) спрощує цю процедуру.
Якщо ви не хочете встановлювати щось локально, скористайтеся онлайн-сервісом Epieos (<https://epieos.com/>), який робить запити до Holehe.

Якщо ви не впевнені в достовірності адреси, скористайтеся Proofy.io (<https://proofy.io/>), щоб перевірити, чи існує ця адреса.
Щоб отримати більше інформації про особу, перевірте пошту за відомими порушеннями на Dehashed.com (<https://dehashed.com/>).
Там можуть з'явитися деякі соціальні мережі, наприклад, нещодавній злом Facebook.

Якщо у вас є номер телефону, перевірте його за допомогою TrueCaller (<https://www.truecaller.com/>) або GetContact (<https://www.getcontact.com/>), щоб отримати можливе ім'я/прізвище, а потім знайдіть акаунт у соціальних мережах.

<https://webmii.com/> - a tool that collects publicly available information about a wanted person by name and indicates the source from which he found it
Telerecon (<https://github.com/sockysec/Telerecon>) - is a comprehensive OSINT-intelligence framework for investigating, investigating and extracting data from Telegram.

FaceCheckID (<https://facecheck.id/>) – безкоштовний інструмент для пошуку за обличчям серед десятків платформ. Сервіс стверджує, що у його базі знаходяться понад 560 млн облич.
<https://github.com/Alb-310/Geogramint> - Geogramint is an OSINT tool that uses Telegram's API to find nearby users and groups.
Vortimo OSINT (<http://find.osint-tool.com/>) – онлайн-інструмент для швидкого пошуку в сотнях різних джерел і подальшої обробки знайденої інформації. Як відправну точку можна використовувати:

<https://osintframework.com/>

https:// (<https://github.com/dimdenGD/OldTweetDeck)geospy.ai> GeoSpy - геолокація зображень за допомогою ШІ

<https://www.picarta.ai> Picarta - геолокалізація зображень за допомогою штучного інтелекту. АІ-модель прогнозує точне місце, де було зроблено фотографію в світі

<https://github.com/krakodjaba/telanalysis> - TelAnalysis - інструмент для аналізу Telegram, аналіз телеграм-каналів, чатів.
Дозволяє вигружати учасників чатів, їх видимі імена, нікнейми, кількість повідомлень тощо

GeoHints – великий довідник з фотографіями предметів з різних країн. Допоможе при проведенні досліджень за фото або відео. Туди входять:

- номерні знаки
- поштові скриньки
- номери будинків
- бічні доріжки
- світлофори
і багато іншого.
geohints.com

Сервіс для пошуку інформації про профіль Whatsapp за номером телефону
Доступний прямо в браузері і не потребує входу в WhatsApp
Можна отримати ідентифікатор профілю, опис, електронну пошту, веб-сайт, місцезнаходження тощо. Працює не тільки для бізнесу, але й для особистих профіль.
whatsapp.checkleaked.cc

<img src="./Images/TBD.jpg" alt="TBD" />

# References

| # | Name                 | Source                | Release date           |  Author                 | Description   |
| - | ---------------------|---------------------- |----------------------- | ----------------------- |:-------------:|
