---
title: DROP-Anweisung (Microsoft Access SQL)
TOCTitle: DROP statement (Microsoft Access SQL)
ms:assetid: a8c79c35-22da-2e6d-88b5-620eb481bb61
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821409(v=office.15)
ms:contentKeyID: 48546907
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 79e844c7694bf399496fb79bebf550e7c51ba8f6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562685"
---
# <a name="drop-statement-microsoft-access-sql"></a>DROP-Anweisung (Microsoft Access SQL)

**Gilt für**: Access 2013, Office 2013

Löscht eine vorhandene Tabelle, Prozedur oder Sicht aus einer Datenbank, oder löscht einen vorhandenen Index aus einer Tabelle.

> [!NOTE]
> Das Microsoft Access-Datenbankmodul unterstützt nicht die Verwendung der DROP-Anweisung oder anderer DDL-Anweisungen in Kombination mit Datenbanken, die nicht aus dem Microsoft Access-Datenbankmodul stammen. Verwenden Sie stattdessen die **Delete**-Methode für Datenzugriffsobjekte (DAO).

## <a name="syntax"></a>Syntax

DROP {TABLE *Tabelle* | INDEX *Index* ON *Tabelle* | PROCEDURE *Prozedur* | VIEW *Sicht*}

Die DROP-Anweisung setzt sich wie folgt zusammen:

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
<td><p><em>Tabelle</em></p></td>
<td><p>Der Name der zu löschenden Tabelle oder der Tabelle, aus der ein Index gelöscht werden soll.</p></td>
</tr>
<tr class="even">
<td><p><em>Prozedur</em></p></td>
<td><p>Der Name der zu löschenden Prozedur.</p></td>
</tr>
<tr class="odd">
<td><p><em>Sicht</em></p></td>
<td><p>Der Name der zu löschenden Sicht.</p></td>
</tr>
<tr class="even">
<td><p><em>Index</em></p></td>
<td><p>Der Name des aus der <em>Tabelle</em> zu löschenden Indexes.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Sie müssen die Tabelle schließen, bevor Sie sie löschen oder einen Index daraus entfernen können.

Sie können auch die [ALTER TABLE](alter-table-statement-microsoft-access-sql.md)-Anweisung verwenden, um einen Index aus einer Tabelle zu löschen.

Die [CREATE TABLE](create-table-statement-microsoft-access-sql.md)-Anweisung kann zum Erstellen einer Tabelle und die [CREATE INDEX](create-index-statement-microsoft-access-sql.md)- oder ALTER TABLE-Anweisung zum Erstellen eines Indexes verwendet werden. Verwenden Sie die ALTER TABLE-Anweisung ebenfalls, wenn Sie eine Tabelle ändern möchten.

## <a name="example"></a>Beispiel

The following example assumes the existence of a hypothetical NewIndex index on the Employees table in the Northwind database.

This example deletes the index MyIndex from the Employees table.

```vb
    Sub DropX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete NewIndex from the Employees table. 
        dbs.Execute "DROP INDEX NewIndex ON Employees;" 
     
        dbs.Close 
     
    End Sub
```

<br/>

This example deletes the Employees table from the database.

```vb
    Sub DropX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete the Employees table. 
        dbs.Execute "DROP TABLE Employees;" 
     
        dbs.Close 
     
    End Sub
```
