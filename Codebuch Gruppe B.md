# Datensatz Gruppe B #
- Codebuch Stand 2021-12
- aktualisiert 2021-12
- erstellt von Karolina Justus (kj026), Philipp Kaltenmark (pk092), Leonie Kühn (lk182), Sarah Liebers (sl139) und Sara Rozic (sr181)

## Inhalt
- Edges.csv (Edgelist)
- Nodes.csv (Nodelist)
- Codebuch.md (Codierung der Datensätze)

## Ursprung und Datenerhebung
Wir haben den Datensatz im Kurs Netzwerkanalyse erhoben. Wir betrachten die Top 10 der globalen Album-Charts ab 2011 (Quelle für Charts ab 2016: "Global Music Reports" der IFPI, https://www.musikindustrie.de/publikationen/global-music-report; Quelle für Charts älter als 2016: "Digital Music Reports" der IFPI, https://www.musikindustrie.de/publikationen/digital-music-report oder "Recording Industry in Numbers" der IFPI, https://www.musikindustrie.de/publikationen/recording-industry-in-numbers-rin). 
Aus jedem Album listen wir alle SongwriterInnen auf (Quelle: https://genius.com/; zum Abgleich ASCAP-Datenbank https://www.ascap.com/repertory#/) und berechnen unter anderem ihren prozentualen "Songwriting-Anteil" am Gesamtwerk.

Das Netzwerk ist ein *ungerichtetes two-mode Akteursnetzwerk*. 

# NODE-Attribute  
  
**id**  

Die ersten vier Zeichen (keine Leerzeichen; keine Anführungszeichen; keine Bindestriche; Punkte werden übernommen, jedoch nicht gezählt, z.B. J.T. Cure -> J.T.Cu) des Namens aus "name" zur Identifikation der Knoten. Groß- und Kleinschreibung werden entsprechend übernommen.

**name**

Namen der KünstlerInnen bzw. SongwriterInnen bzw. der Alben mit Nennung des Artists
  
**type**    

Um welche Art von Knoten handelt es sich?  
- 1 = SongwriterIn
- 2 = Album

**sex**    

Geschlecht der KünstlerInnen und SongwriterInnen  
- 1 = weiblich  
- 2 = männlich 
- 3 = divers

**origin**

Herkunft der KünstlerInnen und SongwriterInnen
-	1 = Vereinigtes Königreich
-	2 = USA
-	3 = Deutschland
-	4 = Spanien
-	5 = Frankreich
-	6 = Italien
-	7 = Kanada
-	8 = Australien
- 9 = Schweden
- 10 = Sonstiges
  
**genre**    

Genre des Albums
- 1 = Pop
- 2 = HipHop 
- 3 = Schlager  
- 4 = Rock
- 5 = Alternative
- 6 = Electro
- 7 = RnB
- 8 = Country
- 9 = Metal
- 10 = Jazz
- 11 = K-Pop
- 12 = Soundtrack
- 13 = Christmas
- 14 = Sonstiges

**language**  

Sprache des Albums
- 1 = englisch   
- 2 = deutsch 
- 3 = spanisch  
- 4 = französisch
- 5 = italienisch
- 6 = sonstiges

**year**

Zahl entspricht Jahr

- 2011
- 2012
- 2013
- 2014
- 2015
- 2016
- 2017
- 2018
- 2019
- 2020

**second year**

Zahl entspricht einem weiteren Jahr, in dem das Album in den Charts war

**tracks**

Zahl entspricht der Gesamtanzahl der Tracks



# EDGE-Attribute

**id**  

Eindeutige Codierung des Knotens

**weight**

Prozentualer "Songwriting-Anteil" am Gesamtwerk  
- 1 = sehr niedriger Anteil (weniger als 20%)
- 3 = niedriger Anteil (20% bis 60%)
- 5 = hoher Anteil (mehr als 60%)
- 7 = sehr hoher Anteil (100%)

**participation** 

Anzahl der Songs eines Albums, an denen mitgearbeitet wurde in Kategorien
- 1 = sehr niedriger Anteil (1-2)
- 3 = niedriger Anteil (3-5)
- 5 = hoher Anteil (6-9)
- 7 = sehr hoher Anteil (>9)

**relation**

Beziehungsart zwischen den Nodes  
- 1 = externe(r) SongwriterIn
- 2 = KünstlerIn des Albums und SongwriterIn
- 3 = Feature und SongwriterIn

**count**

Zahl entspricht der Anzahl der Songs eines Albums, an denen mitgearbeitet wurde


