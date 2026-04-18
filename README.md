# Volvo V70 P2, S60, S80 – Mittariston korjaus

Volvon mittaristot ovat tunnetusti olleet aina hieman ongelmaherkkiä.  
Mekaanisista mittareista siirryttäessä digitaalisiin vaikutti hetken siltä, että viat olisi vähentyneet, mutta ajan myötä piirien ikääntyminen ja erityisesti tietyissä malleissa heikompi juotosten laatu ovat paljastuneet ongelmaksi.  

Kohdeautona vuoden 2007 Volvo V70.

---

## Mittariston vaihto

Mittariston voi vaihtaa toiseen käytettyyn, mutta näitä on vähintään kymmenillä eri varaosanumeroilla.  
Toimivuuden kannalta mittariston on oltava samaa tai lähes samaa mallia.  

Mittaristo ei myöskään toimi pelkkänä näyttölaitteena:  
se tallentaa omaan muistiinsa kilometrilukeman, jota se kasvattaa aina, kun ECU ilmoittaa auton liikkuneen tietyn matkan.  
Lisäksi mittaristolla on ilmeisesti jonkinlainen oma erillinen vikamuistinsa.

Jos mittaristo vaihdetaan toiseen autoon, se jatkaa edellisen auton kilometrilukemasta, eikä lukema synkronoidu auton ECU:n tietoihin.  

Todellinen kilometrilukema voidaan lukea ECU:lta OBD-portin kautta,
tämä ei kuitenkaan ole ihan niin helppo juttu kun sen toivoisi olevan, kilometrilukemaa ei saa ulos tietyllä PID koodilla vaan sen hakemiseen tarvitaan joitain volvon omia protokollia joita ei ole erityisen avoimesti dokumentoitu.
Käytännössä tuon kilometrilukeman saa helpoten vidalla.

---

## Vianetsintä ja testaus

### LCD-näytön häiriöt
Kuvassa näkyvissä LCD-näytöissä esiintyy ajoittain samanaikaista kosketushäiriötä.  
Usein ongelma korjaantuu pienellä kopautuksella.  
![IMG_20250718_192034122](https://github.com/user-attachments/assets/0d64fd36-d602-42cb-b2c3-834a04f00848)

---

### 12 V testaus
Mittaristoa voi testata syöttämällä sille 12 V jännitteen.  
Tällöin kaikkien näytön LED-elementtien tulisi syttyä, mikä mahdollistaa kosketushäiriön paikallistamisen.  
![photo_2025-07-19_18-52-35](https://github.com/user-attachments/assets/00002364-1086-4129-8acd-c095329bcb3b)
![IMG_20250719_184922588](https://github.com/user-attachments/assets/7bcb0cce-c98f-42d1-abfd-4ac8994f9a16)


### Käytetyt menetelmät
Vian paikallistamisessa hyödynnettiin seuraavia keinoja:
- juotosten silmämääräinen tarkastus  
- fyysinen tökkiminen  
- kylmäspray  
- lämmitys  


Kosketushäiriön aiheuttaja löytyi merkitystä kohdasta, ja korjattiin se uudelleenjuottamalla.  
![IMG_20250711_155539033](https://github.com/user-attachments/assets/396a9073-632c-4fce-9305-e8c780fe92c2)

---

## kiteen rikkoutuminen

Korjaustyön yhteydessä yhden mikrokontrollerin käyttämä kidebrikkoutui kuumuudesta.
![0H0A5566](https://github.com/user-attachments/assets/1c13d2ce-0ae1-41cc-8d19-9caf1e4867a6)


Datalehden mukaan **MC9S12DG128B**-mikrokontrolleri vaatii toimiakseen 0,5–16 MHz taajuuden kiteen.  
Tässä oleva kide on hiukan erikoisempi keraaminen kolmijalkainen kide jonka idea lienee se että erillistä kondensaattoria ei tarvita. 

📄 [Datalehti (MC9S12DG128B)](https://www.alldatasheet.com/datasheet-pdf/pdf/135942/MOTOROLA/MC9S12DG128B.html)

Tilattu uusi kide eBaysta ja juotettu piirilevylle.  
![IMG_20250812_174736796_HDR](https://github.com/user-attachments/assets/43904564-e3b5-4804-ad1d-031a99e932c3)


---
