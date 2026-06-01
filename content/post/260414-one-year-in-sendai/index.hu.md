---
title: "Első évfordulóm ideát: Egy főleg akadémiai helyzetjelentés"
description: "Kiköltözés Japánba (3/3)"
slug: draft-lololo
date: 2030-06-24T10:15:47+00:00
image: img/cover.jpg
math: true
hidden: true
comments: true
draft: true
categories:
    - life
    - academia
tags:
    - Japán
    - Szendai
---

<!-- markdownlint-disable MD026 -->
## Upsz, lement több, mint fél év...

Na igen, kicsit megint felgyülemlett a por ezen a csodablogon. Viszont már amúgy is nagyon ideje volt egy ~~tavaszi~~ nyári nagytakarításnak, úgyhogy kezdthetem akár itt is. Gondolom mindenki tűkön ülve várta, hogy miféle kalandokon voltam, hány hegyet másztam meg, hány sárkányt gyilkoltam le. Hát, előbbire azt kell mondjam, egyelőre nem sikerült túl messzi mennem. Utazgattunk ugyan barátokkal közeli helyeken, dombokon, hegyeken, de azokról majd a következő bejegyzésben számolók be, úgy a Betelgeuse csillag kialvásának ideje felé. Utóbbira a válasz viszont az, hogy **egyet**. De az egy igen gigászi bestia volt. *Kezdem is akkor vele.*

## Felvicus brutalis

E bestia nevének hallatán minden első éves külföldi egyetemi hallgatónak libabőr fut végig a hátán. Jöttének rémhíre minden március és augusztus közepéig terjed az Aoba-hegyi kampuszon. Asszonyok ifjoncaikat szekrényekbe zárják. A sorozott férfiúk a kardnál ékesebb ceruzát fenve két idegösszeroppanás között várják az elkerülhetetlent. Ez a Tóhoku Egyetem mechanikai mérnöki felvételi vizsgája.

Őszintén, nem is volt olyan vészes egyébként. Legalábbis önmagában. Tény, cefet sok a tananyag. És mint mérnökinformatikus, bő felét életemben nem is tanultam. De ez még áthidalható probléma. Ami igazán aláásott, az a stressz volt. Egyfelől, ez a vizsga úgy van kalibrálva, hogy esélyed ne legyen az egészet végigcsinálni az adott idő alatt. Nem nagyon tudom jellemezni, hogy miért anélkül, hogy túlzottan belemennék a meglehetősen kocka részletekbe.

<!-- markdownlint-disable MD033 -->
<details>
<summary><b>Kattints ide a meglehetősen kocka részletekért</b></summary>

Na, az én esetemben 3 tárgyból kellett vizsgázni, amik emelkedő nehézségi sorrendben Mechanikai rendszerek dinamikája, Irányítástechnika, Matek A (kb. diszkrét matematika, lineáris algebra) és Matek B (kb. analízis). Sorban akkor végig is megyek rajtuk.

<!-- markdownlint-disable MD001 -->
#### Mechanikai dinamika

Kb. olyasmi feladatok vannak itt, hogy kapsz egy lerajzolt mechanikai rendszert fix falakkal, vonal mentén mozgó elemekkel, súlyokkal, rugókkal, csillapítókkal, igákkal, ezeknek a torziós (tengely körül forgó) megfelelőivel, és ezeknek a mindenféle keverékével. Első ránézésre elég parának tűnt, főleg, hogy a fizikatudásomat egy szigorúan monoton exponenciálisan csökkenő időfüggvény írja le (avagy ahogy ezt megtanultam, kizárólag negatív valós sajátértékű rendszer). A nehézség igazából az, hogy hogyan állítod fel a kép alapján a matematikai egyenleteket. Amint az megvan, onnantól már relatív egyszerű levezetni minden mást. De nagyon könnyű hibázni egy-egy rossz irányba vett vektorral, mert ugye a képpel ellentétben a valóságban minden mozog, és fejben szinkronban kell tartani, mi épp merre indul, és az alapján felállítani az egyenleteket. Emiatt aztán az elején háromszor ugyanazt a feladatot megoldva három különböző választ kaptam.  Viszont miután megnéztem elég Youtube videót a témában, volt szerencsém felfedezni a trükkjét a dolognak. Ez pedig az, hogy nemes egyszerűséggel el kell engedni a középsuliban tanult newtoni megközelítést. Ezutóbbi alapján lényegében mindent irányított erőkre kell visszavezetni. *F=ma*, és társaik. Itt ugye mivel minden erő vektor, ezért egy rossz előjel komplettan el tudja az egész számítást barmolni. És amikor a rendszernek három mozgási egyenlete is van, hát akkor nagyon könnyű véletlen egynek becsúsznia. És utána azt kibogarászni abszolút nincs ideje az embernek.

