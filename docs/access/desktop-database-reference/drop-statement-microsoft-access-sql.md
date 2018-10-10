---
title: DROP-Anweisung (Microsoft Access SQL)
TOCTitle: DROP Statement (Microsoft Access SQL)
ms:assetid: a8c79c35-22da-2e6d-88b5-620eb481bb61
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821409(v=office.15)
ms:contentKeyID: 48546907
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3fc43547d6b9b744e004d44fff14b3fe82360732
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474495"
---
# <a name="drop-statement-microsoft-access-sql"></a>DROP-Anweisung (Microsoft Access SQL)

**Betrifft**: Access 2013 | Office 2013

Löscht eine vorhandene Tabelle, Prozedur oder Sicht aus einer Datenbank, oder löscht einen vorhandenen Index aus einer Tabelle.

> [!NOTE]
> [!HINWEIS] Das Microsoft Access-Datenbankmodul unterstützt nicht die Verwendung der DROP-Anweisung oder anderer DDL-Anweisungen in Kombination mit Datenbanken, die nicht aus dem Microsoft Access-Datenbankmodul stammen. Verwenden Sie stattdessen die **Delete** -Methode für Datenzugriffsobjekte (DAO).

## <a name="syntax"></a>Syntax

DROP {TABLE *Tabelle* | INDEX *Index* ON *Tabelle* | PROCEDURE *Prozedur* | VIEW *Sicht*}

Die DROP-Anweisung besteht aus folgenden Komponenten:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Komponente</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Tabelle</em></p></td>
<td><p>Der Name der zu löschenden Tabelle oder der Tabelle, die den zu löschenden Index enthält.</p></td>
</tr>
<tr class="even">
<td><p><em>Prozedur</em></p></td>
<td><p>Der Name der zu löschenden Prozedur.</p></td>
</tr>
<tr class="odd">
<td><p><em>view</em></p></td>
<td><p>Der Name der zu löschenden Sicht.</p></td>
</tr>
<tr class="even">
<td><p><em>Index</em></p></td>
<td><p>Der Name des aus der <em>Tabelle</em> zu löschenden Indexes.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Die Tabelle muss geschlossen werden, bevor ein Index daraus gelöscht oder entfernt werden kann.

Sie können auch die [ALTER TABLE](alter-table-statement-microsoft-access-sql.md)-Anweisung verwenden, um einen Index aus einer Tabelle zu löschen.

Die [CREATE TABLE](create-table-statement-microsoft-access-sql.md)-Anweisung kann zum Erstellen einer Tabelle und die [CREATE INDEX](create-index-statement-microsoft-access-sql.md)- oder ALTER TABLE-Anweisung zum Erstellen eines Indexes verwendet werden. Verwenden Sie die ALTER TABLE-Anweisung ebenfalls, wenn Sie eine Tabelle ändern möchten.

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird davon ausgegangen, dass der hypothetische NewIndex-Index zur Angabe eines neuen Indexes in der Employees-Tabelle (Personal) in der Datenbank Northwind.mdb (Nordwind.mdb) vorhanden ist. 



Im folgenden Beispiel wird der MyIndex-Index aus der Employees-Tabelle (Personal) gelöscht.



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

Im folgenden Beispiel wird die Employees-Tabelle (Personal) aus der Datenbank gelöscht.



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
