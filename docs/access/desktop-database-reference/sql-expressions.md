---
title: SQL-Ausdrücke (Access PC-Datenbank-Referenz)
TOCTitle: SQL expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5a8d340f008fd198068d6dacc1b2bf847838ede1
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025735"
---
# <a name="sql-expressions"></a>SQL-Ausdrücke

**Betrifft**: Access 2013, Office 2013

Ein SQL-Ausdruck ist eine Zeichenfolge, aus der eine SQL-Anweisung ganz oder teilweise besteht. Die **FindFirst** -Methode eines **Recordset** -Objekts verwendet beispielsweise einen SQL-Ausdruck, der aus den Auswahlkriterien besteht, die in einer SQL- [WHERE-Klausel](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) gefunden wurden.

Microsoft Access-Datenbankmodul verwendet die Microsoft Visual Basic für Applikationen (oder VBA) Ausdruck Service einfache arithmetische und Funktion Bewertung durchführen. Alle Operatoren, die in Microsoft Access-Datenbank-Engine-SQL-Ausdrücke (mit Ausnahme von **[ **[zwischen](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/and-operator)**, und **[wie](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**)](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)** verwendet werden durch den VBA-Ausdrucks-Editor definiert. Darüber hinaus bietet der VBA-Ausdrucks-Editor über 100 VBA-Funktionen, die Sie in SQL-Ausdrücken verwenden können. Angenommen, Sie können diese VBA-Funktionen verwenden, um eine SQL-Abfrage in der Entwurfsansicht des Microsoft Access-Abfrage zum Verfassen und außerdem können diese Funktionen in einer SQL-Abfrage in der DAO- **OpenRecordset** -Methode in Microsoft Visual C++, Microsoft Visual Basic und Microsoft Excel-Code.

## <a name="see-also"></a>Siehe auch

- [Access VBA Konzepte](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/concepts-access-vba-reference)