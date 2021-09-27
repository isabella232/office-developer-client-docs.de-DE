---
title: SQL-Ausdrücke (Access-Desktopdatenbankreferenz)
TOCTitle: SQL expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 06/13/2019
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 003462c4a16ca9a9de809f9dd87f661a0242992a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589099"
---
# <a name="sql-expressions"></a>SQL-Ausdrücke

**Gilt für**: Access 2013, Office 2013

Ein SQL-Ausdruck ist eine Zeichenfolge, aus der eine SQL-Anweisung ganz oder teilweise besteht. Die **FindFirst** -Methode eines **Recordset** -Objekts verwendet beispielsweise einen SQL-Ausdruck, der aus den Auswahlkriterien besteht, die in einer SQL- [WHERE-Klausel](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) gefunden wurden.

Das Microsoft Access-Datenbankmodul verwendet den VBA-Ausdrucksdienst (Microsoft Visual Basic for Applications) für einfache Arithmetik und Funktionsauswertungen. Alle in SQL-Ausdrücken des Microsoft Access-Datenbankmoduls verwendeten Operatoren (außer **[Between](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/between-and-operator)**, **[In](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)** und **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**) werden vom VBA-Ausdrucksdienst definiert. 

Darüber hinaus bietet der VBA-Ausdrucksdienst über 100 VBA-Funktionen, die Sie in SQL-Ausdrücken verwenden können. Beispielsweise können Sie diese VBA-Funktionen verwenden, um eine SQL-Abfrage im Microsoft Access-Abfrage-Designansicht zu erstellen, und Sie können diese Funktionen auch in einer SQL-Abfrage in der DAO- **OpenRecordset-** -Methode in Microsoft Visual C++, Microsoft Visual Basic und Microsoft Excel-Code verwenden.

## <a name="see-also"></a>Siehe auch

- [VBA-Konzepte in Access](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/concepts-access-vba-reference)