Szerencsére van egy másik megközelítés, ami a rendszerben lévő energiából következteti a mozgási egyenleteket. Ez a lagrange-i mechanika, és nekem egészen konkrétan életmentő volt. A nagy trükk benne az, hogy minden elmozdulás, sebesség és gyorsulás négyzetre van emelve, ami kiiktatja az előjeleket. Ergo csak össze kell adogatni az egyes elemek saját energiakomponenseit, és onnantól egyértelmű a hátralévő folyamat. Az már más kérdés, hogy a hátralévő folyamat az valójában egy rakat parciális differenciálegyenletet takar, de legalább gondolkodás nélkül bedarálható, anélkül, hogy látatlanban egy rendszer mozgását fejben le kelljen követnem. Szóval minden nap minden órájában, Viva Lagrange!

![Hogyan vibrálnak a tömegek, ha kicsit meglököd a középső rudat?](img/DM1.png) ![Hogyan fogja a felfüggesztett tömeg befolyásolni a torziós rugót?](img/DM2.png)

#### Irányítástechnika

Ezt a tárgyat már kicsit macerásabb elmagyarázni. Lényegében mindenféle rendszer szabályozásának a módszertana, legyen az egy termosztát, tempomat, presszógép, vagy akár egy bevett gyógyszer felszívódása. A lényeg alapjáraton, hogy van egy "gépünk" ami tud egy értéket szabályozni (szoba hőfoka, autó sebessége, tömörített kávén áz víz nyomása, vérinzulin), tudjuk az aktuális értéket mérni, és van egy célértékünk. Amiről ez a tárgy beszél az az, hogy hogyan érjük el ezt a célértéket valósat minél inkább megközelítő körülmények között.

Ezzel szerencsére már volt valamennyi tapasztalatom, de jobbára csak számítógéppel számoltattam eddig ki a dolgokat, kézzel nem. Így kellett nem kicsit szenvednem megtanulni gráfokat rajzolni és értelmezni, Plusz van nem véletlen bízza ezeket a dolgokat az ember számítógépre, cefet számításigényes tud egy-egy feladat lenni. Ez főleg akkor jönn be a képbe, amikor egy összetettebb rendszerről van szó. Például, egy modern tempomat két értéket befolyásolva szabályoz: a folytószelep állásával és a fékhidraulikus nyomás változtatásával. Ezen felül vannak egyéb zavaró bemenetek amikre nincs befolyása a tempomatnak, de figyelembe kell vennie. Ilyenek példáut az út meredeksége, a légellenállás mértéke, a tapadás, satöbbi. Na, ilyen sok, időben változó, egymást befolyásoló függőségekből álló rendszereket mátrixokkal modellezünk. A mátrixokról meg annyit kell tudni, hogy a műveletek velük nagyságrendekkel válnak komplikáltabbá, ahogy nőnek. Egész konkrétan a számítógépek videokártyái épp az ilyenekkel való műveletekre vannak kitalálva. Szóval még ha nem is komplikált egy konkrét feladat, előfordulhat hogy kegyetlen sok időt felemészt itt.

![Ábrabűbáj](img/CE2.png) ![Mátrixmágia](img/CE3.png)

#### Matek A

