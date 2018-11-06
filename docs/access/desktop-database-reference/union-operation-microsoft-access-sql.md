---
title: UNION-Operation (Microsoft Access SQL)
TOCTitle: UNION operation (Microsoft Access SQL)
ms:assetid: a5139921-51e5-7d96-74e3-11c3fd5f7eaa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821131(v=office.15)
ms:contentKeyID: 48546826
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277582
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ed31f0105d8381667e1398fc5d91577d40998d81
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998819"
---
# <a name="union-operation-microsoft-access-sql"></a>UNION-Operation (Microsoft Access SQL)

**Betrifft**: Access 2013, Office 2013

Erstellt eine Union-Abfrage, in der die Ergebnisse von mindestens zwei unabhängigen Abfragen oder Tabellen miteinander kombiniert werden.

## <a name="syntax"></a>Syntax

\[Tabelle\] *Abfrage1* UNION \[alle\] \[Tabelle\] *abfrage2* \[UNION \[alle\] \[Tabelle\] *Abfragen* \[ ... \]\]

Die UNION-Operation enthält die folgenden Bestandteile:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Abfrage1-N</em></p></td>
<td><p>Eine SELECT-Anweisung, der Name einer gespeicherten Abfrage oder der Name einer gespeicherten Tabelle, der das Schlüsselwort TABLE vorangestellt ist.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Sie können die Ergebnisse von zwei oder mehr Abfragen, Tabellen und SELECT-Anweisungen in jeder beliebigen Kombination in einer einzelnen UNION-Operation zusammenführen. Im folgenden Beispiel wird die vorhandene New Accounts-Tabelle mit einer SELECT-Anweisung zusammengeführt:

```sql
TABLE [New Accounts] UNION ALL 
SELECT * 
FROM Customers 
WHERE OrderAmount > 1000;
```

Standardmäßig werden bei Verwendung einer UNION-Operation keine duplizierten Datensätze zurückgegeben. Sie können jedoch mithilfe des Prädikats [ALL](https://msdn.microsoft.com/library/ff195711\(v=office.15\)) sicherstellen, dass alle Datensätze zurückgegeben werden. Außerdem wird dadurch die Ausführung der Abfrage beschleunigt.

Alle Abfragen in einer UNION-Operation müssen dieselbe Anzahl von Feldern anfordern. Doch die Felder müssen nicht dieselbe Größe oder denselben Datentyp besitzen.

Verwenden Sie Aliase nur in der ersten SELECT-Anweisung, da sie in anderen Anweisungen ignoriert werden. In der ORDER BY-Klausel verweisen Sie auf ein Feld unter dem Namen, der in der ersten SELECT-Anweisung verwendet wird.

> [!NOTE]
> - Eine [GROUP BY-](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) oder [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql) -Klausel können in *jedem Abfrageargument* Sie um die zurückgegebenen Daten zu gruppieren.
> - [ORDER BY](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/order-by-clause-microsoft-access-sql) -Klausel können am Ende des *letzten abfragearguments* Sie die zurückgegebenen Daten in einer bestimmten Reihenfolge angezeigt.

## <a name="example"></a>Beispiel

In diesem Beispiel werden die Namen und Städte aller Lieferanten und Kunden in Brasilien abgerufen. Sie ruft die EnumFields-Prozedur, die Sie in diesem Beispiel wird die SELECT-Anweisung finden.

```vb
    Sub UnionX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Retrieve the names and cities of all suppliers  
        ' and customers in Brazil. 
        Set rst = dbs.OpenRecordset("SELECT CompanyName," _ 
            & " City FROM Suppliers" _ 
            & " WHERE Country = 'Brazil' UNION" _ 
            & " SELECT CompanyName, City FROM Customers" _ 
            & " WHERE Country = 'Brazil';") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 12 
     
        dbs.Close 
     
    End Sub
```
