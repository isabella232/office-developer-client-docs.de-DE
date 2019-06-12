---
title: Vergleich von Microsoft Access SQL und ANSI SQL
TOCTitle: Comparison of Microsoft Access SQL and ANSI SQL
ms:assetid: 0686f98f-10fe-0e02-e9d1-84ff3e755b57
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844937(v=office.15)
ms:contentKeyID: 48543052
ms.date: 06/13/2019
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4e9f30401891452970fdbe80123fc373e26f26c6
ms.sourcegitcommit: d0e1ce095a478d90411abb8c147eb9efe19ffa5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/12/2019
ms.locfileid: "34870857"
---
# <a name="comparison-of-microsoft-access-sql-and-ansi-sql"></a>Microsoft Access SQL und ANSI SQL im Vergleich

**Gilt für**: Access 2013, Office 2013

Das Microsoft Access-Datenbankmodul SQL ist im Allgemeinen mit ANSI-89 Level 1 kompatibel. Bestimmte ANSI SQL-Features werden jedoch nicht in Microsoft Access SQL implementiert. Umgekehrt umfasst Microsoft Access SQL reservierte Wörter und Features, die nicht in ANSI SQL unterstützt werden.

## <a name="major-differences"></a>Wesentliche Unterschiede

- Microsoft Access SQL und ANSI SQL verfügen über unterschiedliche reservierte Wörter und Datentypen. Weitere Informationen finden Sie unter [Reservierte Wörter für das Microsoft Access-Datenbankmodul SQL](sql-reserved-words.md) und [Gleichwertige ANSI SQL-Datentypen](equivalent-ansi-sql-data-types.md). Bei der Verwendung des OLE DB-Anbieters für das Microsoft Office 12.0 Access-Datenbankmodul sind zusätzliche reservierte Wörter vorhanden.

- **[Between…And](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/between-and-operator)**
    
  *expr1* \[Nicht\] **zwischen** *value1* **und** *value2*
    
  In Microsoft Access SQL kann *Wert1* größer sein als *Wert2*. In ANSI SQL dagegen muss *Wert1* kleiner oder gleich *Wert2* sein.

- Microsoft Access SQL unterstützt ANSI SQL-Platzhalterzeichen und [Platzhalterzeichen](using-wildcard-characters-in-string-comparisons.md), die speziell für das Microsoft Access-Datenbankmodul in Kombination mit dem **[Wie](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)** -Operator verwendet werden. Die Verwendung der ANSI-Platzhalterzeichen und der Platzhalterzeichen für das Microsoft Access-Datenbankmodul schließt sich gegenseitig aus. Sie können jeweils nur einen Satz Platzhalterzeichen verwenden, es ist nicht möglich, sie miteinander zu kombinieren. Die ANSI SQL-Platzhalter sind nur verfügbar, wenn das Microsoft Access-Datenbankmodul und der OLE DB-Anbieter für das Microsoft Office 12.0 Access-Datenbankmodul verwendet werden. Wenn Sie versuchen, die ANSI SQL-Platzhalter über Microsoft Access oder Datenzugriffsobjekte (DAO) zu verwenden, werden sie als Literale interpretiert. Umgekehrt verhält es sich, wenn Sie den OLE DB-Anbieter für das Microsoft Access-Datenbankmodul verwenden.
    
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

## <a name="enhanced-features-of-microsoft-access-sql"></a>Erweiterte Features von Microsoft Access SQL

Microsoft Access SQL stellt die folgenden erweiterten Features bereit:

- Die [TRANSFORM](transform-statement-microsoft-access-sql.md)-Anweisung, die Kreuztabellenabfragen unterstützt.

- Zusätzliche [Aggregatfunktionen](sql-aggregate-functions-sql.md) wie **StDev** und **VarP**.

- Die [PARAMETERS](parameters-declaration-microsoft-access-sql.md)-Deklaration zum Definieren von Parameterabfragen.

## <a name="ansi-sql-features-not-supported-in-microsoft-access-sql"></a>ANSI SQL-Features werden in Microsoft Access SQL nicht unterstützt

Microsoft Access SQL unterstützt folgende ANSI SQL-Features nicht:

- Verweise auf die DISTINCT-Aggregatfunktion. Microsoft Access SQL lässt beispielsweise die Syntax SUM(DISTINCT *Spaltenname*) nicht zu.

- Die LIMIT TO *nn* ROWS-Klausel zur Einschränkung der Zeilenanzahl, die von einer Abfrage zurückgegebenen wird. Es kann nur die [WHERE-Klausel](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) verwendet werden, um den Bereich einer Abfrage einzuschränken.

