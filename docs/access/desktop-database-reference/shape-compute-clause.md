---
title: Shape Compute-Klausel
TOCTitle: Shape Compute clause
ms:assetid: f4fee4a6-ec9e-c0b6-40e0-258f76c4696f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250245(v=office.15)
ms:contentKeyID: 48548699
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: eadc448d59814f0573a959c6c1038f9c4afdbac9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711525"
---
# <a name="shape-compute-clause"></a>Shape Compute-Klausel

**Betrifft**: Access 2013, Office 2013

Durch eine COMPUTE-Klausel für Formen wird ein übergeordnetes **Recordset** -Objekt generiert, dessen Spalten aus Folgendem bestehen: aus einem Verweis auf das untergeordnete **Recordset** -Objekt; aus optionalen Spalten, deren Inhalt ein Kapitel, neue oder berechnete Spalten oder das Ergebnis der Ausführung von Aggregatfunktionen für das untergeordnete **Recordset** -Objekt oder ein vorher geformtes **Recordset** -Objekt sein kann; und aus allen Spalten des untergeordneten **Recordset** -Objekts, die in der optionalen BY-Klausel aufgelistet sind.

## <a name="syntax"></a>Syntax

```vb 
 
SHAPE child-command [AS] child-alias 
   COMPUTE child-alias [[AS] name], [appended-column-list] 
   [BY grp-field-list] 
```

## <a name="description"></a>Beschreibung

Die Teile dieser Klausel lauten wie folgt:

- *child-command*

  - Besteht aus einem der Folgenden:
    
    - Ein Abfragebefehl in geschweiften Klammern ("{}"), der ein untergeordnetes **Recordset** -Objekt zurückgibt. Der Befehl wird an den zugrunde liegenden Datenanbieter ausgegeben, und die Syntax des Befehls hängt von den Anforderungen dieses Anbieters ab. Normalerweise handelt es sich dabei um die SQL-Sprache, obwohl für ADO keine bestimmte Abfragesprache erforderlich ist.
    
    - Der Name eines vorhandenen geformten **Recordset** -Objekts.
    
    - Ein weiterer Shape-Befehl.
    
    - Das TABLE-Schlüsselwort, gefolgt vom Namen einer Tabelle im Datenprovider.

- *child-alias*

  - Ein Alias verwendet, um an das **Recordset-Objekt** verweisen zurückgegebene der *untergeordnete Befehl.* Der *Alias des untergeordneten Elements* in der Liste der Spalten in der COMPUTE-Klausel ist erforderlich, und definiert die Beziehung zwischen über- und untergeordnete **Recordset** -Objekte.

- *appended-column-list*

  - Eine Liste, in der durch jedes Element eine Spalte im generierten übergeordneten Element definiert wird. Jedes Element enthält eine Kapitelspalte, eine neue Spalte, eine berechnete Spalte oder einen Wert, der das Ergebnis einer Aggregatfunktion für das untergeordnete **Recordset** -Objekt ist.

- *grp-field-list*

  - Eine Liste der Spalten in den übergeordneten und untergeordneten **Recordset** -Objekten, durch die angegeben wird, wie die Zeilen im untergeordneten Objekt gruppiert werden sollen. Für jede Spalte in der *Gruppe-Feld-Liste* vorhanden ist eine entsprechende Spalte in der untergeordneten und übergeordneten **Recordset** -Objekten. Für jede Zeile im übergeordneten **Recordset-Objekts**, die *Gruppe Feldliste* Spalten eindeutige Werte haben und das untergeordnete **Recordset-Objekt** von der übergeordneten Zeile verwiesen, ausschließlich aus untergeordneten besteht Zeilen, deren *Gruppe Feldliste* Spalten enthalten dieselben Werte wie die übergeordneten Zeile.

Wenn die BY-Klausel enthalten ist, werden die Zeilen des untergeordneten **Recordset**-Objekts basierend auf den Spalten in der COMPUTE-Klausel gruppiert. Das übergeordnete **Recordset**-Objekt enthält eine Zeile für jede Zeilengruppe im untergeordneten **Recordset**-Objekt.

