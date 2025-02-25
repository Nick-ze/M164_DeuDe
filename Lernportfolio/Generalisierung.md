# **Generalisierung**  

**Generalisierung** dient dazu, **Datenverlust vorzubeugen**.  
Es werden **Fremdschlüssel** verwendet, um **spezifische Tabellen** unspezifischen zuzuweisen.  

Diese Beziehungen werden auch als **"is-a"**-Beziehungen bezeichnet, da z. B.:  

- ein **Mensch** auch ein **Fahrer** sein kann.  
- ein **Fahrzeug** ein **Auto** oder ein **Motorrad** sein kann.  

Diese Struktur hilft, **Daten effizient zu organisieren** und **Redundanzen zu vermeiden**.  

# Chat **Ansätze zur praktischen Umsetzung herauszufinden**: 
## Datenbankmodellierung mit dem Attributkonzept

Die Datenbankmodellierung, die wir hier betrachten, beruht auf dem **Attributkonzept**. Wir definieren Attribute mit Attributsausprägungen und ordnen diese den **Entitätstypen** zu.  

### Problemstellung

Problematisch wird es, wenn mehrere Entitätstypen viele Attribute gemeinsam haben und einige nicht. Jetzt könnte **Redundanz** entstehen, wenn ein konkretes Objekt aus der realen Welt durch mehrere Entitätstypen beschrieben wird.  

**Beispiel:**  
- Mitarbeiter, die auch als Kunden auftreten.  
- Fahrer, die auch als Disponenten arbeiten.  

Nach [ZEHNDER, Carl August (1989): Informationssysteme und Datenbanken] dürfen **lokale Attribute** nur einmal in einer Datenbank auftreten, da sonst Redundanz vorliegt.  

### Lösung: Generalisierung und Spezialisierung  

Die Lösung des Problems besteht darin, dass die **gemeinsamen Attribute** in einem allgemeinen **Entitätstyp** zusammengefasst werden (**Generalisierung**).  
Die **nicht gemeinsamen Attribute** verbleiben in den spezialisierten Entitätstypen (**Spezialisierung**).  

#### Umsetzung in der Datenbank  

- Die spezialisierten Tabellen müssen per **Fremdschlüssel** auf die generalisierte Tabelle verweisen.  
- Diese Beziehung wird als **„is_a“-Beziehung** bezeichnet:  
  - *Eine Person ist ein Fahrer.*  

Diese Beziehungsform ist auch in der **objektorientierten Modellierung** bekannt und wird dort mittels **Vererbung** gelöst.