Ez maga három részből áll. Első feladat jellemzően valamiféle elemi művelet. Egy függvény leintegrálása, limesz, szélsőértékek, végtelen sorok összegei, Taylor-polinóm generálás... Ezeket nehéz magyaráznom, igazából csak olyan alapvető dolgok, amik mindenféle gyakorlati alkalmazhatóságú dolog alapjaként szolgálnak. Nagyon változó az időigény itt. Utána van egy kis lineáris algebra. Ez kivétel nélkül mátrixműveletek, mint amik Irányítástechnikán előjönnek. Ez brutál időigényes tud lenni az előbb említett okokból, és ha valahol elírsz valamit, akkor nagyon pórul tudsz járni vele. Cserébe viszont relatíve maguk a folyamatok kevésbé igényelnek aktív gondolkodást. Végül pedig van egy vektoranalízis feladat. Na, ez a krémek krémje. Életemben nem tanultam ez előtt, és kifejezetten nem triviális. Az egésznek az alapja a vektormező, ami egy olyan függvény ami az értelmezési tartomány pontjaihoz vektorokat rendel. Azaz magyarul, olyasmi, mint időjárásjelentéseken a széltérkép: a térkép minden pontján láthatjuk, hogy milyen irányba és milyen erővel fúj a szél. Bumm, vektormező. Csak akkor ugyanezt 3D-ben. Így modellezünk például drónok irányítórendszerei a szelet (nekik fontos a fel-le irányú erő is), mágneses tereket, folyadékáramokat, satöbbi. Nagyon érdekes technika, de nulláról csak Youtube-videók alapján tanulva izzasztó.

![Ilyen például egy vektormező](img/vectorfield.png)

#### Matek B

Na, ez a végső ellenség. Ide kerülnek be a legszárazabb tananyagrészek a mérnöki matematikán belül. Ordináris differenciálegyenletek jellemzően az első feladat. Ezek esetén lényegében az egyetlen amit tenni tudsz, hogy ránézel, és vagy tudod élből, hogy kell megoldani ezt a fajtát, vagy ugrasz a következőre. Kifejezetten kegyetlen dög, és nagyon sok az eltérő megoldási megközelítés rájuk, amibe bele tud az ember futni, de az összefogó kapocs az, hogy ránézel az egyenletre, és tudod milyen alakja van a megoldásnak, onnantól pedig csak a konkrét számokat kell feltörnöd. A végére összeállítottam egy folyamatábrát, és ezen zongoráztam magamat végig fejben minden ilyen feladatnál:

![Nem olyan komplikált ha egyszer megérted](img/ODE_solution_tech.png)

</details>
<br>

Másfelől pedig, ha másodjára is megbuktam volna a felvételin, akkor nem tudtam volna ebbe a laborba belépni. Lévén hogy eleve csak ezt a labort pályáztam meg a kiküldetésem előtt, és hogy abszolúte ebben a témában akartam a kezdetektől fogva dolgozni, ez még a legjobb esetben se lett volna ideális. De van még tovább. Merthogy attól még, hogy ebbe a laborba nem tudtam volna becsatlakozni, az egy dolog, de vannak más laborok az egyetemen, és vannak más egyetemek is. De ahhoz, hogy válts, kell a laborigazgató aláírása. Viszont épp igazgatóváltás volt amikor csináltam a felvételit. Az előző igazgatóról tudni lehetett, hogy ha nem jön össze a felvételi, akkor nem enged váltani. Haza lesz az ember küldve, és ennyi volt. Az új igazgató ennél jelentősen méltányosabbnak tűnik az eddigi tapasztalataim alapján, de voltak beszélgetéseink amik adtak rá indokot, hogy azt feltételezzem, hogy rám is ez a sors várna.

Ez alapján talán érthető, miért voltam úgy rástresszelve a dologra. Nyilván az így kialakult alváshiány se sokat segített a dolgon. Pro tipp az egészségmegőrzéshez a jövőre nézve mindnyájótoknak: *Ne tegyétek a bevándorlási státuszotokat attól függővé, hogy képesek vagytok-e Laplace-párokat megjegyezni.*

## A jövőbeli tervek

## Amik hiányoznak

## Levelek

## Srácok a laborban

## Társaságok
