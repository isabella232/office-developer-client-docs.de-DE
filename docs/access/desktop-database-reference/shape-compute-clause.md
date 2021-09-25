---
title: Shape Compute-Klausel
TOCTitle: Shape Compute clause
ms:assetid: f4fee4a6-ec9e-c0b6-40e0-258f76c4696f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250245(v=office.15)
ms:contentKeyID: 48548699
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: e8edb920e5a4786a8e5bfb7908dd942b8172eb9a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552521"
---
# <a name="shape-compute-clause"></a>Shape Compute-Klausel

**Gilt für**: Access 2013, Office 2013

Durch eine COMPUTE-Klausel für Formen wird ein übergeordnetes **Recordset**-Objekt generiert, dessen Spalten aus Folgendem bestehen: aus einem Verweis auf das untergeordnete **Recordset**-Objekt; aus optionalen Spalten, deren Inhalt ein Kapitel, neue oder berechnete Spalten oder das Ergebnis der Ausführung von Aggregatfunktionen für das untergeordnete **Recordset**-Objekt oder ein vorher geformtes **Recordset**-Objekt sein kann; und aus allen Spalten des untergeordneten **Recordset**-Objekts, die in der optionalen BY-Klausel aufgelistet sind.

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

  - Ein Alias, mit dem auf das **Recordset**-Objekt verwiesen wird, das von *child-command* zurückgegeben wird. *child-alias* ist in der Liste der Spalten in der COMPUTE-Klausel erforderlich und definiert die Beziehung zwischen den übergeordneten und untergeordneten **Recordset**-Objekten.

- *appended-column-list*

  - Eine Liste, in der durch jedes Element eine Spalte im generierten übergeordneten Element definiert wird. Jedes Element enthält eine Kapitelspalte, eine neue Spalte, eine berechnete Spalte oder einen Wert, der das Ergebnis einer Aggregatfunktion für das untergeordnete **Recordset** -Objekt ist.

- *grp-field-list*

  - Eine Liste der Spalten in den übergeordneten und untergeordneten **Recordset**-Objekten, durch die angegeben wird, wie die Zeilen im untergeordneten Objekt gruppiert werden sollen. Für jede Spalte in *grp-field-list* ist in den untergeordneten und übergeordneten **Recordset**-Objekten eine entsprechende Spalte vorhanden. Für jede Zeile im übergeordneten **Recordset**-Objekt enthalten die Spalten von *grp-field-list* eindeutige Werte, und das **Recordset**-Objekt, auf das von der übergeordneten Zeile verwiesen wird, besteht ausschließlich aus untergeordneten Zeilen, deren *grp-field-list*-Spalten die gleichen Werte enthalten wie die übergeordnete Zeile.

Wenn die BY-Klausel enthalten ist, werden die Zeilen des untergeordneten **Recordset**-Objekts basierend auf den Spalten in der COMPUTE-Klausel gruppiert. Das übergeordnete **Recordset**-Objekt enthält eine Zeile für jede Zeilengruppe im untergeordneten **Recordset**-Objekt.

Wenn die BY-Klausel weggelassen wird, wird das gesamte untergeordnete **Recordset** -Objekt als einzelne Gruppe behandelt, und das übergeordnete **Recordset** -Objekt enthält genau eine Zeile. Durch diese Zeile wird auf das gesamte untergeordnete **Recordset** -Objekt verwiesen. Durch Weglassen der BY-Klausel können Sie "Gesamtsummenaggregate" für das gesamte untergeordnete **Recordset** -Objekt berechnen.

Beispiel:

```vb
    SHAPE {select * from Orders} AS orders
       COMPUTE orders, SUM(orders.OrderAmount) as TotalSales
```

Unabhängig davon, auf welche Weise das übergeordnete **Recordset**-Objekt geformt wird (mithilfe von COMPUTE oder mithilfe von APPEND), enthält es eine Kapitelspalte, die verwendet wird, um es in Beziehung zu einem untergeordneten **Recordset**-Objekt zu setzen. Wenn Sie dies möchten, kann das übergeordnete **Recordset**-Objekt auch Spalten enthalten, die Aggregate (SUM, MIN, MAX usw.) für die untergeordneten Zeilen enthalten. Sowohl das übergeordnete als auch das untergeordnete **Recordset**-Objekt können Spalten enthalten, die einen Ausdruck für die Zeile im **Recordset**-Objekt enthalten, sowie Spalten, die neu und anfangs leer sind.

## <a name="operation"></a>Vorgang

*child-command* wird an den Anbieter ausgegeben, von dem ein untergeordnetes **Recordset**-Objekt zurückgegeben wird.

