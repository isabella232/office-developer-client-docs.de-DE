---
title: SELECT.INTO-Anweisung (Microsoft Access SQL)
TOCTitle: SELECT.INTO statement (Microsoft Access SQL)
ms:assetid: 29f3bd55-52f5-a36e-4e33-4b3499c6ce8d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192059(v=office.15)
ms:contentKeyID: 48543897
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 3c5b911c4391dd975c8ed2b1c5ddbf17ccc4bb38
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626106"
---
# <a name="selectinto-statement-microsoft-access-sql"></a>SELECT.INTO-Anweisung (Microsoft Access SQL)

**Gilt für**: Access 2013, Office 2013

Erstellt eine make-table-Abfrage.

## <a name="syntax"></a>Syntax

SELECT *field1*\[, *field2*\[, …\]\] INTO *newtable* \[IN *externaldatabase*\] FROM *source*

Die Anweisung SELECT…INTO besteht aus den folgenden Teilen:

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
<td><p><em>field1</em>, <em>field2</em></p></td>
<td><p>Die Namen der Felder, die in die neue Tabelle kopiert werden sollen.</p></td>
</tr>
<tr class="even">
<td><p><em>neue_Tabelle</em></p></td>
<td><p>Der Name der zu erstellenden Tabelle. Er muss den üblichen Benennungskonventionen entsprechen. Wenn <em>neueTabelle</em> denselben Namen wie eine bereits vorhanden Tabelle hat, tritt ein abfangbarer Fehler auf.</p></td>
</tr>
<tr class="odd">
<td><p><em>externeDatenbank</em></p></td>
<td><p>Ich bin für diese Woche leider bereits ausgebucht. Eine Beschreibung des Pfads finden Sie unter der <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a>-Klausel.</p></td>
</tr>
<tr class="even">
<td><p><em>source</em></p></td>
<td><p>Der Name der vorhandenen Tabelle, in der Datensätze ausgewählt werden. Dabei kann es sich um eine einzelne oder mehrere Tabellen oder eine Abfrage handeln.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Mithilfe von Tabellenerstellungsabfragen können Sie Datensätze archivieren, Sicherungskopien der Tabellen erstellen, Kopien zum Exportieren in eine andere Datenbank erstellen oder Berichte anfertigen, die Daten für einen bestimmten Zeitraum enthalten. Beispielsweise könnten Sie einen Bericht "Monatsumsatz nach Region" erstellen, indem Sie jeden Monat dieselbe Tabellenerstellungsabfrage ausführen.

> [!NOTE]
> - Möglicherweise sollten Sie einen Primärschlüssel für die neue Tabelle festlegen. Bei der Erstellung der Tabelle werden die Datentypen und Feldgrößen aller Felder der der Abfrage zugrunde liegenden Tabellen an die Felder der neuen Tabelle vererbt. Es werden jedoch keine weiteren Feld- oder Tabelleneigenschaften übertragen.
> - Um einer bereits bestehenden Tabelle Daten hinzuzufügen, verwenden Sie die [INSERT INTO](insert-into-statement-microsoft-access-sql.md)-Anweisung anstelle einer Anfügeabfrage.
> - Um herauszufinden, welche Datensätze ausgewählt werden, bevor Sie die make-table-Abfrage ausführen, führen Sie erst einmal eine [SELECT](select-statement-microsoft-access-sql.md)-Anweisung mit denselben Auswahlkriterien aus.



## <a name="example"></a>Beispiel

In diesem Beispiel werden alle Datensätze in der Tabelle "Employees" ausgewählt und in eine neue Tabelle namens "Emp Backup" kopiert.

```vb
    Sub SelectIntoX() 
     
        Dim dbs As Database 
        Dim qdf As QueryDef 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Select all records in the Employees table  
        ' and copy them into a new table, Emp Backup. 
        dbs.Execute "SELECT Employees.* INTO " _ 
            & "[Emp Backup] FROM Employees;" 
             
        ' Delete the table because this is a demonstration. 
        dbs.Execute "DROP TABLE [Emp Backup];" 
         
        dbs.Close 
     
    End Sub
```
