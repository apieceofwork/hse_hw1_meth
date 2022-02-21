# Домашнее задание № 1

Весь код для всех заданий можно найти в Colab по [ссылке](https://colab.research.google.com/drive/1tJ0M8X62A8qllO6LZ-jini9n6X6Ptm2t#scrollTo=RQAK_lggxsXi)

## № 1

**Вопросы:**

**1) Какие особенности можно наблюдать по сравнению с секвенированием ДНК или РНК?** 

Обычно при ДНК/РНК секвенировании соотношение С и G , A и T относительно однородно: кол-во G=C, также как и кол-во А=T (в РНК могут быть незначительные расхождения). Однако, в данном случае наблюдается достаточно яркое различие с секвенированием ДНК/РНК, посколько кол-во нуклеотидов С намного меньше кол-ва нуклеотидов G. Чем это можно объяснить?
Вследствие воздействия бисульфитного секвенирования на одноцепочечную ДНК, в частности самого бисульфита, цитозин (С) превращается в урацил (U) (он считывается как тимин, а в комлементарной цепи - как аденин) при условии, что цитозин не метилирован. Если же цитозин все-таки метилирован, С не превращается в U.


**Отчёты FASTQC (статистику можно найти ниже)**

<img width="700" alt="Screenshot 2022-02-21 at 12 42 38" src="https://user-images.githubusercontent.com/57996343/154930181-414bfe99-42a5-49fc-b326-035fab5caad7.png">

<img width="700" alt="Screenshot 2022-02-21 at 12 49 38" src="https://user-images.githubusercontent.com/57996343/154932052-b87541c4-7b94-4625-9e17-5ae3119ffa11.png">


<img width="700" alt="Screenshot 2022-02-21 at 12 50 01" src="https://user-images.githubusercontent.com/57996343/154930926-cbe33016-4f6b-4910-bd95-d645b44d4459.png">


<img width="700" alt="Screenshot 2022-02-21 at 12 50 15" src="https://user-images.githubusercontent.com/57996343/154930953-38bfc1dc-6c20-4696-b53f-2b99bfa06f97.png">


<img width="700" alt="Screenshot 2022-02-21 at 12 50 27" src="https://user-images.githubusercontent.com/57996343/154930963-655f6be5-4112-413c-b0bb-addad84aa361.png">


<img width="700" alt="Screenshot 2022-02-21 at 12 50 38" src="https://user-images.githubusercontent.com/57996343/154930972-9e9e7e64-516b-4871-b245-aa9af80b5ef9.png">


<img width="700" alt="Screenshot 2022-02-21 at 12 51 25" src="https://user-images.githubusercontent.com/57996343/154930998-db8ca463-9050-4809-87e8-cbe9b6db7fdb.png">


<img width="700" alt="Screenshot 2022-02-21 at 12 55 30" src="https://user-images.githubusercontent.com/57996343/154931655-55bd692f-cb44-4b77-83e0-39f832736d24.png">

<img width="700" alt="Screenshot 2022-02-21 at 12 55 54" src="https://user-images.githubusercontent.com/57996343/154931671-fefcd4c9-368d-43f1-abbc-8724f4d40bc1.png">

## №2

**а)Таблица с числом ридов для каждого образца**

<img width="458" alt="Screenshot 2022-02-21 at 13 19 40" src="https://user-images.githubusercontent.com/57996343/154937122-c609571c-71a1-4c1d-b0d7-36bb6f90bdca.png">


**b)Таблица с дедуплицированными ридами** 

<img width="458" alt="Screenshot 2022-02-21 at 18 38 00" src="https://user-images.githubusercontent.com/57996343/154986785-c3c2bcc7-0d47-4aa3-8a51-b79bd38e8c22.png">





**d) Скриншоты M-bias plot** 

Анализ графиков:

