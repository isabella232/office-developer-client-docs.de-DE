---
title: CREATE INDEX-Anweisung (Microsoft Access SQL)
TOCTitle: CREATE INDEX Statement (Microsoft Access SQL)
ms:assetid: c5919ef4-a08d-df06-7078-5331adbcb45c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823109(v=office.15)
ms:contentKeyID: 48547612
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277562
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ab501348d19ad8577bf1a55a3f37c6c3923381b1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473035"
---
# <a name="create-index-statement-microsoft-access-sql"></a>CREATE INDEX-Anweisung (Microsoft Access SQL)

**Betrifft**: Access 2013 | Office 2013

Erstellt einen neuen Index für eine vorhandene Tabelle.

> [!NOTE]
> Für Datenbanken, die nicht aus dem Microsoft Access-Datenbankmodul stammen, unterstützt das Microsoft Access-Datenbankmodul weder die CREATE INDEX-Anweisung (mit Ausnahme zur Erstellung eines Pseudoindexes für eine verknüpfte ODBC-Tabelle) noch eine der übrigen DDL-Anweisungen (Data Definition Language). Verwenden Sie stattdessen die Create-Methoden für Datenzugriffsobjekte (DAO). Weitere Informationen finden Sie im Abschnitt mit den Hinweisen.

## <a name="syntax"></a>Syntax

Erstellen von \[ UNIQUE \] INDEX *Index* ON *Tabelle* (*Feld* \[ASC | DESC\]\[, *Feld* \[ASC | DESC\],... \]) \[WITH {PRIMARY | DISALLOW NULL | IGNORE NULL}\]

Die CREATE INDEX-Anweisung besteht aus folgenden Komponenten:

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
<td><p><em>Index</em></p></td>
<td><p>Der Name des zu erstellenden Indexes.</p></td>
</tr>
<tr class="even">
<td><p><em>Tabelle</em></p></td>
<td><p>Der Name der vorhandenen Tabelle, in der der Index enthalten sein wird.</p></td>
</tr>
<tr class="odd">
<td><p><em>Feld</em></p></td>
<td><p>Der Name des oder der zu indizierenden Felder. Setzen Sie den Feldnamen in Klammern, und listen Sie ihn im Anschluss an den Tabellennamen auf, um einen Index mit einem Feld zu erstellen. Wenn Sie einen Index mit mehreren Feldern erstellen möchten, listen Sie jedes Feld auf, dass im Index eingeschlossen werden soll. Verwenden Sie das reservierte Wort DESC, um Indizes in absteigender Reihenfolge zu erstellen. Andernfalls wird davon ausgegangen, dass die Indizes in aufsteigender Reihenfolge erstellt werden sollen.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Um im indizierten Feld bzw. in den indizierten Feldern keine duplizierten Werte zuzulassen, verwenden Sie das reservierte Wort UNIQUE.

In der optionalen WITH-Klausel können Sie Gültigkeitsprüfungsregeln für Daten erzwingen. Es bestehen folgende Möglichkeiten:

- Unter Verwendung der DISALLOW NULL-Option Einträge vom Typ Null in dem oder den indizierten Feldern neuer Datensätze nicht zulassen.

- Datensätze mit **Null** -Werten in dem oder den indizierten Feldern unter Verwendung der IGNORE NULL-Option vom Index ausschließen.

- Das oder die indizierten Felder unter Verwendung des reservierten Worts PRIMARY als Primärschlüssel bestimmen. Dies setzt voraus, dass der Schlüssel eindeutig ist, sodass das reservierte Wort UNIQUE ausgelassen werden kann.

Sie können die CREATE INDEX-Anweisung verwenden, um einen Pseudoindex für eine verknüpfte Tabelle in einer ODBC-Datenquelle, zum Beispiel Microsoft® SQL Server, zu erstellen, wenn die Datenquelle bereits über einen Index verfügt. Sie benötigen zum Erstellen des Pseudoindexes keine Berechtigung für bzw. keinen Zugriff auf den Remoteserver. Der Pseudoindex wird von der Remotedatenbank ignoriert und hat keine Auswirkung auf die Remotedatenbank. Sie können für verknüpfte und systemeigene Tabellen die gleiche Syntax verwenden. Die Erstellung eines Pseudoindexes kann besonders hilfreich für Tabellen sein, die normalerweise schreibgeschützt sind.

Sie können auch die [ALTER TABLE](alter-table-statement-microsoft-access-sql.md)-Anweisung verwenden, um einen Index mit einem oder mehreren Feldern zu einer Tabelle hinzuzufügen, und Sie können die ALTER TABLE-Anweisung oder die [DROP](drop-statement-microsoft-access-sql.md)-Anweisung verwenden, um einen Index zu entfernen, der über die ALTER TABLE- oder CREATE INDEX-Anweisung erstellt wurde.

> [!NOTE]
> [!HINWEIS] Verwenden Sie nicht das reservierte Wort PRIMARY, wenn Sie einen neuen Index für eine Tabelle erstellen, die bereits über einen Primärschlüssel verfügt. Andernfalls wird in diesem Fall ein Fehler generiert.

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird ein Index erstellt, der aus dem Home Phone-Feld (Telefon privat) und dem Extension-Feld (Durchwahl) in der Employees-Tabelle (Personal) besteht.

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

Im folgenden Beispiel wird ein Index für die Customers-Tabelle (Kunden) unter Verwendung des CustomerID-Felds (Kunden-Nr) erstellt. Für das CustomerID-Feld sind keine duplizierten Datensätze zulässig, und darüber hinaus sind keine Nullwerte zulässig.



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
