# Tutorial 2019/2020
 Folder na kod, pliki i zestawy danych z tutorialu Collegium Invisible z edycji 2019/2020
 
 Uwaga: Z powodu problemów z renderowaniem niektórych notatników Jupyter przez GitHub wyrenderowane notatniki są dostępne również tu:
 https://nbviewer.org/github/dawidratynski/Tutorial-2019-2020/tree/master/Tutorial%202019-2020/

1) Klasyfikacja tekstu

	Celem tej części było poznanie podstaw uczenia maszynowego na przykładzie rozpoznawania języka / kategorii dokumentu oraz
	napisanie w pełni funkcjonalnego kodu do własnego modelu ze słownikiem, modelu Naive Bayes oraz z wykorzystaniem modeli
	regresji logistycznej oraz drzew losowych.
	Aby w pełni zrozumieć istotę regresji logistycznej próbowałem też napisać własny kod, którego jednak nie jestem w stanie 
	naprawić (zdebugować) z powodu jeszcze nie wystarczającej wiedzy technicznej.
	Pierwsze dwa projekty (własny model i Naive Bayes) używały słowników aby ocenić język dokumentu.
	Trzeci projekt (regresja logistyczna oraz lasy losowe) miał ocenić przynależność dokumentu do danej kategorii,
	np. spam / nie-spam, za pomocą zestawu odpowiednio opisanych przykładów. Z testów obydwu modeli jednoznacznie wynika, że
	do wybranego zadania (oddzielanie spamu) najlepiej sprawdzają się lasy losowe.
	W czasie pierwszej części zacząłem czytać książki: The Master Algorythm, Uczenie maszynowe z użyciem Scikit-Learn i TensorFlow 
	oraz zacząłem przerabiać kurs fastAI. Czytałem również kilka artykułów oraz obejrzałem kilka tutoriali online aby 
	dowiedzieć się więcej o akurat przerabianym temacie.
	
	
2) Klasyfikacja obrazków

	Celem tej części było poznanie i zaimplementowanie modelu klasyfikacji obrazków opartej na popularnej architekturze resNet. 
	Nauczyłem się jak tworzyć własne zestawy danych, korzystać z gotowych modeli, jak zwizualizować i wyczyścić dane przed uczeniem modelu, 
	a także pierwszy raz pracowałem z profesjonalnymi bibliotekami przydatnymi podczas uczenia maszynowego (np. matplotlib, numpy, fastAI).
	Nauczyłem się w pełni korzystać z możliwości notatników Jupyter (pisanie "ładnego" kodu, eksperymentowanie itp.) oraz kontynowałem naukę 
	z kursów i tutoriali online.
	
	Na projekt zdecydowałem się wybrać klasyfikację gatunków wilków. Nie jest to rzecz tak oczywista jak klasyfikacja koty-psy, ale zarazem na tyle
	prosta, by umożliwić mojemu modelowi rozpoznanie ich (gatunki różnią się pewnymi cechami, które model powinien wyłapać). Model uzyskał dokładność ok. 82%
	na moim zestawie danych.
	
	
3) Generacja muzyki

	Celem tej części było poznanie popularnych bibliotek uczenia maszynowego (np. Keras), stworzenie własnego modelu sieci neuronowej,
	poznanie Autoencoderów i próba stworzenia modlu generującego proste melodie.
	
	Do tego projektu utworzyłem kilka notatników, każdy z próbą podejścia tego problemu od innej strony. Mimo iż nie udało się osiągnąć oczekiwanego rezultatu
	(wygenerować melodię), to było dość blisko. Notaniki bazowały na zestawach daych NES Music Dataset 
	(muzyka z gier Nintendo - powtarzające się melodie) https://github.com/chrisdonahue/nesmdb oraz na Maestro Dataset 2.0.
	
	Muzyka z plików midi była konwertowana (w pierwszym notatniku próbowałem napisać własną, ale w następnych skorzystałem z gotowej funckji)
	do tablic 96 na 128 na X. Pierwszy wimar odpowiadał czasowi w takcie, drugi - wysokości nuty, trzeci - numerowi taktu (jako X - ilość taktów wybrałem 16). 
	Model następnie uczył się skompresować każdy takt do tablicy 200 cech, a po połączeniu wszystkich tablic cech skompresować je do tablicy 120 cech. 
	Jako że zdecydowałem się korzystać z autoencoderów model miał następnie za zadanie nauczyć się kompresować i odkodowywać przykłądowe melodie.
	Aby generować nowe wystarczyło usunąć część kodującą i użyć losowych liczb między 0 a 1 jako cech z których model powinien utworzyć nową melodię
	
	W notatnikach eksperymentowałem z różnymi podejściami do tego problemu. Próbowałem zmieniać architektury (mój prosty autoencoder, a moja implementacja
	códzej architektury), sposoby uczenia, zestawy danych (nesDB a Maestro) i uczyć model naprawdę długo. 
	Problemem było to, że model zawsze wpadał w lokalne minimum nie grania żadnych nut. Proawdopodbnie przyczyną było wybranie złej architektury 
	do tego zadania lub złej funkcji oceniania (funkcja wynagradzająca dobre nuty bardziej niż każąca złe mogłaby roziązać ten problem).
	
	Mimo iż ten projekt się nie udał nauczyłem się naprawdę wiele: korzystanie z bibloiteki Keras i projektowanie własnych modeli, korzystanie z zestawów danych
	bezpośrednio z notatnika, "podpinanie" kodu do różnych bibliotek i zestawów danych, a także poznałem podstawy autoencoderów i miałem okazję poeksperymentować 
	z wpływyem róznych czynników na uczenie się modelu.  
	
	
