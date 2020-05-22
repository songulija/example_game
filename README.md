# example_game

Pradėkime nuo 
BirdScript kuris yra skirtas paukščiui tam kad jis galėtų judėti. Scriptas yra parašytas taip kad kai atsitrenki i viena iš sienų paukštis keičia kryptį ir pradeda bėgti į kitą pusę. Pasinaudojame rigidbody.velocity kuris mums padeda judinti paukštį į vieną ar į kitą pusę. Paukštis bėgioja iš vienos pusės į kitą pats. Jeigu paspausime kairyjį pelės mygtuką paukštis pašoks. Taip pat naudojame rigidbody.velocity kad tai padaryti. Paukštis gali pašokti du kartus. OnCollisionEnter2D mums padeda nustatyti kada paukštis stovi ar nusileidžia ant Ground(ant žemės). Kai paukštis stovi ant žemės mes galime pašokti du kartus. PAšokes laukia kol nusileidžiame tik tada galėsime vėl pašokti vieną ar du kartus.

Spawner Script
Yra skirtas tam kad atsirastu vis naujos platformos. Veikia labai paprastu principu. Turime float ground_Y_Distance = 3.3f, tai yra atsumas. Pagal jį mes skaičiuojame kur turi atsirasti kita platforma. Tiesiog kiekviena karta pridedami prie float current_Y_Position šitą atstumą. Kai pradedame žaidimą naudojant for loop mes padarome jog atsirastu mums reikalingas kiekis platformu. Kada Camera pasikelia į tam tikrą aukštį nuo platformos ta platforma dingsta ir atsiranda kita viršuje ir taip su visomis. Spawner script mes taip pat naudojame kad atsirastu šunys ir kiti objektai kurie trukdytu ir darytu žaidimą truputi įdomesnį. Kiekviena karta kai atsiranda platforma atsiranda ir šuo ar kitas gyvunas. Naudojame Random.range. 90 procentu yra kad atsiras nejudantis gyvunas. Ir 10 procentu yra kad kaireje arba dešinėje atsiras gyvūnas kuris judės kažkokia kryptimi. Jeigu tai yra judantis šuo mes naudojame rigidbody.velocity kad jis judėtu į kažkokią pusę.

Camera script yra skirtas kad kamera judėtu kartu su paukščiu. 
transform.position = new Vector3 (transform.position.x,
				player.transform.position.y, transform.position.z);
Kameros pozicija yra. Vector 3 mums duoda X,Y,Z ašis. Mūsu atveju mums reikia kad kamera judėtu tik pagal Y ašį. Mums nereikia kad kamera judėtų į šonus tik į viršų. Dėl to į Y pozicija įrašome player Y pozicija. Tai reiškia kad kameros pozicija visada sutaps su player(paukščio) pozicija. Camera judės žiūrint į paukščio pozicija.

Gameplay Controler
Padeda mums Controliuoti žaidimą. Yra tokios funkcijos kaip pradėti žaidimą, pralaimėtas žaidimas. Kada mes paspaudžiame ant mainMenu ekrano tada prasideda mūsų žaidimas. Jeigu mes paliečiame vieną iš šūnų tada iš Gameplay Controler kviečiame funkcija GameOver kuri baigia žaidimą ir atsiranda GameOver ekranas, paleidžiame paukščio dead animaciją. Kai atsiranda GameOver ekranas yra mygtukas Restart. Ant jo yra uždėta Gameplay Controler funkcija Restart kuri paleidžia žaidimą iš naujo.


GameData mes naudojame kad gauti ir nustatyti duomenis naudojant get ir set. Kad gauti bestscore, diamondScore, selectedIndex ir t.t. Tai veliau panaudojame GameManager. Išsaugoti ir užkrauti data.