Durch die COMPUTE-Klausel werden die Spalten des übergeordneten **Recordset**-Objekts angegeben, bei dem es sich um einen Verweis auf das untergeordnete **Recordset**-Objekt, auf eines oder mehrere Aggregate, auf einen berechneten Ausdruck oder auf neue Spalten handeln kann. Wenn eine BY-Klausel vorhanden ist, werden die dadurch definierten Spalten ebenfalls dem übergeordneten **Recordset**-Objekt angefügt. Durch die BY-Klausel wird angegeben, wie die Zeilen des untergeordneten **Recordset**-Objekts gruppiert werden.

Nehmen wir z. B. an, Sie haben eine Tabelle namens Demografische Daten, die aus den Feldern Bundesland, Ort und Bevölkerung besteht (die Bevölkerungszahlen dienen ausschließlich der Veranschaulichung).

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Status</p></th>
<th><p>Stadt</p></th>
<th><p>Bevölkerung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>WA</p></td>
<td><p>Seattle</p></td>
<td><p>700,000</p></td>
</tr>
<tr class="even">
<td><p>OR</p></td>
<td><p>Medford</p></td>
<td><p>200.000</p></td>
</tr>
<tr class="odd">
<td><p>OR</p></td>
<td><p>Portland</p></td>
<td><p>400,000</p></td>
</tr>
<tr class="even">
<td><p>CA</p></td>
<td><p>München</p></td>
<td><p>800,000</p></td>
</tr>
<tr class="odd">
<td><p>CA</p></td>
<td><p>Nürnberg</p></td>
<td><p>600.000</p></td>
</tr>
<tr class="even">
<td><p>WA</p></td>
<td><p>Tacoma</p></td>
<td><p>500.000</p></td>
</tr>
<tr class="odd">
<td><p>OR</p></td>
<td><p>Corvallis</p></td>
<td><p>300,000</p></td>
</tr>
</tbody>
</table>


Geben Sie nun diesen Shape-Befehl aus:

```vb 
 
rst.Open  "SHAPE {select * from demographics} AS rs "  & _ 
          "COMPUTE rs, SUM(rs.population) BY state", _ 
           objConnection 
```

Durch diesen Befehl wird ein geformtes **Recordset** -Objekt mit zwei Ebenen geöffnet. Die übergeordnete Ebene ist ein generiertes **Recordset** mit einer Aggregatspalte (SUM(rs.population) ), einer Spalte, die auf das untergeordnete **Recordset** (rs) verweist, und einer Spalte zum Gruppieren des untergeordneten **Recordset** (Status). Die untergeordnete Ebene ist das **Recordset,** das vom Abfragebefehl (), einer Spalte, die auf das untergeordnete **Recordset** (rs) verweist, und einer Spalte zum Gruppieren des untergeordneten **Recordset** -Objekts (Status) zurückgegeben wird. Die untergeordnete Ebene ist das **Recordset,** das vom Abfragebefehl zurückgegeben wird (auswahl \* aus dem demografischen Bereich).

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
<th><p>SUM (rs. Population)</p></th>
<th><p>rs</p></th>
<th><p>Status</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1,300,000</p></td>
<td><p>Verweis auf "child1"</p></td>
<td><p>CA</p></td>
</tr>
<tr class="even">
<td><p>1,200,000</p></td>
<td><p>Verweis auf untergeordnetes Element2</p></td>
<td><p>WA</p></td>
</tr>
<tr class="odd">
<td><p>1,100,000</p></td>
<td><p>Verweis auf untergeordnetes Element3</p></td>
<td><p>OR</p></td>
</tr>
</tbody>
</table>


**Child1**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Status</p></th>
<th><p>Stadt</p></th>
<th><p>Bevölkerung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>CA</p></td>
<td><p>München</p></td>
<td><p>800,000</p></td>
</tr>
<tr class="even">
<td><p>CA</p></td>
<td><p>Nürnberg</p></td>
<td><p>600.000</p></td>
</tr>
</tbody>
</table>


**Untergeordnetes Element2**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Status</p></th>
<th><p>Stadt</p></th>
<th><p>Bevölkerung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>WA</p></td>
<td><p>Seattle</p></td>
<td><p>700,000</p></td>
</tr>
<tr class="even">
<td><p>WA</p></td>
<td><p>Tacoma</p></td>
<td><p>500.000</p></td>
</tr>
</tbody>
</table>


**Untergeordnetes Element3**

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Status</p></th>
<th><p>Stadt</p></th>
<th><p>Bevölkerung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>OR</p></td>
<td><p>Medford</p></td>
<td><p>200.000</p></td>
</tr>
<tr class="even">
<td><p>OR</p></td>
<td><p>Portland</p></td>
<td><p>400,000</p></td>
</tr>
<tr class="odd">
<td><p>OR</p></td>
<td><p>Corvallis</p></td>
<td><p>300,000</p></td>
</tr>
</tbody>
</table>

