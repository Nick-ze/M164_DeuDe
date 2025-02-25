# Identifying und Non-Identifying Relationship

**Identifying** und **Non-Identifying Relationship** sind beides Beziehungsarten zwischen Tabellen.  

- **Identifying** ist viel strikter und lässt dadurch auch weniger Fehler zu. Es wird mit einer durchgezogene linie gezeichnet.
- **Non-Identifying** ist weniger genau und hängt nicht von dem Parent-Element ab. Es wird mit einer gestrichelten linie gezeichnet.

## Diagramme

![Identifying Relationship](https://github.com/user-attachments/assets/136811f4-4385-464b-85f0-4e9d666bb3b2)

![Non-Identifying Relationship](https://github.com/user-attachments/assets/c3316acd-494f-4f87-a550-f4670c6143a1)
# Beispiel
## Identifying Relationship: Bestellung & Bestellpositionen

Ein gutes Beispiel für eine **Identifying Relationship** ist die Beziehung zwischen **Bestellung** und **Bestellpositionen** in einem Onlineshop.

### Tabellenstruktur

**Bestellung (Order)**  
- `order_id` (Primärschlüssel)  
- `order_date`  
- `customer_id`  

**Bestellposition (OrderItem)**  
- `order_id` (Fremdschlüssel, Teil des Primärschlüssels)  
- `item_id` (Fremdschlüssel, Teil des Primärschlüssels)  
- `quantity`  
- `price`  

### Warum Identifying?  
- **Bestellpositionen existieren nur in Verbindung mit einer Bestellung.**  
- Sie haben keinen eigenen Primärschlüssel, sondern eine **kombinierte Primärschlüssel-Beziehung (`order_id` + `item_id`)**.

# Chat
## Anwendungsfälle von Identifying Relationships

Identifying Relationships (identifizierende Beziehungen) sind ein Konzept aus der Datenbankmodellierung, insbesondere in der Entity-Relationship-Modellierung (ERM). Sie treten auf, wenn eine Entität von einer anderen Entität abhängig ist, um ihre Existenz zu definieren. Diese Beziehungen sind in der Praxis in vielen Bereichen zu finden.

### 1. **Datenbanken und relationale Systeme**
   - **Primärschlüssel-Verknüpfungen**: Ein typisches Beispiel ist die Beziehung zwischen einer **Bestellung** und den **Bestellpositionen**. Die Bestellpositionen existieren nur innerhalb einer Bestellung, daher wird die Bestellung als Identifizierer für die Bestellpositionen verwendet.
   
### 2. **Software-Engineering**
   - **Vererbung in objektorientierten Systemen**: In objektorientierten Modellen, wie bei **Klassendiagrammen**, könnte ein Subtyp von einer übergeordneten Klasse abhängen. Hierbei könnte der Subtyp ohne den Supertype nicht existieren, was eine identifizierende Beziehung darstellt.

### 3. **Supply Chain Management**
   - **Lagerhaltung und Bestandseinheiten**: Eine **Lagerposition** innerhalb eines Lagers könnte von einem spezifischen Lagerort abhängen, was bedeutet, dass die Position ohne den Lagerort nicht definiert wäre.

### 4. **Gesundheitswesen**
   - **Patientenakte und Behandlungseinheiten**: Eine **Behandlungseinheit** könnte nur in Bezug auf eine **Patientenakte** existieren. Eine Behandlungseinheit ist nicht sinnvoll, ohne auf einen spezifischen Patienten zu verweisen.

### 5. **Finanzwesen**
   - **Konten und Transaktionen**: In einem Bankensystem sind **Transaktionen** oft mit einem bestimmten **Konto** verknüpft. Ein Konto ist daher der Identifikator für eine Transaktion.

### 6. **E-Commerce**
   - **Kunden und Bestellungen**: **Bestellungen** können nur in Bezug auf **Kunden** existieren. Ein Kunde muss eindeutig identifiziert werden, um eine Bestellung zu erstellen.

### 7. **Personalmanagement**
   - **Angestelltennummer und Gehaltsabrechnung**: Eine **Gehaltsabrechnung** könnte nur in Bezug auf eine spezifische **Angestelltennummer** existieren, wodurch eine Identifizierung der Gehaltsabrechnung durch die Mitarbeiter-ID erforderlich ist.

### Fazit
Identifying Relationships sind in vielen Bereichen von entscheidender Bedeutung, um die Integrität und Struktur von Daten zu gewährleisten. Sie helfen dabei, abhängige Entitäten in einer relationalen Struktur korrekt miteinander zu verbinden und stellen sicher, dass jede Entität eindeutig identifiziert werden kann.