Wenn die BY-Klausel weggelassen wird, wird das gesamte untergeordnete **Recordset** -Objekt als einzelne Gruppe behandelt, und das übergeordnete **Recordset** -Objekt enthält genau eine Zeile. Durch diese Zeile wird auf das gesamte untergeordnete **Recordset** -Objekt verwiesen. Durch Weglassen der BY-Klausel können Sie "Gesamtsummenaggregate" für das gesamte untergeordnete **Recordset** -Objekt berechnen.

Beispiel:

```vb
    SHAPE {select * from Orders} AS orders
       COMPUTE orders, SUM(orders.OrderAmount) as TotalSales
```

Unabhängig davon, auf welche Weise das übergeordnete **Recordset** -Objekt geformt wird (mithilfe von COMPUTE oder mithilfe von APPEND), enthält es eine Kapitelspalte, die verwendet wird, um es in Beziehung zu einem untergeordneten **Recordset** -Objekt zu setzen. Wenn Sie dies möchten, kann das übergeordnete **Recordset** -Objekt auch Spalten enthalten, die Aggregate (SUM, MIN, MAX usw.) für die untergeordneten Zeilen enthalten. Sowohl das übergeordnete als auch das untergeordnete **Recordset** -Objekt können Spalten enthalten, die einen Ausdruck für die Zeile im **Recordset** -Objekt enthalten, sowie Spalten, die neu und anfangs leer sind.

## <a name="operation"></a>Verwendung

Der *untergeordnete Befehl* wird an den Anbieter ausgegeben, von dem ein untergeordnetes **Recordset-Objekt**zurückgegeben.

Durch die COMPUTE-Klausel werden die Spalten des übergeordneten **Recordset** -Objekts angegeben, bei dem es sich um einen Verweis auf das untergeordnete **Recordset** -Objekt, auf eines oder mehrere Aggregate, auf einen berechneten Ausdruck oder auf neue Spalten handeln kann. Wenn eine BY-Klausel vorhanden ist, werden die dadurch definierten Spalten ebenfalls dem übergeordneten **Recordset** -Objekt angefügt. Durch die BY-Klausel wird angegeben, wie die Zeilen des untergeordneten **Recordset** -Objekts gruppiert werden.

Nehmen wir z. B. an, Sie haben eine Tabelle namens Demografische Daten, die aus den Feldern Bundesland, Ort und Bevölkerung besteht (die Bevölkerungszahlen dienen ausschließlich der Veranschaulichung).

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Bundesland</p></th>
<th><p>Ort</p></th>
<th><p>Bevölkerung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Hessen</p></td>
<td><p>Frankfurt</p></td>
<td><p>700.000</p></td>
</tr>
<tr class="even">
<td><p>Nordrhein-Westfalen</p></td>
<td><p>Köln</p></td>
<td><p>200.000</p></td>
</tr>
<tr class="odd">
<td><p>Nordrhein-Westfalen</p></td>
<td><p>Düsseldorf</p></td>
<td><p>400.000</p></td>
</tr>
<tr class="even">
<td><p>Bayern</p></td>
<td><p>München</p></td>
<td><p>Um 800.000</p></td>
</tr>
<tr class="odd">
<td><p>Bayern</p></td>
<td><p>Nürnberg</p></td>
<td><p>600.000</p></td>
</tr>
<tr class="even">
<td><p>Hessen</p></td>
<td><p>Offenbach</p></td>
<td><p>500.000</p></td>
</tr>
<tr class="odd">
<td><p>Nordrhein-Westfalen</p></td>
<td><p>Dortmund</p></td>
<td><p>300.000</p></td>
</tr>
</tbody>
</table>


Geben Sie nun diesen Shape-Befehl aus:

```vb 
 
rst.Open  "SHAPE {select * from demographics} AS rs "  & _ 
          "COMPUTE rs, SUM(rs.population) BY state", _ 
           objConnection 
```

