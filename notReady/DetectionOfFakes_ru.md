# Headline
TBD

# Alternative headline

TBD

# Table of contents

- [Tags](./!Template.md#tags)
- [Definitions, Acronyms, Abbreviations](./!Template.md#definitions-acronyms-abbreviations)
- [Overview](./!Template.md#overview)
- [Introduction](./!Template.md#introduction)
- [References](./!Template.md#references)

# Tags

TBD


# Overview

TBD

or ---

# Introduction

Итак, мы взяли 3 фотографии:
 
1. точный фейк (женщина с открытым ртом) 

<img src="./images/DetectionOfFakes1.jpg"  style="max-width: 200" />

2. Реальную нефейковую фотографию  (женщина с закрытым ртом)

<img src="./images/DetectionOfFakes2.jpg"  style="max-width: 200" />

3. <??Неизвестно> (парни дурачатся в кафе)

 <img src="./images/DetectionOfFakes3.jpg"  style="max-width: 200" />

Закинули их в разные детекторы фейков  

# Decopy ai

Сначала в [AI Image Detector Identify](https://decopy.ai/ai-image-detector/)

И вот какой результат мы получили:

<img src="./images/DetectionOfFakes4.jpg"  style="max-width: 200" />
<img src="./images/DetectionOfFakes5.jpg"  style="max-width: 200" />
<img src="./images/DetectionOfFakes6.jpg"  style="max-width: 200" />

Детектор идентифицировал все фотографии как нефейковые (не созданные с помощью ИИ), даже то, которое мы точно знаем что фейковое.

Какие выводы мы можем сделать на основе проведённого эксперимента?

Однозначно рекомендовать не можем😔

# Was it ai
Берем следующий детектор - [Was it ai](https://wasitai.com/) и теже самые фото

И вот какой результат мы получили:

<img src="./images/DetectionOfFakes7.jpg"  style="max-width: 200" />
<img src="./images/DetectionOfFakes8.jpg"  style="max-width: 200" />
<img src="./images/DetectionOfFakes9.jpg"  style="max-width: 200" />

Детектор идентифицировал все фотографии как нефейковые (не созданные с помощью ИИ), даже то, которое мы точно знаем что фейковое.

Какой вывод можем сделать, друзья?

Однозначно рекомендовать не можем, так же как и предыдущий 😔

Можем предположить что оба детектора не определили фейковую фотографию, потому что не умеют работать именно с дипфейками.

# hivedetect ai

Итак, тестируем третий детектор - [hivedetect ai](https://hivedetect.ai/). Берем теже 3 фотографии
 
И вот какой результат мы получили:

<img src="./images/DetectionOfFakes10.jpg"  style="max-width: 200" />
<img src="./images/DetectionOfFakes11.jpg"  style="max-width: 200" />
<img src="./images/DetectionOfFakes12.jpg"  style="max-width: 200" />

Какие выводы мы можем сделать на основе проведённого эксперимента?

Детектор идентифицировал обе фотографии с женщиной как фейковые (не созданные с помощью ИИ а с помощью дипфейка), даже то, которое мы точно знаем что нефейковое.

А фотографию с парнями как чистый ИИ (даже с указанием нейросети, которой оно было создано). Откроем секрет, мы изначально знали, что фотография с парнями является фейком, т.к. мы действительно сами создали её в chatgpt.

Какой вывод можем сделать, друзья?

100%-но умеет определять изображения сгенерированные ИИ. И умеет работать с дипфейками. 

# Conclusion
Открытым остаётся вопрос, почему hivedetect ai указал настоящую фотографию как дипфейк. 

Попробуем разобраться. Ведь о реальности фото мы знаем лишь со слов женщины, которая любезно нам предоставила свое фото.

Возьмём фотографию другого человека, например Анжелины Джоли

 <img src="./images/DetectionOfFakes13.jpg"  style="max-width: 200" />

Детектор не выявил признаков ИИ и дипфейков,

<img src="./images/DetectionOfFakes14.jpg"  style="max-width: 200" />

 потому что фотография реальна, она не студийная и без обработки. Детектор #1 и #2 предсказуемо тоже определили Джоли как реальную. Обратите внимание, даже несмотря на идеальные зубы, которые всем рисует ИИ, детектор не определил фото как фейк.

Стоит отметить, что выше указанный детектор сотрудничает с Министерством обороны США в сфере определения фейковой информации. И как мы лично убедились, не зря, т.к. выдал нам достойные результаты проверки.

# References

| # | Name                 | Source                | Release date           |  Author                 | Description   |
| - | ---------------------|---------------------- |----------------------- | ----------------------- |:-------------:|
