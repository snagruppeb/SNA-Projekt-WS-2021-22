# Datensatz Gruppe B #
Codebuch Stand 2021-12, aktualisiert 2021-12
erstellt von Karolina Justus (kj026), Philipp Kaltenmark (pk092), Leonie Kühn (lk182), Sarah Liebers (sl139) und Sara Rozic (sr181)

## Inhalt
- Edges.csv (Edgelist)
- Nodes.csv (Nodelist)
- Codebuch.md (Codierung der Datensätze)

## Ursprung und Datenerhebung
Wir haben den Datensatz im Kurs Netzwerkanalyse erhoben. Wir betrachten die wöchentlichen Top 3 Alben des Jahres 2021 der deutschen Alben-Charts (Quelle: https://www.offiziellecharts.de/charts/album). Aus jedem Album listen wir alle SongwriterInnen auf (Quelle: genius.com) und berechnen ihren prozentualen "Songwriting-Anteil" am Gesamtwerk.

Das Netzwerk ist ein *ungerichtetes two-mode Akteursnetzwerk*. 

# NODE-Attribute  
  
**id**  
Identische ID wie aus der edgelist zur Identifikation der Knoten. 

**name**
Namen der KünstlerInnen bzw. SongwriterInnen und der Alben mit Nennung des Artists
  
**type***    
Um welche Art von Knoten handelt es sich?  
1 = SongwriterIn,  
2 = KünstlerIn, 
3 = Album. 

**sex**    
Bitte geben Sie ihr Geschlecht an:  
1 = weiblich,  
2 = männlich, 
3 = divers.

**origin**
Herkunft der KünstlerInnen bzw. SongwriterInnen
1 = britisch,
2 = US-amerikanisch,
3 = deutsch,
4 = spanisch,
5 = französisch,
6 = italienisch,
7 = kanadisch,
8 = australisch,
9 = schwedisch
10 = sonstiges.
  
**genre**    
Welches Genre?    
1 = Pop,   
2 = HipHop,   
3 = Schlager,   
4 = Rock,
5 = Alternative,
6 = Electro,
7 = RnB,
8 = Country,
9 = Metal,
10 = Jazz.

**language**  
Sprache des Albums?  
1 = englisch,      
2 = deutsch,   
3 = spanisch,    
4 = französisch,
5 = italienisch,
6 = sonstiges.  

**time**
Wie lange ist das Album in den Top 3 Charts (in Wochen)?
1 = 1-2 Wochen,
2 = 3-4 Wochen,
3 = 5 und mehr Wochen.



# EDGE-Attribute

**id**  
(eindeutige Codierung des Knoten)   

**weight**  
prozentualer "Songwriting-Anteil" am Gesamtwerk  
1 = niedriger Anteil (weniger als 20%),
3 = hoher Anteil (20% bis 60%),
5 = sehr hoher Anteil (mehr als 60%).

**relation**
Beziehungsart zwischen den Nodes  
1 = externe(r) SongwriterIn, 
2 = KünstlerIn selbst hat am Album mitgewirkt.
