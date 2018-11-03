---
title: Vergleich von Microsoft Access SQL und ANSI SQL
TOCTitle: Comparison of Microsoft Access SQL and ANSI SQL
ms:assetid: 0686f98f-10fe-0e02-e9d1-84ff3e755b57
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844937(v=office.15)
ms:contentKeyID: 48543052
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cd5350248c33b344695a02020b4b91bdbb1bb984
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937176"
---
# <a name="comparison-of-microsoft-access-sql-and-ansi-sql"></a>Vergleich von Microsoft Access SQL und ANSI SQL


**Betrifft**: Access 2013, Office 2013

Das Microsoft Access-Datenbankmodul SQL ist im Allgemeinen mit ANSI-89 Level 1 kompatibel. Bestimmte ANSI SQL-Features sind jedoch nicht in Microsoft Access SQL implementiert. Umgekehrt umfasst Microsoft Access SQL reservierte Wörter und Features, die nicht in ANSI SQL unterstützt werden.

## <a name="major-differences"></a>Hauptunterschiede

  - Microsoft Access SQL und ANSI SQL verfügen über unterschiedliche reservierte Wörter und Datentypen. Weitere Informationen finden Sie unter [Reservierte Wörter für das Microsoft Access-Datenbankmodul SQL](sql-reserved-words.md) und [Gleichwertige ANSI SQL-Datentypen](equivalent-ansi-sql-data-types.md). Bei der Verwendung des OLE DB-Anbieters für das Microsoft Office 12.0 Access-Datenbankmodul sind zusätzliche reservierte Wörter vorhanden.

  - **[Between…And](https://msdn.microsoft.com/library/ff192436\(v=office.15\))**
    
    *expr1* \[Nicht\] **zwischen** *Wert1* **und** *Wert2*
    
    In Microsoft Access SQL kann *Wert1* größer sein als *Wert2*. In ANSI SQL dagegen muss *Wert1* kleiner oder gleich *Wert2* sein.

  - Microsoft Access SQL unterstützt ANSI SQL-Platzhalterzeichen und [Platzhalterzeichen](using-wildcard-characters-in-string-comparisons.md), die speziell für das Microsoft Access-Datenbankmodul in Kombination mit dem **[Wie](https://msdn.microsoft.com/library/ff195752\(v=office.15\))** -Operator verwendet werden. Die Verwendung der ANSI-Platzhalterzeichen und der Platzhalterzeichen für das Microsoft Access-Datenbankmodul schließt sich gegenseitig aus. Sie können jeweils nur einen Satz Platzhalterzeichen verwenden, es ist nicht möglich, sie miteinander zu kombinieren. Die ANSI SQL-Platzhalter sind nur verfügbar, wenn das Microsoft Access-Datenbankmodul und der OLE DB-Anbieter für das Microsoft Office 12.0 Access-Datenbankmodul verwendet werden. Wenn Sie versuchen, die ANSI SQL-Platzhalter über Microsoft Access oder Datenzugriffsobjekte (DAO) zu verwenden, werden sie als Literale interpretiert. Umgekehrt verhält es sich, wenn Sie den OLE DB-Anbieter für das Microsoft Access-Datenbankmodul verwenden.
    
    <table>
    <colgroup>
    <col style="width: 33%" />
    <col style="width: 33%" />
    <col style="width: 33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p>Übereinstimmendes Zeichen</p></th>
    <th><p>Microsoft Access SQL</p></th>
    <th><p>ANSI SQL</p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p>Ein beliebiges Zeichen</p></td>
    <td><p>?</p></td>
    <td><p>_ (Unterstrich)</p></td>
    </tr>
    <tr class="even">
    <td><p>Null oder mehrere Zeichen</p></td>
    <td><p>*</p></td>
    <td><p>%</p></td>
    </tr>
    </tbody>
    </table>


  - Microsoft Access SQL ist im Allgemeinen weniger einschränkend, so können Ausdrücke beispielsweise gruppiert und sortiert werden.

  - Microsoft Access SQL unterstützt leistungsstärkere Ausdrücke.

## <a name="enhanced-features-of-microsoft-access-sql"></a>Erweiterte Microsoft Access SQL-Features

Microsoft Access SQL stellt die folgenden erweiterten Features bereit:

  - Die [TRANSFORM](transform-statement-microsoft-access-sql.md)-Anweisung, die Kreuztabellenabfragen unterstützt.

  - Zusätzliche [Aggregatfunktionen](sql-aggregate-functions-sql.md) wie **StDev** und **VarP**.

  - Die [PARAMETERS](parameters-declaration-microsoft-access-sql.md)-Deklaration zum Definieren von Parameterabfragen.

## <a name="ansi-sql-features-not-supported-in-microsoft-access-sql"></a>ANSI SQL-Features ohne Unterstützung in Microsoft Access SQL

Microsoft Access SQL unterstützt folgende ANSI SQL-Features nicht:

  - Verweise auf die DISTINCT-Aggregatfunktion. Microsoft Access SQL lässt beispielsweise die Syntax SUM(DISTINCT *Spaltenname*) nicht zu.

  - Die LIMIT TO *Nn* ROWS-Klausel, zur Begrenzung der Anzahl von Zeilen, die von einer Abfrage zurückgegeben. Es kann nur die [WHERE-Klausel](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) verwendet werden, um den Bereich einer Abfrage einzuschränken.

