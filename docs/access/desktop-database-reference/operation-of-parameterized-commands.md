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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288287"
---
# <a name="operation-of-parameterized-commands"></a>Verwendung von parametrisierten Befehlen

**Gilt für**: Access 2013, Office 2013

Wenn Sie ein umfangreiches untergeordnetes **Recordset**-Objekt verwenden, insbesondere im Vergleich zur Größe des übergeordneten **Recordset**-Objekts, aber nur auf ein paar untergeordnete Kapitel zugreifen müssen, könnte die Verwendung eines parametrisierten Befehls effizienter sein.

Mit einem *nicht parametrisierten Befehl* werden die gesamten über- und untergeordneten **Recordset**-Objekte abgerufen, eine Kapitelspalte wird an das übergeordnete Elemente angefügt, und anschließend wird ein Verweis auf das zugehörige untergeordnete Kapitel für jede übergeordnete Zeile zugewiesen.

Mit einem *parametrisierten Befehl* wird das gesamte übergeordnete **Recordset**-Objekt abgerufen, aber es wird nur das Kapitel des **Recordset**-Objekts abgerufen, wenn auf die Kapitelspalte zugegriffen wird. Dieser Unterschied bei der Abrufstrategie kann erhebliche Leistungsvorteile bieten.

Beispielsweise können Sie Folgendes angeben:

```vb 
 
SHAPE {SELECT * FROM customer} 
 APPEND ({SELECT * FROM orders WHERE cust_id = ?} 
 RELATE cust_id TO PARAMETER 0) 
```

Die über-und untergeordneten Tabellen haben einen gemeinsamen Spalten\_Namen, cust ID *.* Der *untergeordnete Befehl* enthält den Platzhalter "?", auf den die RELATE-Klausel verweist (das heißt, "...PARAMETER 0").

> [!NOTE]
> [!HINWEIS] Die PARAMETER-Klausel bezieht sich ausschließlich auf die SHAPE-Befehlssyntax. Sie ist weder dem [Parameter](parameter-object-ado.md)-Objekt noch der [Parameters](parameters-collection-ado.md)-Auflistung von ADO zugeordnet.

Wenn der parametrisierte SHAPE-Befehl ausgeführt wird, passiert Folgendes:

1.  Der *übergeordnete Befehl* wird ausgeführt und gibt ein übergeordnetes **Recordset** -Objekt aus der Customers-Tabelle zurück.

2.  Eine Kapitelspalte wird an das übergeordnete **Recordset**-Objekt angefügt.

3.  Wenn auf die Kapitelspalte einer übergeordneten Zeile zugegriffen wird, wird der *untergeordnete Befehl* mit dem Wert der Customer.\_cust-ID als Wert des Parameters ausgeführt.

4.  All rows in the data provider rowset created in step 3 are used to populate the child **Recordset**. In diesem Beispiel sind das alle Zeilen in der Orders-Tabelle, in der die\_cust-ID dem Wert von "Customer\_. cust ID" entspricht. Standardmäßig wird das untergeordnete **Recordset**-Objekt auf dem Client zwischengespeichert, bis alle Verweise auf das übergeordnete **Recordset** -Objekt freigegeben werden. Um dieses Verhalten zu ändern, legen Sie die**UntergeordnetEn Datensätze** des **Recordset** [-dynamischen](ado-dynamic-property-index.md)Caches auf **false**fest.

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

## <a name="parameterized-commands-and-complex-parent-child-relations"></a>Parametrisierte Befehle und komplexe Parent-Child-Beziehungen

In addition to using parameterized commands to improve performance of an equi-join type hierarchy, parameterized commands can be used to support more complex parent-child relationships. Betrachten Sie beispielsweise eine kleine Liga Datenbank mit zwei Tabellen: eine bestehend aus den Teams\_(Team ID\_, Teamname) und den anderen spielen (Datum,\_Heimmannschaft,\_Besuchs Team).

Mit einer nicht parametrisierten Hierarchie können die Teams- und Spieletabellen nicht so miteinander verknüpft werden, dass das untergeordnete **Recordset** -Objekt für jedes Team den vollständigen Spielplan enthält. Sie können Kapitel erstellen, die den Heimspielplan oder den Auswärtsspielplan enthalten, jedoch nicht beides. Denn die RELATE-Klausel beschränkt Sie auf Beziehungen zwischen über- und untergeordneten Elementen im Format (pc1=cc1) AND (pc2=pc2). Wenn Ihr Befehl also\_"Relate Team ID to Home\_Team, Team\_ID to Visiting\_Team" enthält, würden Sie nur Spiele erhalten, bei denen sich ein Team selbst anspielte. \_Sie möchten "(Team ID = Home\_Team) oder (Team\_ID = Besuchs\_Team)", aber der Shape-Anbieter unterstützt die or-Klausel nicht.

Sie können einen parametrisierten Befehl verwenden, um das gewünschte Ergebnis zu erhalten. Beispiel:

```vb 
 
SHAPE {SELECT * FROM teams} 
APPEND ({SELECT * FROM games WHERE home_team = ? OR visiting_team = ?} 
 RELATE team_id TO PARAMETER 0, 
 team_id TO PARAMETER 1) 
```

Dieses Beispiel nutzt die größere Flexibilität der WHERE-Klausel von SQL, um das gewünschte Ergebnis zu erhalten.

