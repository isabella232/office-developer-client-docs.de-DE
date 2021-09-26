---
title: INSERT INTO-Anweisung (Microsoft Access SQL)
TOCTitle: INSERT INTO statement (Microsoft Access SQL)
ms:assetid: d3e44258-79f2-caba-8629-bde03f898f2d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834799(v=office.15)
ms:contentKeyID: 48547918
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277575
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: 0a4c94e90e2c9efd29d0d07eae852ab2a2c009f2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568901"
---
# <a name="insert-into-statement-microsoft-access-sql"></a>INSERT INTO-Anweisung (Microsoft Access SQL)

**Gilt für**: Access 2013, Office 2013

Fügt einen Datensatz oder mehrere Datensätze einer Tabelle hinzu. Dies wird als Anfügeabfrage bezeichnet.

## <a name="syntax"></a>Syntax

### <a name="multiple-record-append-query"></a>Anfügeabfrage mit mehreren Datensätzen

INSERT INTO *target* \[(*field1*\[, *field2*\[, …\]\])\] \[IN *externaldatabase*\] SELECT \[*source*.\]*field1*\[, *field2*\[, …\] FROM *tableexpression*

### <a name="single-record-append-query"></a>Anfügeabfrage mit einem Datensatz

INSERT INTO *target* \[(*field1*\[, *field2*\[, …\]\])\] VALUES (*value1*\[, *value2*\[, …\])

Die INSERT INTO-Anweisung besteht aus folgenden Teilen:

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
<td><p><em>target</em></p></td>
<td><p>Der Name der Tabelle oder Abfrage, an die Datensätze angefügt werden sollen.</p></td>
</tr>
<tr class="even">
<td><p><em>Feld1</em>, <em>Feld2</em></p></td>
<td><p>Namen der Felder, an die Daten angehängt werden sollen, falls nach einem <em>target</em>-Argument, oder die Namen von Feldern, aus denen Daten abgerufen werden sollen, falls nach einem <em>source</em>-Argument.</p></td>
</tr>
<tr class="odd">
<td><p><em>externeDatenbank</em></p></td>
<td><p>Ich bin für diese Woche leider bereits ausgebucht. Eine Beschreibung des Pfads finden Sie unter der <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a>-Klausel.</p></td>
</tr>
<tr class="even">
<td><p><em>source</em></p></td>
<td><p>Der Name der Tabelle oder Abfrage, aus der Datensätze kopiert werden sollen.</p></td>
</tr>
<tr class="odd">
<td><p><em>Tabellenausdruck</em></p></td>
<td><p>Die Namen der Tabellen, aus denen Datensätze eingefügt werden. Dieses Argument kann ein einzelner Tabellenname oder eine Kombination aus den Vorgängen <a href="inner-join-operation-microsoft-access-sql.md">INNER JOIN</a>, <a href="left-join-right-join-operations-microsoft-access-sql.md">LEFT JOIN</a> oder <a href="left-join-right-join-operations-microsoft-access-sql.md">RIGHT JOIN</a> oder eine gespeicherte Abfrage sein.</p></td>
</tr>
<tr class="even">
<td><p><em>Wert1</em>, <em>Wert2</em></p></td>
<td><p>Die Werte, die in die entsprechenden Felder des neuen Datensatzes eingefügt werden sollen. Jeder Wert wird in das Feld eingefügt, das der Position des Werts in der Liste entspricht: <em>Wert1</em> wird in <em>Feld1</em> des neuen Datensatzes eingefügt, <em>Wert2</em> in <em>Feld2</em> usw. Sie müssen Werte durch Kommata trennen und Textfelder in einfache Anführungszeichen (' ') einschließen.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Sie können die INSERT INTO-Anweisung verwenden, um einen einzelnen Datensatz einer Tabelle mit der Syntax der Anfügeabfrage für einzelne Datensätze hinzuzufügen. In diesem Fall gibt der Code den Namen und Wert für jedes Feld des Datensatzes an. Sie müssen jedes Feld des Datensatzes angeben, dem ein Wert zugewiesen werden soll, sowie einen Wert für dieses Feld. Wenn Sie nicht alle Felder angeben, wird der Standardwert oder **Null** für fehlende Spalten eingefügt. Datensätze werden am Ende der Tabelle hinzugefügt.

Sie können auch INSERT INTO verwenden, um eine Gruppe von Datensätzen aus einer anderen Tabelle oder Abfrage mithilfe der SELECT … FROM-Klausel anzufügen, wie oben in der Syntax zur Anfügeabfrage für mehrere Datensätze gezeigt wird. In diesem Fall gibt die SELECT-Klausel die Felder an, die an die angegebene *target*-Tabelle angefügt werden sollen.

Die *source*- oder *target*-Tabelle kann eine Tabelle oder Abfrage angeben. Wenn eine Abfrage angegeben wird, fügt das Microsoft Access-Datenbankmodul Datensätze an alle in der Abfrage angegebenen Tabellen an.

INSERT INTO ist optional. Wenn es eingeschlossen wird, steht es aber vor der [SELECT](select-statement-microsoft-access-sql.md)-Anweisung.

Wenn die Zieltabelle einen Primärschlüssel enthält, stellen Sie sicher, dass Sie eindeutige Nicht-**Null**-Werte an das Primärschlüsselfeld bzw. die Primärschlüsselfelder anfügen. Andernfalls fügt das Microsoft Access-Datenbankmodul die Datensätze nicht an.

Wenn Sie Datensätze an eine Tabelle mit einem "AutoNumber"-Feld anfügen und die angefügten Datensätze neu nummerieren möchten, schließen Sie das Feld "AutoNumber" nicht in die Abfrage ein, Schließen Sie das Feld "AutoNumber" in die Abfrage ein, wenn Sie die ursprünglichen Werte aus dem Feld beibehalten möchten.

Verwenden Sie die IN-Klausel, um Datensätze an eine Tabelle in einer anderen Datenbank anzufügen.

Um eine neue Tabelle zu erstellen, verwenden Sie stattdessen die [SELECT… INTO](select-into-statement-microsoft-access-sql.md)-Anweisung, um eine Tabellenerstellungsabfrage zu erstellen.

Um herauszufinden, welche Datensätze angefügt werden, bevor Sie die Anfügeabfrage ausführen, müssen Sie zuerst eine Auswahlabfrage ausführen, die die gleichen Auswahlkriterien verwendet, und sich die Ergebnisse ansehen.

Eine Anfügeabfrage kopiert Datensätze aus einer oder mehreren Tabellen in eine andere. Die Tabellen mit den Datensätzen, die Sie anfügen, werden von der Anfügeabfrage nicht beeinflusst.

Anstatt vorhandene Datensätze aus einer anderen Tabelle anzufügen, können Sie den Wert für die einzelnen Felder in einem einzigen neuen Datensatz mit der VALUES-Klausel angeben. Wenn Sie die Feldliste auslassen, muss die VALUES-Klausel einen Wert für jedes Feld in der Tabelle enthalten. Andernfalls schlägt der INSERT-Vorgang fehl. Verwenden Sie eine zusätzliche INSERT INTO-Anweisung mit einer VALUES-Klausel für jeden zusätzlichen Datensatz, den Sie erstellen möchten.

**Links zur Verfügung gestellt von:** [UtterAccess](https://www.utteraccess.com)-Community. UtterAccess ist das führende Microsoft Access-Wiki und -Hilfeforum.

- [Generieren fortlaufender Nummern für INSERT/UPDATE-Anweisungen](https://www.utteraccess.com/forum/generating-sequential-num-t446039.html)

- [SQL-zu-VBA-Formatierungsprogramm](https://www.utteraccess.com/forum/sql-vba-formatter-t1165308.html)

## <a name="example"></a>Beispiel

Dieses Beispiel wählt alle Datensätze in einer hypothetischen Tabelle "New Customers" aus und fügt sie der Tabelle "Customers" hinzu. Wenn einzelne Spalten nicht angegeben werden, müssen die SELECT-Tabellenspaltennamen exakt mit denen in der INSERT INTO-Tabelle übereinstimmen.

```vb
    Sub InsertIntoX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Select all records in the New Customers table  
        ' and add them to the Customers table. 
        dbs.Execute " INSERT INTO Customers " _ 
            & "SELECT * " _ 
            & "FROM [New Customers];" 
             
        dbs.Close 
     
    End Sub
```

<br/>

Dieses Beispiel erstellt einen neuen Datensatz in der Tabelle "Employees".

```vb
    Sub InsertIntoX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Create a new record in the Employees table. The  
        ' first name is Harry, the last name is Washington,  
        ' and the job title is Trainee. 
        dbs.Execute " INSERT INTO Employees " _ 
            & "(FirstName,LastName, Title) VALUES " _ 
            & "('Harry', 'Washington', 'Trainee');" 
             
        dbs.Close 
     
    End Sub 
```

