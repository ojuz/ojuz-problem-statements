You are to write an
interactive program that, given a sequence of Wikipedia excerpts 
(see example below), guesses the language of each, in turn.  
After each guess, your program is given the correct answer, 
so that it may learn to make better guesses the longer it plays.
<p>
Each language is represented by a number L between 0 and 55.
Each excerpt has exactly 100 symbols,
represented as an array E of 100 integers between 1 and 65 535.
These integers between 1 and 65 535 have been assigned
arbitrarily, and do not correspond to any standard encoding.
</p><p>
You are to implement the procedure <b>excerpt(E)</b> where <b>E</b> is an
array of 100 numbers representing a Wikipedia excerpt as described above.
Your implementation must call <b>language(L)</b> once,
where <b>L</b> is its guess of the language of the
Wikipedia edition from which E was extracted.
The grading server implements <b>language(L)</b>, which
scores your guess and returns the correct language.
That is, the guess was correct
if <b>language(L)</b> = <b>L</b>.
</p><p>
The grading server calls <b>excerpt(E)</b> 10 000 times,
once for each excerpt in its input file.
Your implementation's <i>accuracy</i> is the fraction of excerpts
for which <b>excerpt(E)</b> guessed the correct language.
</p><p>
You may use any method you wish to solve this problem.
<i>Rocchio's method</i> is an approach
that will yield accuracy of approximately 0.4.  Rocchio's method computes the
similarity of E to each language L seen so far, and
chooses the language that is most similar.  Similarity
is defined as the total number of distinct symbols in E that appear
anywhere amongst the previous excerpts from language L.
</p><p>
Note that the input data have been downloaded from real Wikipedia
articles, and that there may be a few malformed characters or fragments
of text.  This is to be expected, and forms part of the task.

</p><h3>Example</h3>
For illustration only,
we show the textual representation of excerpts
from 56 language-specific editions of Wikipedia.

<p>

<table border="1">
<tr>
	<td style="text-align: left;">
