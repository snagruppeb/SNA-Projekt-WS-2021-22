# Datensatz Gruppe B #
- Codebuch Stand 2021-12
- aktualisiert 2021-12
- erstellt von Karolina Justus (kj026), Philipp Kaltenmark (pk092), Leonie Kühn (lk182), Sarah Liebers (sl139) und Sara Rozic (sr181)

## Inhalt
- Edges.csv (Edgelist)
- Nodes.csv (Nodelist)
- Codebuch.md (Codierung der Datensätze)

## Ursprung und Datenerhebung
Wir haben den Datensatz im Kurs Netzwerkanalyse erhoben. Wir betrachten die Top 10 der internationalen Album-Charts ab 2011 (Quelle für Charts ab 2016: Global Music Reports der IFPI, https://www.musikindustrie.de/publikationen/global-music-report; Quelle für Charts älter als 2016: Digital Music Reports der IFPI, https://www.musikindustrie.de/publikationen/digital-music-report). 
Aus jedem Album listen wir alle SongwriterInnen auf (Quelle: https://genius.com/; zum Abgleich GEMA-Datenbank https://online.gema.de/werke/search.faces) und berechnen unter anderem ihren prozentualen "Songwriting-Anteil" am Gesamtwerk.

Das Netzwerk ist ein *ungerichtetes two-mode Akteursnetzwerk*. 

# NODE-Attribute  
  
**id**  

Die ersten vier Zeichen (keine Leerzeichen; keine Anführungszeichen; Punkte werden übernommen, jedoch nicht gezählt, z.B. J.T. Cure -> J.T.Cu) des Namens aus "name" zur Identifikation der Knoten. Groß- und Kleinschreibung werden entsprechend übernommen.

**name**

Namen der KünstlerInnen bzw. SongwriterInnen und der Alben mit Nennung des Artists
  
**type**    

Um welche Art von Knoten handelt es sich?  
- 1 = SongwriterIn
- 2 = KünstlerIn und SongwriterIn
- 3 = Album
- 4 = Feature und SongwriterIn

**sex**    

Geschlecht der KünstlerInnen und SongwriterInnen  
- 1 = weiblich  
- 2 = männlich 
- 3 = divers

**origin**

Herkunft der KünstlerInnen und SongwriterInnen
-	1 = britisch
-	2 = US-amerikanisch
-	3 = deutsch
-	4 = spanisch
-	5 = französisch
-	6 = italienisch
-	7 = kanadisch
-	8 = australisch
- 9 = schwedisch
-	10 = sonstiges
  
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

**language**  

Sprache des Albums
- 1 = englisch   
- 2 = deutsch 
- 3 = spanisch  
- 4 = französisch
- 5 = italienisch
- 6 = sonstiges

**time**

Wie lange ist das Album in den Top 3 Global Charts (in Wochen)?
- 1 = ein bis zwei Wochen
- 2 = drei bis vier Wochen
- 3 = fünf und mehr Wochen

**year**

(Zahl entspricht Jahr)

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



# EDGE-Attribute

**id**  

Eindeutige Codierung des Knotens

**participation** 

Anzahl der Songs eines Albums, an denen mitgearbeitet wurde
- 1 = sehr niedriger Anteil (1-2)
- 3 = niedriger Anteil (3-5)
- 5 = hoher Anteil (6-9)
- 7 = sehr hoher Anteil (>9)

**weight**

Prozentualer "Songwriting-Anteil" am Gesamtwerk  
- 1 = niedriger Anteil (weniger als 20%)
- 3 = hoher Anteil (20% bis 60%)
- 5 = sehr hoher Anteil (mehr als 60%)

**relation**

Beziehungsart zwischen den Nodes  
- 1 = externe(r) SongwriterIn
- 2 = KünstlerIn selbst hat am Album mitgewirkt
