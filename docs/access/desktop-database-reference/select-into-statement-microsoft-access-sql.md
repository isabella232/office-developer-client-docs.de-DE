---
title: SELECT.INTO-Anweisung (Microsoft Access SQL)
TOCTitle: SELECT.INTO Statement (Microsoft Access SQL)
ms:assetid: 29f3bd55-52f5-a36e-4e33-4b3499c6ce8d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192059(v=office.15)
ms:contentKeyID: 48543897
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4122421642b9746b5832984bf784faf65c603fda
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473216"
---
# <a name="selectinto-statement-microsoft-access-sql"></a>SELECT.INTO-Anweisung (Microsoft Access SQL)


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
<td><p>Der Pfad zu einer externen Datenbank. Eine Beschreibung des Pfads finden Sie unter der <a href="https://msdn.microsoft.com/library/ff194542(v=office.15)">IN</a>-Klausel.  </p></td>
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
> <UL>
> <LI>
> <P>Möglicherweise sollten Sie einen Primärschlüssel für die neue Tabelle festlegen. Bei der Erstellung der Tabelle werden die Datentypen und Feldgrößen aller Felder der der Abfrage zugrunde liegenden Tabellen an die Felder der neuen Tabelle vererbt. Es werden jedoch keine weiteren Feld- oder Tabelleneigenschaften übertragen.</P>
> <LI>
> <P>Um einer bereits bestehenden Tabelle Daten hinzuzufügen, verwenden Sie die <A href="insert-into-statement-microsoft-access-sql.md">INSERT INTO</A>-Anweisung anstelle einer Anfügeabfrage.</P>
> <LI>
> <P>Um herauszufinden, welche Datensätze ausgewählt werden, bevor Sie die make-table-Abfrage ausführen, führen Sie erst einmal eine <A href="select-statement-microsoft-access-sql.md">SELECT</A>-Anweisung mit denselben Auswahlkriterien aus.</P></LI></UL>



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
