---
title: UPDATE-Anweisung (Microsoft Access SQL)
TOCTitle: UPDATE Statement (Microsoft Access SQL)
ms:assetid: 08f9c3d6-c020-ecf1-5748-43b93a76dfbb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845036(v=office.15)
ms:contentKeyID: 48543111
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277583
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 3affce9346e9e322bc588ca1c3be24867a1469d6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473875"
---
# <a name="update-statement-microsoft-access-sql"></a>UPDATE-Anweisung (Microsoft Access SQL)


**Betrifft**: Access 2013 | Office 2013

Erstellt eine Aktualisierungsabfrage, die Werte in Feldern in einer angegebenen Tabelle basierend auf angegebenen Kriterien ändert.

## <a name="syntax"></a>Syntax

UPDATE *Tabelle* SET *Neuer Wert* WHERE *Kriterien*;

Die UPDATE-Anweisung hat diese Teile:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Teil</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Tabelle</em></p></td>
<td><p>Der Name der Tabelle mit den zu ändernden Daten.</p></td>
</tr>
<tr class="even">
<td><p><em>newvalue</em></p></td>
<td><p>Ein Ausdruck, der den Wert bestimmt, der in ein bestimmtes Feld in die aktualisierten Datensätze eingefügt werden soll.</p></td>
</tr>
<tr class="odd">
<td><p><em>Kriterien</em></p></td>
<td><p>Ein Ausdruck, der bestimmt, welche Datensätze aktualisiert werden. Nur Datensätze, die dem Ausdruck entsprechen, werden aktualisiert.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

UPDATE ist besonders dann nützlich, wenn Sie viele Datensätze ändern möchten oder wenn sich die zu ändernden Datensätze in mehreren Tabellen befinden.

Sie können mehrere Felder gleichzeitig ändern. Das folgende Beispiel erhöht für Versender in Großbritannien den Wert der Bestellmenge um zehn Prozent und den Wert der Fracht um drei Prozent.

```sql
UPDATE Orders 
SET OrderAmount = OrderAmount * 1.1, 
Freight = Freight * 1.03 
WHERE ShipCountry = 'UK';
```


> [!IMPORTANT]
> <UL>
> <LI>
> <P>UPDATE generiert kein Resultset. Nach dem Aktualisieren von Datensätzen mit einer Aktualisierungsabfrage können Sie den Vorgang außerdem nicht rückgängig machen. Wenn Sie wissen möchten, welche Datensätze aktualisiert wurden, untersuchen Sie zunächst die Ergebnisse einer Auswahlabfrage, die die gleichen Kriterien verwendet, und führen Sie dann die Aktualisierungsabfrage aus.</P>
> <LI>
> <P>Behalten Sie immer Sicherungskopien Ihrer Daten. Wenn Sie die falschen Datensätze aktualisieren, können Sie sie aus den Sicherungskopien abrufen.</P></LI></UL>



## <a name="example"></a>Beispiel

Dieses Beispiel ändert Werte im Feld "ReportsTo" für alle Mitarbeiterdatensätze, für die "ReportsTo" aktuell auf den Wert "2" festgelegt ist.

```vb
    Sub UpdateX() 
     
        Dim dbs As Database 
        Dim qdf As QueryDef 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Change values in the ReportsTo field to 5 for all  
        ' employee records that currently have ReportsTo  
        ' values of 2. 
        dbs.Execute "UPDATE Employees " _ 
            & "SET ReportsTo = 5 " _ 
            & "WHERE ReportsTo = 2;" 
             
        dbs.Close 
     
    End Sub
```
