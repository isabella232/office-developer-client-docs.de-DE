---
title: SQL-Ausdrücke (Access PC-Datenbank-Referenz)
TOCTitle: SQL expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 25b7d11430b730b6cedd1d8a084acd4984c5f292
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944150"
---
# <a name="sql-expressions"></a>SQL-Ausdrücke


**Betrifft**: Access 2013, Office 2013

Ein SQL-Ausdruck ist eine Zeichenfolge, aus der eine SQL-Anweisung ganz oder teilweise besteht. Die **FindFirst**-Methode eines **Recordset**-Objekts verwendet beispielsweise einen SQL-Ausdruck, der aus den Auswahlkriterien besteht, die in einer SQL-[WHERE-Klausel](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) gefunden wurden.

Microsoft Access-Datenbankmodul verwendet die Microsoft Visual Basic für Applikationen (oder VBA) Ausdruck Service einfache arithmetische und Funktion Bewertung durchführen. Alle Operatoren, die in Microsoft Access-Datenbank-Engine-SQL-Ausdrücke (mit Ausnahme von **[ **[zwischen](https://msdn.microsoft.com/library/ff192436\(v=office.15\))**, und **[wie](https://msdn.microsoft.com/library/ff195752\(v=office.15\))**)](https://msdn.microsoft.com/library/ff836369\(v=office.15\))** verwendet werden durch den VBA-Ausdrucks-Editor definiert. Darüber hinaus bietet der VBA-Ausdrucks-Editor über 100 VBA-Funktionen, die Sie in SQL-Ausdrücken verwenden können. Angenommen, Sie können diese VBA-Funktionen verwenden, um eine SQL-Abfrage in der Entwurfsansicht des Microsoft Access-Abfrage zum Verfassen und außerdem können diese Funktionen in einer SQL-Abfrage in der DAO- **OpenRecordset** -Methode in Microsoft Visual C++, Microsoft Visual Basic und Microsoft Excel-Code.

