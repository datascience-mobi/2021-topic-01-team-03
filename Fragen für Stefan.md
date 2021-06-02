# 2021-topic-01-team-03

**31.05.21** 
- Glioma: Effektivität und Unterschied zu den anderen Subtypen
- **schauen ob wir kandidatengene gegeneinander plotten. Untershied von genexpression bestimmen. mit 0 hypothese und einem test (alle cell lines sind homogen). CLUSTERING MACHEN von genetische information; PCA von expression und copy anzahl: respondet auf besonderere wenig drugs (z.B)** 
- Abspaltung der Glioma von den anderen subtypes 
- **Vieleicht unsere Glioma ist mehr drugresistent. Hierarchisches clustering oder kmeans zu machen**
- Wir wollen schauen ob von unseren effectiven drogen irgendwelche ubterschied in Wirksamkeit nach cancer subtyp gibt. Müssen wir es in allen dosen vergleichen oder nur in eine? Macht es ein wesentlicheres unterschied welche dose wir für diese Verglech nehmen. 
- **mittlere dosis nehmen. Varianz von dosen ausrechnen. Große Varianz aussuchen, da es mehr info dargestellt ist. Validieren welche dose wir nehmen. Mit einer dose einfach weiter arbeiten**
- Threshold für die effectivity 
- **Median genommen: klingt gut, Stefan approved**
- Definition der over und underexpression 
- TPM
- Wie können wir weiter arbeiten? Was könnten unsere weitere Schritte mit Genexpression sein?
-**Summary statistiks from prism.treat von unseren targets von drugs. Kein muster: expressionsdaten PCA auf daten punkten, scatterplott. oder Kmeans clustering von allen cell lines nach expression/cnv clustern. Oder heatmap hierarchisches clustering. Vieleicht überlegen neue subtypen definieren** 

**26.05.21**
- Wie erstellt man einen Vektor mit Einträgen aus einem for loop?
- Wie speichert man eine neue Variable von einem loop oder apply?


- Threshold 0 oder 0,3?
+ **Make clusters, look in more detail if there is more subgroups to identify**
+ **Gucken ob median von datansatz 0 ist**
+ **Gut begründen warum wir ein threshold aussuchen**
+ **Clusters in brain cancer cells**
+ **Schauen ob da irgendwelche trends in genexpression von cell lines gibt**

- What do we do with the repeated drug?

- What is moa in prism.treat?
+ **Pick one?**
+ **Dosenzahl weniger zu machen?**

+ **Nicht der wichtigste dataframe**
+ **Was sind die wirkung von drugs auf die gene** 

**19.05.21**
- Cedrik pull and push
+ **späteres Meeting zusammen**

- Threshold definiert
+ **Xenia schreibt Stefan nochmal deswegen eine Mail aber evtl. kein threshold definieren**

- Strukturieren: ob es sinnvoll ist verschiedene Markdowns erstellen
+ **Mehr Infos in RMarkdown zwischen chunks?**
+ **Tab "Issues" auf GitHub; zur Kommunikation untereinander; Stefan kann markiert werden um ein Kommentar dazu abzugeben**
+ **Mehr Ordnerstrukturen erstellen; z.B. erstes Data Cleanup; weitere Analysen darauf aufbauend**
+ **Variablennamen Strukturieren -> z.B. bei dd1 und dafür einen Dataframe erstellen damit es nicht flach im Code vorkommt**
+ **Struktur zur Benennung von Variablen**

- Wie sieht das Enddokument aus?
+ **in dem pdf muss kein Code enthalten sein**
+ **Ergebnisse sollen wissenschaftliche Erkenntnisse repräsentieren**
+ **Plots oder Tests können enthalten sein(?)**
+ **wenn Code aussagekräftiger ist als Text dann könnte evtl auch Code eingebaut werden**

