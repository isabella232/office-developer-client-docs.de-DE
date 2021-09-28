---
title: DELETE-Anweisung (Microsoft Access SQL)
TOCTitle: DELETE statement (Microsoft Access SQL)
ms:assetid: 64c235bc-5b1a-0a33-714a-9933ba7a81e5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195097(v=office.15)
ms:contentKeyID: 48545299
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277573
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: 5eba43d04f1d0eccf1b7e0ce63c6c6aedd3946d6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618245"
---
# <a name="delete-statement-microsoft-access-sql"></a>DELETE-Anweisung (Microsoft Access SQL)

**Gilt für**: Access 2013, Office 2013

Erstellt eine Löschabfrage, die Datensätze aus einer oder mehreren Tabellen in der [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql)-Klausel löscht, die die Kriterien der [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql)-Klausel erfüllen.

## <a name="syntax"></a>Syntax

DELETE \[*Tabelle*.\*\] FROM *Tabelle* WHERE *Kriterien*

Die DELETE-Anweisung setzt sich wie folgt zusammen:

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
<td><p>Der optionale Name der Tabelle, aus der Datensätze gelöscht werden.</p></td>
</tr>
<tr class="even">
<td><p><em>Tabelle</em></p></td>
<td><p>Der Name der Tabelle, aus der Datensätze gelöscht werden.</p></td>
</tr>
<tr class="odd">
<td><p><em>Kriterien</em></p></td>
<td><p>Ein Ausdruck, der bestimmt, welche Datensätze gelöscht werden sollen.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

DELETE ist besonders nützlich, wenn Sie viele Datensätze löschen möchten.

Wenn Sie eine Tabelle vollständig aus der Datenbank löschen möchten, können Sie die **Execute**-Methode mit einer [DROP](drop-statement-microsoft-access-sql.md)-Anweisung verwenden. Beim Löschen der Tabelle geht allerdings auch die Struktur verloren. Wenn Sie dagegen die DELETE-Anweisung verwenden, werden nur die Daten gelöscht, die Tabellenstruktur und alle Tabelleneigenschaften wie Feldattribute und Indizes bleiben erhalten.

Sie können die DELETE-Anweisung verwenden, um Datensätze aus Tabellen zu entfernen, die in einer 1:n-Beziehung mit anderen Tabellen stehen. Durch Löschweitergaben werden Datensätze in Tabellen, die sich auf der n-Seite der Beziehung befinden, gelöscht, wenn der entsprechende Datensatz auf der 1-Seite der Beziehung in der Abfrage gelöscht wird. In der Beziehung zwischen der Customers-Tabelle (Kunden) und der Orders-Tabelle (Bestellungen) stellt erstgenannte Tabelle die 1-Seite und letztgenannte Tabelle die n-Seite der Beziehung zwischen den Tabellen dar. Wird ein Datensatz aus der Customers-Tabelle gelöscht, werden die entsprechenden Datensätze auch aus der Orders-Tabelle gelöscht, wenn die Option für Löschweitergaben angegeben wurde.

Über eine Löschabfrage werden Datensätze vollständig gelöscht, nicht nur die Daten in spezifischen Feldern. Wenn Sie Daten aus einem spezifischen Feld löschen möchten, erstellen Sie eine Aktualisierungabfrage, die die Werte in diesen Feldern in den Wert **Null** ändert.

> [!IMPORTANT]
> - Nachdem Sie Datensätze über eine Löschabfrage entfernt haben, können Sie diesen Vorgang nicht rückgängig machen. Wenn Sie zunächst wissen möchten, welche Datensätze gelöscht werden, überprüfen Sie im Vorfeld die Ergebnisse einer Auswahlabfrage, die die gleichen Kriterien wie die Löschabfrage verwendet, und führen Sie dann erst die Löschabfrage aus.
> - Bewahren Sie jederzeit Sicherungskopien Ihrer Daten auf. Wenn Sie die falschen Datensätze gelöscht haben, können Sie sie aus Ihren Sicherungskopien wieder abrufen.

## <a name="example"></a>Beispiel

Im folgenden Beispiel werden alle Datensätze der Mitarbeiter gelöscht, die über die Position eines Trainees verfügen. Wenn die FROM-Klausel nur eine Tabelle einschließt, muss der Tabellenname nicht in der DELETE-Anweisung aufgelistet werden.



```vb
    Sub DeleteX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete employee records where title is Trainee.     
        dbs.Execute "DELETE * FROM " _ 
            & "Employees WHERE Title = 'Trainee';" 
         
        dbs.Close 
     
    End Sub
```
