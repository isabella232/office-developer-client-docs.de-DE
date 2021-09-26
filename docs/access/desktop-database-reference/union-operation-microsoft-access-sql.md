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
ms.localizationpriority: high
ms.openlocfilehash: fe90799406b66be08b1088113665ce12ab55faa1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580706"
---
# <a name="union-operation-microsoft-access-sql"></a>UNION-Operation (Microsoft Access SQL)

**Gilt für**: Access 2013, Office 2013

Erstellt eine Union-Abfrage, in der die Ergebnisse von mindestens zwei unabhängigen Abfragen oder Tabellen miteinander kombiniert werden.

## <a name="syntax"></a>Syntax

\[TABLE\] *Abfrage1* UNION \[ALL\] \[TABLE\] *Abfrage2* \[UNION \[ALL\] \[TABLE\] *Abfrage-n* \[ … \]\]

Der UNION-Vorgang besteht aus den folgenden Teilen:

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
<td><p><em>Abfrage1-n</em></p></td>
<td><p>Eine SELECT-Anweisung, der Name einer gespeicherten Abfrage oder der Name einer gespeicherten Tabelle, der das Schlüsselwort TABLE vorangestellt ist.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Sie können die Ergebnisse von mindestens zwei Abfragen, Tabellen und SELECT-Anweisungen in einer beliebigen Kombination in einem einzigen UNION-Vorgang zusammenführen. Im folgenden Beispiel werden die vorhandene Tabelle "Neue Konten" und eine SELECT-Anweisung zusammengeführt:

```sql
TABLE [New Accounts] UNION ALL 
SELECT * 
FROM Customers 
WHERE OrderAmount > 1000;
```

Standardmäßig werden bei Verwendung einer UNION-Operation keine duplizierten Datensätze zurückgegeben. Sie können jedoch mithilfe des Prädikats [ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) sicherstellen, dass alle Datensätze zurückgegeben werden. Außerdem wird dadurch die Ausführung der Abfrage beschleunigt.

Alle Abfragen in einer UNION-Operation müssen dieselbe Anzahl von Feldern anfordern. Doch die Felder müssen nicht dieselbe Größe oder denselben Datentyp besitzen.

Verwenden Sie Aliase nur in der ersten SELECT-Anweisung, weil sie in anderen Anweisungen ignoriert werden. Verweisen Sie in der ORDER BY-Klausel so auf die Felder, wie sie in der ersten SELECT-Anweisung bezeichnet werden.

> [!NOTE]
> - Sie können in jedem *Abfrage* argument eine [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql)- oder eine [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql)-Klausel verwenden, um die zurückgegebenen Daten zu gruppieren.
> - Sie können am Ende des letzten *Abfrage* arguments eine [ORDER BY](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/order-by-clause-microsoft-access-sql)-Klausel verwenden, um die zurückgegebenen Daten in einer bestimmten Reihenfolge anzuzeigen.

## <a name="example"></a>Beispiel

In diesem Beispiel werden die Namen und Städte aller Händler und Kunden in Brasilien abgerufen. Dabei wird die EnumFields-Prozedur aufgerufen, die im Beispiel für die SELECT-Anweisung enthalten ist.

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