Durch diesen Befehl wird ein geformtes **Recordset** -Objekt mit zwei Ebenen geöffnet. Die übergeordnete Ebene ist ein generierten **Recordset-Objekt** mit einer Aggregatspalte (SUM(rs.population)), eine Spalte verweisen auf das untergeordnete **Recordset-Objekt** (Rs) und eine Spalte zum Gruppieren des untergeordneten **Recordset-Objekt** (Zustand). Die untergeordneten Ebene ist das **Recordset-Objekt** durch den Befehl (Abfrage), eine Spalte verweisen auf das untergeordnete **Recordset-Objekt** (Rs) und eine Spalte zum Gruppieren des untergeordneten **Recordset-Objekt** (Zustand) zurückgegeben. Die untergeordneten Ebene ist das **Recordset-Objekt** durch den Abfragebefehl zurückgegebenen (Wählen Sie \* aus demografischer).

Die Detailzeilen des untergeordneten **Recordset** -Objekts werden nach Bundesland, aber ansonsten ohne besondere Reihenfolge gruppiert. Das heißt, die Gruppen befinden sich nicht in einer alphabetischen oder numerischen Reihenfolge. Wenn das übergeordnete **Recordset** -Objekt sortiert werden soll, können Sie die **Sort** -Methode für das **Recordset** -Objekt zum Sortieren des übergeordneten **Recordset** -Objekts verwenden.

Sie können jetzt im geöffneten übergeordneten **Recordset** -Objekt navigieren und auf die untergeordneten **Recordset** -Detailobjekte zugreifen. Weitere Informationen finden Sie unter [Zugreifen auf Zeilen in einem hierarchischen Recordset](accessing-rows-in-a-hierarchical-recordset.md).

**Übergeordnete und untergeordnete Detailergebnisdatensätze**

**Übergeordnet**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>SUM (rs.Bevölkerung)</p></th>
<th><p>rs</p></th>
<th><p>Bundesland</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1,300,000</p></td>
<td><p>Verweis auf untergeordnetes Recordset (Stufe 1)</p></td>
<td><p>Bayern</p></td>
</tr>
<tr class="even">
<td><p>1,200,000</p></td>
<td><p>Verweis auf untergeordnetes Recordset (Stufe 2)</p></td>
<td><p>Hessen</p></td>
</tr>
<tr class="odd">
<td><p>1,100,000</p></td>
<td><p>Verweis auf untergeordnetes Recordset (Stufe 3)</p></td>
<td><p>Nordrhein-Westfalen</p></td>
</tr>
</tbody>
</table>


**Untergeordneter Knoten 1**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Bundesland</p></th>
<th><p>Ort</p></th>
<th><p>Bevölkerung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Bayern</p></td>
<td><p>München</p></td>
<td><p>Um 800.000</p></td>
</tr>
<tr class="even">
<td><p>Bayern</p></td>
<td><p>Nürnberg</p></td>
<td><p>600.000</p></td>
</tr>
</tbody>
</table>


**Child2**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Bundesland</p></th>
<th><p>Ort</p></th>
<th><p>Bevölkerung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Hessen</p></td>
<td><p>Frankfurt</p></td>
<td><p>700.000</p></td>
</tr>
<tr class="even">
<td><p>Hessen</p></td>
<td><p>Offenbach</p></td>
<td><p>500.000</p></td>
</tr>
</tbody>
</table>


**Child3**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Bundesland</p></th>
<th><p>Ort</p></th>
<th><p>Bevölkerung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Nordrhein-Westfalen</p></td>
<td><p>Köln</p></td>
<td><p>200.000</p></td>
</tr>
<tr class="even">
<td><p>Nordrhein-Westfalen</p></td>
<td><p>Düsseldorf</p></td>
<td><p>400.000</p></td>
</tr>
<tr class="odd">
<td><p>Nordrhein-Westfalen</p></td>
<td><p>Dortmund</p></td>
<td><p>300.000</p></td>
</tr>
</tbody>
</table>

