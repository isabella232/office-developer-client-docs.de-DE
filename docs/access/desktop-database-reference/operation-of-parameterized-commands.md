---
title: Verwendung von parametrisierten Befehlen
TOCTitle: Operation of parameterized commands
ms:assetid: 71edbd16-21db-7afa-356b-d8e7afb92b3a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249456(v=office.15)
ms:contentKeyID: 48545596
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 145a2ee6c3d3c614eb9660350a0bb8a00d44d04c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717447"
---
# <a name="operation-of-parameterized-commands"></a>Verwendung von parametrisierten Befehlen

**Betrifft**: Access 2013, Office 2013

Wenn Sie ein umfangreiches untergeordnetes **Recordset** -Objekt verwenden, insbesondere im Vergleich zur Größe des übergeordneten **Recordset** -Objekts, aber nur auf ein paar untergeordnete Kapitel zugreifen müssen, könnte die Verwendung eines parametrisierten Befehls effizienter sein.

Einen *nicht parametrisierten Befehl* Ruft die gesamte über- und untergeordnete **Recordset-Objekte**, fügt eine Kapitelspalte an das übergeordnete Element und weist einen Verweis auf das zugehörige untergeordnete Kapitel für jede Zeile des übergeordneten.

Einen *parametrisierten Befehl* Ruft das gesamte übergeordnete **Recordset-Objekt**, sondern nur das Kapitel des **Recordset-Objekt** abgerufen, wenn auf die Kapitelspalte zugegriffen wird. Dieser Unterschied bei der Abrufstrategie kann erhebliche Leistungsvorteile bieten.

Beispielsweise können Sie Folgendes angeben:

```vb 
 
SHAPE {SELECT * FROM customer} 
 APPEND ({SELECT * FROM orders WHERE cust_id = ?} 
 RELATE cust_id TO PARAMETER 0) 
```

Die über- und untergeordneten Tabellen haben einen Spaltennamen in allgemeine, Cust\_Id *.* Der *untergeordnete Befehl* weist Platzhalter "?" die Klausel verknüpfen bezieht (d. h., "... PARAMETER 0").

> [!NOTE]
> [!HINWEIS] Die PARAMETER-Klausel bezieht sich ausschließlich auf die SHAPE-Befehlssyntax. Sie ist weder dem [Parameter](parameter-object-ado.md)-Objekt noch der [Parameters](parameters-collection-ado.md)-Auflistung von ADO zugeordnet.

Wenn der parametrisierte SHAPE-Befehl ausgeführt wird, passiert Folgendes:

1.  Der übergeordnete Befehl wird ausgeführt und gibt ein übergeordnetes Recordset-Objekt aus der Customers-Tabelle zurück.

2.  Eine Kapitelspalte wird an das übergeordnete **Recordset** -Objekt angefügt.

3.  Wenn auf die Kapitelspalte einer übergeordneten Zeile zugegriffen wird, der *untergeordnete Befehl* wird ausgeführt, mit dem Wert der customer.cust\_Id als Wert des Parameters.

4.  Alle Zeilen in der in Schritt 3 erstellte Anbieter Datenrowset dienen zum Auffüllen des untergeordneten **Recordset-Objekts**. In diesem Beispiel wird, die alle Zeilen in der Orders-Tabelle, in dem die Cust\_Id gleich dem Wert der customer.cust\_Id. Standardmäßig wird das untergeordnete **Recordset**s auf dem Client zwischengespeichert werden, bis alle Verweise auf das übergeordnete **Recordset** freigegeben werden. Wenn dieses Verhalten ändern möchten, legen Sie die **Recordset** - [dynamische Eigenschaft](ado-dynamic-property-index.md)**Cache untergeordneten Zeilen** auf **false festgelegt**.

5.  Ein Verweis auf die abgerufenen untergeordneten Zeilen (das heißt, das Kapitel des untergeordneten **Recordset**-Objekts) wird in der Kapitelspalte der aktuellen Zeile des übergeordneten **Recordset**-Objekts eingefügt.

6.  Die Schritte 3 bis 5 werden wiederholt, wenn auf die Kapitelspalte einer anderen Zeile zugegriffen wird.

Die dynamische Eigenschaft **Cache Child Rows** wird standardmäßig auf **True** festgelegt. Das Zwischenspeicherungsverhalten hängt von den Parameterwerten der Abfrage ab. Bei einer Abfrage mit einem einzelnen Parameter wird das untergeordnete **Recordset** -Objekt für einen bestimmten Parameterwert zwischen den Anforderungen für ein untergeordnetes Element mit diesem Wert zwischengespeichert. Der folgende Code veranschaulicht dies:

```vb
... 
SCmd = "SHAPE {select * from customer} " & _ 
 "APPEND({select * from orders where cust_id = ?} " & _ 
 "RELATE cust_id TO PARAMETER 0) AS chpCustOrder" 
Rst1.Open sCmd, Cnn1 
Set RstChild = Rst1("chpCustOrder").Value 
Rst1.MoveNext ' Next cust_id passed to Param 0, & new rs fetched 
 ' into RstChild. 
Rst1.MovePrevious ' RstChild now holds cached rs, saving round trip. 
... 
```

Bei einer Abfrage mit mehreren Parametern wird nur ein zwischengespeichertes untergeordnetes Element verwendet, wenn alle Parameterwerte den zwischengespeicherten Werten entsprechen.

## <a name="parameterized-commands-and-complex-parent-child-relations"></a>Parametrisierte Befehle und komplexe übergeordneten untergeordneten Elementen

Zusätzlich zur Verwendung von parametrisierter Befehlen zum Verbessern der Leistung einer Equi-Join-Typ-Hierarchie, können parametrisierte Befehle zur Unterstützung von komplexerer über-und untergeordneten Elementen verwendet werden. Angenommen, Sie verwenden eine Datenbank Little League mit zwei Tabellen: Basisplan, der die Teams (Team\_-Id, Team\_Name) und andere Spiele (Datum und private\_Team, besuchen\_Team).

Mit einer nicht parametrisierten Hierarchie können die Teams- und Spieletabellen nicht so miteinander verknüpft werden, dass das untergeordnete **Recordset** -Objekt für jedes Team den vollständigen Spielplan enthält. Sie können Kapitel erstellen, die den Heimspielplan oder den Auswärtsspielplan enthalten, jedoch nicht beides. Denn die RELATE-Klausel beschränkt Sie auf Beziehungen zwischen über- und untergeordneten Elementen im Format (pc1=cc1) AND (pc2=pc2). Dies, wenn der Befehl enthielt "verknüpfen Team\_Id zu Hause\_Team, Team\_Id zu besuchen\_Team", erhalten Sie nur spielen, wurde ein Team selbst wiedergeben. Verfügbare ist "(Team\_Id = home\_Team) oder (Team\_Id = Vorsichtsmaßnahmen\_Team)", aber der Shape-Anbieter Momentaufnahmen nicht unterstützt die OR-Klausel.

Sie können einen parametrisierten Befehl verwenden, um das gewünschte Ergebnis zu erhalten. Beispiel:

```vb 
 
SHAPE {SELECT * FROM teams} 
APPEND ({SELECT * FROM games WHERE home_team = ? OR visiting_team = ?} 
 RELATE team_id TO PARAMETER 0, 
 team_id TO PARAMETER 1) 
```

Dieses Beispiel nutzt die größere Flexibilität der WHERE-Klausel von SQL, um das gewünschte Ergebnis zu erhalten.