Во всех стадиях наблюдается некое изменение в % метилирования: волны метилирования при переходе из 1 стадии во 2 падают, а при переходе из 2 в третью наоборот возрастают почти в 2 раза, например: если на графике в стадии (8cell) можно наблюдать % метилирования чуть больше 40%, уже во 2 стадии (ICM) этот показатель уменьшается примерно до 21-22%, а в последней стадии (epiblast) он снова возрастает на +- 20%, что может быть объяснено тем, что по мере дифференцировки тканей % метилирования очень сильно возрастает (поэтому этот показель высок в стадии эпибласта). Это подтверждено данными из приведенной в условии домашнего задания [статьи](https://en.wikipedia.org/wiki/DNA_methylation#During_embryonic_development).

**8 cell**

<p float="left">
  <img src="https://user-images.githubusercontent.com/57996343/154942793-bb2225a5-31a5-497d-8ae3-863f5940030e.png" width="500" />
  <img src="https://user-images.githubusercontent.com/57996343/154942935-eef95efc-5241-43f4-8413-9af417a999be.png" width="505" /> 
</p>

**ICM**

<p float="left">
<img src="https://user-images.githubusercontent.com/57996343/154947998-3a7a6de0-fd24-4d75-bd50-5fb546352ffc.png" width="500" />
<img src="https://user-images.githubusercontent.com/57996343/154948026-ce05bb12-541c-4d94-85ec-fa9413143996.png" width="500" />
</p>



**Epiblast**

<p float="left">
<img src="https://user-images.githubusercontent.com/57996343/154948200-eca69bbe-c052-4ce7-a36a-6608d7bc1369.png" width="500" />
<img src="https://user-images.githubusercontent.com/57996343/154948235-272cef3e-1121-445c-8efa-1f28f2575fa2.png" width="507" />
</p>

**e)Гистограммы с распределением цитозинов по хромосоме** 

Выводы:

Анализируя каждый график, можно сказать, что частота и % метилирования С (цитозинов) меняются в зависимости от смены стадий эмбрионального развития мыши (от 8 сеll до epiblast). В частности: в стадии 8cell частота в 50% случаев - 0% метилирования; в стадии ICM частота в 60% случаев - 0% (это означает, что процесс метилирования на этой стадии происходит на самом деле еще реже, чем на стадии 8 cell, потому что в еще большей части случаев процент метилирования минимален), однако это все меняется на последней стадии epiblast - в большей части случаев метилирование происходит. Это и подтверждено графиком + данными из [статьи](https://en.wikipedia.org/wiki/DNA_methylation#During_embryonic_development), потому что ближе к стадии эпибласта % метилирования начинает резко возрастать.

* код для этого задания лежит также в моем [Colab'e](https://colab.research.google.com/drive/1tJ0M8X62A8qllO6LZ-jini9n6X6Ptm2t#scrollTo=RQAK_lggxsXi)

![photo_2022-02-21 19 11 06](https://user-images.githubusercontent.com/57996343/154992674-c57b6a78-57cc-481e-976f-acd2fa4863ff.jpeg)


<img width="600" alt="Screenshot 2022-02-21 at 19 19 07" src="https://user-images.githubusercontent.com/57996343/154992991-99ebd436-7450-4065-afc6-ed07438f2dd1.png">



![photo_2022-02-21 19 11 17](https://user-images.githubusercontent.com/57996343/154992535-1056d025-cc8f-415d-901a-fb72de596f56.jpeg)


**f) Визуализация метилирования и покрытия каждого образца**

Вывод: 

% Метирования и покрытия коррелируют со сменой стадий эмбрионального развития. Покрытие, как и метилирование уменьшается на стадии icm, а потом резко увеличивается на стадии epiblast.

<img width="805" alt="Screenshot 2022-02-21 at 21 29 29" src="https://user-images.githubusercontent.com/57996343/155009923-1970d6e8-620f-40c9-9daa-428dc84b79b5.png">

<img width="805" alt="Screenshot 2022-02-21 at 21 29 46" src="https://user-images.githubusercontent.com/57996343/155009934-39fe156e-beae-4d99-b0bf-fe92018f7bbe.png">



