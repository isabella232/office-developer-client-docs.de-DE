---
title: SQL-Ausdrücke (Access PC-Datenbank-Referenz)
TOCTitle: SQL Expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 328804dc8186c082cf22d409b4071368af8873e2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472665"
---
# <a name="sql-expressions"></a>SQL-Ausdrücke


**Betrifft**: Access 2013 | Office 2013

Ein SQL-Ausdruck ist eine Zeichenfolge, aus der eine SQL-Anweisung ganz oder teilweise besteht. Die **FindFirst**-Methode eines **Recordset**-Objekts verwendet beispielsweise einen SQL-Ausdruck, der aus den Auswahlkriterien besteht, die in einer SQL-[WHERE-Klausel](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) gefunden wurden.

Das Microsoft Access-Datenbankmodul verwendet den VBA-Ausdrucksdienst (Microsoft® Visual Basic® für Applikationen), um einfache arithmetische Berechnungen und Funktionsauswertungen durchzuführen. Alle Operatoren, die in Ausdrücken für das Microsoft Access-Datenbankmodul SQL (mit Ausnahme der Operatoren **[Zwischen](https://msdn.microsoft.com/library/ff192436\(v=office.15\))**, **[In](https://msdn.microsoft.com/library/ff836369\(v=office.15\))** und **[Wie](https://msdn.microsoft.com/library/ff195752\(v=office.15\))**) verwendet werden, werden von dem VBA-Ausdrucksdienst definiert. Zusätzlich bietet der VBA-Ausdrucksdienst über 100 VBA-Funktionen, die in SQL-Ausdrücken verwendet werden können. Sie können mit diesen VBA-Funktionen zum Beispiel eine SQL-Abfrage innerhalb der Entwurfsansicht für Microsoft Access-Abfragen zusammenstellen. Darüber hinaus können Sie diese Funktionen in einer SQL-Abfrage innerhalb der **OpenRecordset**-Methode für Datenzugriffsobjekte (DAO) in Microsoft Visual C++®-, Microsoft Visual Basic- und Microsoft Excel-Code verwenden.

