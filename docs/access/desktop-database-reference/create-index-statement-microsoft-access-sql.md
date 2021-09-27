---
title: CREATE INDEX-Anweisung (Microsoft Access SQL)
TOCTitle: CREATE INDEX statement (Microsoft Access SQL)
ms:assetid: c5919ef4-a08d-df06-7078-5331adbcb45c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823109(v=office.15)
ms:contentKeyID: 48547612
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277562
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: a831ae35f91bae1cd81c3db5dfd723ed31389295
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618357"
---
# <a name="create-index-statement-microsoft-access-sql"></a>CREATE INDEX-Anweisung (Microsoft Access SQL)

**Gilt für**: Access 2013, Office 2013

Erstellt einen neuen Index für eine vorhandene Tabelle.

> [!NOTE]
> Für Datenbanken, die nicht vom Microsoft Konnektivitätsmodul für Access stammen, unterstützt Microsoft Konnektivitätsmodul für Access nicht die Verwendung von CREATE INDEX (mit Ausnahme der Erstellung eines Pseudoindexes für eine verknüpfte ODBC-Tabelle) oder einer der DDL-Anweisungen (Data Definition Language). Verwenden Sie stattdessen die DAO **Erstellungs** -Methoden. Weitere Informationen finden Sie im Abschnitt "Hinweise".

## <a name="syntax"></a>Syntax

CREATE \[ UNIQUE \] INDEX *index* ON *table* (*field* \[ASC|DESC\]\[, *field* \[ASC|DESC\], …\]) \[WITH { PRIMARY | DISALLOW NULL | IGNORE NULL }\]

Die CREATE INDEX-Anweisung setzt sich wie folgt zusammen:

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
<td><p><em>Index</em></p></td>
<td><p>Der Name des zu erstellenden Index.</p></td>
</tr>
<tr class="even">
<td><p><em>table</em></p></td>
<td><p>Der Name der vorhandenen Tabelle, die den Index enthalten soll.</p></td>
</tr>
<tr class="odd">
<td><p><em>field</em></p></td>
<td><p>Der Name des oder der zu indizierenden Felder. Setzen Sie den Feldnamen in Klammern, und listen Sie ihn im Anschluss an den Tabellennamen auf, um einen Index mit einem Feld zu erstellen. Wenn Sie einen Index mit mehreren Feldern erstellen möchten, listen Sie jedes Feld auf, dass im Index eingeschlossen werden soll. Verwenden Sie das reservierte Wort DESC, um Indizes in absteigender Reihenfolge zu erstellen. Andernfalls wird davon ausgegangen, dass die Indizes in aufsteigender Reihenfolge erstellt werden sollen.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Verwenden Sie das reservierte Wort UNIQUE, um doppelte Werte im indizierten Feld oder in Feldern verschiedener Datensätze zu verhindern.

In der optionalen WITH-Klausel können Sie Datenüberprüfungsregeln in Kraft setzen. Sie können:

- Sie können NULL-Einträge im indizierten Feld oder in Feldern neuer Datensätze untersagen, indem Sie die Option DISALLOW NULL verwenden.

- Sie können verhindern, dass Datensätze mit **NULL**-Werten in dem/den indizierten Feld/Feldern in den Index aufgenommen werden, indem Sie die Option IGNORE NULL verwenden.

- Das oder die indizierten Felder unter Verwendung des reservierten Worts PRIMARY als Primärschlüssel bestimmen. Dies setzt voraus, dass der Schlüssel eindeutig ist, sodass das reservierte Wort UNIQUE ausgelassen werden kann.

Sie können CREATE INDEX verwenden, um einen Pseudoindex für eine verknüpfte Tabelle in einer ODBC-Datenquelle zu erstellen, z. B. Microsoft SQL Server, die nicht bereits über einen Index verfügt. Sie benötigen keine Berechtigung oder keinen Zugriff auf den Remoteserver, um einen Pseudoindex zu erstellen und die Remotedatenbank ist vom Pseudoindex nicht betroffen. Sie verwenden die gleiche Syntax für verknüpfte und native Tabellen. Das Erstellen eines Pseudoindexes für eine Tabelle, die normalerweise schreibgeschützt wäre, kann besonders nützlich sein.

Sie können auch die [ALTER TABLE](alter-table-statement-microsoft-access-sql.md)-Anweisung verwenden, um einen Index mit einem oder mehreren Feldern zu einer Tabelle hinzuzufügen, und Sie können die ALTER TABLE-Anweisung oder die [DROP](drop-statement-microsoft-access-sql.md)-Anweisung verwenden, um einen Index zu entfernen, der über die ALTER TABLE- oder CREATE INDEX-Anweisung erstellt wurde.

> [!NOTE]
> Verwenden Sie das reservierte Wort PRIMARY nicht, wenn Sie einen neuen Index für eine Tabelle erstellen, die bereits einen Primärschlüssel aufweist. Andernfalls tritt ein Fehler auf.

## <a name="example"></a>Beispiel

This example creates an index consisting of the fields Home Phone and Extension in the Employees table.

```vb
    Sub CreateIndexX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create the NewIndex index on the Employees table. 
        dbs.Execute "CREATE INDEX NewIndex ON Employees " _ 
            & "(HomePhone, Extension);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

This example creates an index on the Customers table using the CustomerID field. No two records can have the same data in the CustomerID field, and no Null values are allowed.

```vb
    Sub CreateIndexX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a unique index, CustID, on the  
        ' CustomerID field. 
        dbs.Execute "CREATE UNIQUE INDEX CustID " _ 
            & "ON Customers (CustomerID) " _ 
            & "WITH DISALLOW NULL;" 
     
        dbs.Close 
     
    End Sub
```