<small>
<ol start="0" style="float:left;">
<li>Yshokkie word meestal in Kanada , die noorde van die VSA en in Europa gespeel. Dit is bekend as 'n b
<li>المنتج الحدي Marginal Producer ، وهو المنتج الذي يجعل المنظم لا يكسب ربحا ولا يخسر ويحصل على دخل يكف
<li>"BAKILI" Futbol Klubu 1995-ci ildə Misir Səttаr oğlu Əbilov tərəfindən yаrаdılmış və həvəskаr futbol
<li>Квинт Фулвий Флак (Quintus Fulvius Flaccus; † 205 пр.н.е. ) e политик и генерал на Римската републик
<li>ইন্ডিয়ান ইনস্টিটিউট অফ সোশ্যাল ওয়েলফেয়ার অ্যান্ড বিজনেস ম্যানেজমেন্ট (সংক্ষেপে আইআইএসডব্লিউবিএম )
<li>5. juni ( lipanj ) ( 5.6. ) je 156. dan godine po gregorijanskom kalendaru (157. u prestupnoj godini
<li>La Caunette és un municipi francès , situat al departament de l' Erau i a la regió de Llenguadoc-Ros
<li>Praha je malé městečko v Texasu , které leží cca 85&#160;km na jihozápad od Austinu . Bylo založeno 
<li>Graeme Allen Brown (født 9. april 1979 i Darwin , Northern Territory , Australien ) er en australsk 
<li>Der Plattiger Habach ( 3.214&#160; m&#160;ü.&#160;A. , nach anderen Angaben nur 3.207&#160; m [1] ) 
<li>Το Νησί Γκρέιτ Μπάρριερ ( Αγγλικά : Great Barrier Island , Μαορί : Motu Aotea ) είναι νησί στα βόρει
<li>Sid Bernstein Presents... is a 2010 feature-length documentary film by directors Jason Ressler and E
<li>El término latino lex loci celebrationis aplicado al derecho internacional privado quiere decir: "le
<li>Apollo 5 oli kosmoselaev , mis sooritas Apollo programmi teise mehitamata lennu. Lennu käigus testit
<li>سیارک ۱۳۵۰ (به انگلیسی : 1350 Rosselia ، نامگذاری :1934TA )‏ هزار و سیصد و پنجاهمین سیارک کشف شده‌اس
<li>V. I. Beretti (myös Vikenty Ivanovitš Beretti , alk. Vincent Beretti ; 1781 Milano Italia – 18. elok
<li>Le 5 e bataillon de parachutistes vietnamiens (ou 5 e BPVN ou encore 5 e Bawouan ) est une unité par
<li>Amina Sarauniyar Zazzau,, wadda ta rayu daga shekarar 1533 zuwa 1610, ɗaya ce daga cikin ‘ya'ya biyu
<li>ב מתמטיקה , השערת רימן היא השערה שהציע בשנת 1859 ה מתמטיקאי ברנרד רימן , מגדולי המתמטיקאים של אותה ע
<li>Sudski proces Doe protiv Boltona je sudski proces iz 1973 . godine kojim je američki Vrhovni sud uki
<li>Owen Cunningham Wilson ( 1968 . november 18. , Dallas , Texas , Egyesült Államok ) amerikai színész 
<li>Հայ Կաթողիկե Եկեղեցին պատկանում է Արևելյան Կաթոլիկ Եկեղեցիներին և այսպիսով ենթարկվում է Հռոմի Պապի ա
<li>Dionysios dari Halicarnassus ( Bahasa Yunani : Διονύσιος Ἀλεξάνδρου Ἀλικαρνᾱσσεύς , Dionysios putra 
<li>Nnamdi "Zik" Azikiwe , bu onye isi-ala izizi Nijiria nwere. Ochichi ya bidolu na afo 1954 welu ruo n
<li>La Riserva naturale orientata Serre della Pizzuta è un'area protetta del dipartimento Regionale di S
<li>石橋和義 （いしばし かずよし/まさよし、生没年不詳）は、 �詳。 石橋氏 初代当主。初名氏義。 尾張 三郎を通称とし、官途は、 左近将監 → 三河守 → 左衛門佐 。 足利直義
<li>კორბინ ბლიუ ( ინგლ. Corbin Bleu ; დ. 21 თებერვალი , 1989 , დაბადების ადგილი ბრუკლინი , ნიუ-იორკი , ა
<li>Та́рья Ка́арина Ха́лонен (Tarja Kaarina Halonen)); 24 желтоқсан , 1943 , Каллио , Хельсинки , Финлан
<li>딜롱 ( Dilong )은 중국 랴오닝(Liaoning) 지방의 익시안층(Yixian Formation)에서 온전한 4구의 화석으로 발견되었다. 이 공룡은 가장 원시적인 초기의 티
<li>Сүймөнкул Чокморов - советтик актёр. Жетинин айынын 9 (ноябрь) 1939-жылы, Фрунзе шаарын жанындагы Чо
<li>D' Mirjam vun Abellin war eng Nonn a Mystikerin , och " Maria vum gekräizegte Jesus " genannt. Si as
<li>Panopea abrupta ( angl. Geoduck ) - jūrinių dvigeldžių moliuskų rūšis, priklausanti Hiatellidae šeim
<li>"Dzimis Latvijā" ir Liepājas dueta Fomins &amp; Kleins 2004 . gada 23. februārī izdotais otrais albu
<li>I Ludwik Lejzer Zamenhof dia dokotera mpijery maso nipetraka any Polonia . Fantantsika izy ankehitri
<li>Седумстотини милиони малечки алвеоли во белите дробови , всушност се шупливи чаури - алвеоли прекрие
<li>Энэхүү шувуу нь Бутан , Хятад , Гонконг , Энэтхэг , Пакистан , Иран , Япон , Казакстан , Солонгос , 
<li>भारतातील महाराष्ट्र राज्याच्या नागपूर पासुन २१६ कि.मी. दूर असलेले एक गाव. ते वैनगंगा नदीच्या काठावर 
<li>De Slotervaart was oorspronkelijk de waterweg die sinds de Middeleeuwen het dorp Sloten verbond met 
<li>Macierz S (macierz rozpraszania, od ang. scattering matrix ) jest centralnym elementem w mechanice k
<li>A Hora do Rush 3 ( Rush Hour 3 , no original) é o terceiro filme da franquia Rush Hour . Dirigido po
<li>Coordonate : 51°34′0″N 12°3′0″E ﻿ / ﻿ 51.56667 , 12.05 Brachstedt este o comună din landul Saxonia-A
<li>Гробницы императоров династии Мин и Цин — памятник Всемирного наследия ЮНЕСКО , состоящий из несколь
<li>Kovalentni radijus atoma - ponekad se naziva i valentni radijus. Kovalentni radijus je srednje rasto
<li>Koniecpol je mesto v Poľsku v Sliezskom vojvodstve v okrese Powiat częstochowski v rovnomennej gmine
<li>Hoxhë Vokrri vije nga Shqipëria ishte një klerik shqiptar i cili luftonte për Çështjën Kombëtare . A
<li>Гурдијеље је насеље у општини Тутин у Рашком округу . Према попису из 2002. било је 93 становника (п
<li>Underhållsstöd betalas ut av Försäkringskassan (FK) till en förälder som är vårdnadshavare och bor e
<li>இந்தியாவின் தேசிய நெடுஞ்சாலைகள் நடுவண் அரசின் தேசிய நெடுஞ்சாலைத் துறையால் பராமரிக்கப்படுகின்றன. பெரு
<li>Дар он зиндаги .маишат ,фаолияти мехнати,муборизаи ичтимои, русуму омол, хислат ва эхсосоти халк ифо
<li>ไฟทอฟธอรา อินเฟสทันส ( อังกฤษ : Phytophthora infestans ) คือเชื้อ ราโอโอไมซีท หรือ ราน้ำ ที่เป็นสาเห
<li>ABUL FAWARIS BERRANY - 11. asyrda Orta Aziýadaky oguz taýpalarynyň berrany dinastiýasynyň wekili. Ol
<li>Egemenlik ya da hâkimiyet , bir toprak parçası ya da mekan üzerindeki kural koyma gücü ve hukuk yara
<li>Темне фентезі (від англ. Dark Fantasy - темне, похмуре фентезі ) - піджанр літератури, який включає 
<li>Paris By Night 84: In Atlanta - Passport to Music &amp; Fashion (Âm nhạc và Thời trang) là chương tr
<li>ISO 3166-2:GU ni akoole ninu ISO 3166-2 , apa opagun ISO 3166 ti International Organization for Stan
<li>下卡姆斯克 （ 俄文 ： Нижнека́мск ； 韃靼語 ： Түбән Кама/Tübän Kama ）是 俄羅斯 韃靼斯坦共和國 東北部的一個城市，位於 卡馬河 南岸。 2002年 人口22
</ol>
</small>
</td>
</tr>
</table>
<p>
The sample input file <tt>grader.in.1</tt> contains 
10 000 such examples.  The 56 languages are those listed as
"mother tongue" in the IOI 2010 registration data.
The language for each excerpt is chosen at random from these 56 languages,
and each excerpt is taken from the first paragraph of an article
chosen at random from the corresponding Wikipedia edition.  Each line of
the file contains:
</p><ul>
<li>The two-letter ISO code for the Wikipedia language edition;
</li><li>100 numbers between 1 and 65 535, representing the first 100 symbols,
  in sequence, of the first paragraph of the article;
</li><li>a viewable representation (in UTF-8) of the 100 symbols that you can read
in your text editor or Firefox web browser.  This viewable
representation is for your convenience only, and is not intended to be used
as input for your program.
</li></ul>
<p>
The official grader uses 10 000 different excerpts,
selected in the same way
from the same 56 Wikipedia editions.  However, the grader assigns a different
number between 0 and 55 to each language, and a different number between
1 and 65 535 to each symbol.

</p><h3>Subtask 1 [30 points]</h3>
Your submission must achieve accuracy of 0.3 or better on the grading server.
<h3>Subtask 2 [up to 80 points]</h3>
Your score will be 114(α-0.3), rounded to the nearest integer,
where α is the accuracy of your submission.

<h3>Implementation Details</h3>
<ul>
</li><li>To be implemented by contestant: <tt>lang.c</tt> or <tt>lang.cpp</tt> or <tt>lang.pas</tt>
</li><li>Contestant interface: <tt>lang.h</tt> or <tt>lang.pas</tt>
</li><li>Grader interface: <tt>grader.h</tt> or <tt>graderlib.pas</tt>
</li><li>Sample grader: <tt>grader.c</tt> or <tt>grader.cpp</tt> or <tt>grader.pas</tt> <i>and</i> <tt>graderlib.pas</tt>
</li><li>Sample grader input:  <tt>grader.in.1</tt>. <br><i>Note: Each 
line of input contains: a two-character language code; an excerpt 
represented as 100 numbers  separated by spaces; the text representation
 of the excerpt.</i>
</li><li>Expected output for sample grader input: <i>If the implementation calls language as specified for each of the 10 000 examples, the sample grader will output <tt>OK  <i>alpha</i></tt> where <i>alpha</i> is the accuracy.</i>
</li></ul>
 
