---
title: WÄHLEN SIE AUS. INTO-Anweisung (Microsoft Access SQL)
TOCTitle: SELECT.INTO statement (Microsoft Access SQL)
ms:assetid: 29f3bd55-52f5-a36e-4e33-4b3499c6ce8d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192059(v=office.15)
ms:contentKeyID: 48543897
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 1c05679994cfd98fdc5d6ffb389df00c2f5c9b94
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861995"
---
# <a name="selectinto-statement-microsoft-access-sql"></a>WÄHLEN SIE AUS. INTO-Anweisung (Microsoft Access SQL)

**Betrifft**: Access 2013 | Office 2013

Erstellt eine make-table-Abfrage.

## <a name="syntax"></a>Syntax

SELECT *Feld1*\[, *Feld2*\[,... \] \] INTO *neue Tabelle* \[IN *externe Datenbank* \] aus der *Datenquelle*

Die Anweisung SELECT…INTO besteht aus den folgenden Teilen:

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
<td><p><em>Feld1</em>, <em>Feld2</em></p></td>
<td><p>Die Namen der Felder, die in die neue Tabelle kopiert werden sollen.</p></td>
</tr>
<tr class="even">
<td><p><em>neueTabelle</em></p></td>
<td><p>Der Name der zu erstellenden Tabelle. Er muss den üblichen Benennungskonventionen entsprechen. Wenn die <em>neue Tabelle</em> den Namen einer vorhandenen Tabelle identisch ist, tritt ein auffangbarer Fehler auf.</p></td>
</tr>
<tr class="odd">
<td><p><em>externeDatenbank</em></p></td>
<td><p>Der Pfad zu einer externen Datenbank. Eine Beschreibung des Pfads finden Sie unter der <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a>-Klausel.  </p></td>
</tr>
<tr class="even">
<td><p><em>Quelle</em></p></td>
<td><p>Der Name einer bereits bestehenden Tabelle, in der Datensätze ausgewählt werden. Dabei kann es es sich um eine oder mehrere Tabellen sowie eine Abfrage handeln.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Sie können make-table-Abfragen zur Archivierung von Datensätzen, Sicherung Ihrer Tabellen, Anlage von Kopien zum Export in eine andere Datenbank oder als Grundlage für Berichte auf Basis der Daten aus einem bestimmten Zeitraum verwenden. Beispielsweise könnten Sie  mithilfe derselben make-table-Abfrage monatlich einen Bericht über die Verkäufe in diesem Monat nach Region erstellen.

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
