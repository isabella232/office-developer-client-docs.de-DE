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
# <a name="sql-expressions"></a><span data-ttu-id="8d033-102">SQL-Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="8d033-102">SQL Expressions</span></span>


<span data-ttu-id="8d033-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8d033-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8d033-p101">Ein SQL-Ausdruck ist eine Zeichenfolge, aus der eine SQL-Anweisung ganz oder teilweise besteht. Die **FindFirst**-Methode eines **Recordset**-Objekts verwendet beispielsweise einen SQL-Ausdruck, der aus den Auswahlkriterien besteht, die in einer SQL-[WHERE-Klausel](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="8d033-p101">An SQL expression is a string that makes up all or part of an SQL statement. For example, the**FindFirst** method on a **Recordset** object uses an SQL expression consisting of the selection criteria found in an SQL [WHERE clause](https://msdn.microsoft.com/library/ff195245\(v=office.15\)).</span></span>

<span data-ttu-id="8d033-p102">Das Microsoft Access-Datenbankmodul verwendet den VBA-Ausdrucksdienst (Microsoft® Visual Basic® für Applikationen), um einfache arithmetische Berechnungen und Funktionsauswertungen durchzuführen. Alle Operatoren, die in Ausdrücken für das Microsoft Access-Datenbankmodul SQL (mit Ausnahme der Operatoren **[Zwischen](https://msdn.microsoft.com/library/ff192436\(v=office.15\))**, **[In](https://msdn.microsoft.com/library/ff836369\(v=office.15\))** und **[Wie](https://msdn.microsoft.com/library/ff195752\(v=office.15\))**) verwendet werden, werden von dem VBA-Ausdrucksdienst definiert. Zusätzlich bietet der VBA-Ausdrucksdienst über 100 VBA-Funktionen, die in SQL-Ausdrücken verwendet werden können. Sie können mit diesen VBA-Funktionen zum Beispiel eine SQL-Abfrage innerhalb der Entwurfsansicht für Microsoft Access-Abfragen zusammenstellen. Darüber hinaus können Sie diese Funktionen in einer SQL-Abfrage innerhalb der **OpenRecordset**-Methode für Datenzugriffsobjekte (DAO) in Microsoft Visual C++®-, Microsoft Visual Basic- und Microsoft Excel-Code verwenden.</span><span class="sxs-lookup"><span data-stu-id="8d033-p102">The Microsoft Access database engine uses the Microsoft® Visual Basic® for Applications (or VBA) expression service to perform simple arithmetic and function evaluation. All of the operators used in Microsoft Access database engine SQL expressions (except **[Between](https://msdn.microsoft.com/library/ff192436\(v=office.15\))**, **[In](https://msdn.microsoft.com/library/ff836369\(v=office.15\))**, and **[Like](https://msdn.microsoft.com/library/ff195752\(v=office.15\))**) are defined by the VBA expression service. In addition, the VBA expression service offers over 100 VBA functions that you can use in SQL expressions. For example, you can use these VBA functions to compose an SQL query in the Microsoft Access query Design view, and you can also use these functions in an SQL query in the DAO **OpenRecordset** method in Microsoft Visual C++®, Microsoft Visual Basic, and Microsoft Excel code.</span></span>

