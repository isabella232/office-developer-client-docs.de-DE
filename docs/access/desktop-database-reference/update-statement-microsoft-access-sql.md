---
title: UPDATE-Anweisung (Microsoft Access SQL)
TOCTitle: UPDATE statement (Microsoft Access SQL)
ms:assetid: 08f9c3d6-c020-ecf1-5748-43b93a76dfbb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845036(v=office.15)
ms:contentKeyID: 48543111
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277583
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: 97b41c7c4b296f931c04108568735f2bd38877e9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601632"
---
# <a name="update-statement-microsoft-access-sql"></a>UPDATE-Anweisung (Microsoft Access SQL)

**Gilt für**: Access 2013, Office 2013

Erstellt eine Aktualisierungsabfrage, die Werte in Feldern in einer angegebenen Tabelle basierend auf angegebenen Kriterien ändert.

## <a name="syntax"></a>Syntax

UPDATE *Tabelle* SET *neuerWert* WHERE *Kriterien*;

Die UPDATE-Anweisung setzt sich wie folgt zusammen:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Part</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>table</em></p></td>
<td><p>Der Name der Tabelle mit den Daten, die Sie ändern möchten.</p></td>
</tr>
<tr class="even">
<td><p><em>NeuerWert</em></p></td>
<td><p>Ein Ausdruck für den Wert, der in ein bestimmtes Feld in den aktualisierten Datensätzen eingefügt werden soll.</p></td>
</tr>
<tr class="odd">
<td><p><em>criteria</em></p></td>
<td><p>Ein Ausdruck, der festlegt, welche Datensätze aktualisiert werden. Nur Datensätze, die dem Ausdruck entsprechen, werden aktualisiert.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Die UPDATE-Anweisung ist besonders hilfreich, wenn Sie viele Datensätze ändern möchten oder die zu ändernden Datensätze in mehreren Tabellen vorhanden sind.

Mehrere Felder können gleichzeitig geändert werden. Im folgenden Beispiel werden für Versandfirmen im Vereinigten Königreich die Werte für "Order Amount" um 10 % und die Werte für "Freight" um 3 % erhöht:

```sql
UPDATE Orders 
SET OrderAmount = OrderAmount * 1.1, 
Freight = Freight * 1.03 
WHERE ShipCountry = 'UK';
```


> [!IMPORTANT]
- UPDATE generiert kein Resultset. Nach dem Aktualisieren von Datensätzen mit einer Aktualisierungsabfrage können Sie den Vorgang außerdem nicht rückgängig machen. Wenn Sie wissen möchten, welche Datensätze aktualisiert wurden, untersuchen Sie zunächst die Ergebnisse einer Auswahlabfrage, die die gleichen Kriterien verwendet, und führen Sie dann die Aktualisierungsabfrage aus.
- Bewahren Sie jederzeit Sicherungskopien Ihrer Daten auf. Wenn Sie die falschen Datensätze aktualisieren, können Sie diese aus Ihren Sicherungskopien abrufen.



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
