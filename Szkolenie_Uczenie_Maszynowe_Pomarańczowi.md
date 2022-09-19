# Szkolenie Uczenie Maszynowe Pomarańczowi


1. Co to jest uczenie maszynowe?
    - Statystyka a uczenie maszynowe
    - Rodzaje problemów
    - Przykładowe metody
    - Rodzaje błędów popełnianych przez algorytmy
    - Ekosystem uczenia maszynowego w Pythonie


## Co to jest uczenie maszynowe?

Zbiór algorytmów, które ma za cel znalezienie takiej funkcji **f(X),** która dla zadanych **X**(danych wejściowych), dobrze aproksymuje zmienna **y.**

## Statystyka a uczenie maszynowe

Uczenie maszynowe to pojęcie łączące różne modele, techniki i technologie uczenia się, które mogą obejmować statystykę. Sama statystyka koncentruje się na wykorzystaniu danych do formułowania prognoz i tworzenia modeli do analizy.
Prościej rzecz mówiąc, statystyka bada zależność między zmiennymi, natomiast przy użyciu chcemy uogólnić badane związki, by móc wykonać prognozy.






## Ogólny schemat przepływu pracy w procesie tworzenia modelu uczenia maszynowego


![](https://paper-attachments.dropbox.com/s_3705274B2AB7EC865CC9A44CB8D10436BAA5CDAE363F79767820876F4BB5A93C_1663516954648_ML_process1.png)


Czerwony krzyż - szkolenie nie obejmuje tego zakresu

- dane mam zebrane wcześniej, na szkoleniu nie ma czasu na ściaganie danych
- deployment stworzonego modelu - nie obejmuje tego tematu szkolenie, ale jesli na koniec starczy czasu, moge cos pokazac

 

## Rodzaje problemów


![](https://paper-attachments.dropbox.com/s_3705274B2AB7EC865CC9A44CB8D10436BAA5CDAE363F79767820876F4BB5A93C_1663536084276_ml1.png)


Zielonym prostokątem zostały oznaczone algorytmy, które będą omawiane na szkoleniu. Na zółto, algorytmy, które nie są w programie, natomiast jeśli na koniec starczy czasu i będą chętni, to na szybko je omówimy. Czerwone - nie jest to temat szkolenia i nie omówimy ich. Na każdy z tych algorytmów należało by przygotować oddzielne szkolenie.






## Uczenie z nadzorem(z nauczycielem) 
##  
- Klasyfikacja

to takie algorytmy, które pozwalają przypisać dane do odpowiednich kategorii. Przykład najbardziej znany, to podział maili na spam i nie-spam. Oprócz tego rozpoznawanie kwiatków po wyglądzie albo ręcznie napisanych cyferek. Jeśli przypisujemy dane do dwóch kategorii, to mamy do czynienia z klasyfikacją dwuklasową (ang. *two-class classification*). Jeśli etykiet jest więcej, to mówimy o klasyfikacji wieloklasowej (ang. *multiclass classification*).


**Przykład klasyfikacji binarnej**


![](https://paper-attachments.dropbox.com/s_3705274B2AB7EC865CC9A44CB8D10436BAA5CDAE363F79767820876F4BB5A93C_1663518585399_Screenshot+2022-09-18+at+18.28.30.png)



**Przykład klasyfikacji wieloklasowej**

U jakiego operatora posiadamy abonament na telefon z korbką?


![](https://paper-attachments.dropbox.com/s_3705274B2AB7EC865CC9A44CB8D10436BAA5CDAE363F79767820876F4BB5A93C_1663519611617_noname1.png)
![](https://paper-attachments.dropbox.com/s_3705274B2AB7EC865CC9A44CB8D10436BAA5CDAE363F79767820876F4BB5A93C_1663519605761_noname2.png)
![](https://paper-attachments.dropbox.com/s_3705274B2AB7EC865CC9A44CB8D10436BAA5CDAE363F79767820876F4BB5A93C_1663519562745_chad1.png)




- Regresja

To samo co klasyfikacja, tylko próbujemy przewidzieć zmienną ciągłą, a nie dyskretną jak w przypadku klasyfikacji(cena mieszkania, wartość pary BTC/USD, zarobki na OnlyFans).


![](https://paper-attachments.dropbox.com/s_3705274B2AB7EC865CC9A44CB8D10436BAA5CDAE363F79767820876F4BB5A93C_1663520235383_Screenshot+2022-09-18+at+15.33.34.png)






## Uczenie bez nadzoru (bez nauczyciela) - możemy omówić jeśli starczy czasu i grupa sobie będzie miała takie życzenie.
- Klasteryzacja(Kmeans, DBSCAN)

 Zadaniem tych algorytmów jest podzielenie danych na grupy (klastry) na podstawie podobieństw  np. klientów banku o podobnej historii.
 

![https://static.javatpoint.com/tutorial/machine-learning/images/clustering-in-machine-learning.png](https://paper-attachments.dropbox.com/s_3705274B2AB7EC865CC9A44CB8D10436BAA5CDAE363F79767820876F4BB5A93C_1663521257061_Screenshot+2022-09-18+at+19.13.04.png)


 
 
 Przykład złego i prawidłowego pogrupowania danych.
 

![https://www.semanticscholar.org/paper/The-MinMax-k-Means-clustering-algorithm-Tzortzis-Likas/e005940c7c758ea6ba830d1db4cf0f74c3c10514/figure/0](https://paper-attachments.dropbox.com/s_3705274B2AB7EC865CC9A44CB8D10436BAA5CDAE363F79767820876F4BB5A93C_1663521382230_Screenshot+2022-09-18+at+19.16.01.png)


 
 
 Nie ma obiektywnej miary, by okreslić liczbę klastrów, mały przykładzik



https://www.youtube.com/watch?v=evthRoKoE1o&


[https://youtu.be/evthRoKoE1o](https://youtu.be/evthRoKoE1o)


 

- Redukcja wymiarów(np LDA, PCA)



![https://blog.prokulski.science/2019/05/17/jak-interpretowac-pca/](https://paper-attachments.dropbox.com/s_3705274B2AB7EC865CC9A44CB8D10436BAA5CDAE363F79767820876F4BB5A93C_1663521607327_Screenshot+2022-09-18+at+15.37.49.png)


W PCA zakłada się, że im większa rozpiętość (czyli wariancja) tym lepsza zmienna (cecha) bo niesie w sobie więcej informacji. I odwrotnie, jeśli wartość własna jest bardzo mała –> wariancja jest bardzo mała –> dane są skupione na prostej, na której leży dany wektor własny –> cecha wnosi niewiele informacji.

Czas na quiz!(5 min)

https://www.flexiquiz.com/SC/N/bf063239-7cfe-4276-94dc-04073df0240f





## Rodzaje błędów popełnianych przez algorytmy


## Klasyfikacja

Żeby móc przedstawić metryki, na początku musimy wprowadzić pojęcie macierzy pomyłek (confusion matrix).


![](https://paper-attachments.dropbox.com/s_3705274B2AB7EC865CC9A44CB8D10436BAA5CDAE363F79767820876F4BB5A93C_1663523916632_image.png)





Czego możemy się dowiedzieć z tej macierzy?

Istnieją dwie możliwe klasy przewidywań: "tak" i "nie". Jeśli przewidywalibyśmy czy ktoś chce nas oszukać przez telefon, "tak" oznaczałoby że mamy do czynienia ze oszustem, oraz nie w przeciwnym przypadku.


Zdefiniujmy teraz najbardziej podstawowe pojęcia:

- **True Positive** (wyniki prawdziwie pozytywne) (**TP**): Nasz model przewidział, że mam do czynienia z oszustem  i rzeczywiście tak jest.
- **True Negative** (wyniki prawdziwie negatywne) (**TN**): Nasz model przewidział, że mamy do czynienia z uczciwa osoba  i rzeczywiście tak jest.
- **False Positive** (wyniki fałszywie dodatnie (**FP**):Nasz model przewidział, że dany pacjent jest oszustem ale w rzeczystosci jest uczciwy. (Znany również jako "błąd I rodzaju").
- **False Negative ( wyniki** fałszywie negatywne (**FN**)): Nasz model przewidział, że czlowiek jest uczciwy  i a w rzeczywistości jest oszustem (“błąd II rodzaju”).



![User-uploaded image: Screen+Shot+2021-11-14+at+15.21.28.png](https://paper-attachments.dropbox.com/s_5E7DF8AD02CB505BB463C7D83D16F66C681D0804B01EBBB61DA0200EFD7B4029_1636903305771_Screen+Shot+2021-11-14+at+15.21.28.png)


Używając wyżej wymienionych wskażników, możemy zdefiniować metryki oceniające jakość klasyfikatora:


- czułość: (inne spotykane nazwy: sensitivity, true positive rate TPR, hit rate, recall). Można ją interpretować jako prawdopodobieństwo, że klasyfikacja będzie poprawna pod warunkiem, że przypadek jest pozytywny
    $$TPR = \frac{TP}{TP+FN}$$
    
- częstość fałszywych alarmów ( false positive rate (FPR), fall-out): 


    $$FPR = \frac{FP}{TP+FN}$$


- precyzja pozytywna: (positive predictive value (PPV), precision)
    $$PPV = \frac{TP}{TP+FP}$$


- precyzja negatywna: (NPV)
    $$NPV = \frac{TN}{TN+FN}$$
    
- dokładność ( accuracy (ACC)): Prawdopodobieństwo prawidłowej klasyfikacji.

      $$ACC = \frac{TP+TN}{TP+TN+FP+FN}$$
      

- F1-score: średnia harminiczna z precyzji i czułości:
    $$F1 = \frac{2 PPV \cdot TPR}{PPV+TPR}$$
- współczynnik korelacji Matthews ( Matthews correlation coefficien)t:

$$MCC = \frac{TP \cdot TN - FP \cdot FN}{\sqrt{(TP+FP)(TP+FN)(TN+FP)(TN+FN)}}$$

Ten współczynnik uwzględnia wyniki zarówno prawdziwie jaki i fałszywie pozytywne i negatywne i jest na ogół uważany jako zrównoważona miara, która może być stosowana nawet wtedy, gdy klasy są bardzo różnej liczebności. MCC jest w istocie współczynnikiem korelacji pomiędzy obserwowanymi i przewidywanymi klasyfikacjami binarnymi; zwraca wartość od -1 do +1. Współczynnik +1 odpowiada idealnej klasyfikacji, 0 nie lepiej niż losowe przypisanie wyniku i -1 oznacza całkowitą niezgodę między klasyfikacją i stanem faktycznym.

Ten współczynnik uwzględnia wyniki zarówno prawdziwie jaki i fałszywie pozytywne i negatywne i jest na ogół uważany jako zrównoważona miara, która może być stosowana nawet wtedy, gdy klasy są bardzo różnej liczebności. MCC jest w istocie współczynnikiem korelacji pomiędzy obserwowanymi i przewidywanymi klasyfikacjami binarnymi; zwraca wartość od -1 do +1. Współczynnik +1 odpowiada idealnej klasyfikacji, 0 nie lepiej niż losowe przypisanie wyniku i -1 oznacza całkowitą niezgodę między klasyfikacją i stanem faktycznym.


- **Krzywą ROC** to wykres pokazujący działanie klasyfikatora binarnego funkcji jej odcięcia progu. **Zasadniczo pokazuje rzeczywistą liczbę wyników pozytywnych (TPR) w porównaniu z odsetkiem wyników fałszywie dodatnich (FPR) dla różnych wartości progowych.** 


    **Obszar pod krzywą** (AUC) jest zespolony miarą wydajności binarnej klasyfikatora o wszystkich możliwych wartości progowych (a zatem jest próg niezmienna **)** .
    AUC oblicza obszar pod krzywą ROC, a zatem mieści się w zakresie od 0 do 1. Jednym ze sposobów interpretacji AUC jest prawdopodobieństwo, że model plasuje losowo pozytywny przykład wyżej niż losowy przykład negatywny.


![User-uploaded image: Screen+Shot+2021-11-14+at+16.53.37.png](https://paper-attachments.dropbox.com/s_5E7DF8AD02CB505BB463C7D83D16F66C681D0804B01EBBB61DA0200EFD7B4029_1636908844033_Screen+Shot+2021-11-14+at+16.53.37.png)



Przyklady najlepszego, najgorszego i losowego klasyfikatora



![https://towardsdatascience.com/demystifying-roc-curves-df809474529a](https://paper-attachments.dropbox.com/s_3705274B2AB7EC865CC9A44CB8D10436BAA5CDAE363F79767820876F4BB5A93C_1663536759048_Screenshot+2022-09-18+at+23.31.39.png)



![](https://upload.wikimedia.org/wikipedia/commons/thumb/1/13/Roc_curve.svg/440px-Roc_curve.svg.png)


[https://upload.wikimedia.org/wikipedia/commons/thumb/1/13/Roc_curve.svg/440px-Roc_curve.svg.png](https://upload.wikimedia.org/wikipedia/commons/thumb/1/13/Roc_curve.svg/440px-Roc_curve.svg.png)



Ważna uwaga: Krzywą **ROC** uźywamy tylko dla klasyfikacji binarnej.



![](https://paper-attachments.dropbox.com/s_3705274B2AB7EC865CC9A44CB8D10436BAA5CDAE363F79767820876F4BB5A93C_1663524450759_Screenshot+2022-09-18+at+16.17.31.png)


Krotkie zadanko:

https://docs.google.com/spreadsheets/d/1-ftRcblRyra5SZP62IE5AcKyZPI1ld6Da7dAIZAblW8/edit#gid=0


[https://docs.google.com/spreadsheets/d/1-ftRcblRyra5SZP62IE5AcKyZPI1ld6Da7dAIZAblW8/edit](https://docs.google.com/spreadsheets/d/1-ftRcblRyra5SZP62IE5AcKyZPI1ld6Da7dAIZAblW8/edit)






## Regresja - metryki


## MSE

**Błąd średniokwadratowy** - znajduje średni kwadrat błędu między wartościami przewidywanymi i rzeczywistymi.

Załóżmy, że mamy model regresji, który przewiduje cenę domów w  (pokaż je za pomocą ŷᵢ) i powiedzmy, że dla każdego domu mamy również rzeczywistą cenę, za którą został sprzedany dom (oznaczony przez yᵢ). Następnie MSE można obliczyć jako:


![](https://paper-attachments.dropbox.com/s_5E7DF8AD02CB505BB463C7D83D16F66C681D0804B01EBBB61DA0200EFD7B4029_1636913470024_Screen+Shot+2021-11-14+at+18.10.50.png)



## RMSE


![](https://paper-attachments.dropbox.com/s_5E7DF8AD02CB505BB463C7D83D16F66C681D0804B01EBBB61DA0200EFD7B4029_1636913694126_Screen+Shot+2021-11-14+at+18.14.23.png)


Wlasności:

-  Jest bardzo popularna - jest to metryka, którą zasadniczo standardowa regresja liniowa optymalizuje/minimalizuje. 


- Im jest mniejsza tym lepiej - w końcu to błąd. Musi być >=0.


-  Większą wagę przykłada się do większych błędów. Mniejsze błędy (które są na przykład mniejsze niż 1.) będą miały jeszcze mniejszy wkład w ogólny błąd po podniesieniu do kwadratu, podczas gdy większe błędy będą miały znacznie większą wagę po podniesieniu do kwadratu.
-  Jest podatny na wartości skrajne. Duży błąd w danej próbce może mieć ogromny wpływ na ogólne wyniki i sprawić, że optymalizator skupi się na redukcji błędu dla tej jednej próbki, pogarszając przewidywania dla każdej innej próbki.


-  Jest łatwo optymalizowalny. Dzieje się tak ze względu na atrybut "kwadratowy", który sprawia, że jest on łatwo różniczkowalny, coś, co algorytmy oparte na gradiencie (takie jak Stochastic Gradient Descent) mogą wykorzystać.


-  Wiele znanych algorytmów (takich jak Lightgbm, Xgboost, Keras, itp.), Ma optymalizator dla niego.



## MAE

Średni błąd bezwzględny (lub średnie odchylenie bezwzględne) to kolejna miara, która znajduje średnią bezwzględną odległość między wartościami przewidywanymi i docelowymi. MAE zdefiniowano poniżej:


![](https://paper-attachments.dropbox.com/s_5E7DF8AD02CB505BB463C7D83D16F66C681D0804B01EBBB61DA0200EFD7B4029_1636913607258_Screen+Shot+2021-11-14+at+18.12.54.png)


Własności metryki MAE:
1) MAE jest również popularna i jako ciekawostka, istnieje niekończąca się dyskusja na temat tego, która metryka jest lepsza, MAE czy RMSE. Wszystko zależy od konkretnego przypadku.

2) Im jest mniejsza tym lepiej. Musi być >=0.

3) Wszystkie błędy są analogicznie ważone w tej metryce. Błąd równy 2 jest dwa razy gorszy niż błąd równy 1.

4) Jest podatna na wartości odstające (ale mniej niż RMSE).

5) Nie jest tak łatwo optymalizowalna. MAE nie jest różniczkowalne w zerze (gdy przewidywania są równe rzeczywistym) i w zależności od rozkładu celu, może to sprawić, że różne przybliżenia MAE będą lepsze od innych.


## MAPE

Średni bezwzględny błąd procentowy (MAPE): MAPE mierzy wielkość błędu w ujęciu procentowym (w porównaniu z wartościami rzeczywistymi). Jest to w zasadzie MAE, ale w procentach, ponieważ każdy błąd bezwzględny jest dzielony przez (bezwzględne) wartości rzeczywiste.


![](https://paper-attachments.dropbox.com/s_5E7DF8AD02CB505BB463C7D83D16F66C681D0804B01EBBB61DA0200EFD7B4029_1636914290383_Screen+Shot+2021-11-14+at+18.24.33.png)


Jest ona popularna wśród interesariuszy biznesowych. Dzieje się tak dlatego, że jest on łatwo zrozumiały i/lub możliwy do skonsumowania, ponieważ jest przedstawiony w formie procentowej. Np. "średnio we wszystkich kanałach otrzymujemy błąd x% z naszego modelu".

2) Im jest mniejszy, tym lepiej. Należy zauważyć, że może on przyjmować wartości wyższe niż 100%.

3) Wszystkie błędy % są analogicznie ważone. Błąd na poziomie 20% jest dwa razy gorszy niż błąd na poziomie 10%.

4) Błąd ten nie uwzględnia objętości/wielkości normalnego błędu. Błąd o wartości 1.000$, gdzie rzeczywiste wartości wynosiły 10.000$ (np. 1.000$/10.000$ =10%) ma taki sam udział jak błąd o wartości 1.000.000$, gdzie rzeczywiste wartości wynosiły 10.000.000$ (np. 1.000.000$ /10.000.000$ =10%). Na innym przykładzie, gdy błąd bezwzględny wynosi 0,2 $, a rzeczywisty 0,1 $, MAPE wynosi 200%, czyli 20 razy więcej niż w powyższych przykładach i będzie miał 20 razy większą wagę w minimalizacji metryki. Oznacza to również, że możesz zgłaszać mniejszy błąd, ponieważ wszystkie te przypadki o małej objętości są zbliżone procentowo, podczas gdy brakuje niektórych z bardzo wysokimi wartościami rzeczywistymi o miliony / miliardy. Każdy błąd staje się względny w stosunku do wartości rzeczywistych.

5) Metryka nie jest zdefiniowana, gdy rzeczywiste wartości są zerowe. Istnieją różne sposoby radzenia sobie z tym. Na przykład, zerowe wartości rzeczywiste mogą zostać usunięte z obliczeń lub może zostać dodana stała. Każdy sposób postępowania w przypadku zerowych wartości rzeczywistych ma swoje wady, dlatego też metryka ta nie jest zalecana w przypadku problemów z wieloma zerami. 

6) Nie jest podatny na wartości odstające w tym samym sensie, w jakim są RMSE i MAE. Oznacza to, że jeden lub dwa wysokie błędy mogą nie być wystarczające, aby spowodować, że ta metryka "oszaleje"(!), zwłaszcza jeśli rzeczywiste wartości są również bardzo wysokie, jednak problemy mogą wynikać z ogólnego rozkładu celu (patrz następny punkt).




## R2


![](https://paper-attachments.dropbox.com/s_5E7DF8AD02CB505BB463C7D83D16F66C681D0804B01EBBB61DA0200EFD7B4029_1636914575762_Screen+Shot+2021-11-14+at+18.29.13.png)


Własności:

- Im jest wyższa, tym lepszy model.  Przyjmuje wartości od minus nieskończoności do +1.
- Ułatwia porównanie jakości modeli.


**R-kwadrat** Ocena
< 0,0 Gorzej niż przy użyciu średniej z celu
< 0,1 Słaby
< 0.2 Dość słaba
< 0,3 Słaby do średniego
< 0,5 Średni
< 0,7 Średni do silnego
< 0,9 Silny

0,9 Znakomity!


https://docs.google.com/spreadsheets/d/1-ftRcblRyra5SZP62IE5AcKyZPI1ld6Da7dAIZAblW8/edit#gid=0


[https://docs.google.com/spreadsheets/d/1-ftRcblRyra5SZP62IE5AcKyZPI1ld6Da7dAIZAblW8/edit](https://docs.google.com/spreadsheets/d/1-ftRcblRyra5SZP62IE5AcKyZPI1ld6Da7dAIZAblW8/edit)






# Rodzaje błędów popełnianych przez algorytmy




![](https://paper-attachments.dropbox.com/s_3705274B2AB7EC865CC9A44CB8D10436BAA5CDAE363F79767820876F4BB5A93C_1663525504132_Screenshot+2022-09-18+at+15.56.10.png)




![](https://paper-attachments.dropbox.com/s_3705274B2AB7EC865CC9A44CB8D10436BAA5CDAE363F79767820876F4BB5A93C_1663525598304_Screenshot+2022-09-18+at+16.43.57.png)

![](https://paper-attachments.dropbox.com/s_3705274B2AB7EC865CC9A44CB8D10436BAA5CDAE363F79767820876F4BB5A93C_1663525673123_Screenshot+2022-09-18+at+16.30.44.png)




![](https://paper-attachments.dropbox.com/s_3705274B2AB7EC865CC9A44CB8D10436BAA5CDAE363F79767820876F4BB5A93C_1663525700189_Screenshot+2022-09-18+at+15.45.45.png)



![](https://paper-attachments.dropbox.com/s_3705274B2AB7EC865CC9A44CB8D10436BAA5CDAE363F79767820876F4BB5A93C_1663525802118_Screenshot+2022-09-18+at+16.02.04.png)

# Ekosystem uczenia maszynowego w Pythonie



![](https://paper-attachments.dropbox.com/s_3705274B2AB7EC865CC9A44CB8D10436BAA5CDAE363F79767820876F4BB5A93C_1663524803642_Screenshot+2022-09-18+at+20.12.53.png)






- Google colab - nasze główne narzędzie

https://colab.research.google.com 



![](https://paper-attachments.dropbox.com/s_3705274B2AB7EC865CC9A44CB8D10436BAA5CDAE363F79767820876F4BB5A93C_1663524592630_Screenshot+2022-09-18+at+15.42.52.png)




- Środowisko do pracy interaktywnej z kodem.
- Google Colab — implementacja jupytera od Google.
- Używając go, uciekamy od konieczności tworzenia środowiska wirtualnego czy dockera - 
    każdy ma ten sam zestaw bibliotek i modułów.
- Z racji tego, że Colab używa Ubuntu, możemy używać również składni BASHA -
    czasami korzysta się z tej własności, na przykład przy wspólnej pracy z Google Drive.

Czym się różni Jupyter(Colab) od standardowego pliku *.py? 

- W pliku kod jest wywołany sekwencyjnie-linia za linią, w notebooku każda komórka możemy odpalić w dowolnej kolejności — to ma swoje zalety, jak i wady.
- Kod napisany  w notatniku nie zawsze zadziała, jeśli nastąpi jego bezpośrednia konwersja na plik *.py(na przykład w kodzie znajdują się linie związane z instalacją modułów przy pomocy **pip(**pip is the package installer for Python).







UŹYWANE BIBLIOTEKI


![](https://paper-attachments.dropbox.com/s_3705274B2AB7EC865CC9A44CB8D10436BAA5CDAE363F79767820876F4BB5A93C_1663525370407_Screenshot+2022-09-18+at+20.21.51.png)



- Pandas - do działania na danych w formacie tabularycznym - analogia do SQL czy Excel 
- Numpy - słuzy do operacji na macierzach, czasami istnieje potrzeba zamiany tabeli na macierz - wszystko wychodzi w praniu
- Sklearn - najpopularniejszy framework do Machine Learing, świetny dla początkujących oraz prototypowania rozwiązań.
- Matplotlib i Seaborn - wizualizacje danych

