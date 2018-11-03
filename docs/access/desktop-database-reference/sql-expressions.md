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
# <a name="sql-expressions"></a><span data-ttu-id="2aa90-102">SQL-Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="2aa90-102">SQL expressions</span></span>


<span data-ttu-id="2aa90-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2aa90-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2aa90-p101">Ein SQL-Ausdruck ist eine Zeichenfolge, aus der eine SQL-Anweisung ganz oder teilweise besteht. Die **FindFirst**-Methode eines **Recordset**-Objekts verwendet beispielsweise einen SQL-Ausdruck, der aus den Auswahlkriterien besteht, die in einer SQL-[WHERE-Klausel](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="2aa90-p101">An SQL expression is a string that makes up all or part of an SQL statement. For example, the**FindFirst** method on a **Recordset** object uses an SQL expression consisting of the selection criteria found in an SQL [WHERE clause](https://msdn.microsoft.com/library/ff195245\(v=office.15\)).</span></span>

<span data-ttu-id="2aa90-106">Microsoft Access-Datenbankmodul verwendet die Microsoft Visual Basic für Applikationen (oder VBA) Ausdruck Service einfache arithmetische und Funktion Bewertung durchführen.</span><span class="sxs-lookup"><span data-stu-id="2aa90-106">The Microsoft Access database engine uses the Microsoft Visual Basic for Applications (or VBA) expression service to perform simple arithmetic and function evaluation.</span></span> <span data-ttu-id="2aa90-107">Alle Operatoren, die in Microsoft Access-Datenbank-Engine-SQL-Ausdrücke (mit Ausnahme von **[ **[zwischen](https://msdn.microsoft.com/library/ff192436\(v=office.15\))**, und **[wie](https://msdn.microsoft.com/library/ff195752\(v=office.15\))**)](https://msdn.microsoft.com/library/ff836369\(v=office.15\))** verwendet werden durch den VBA-Ausdrucks-Editor definiert.</span><span class="sxs-lookup"><span data-stu-id="2aa90-107">All of the operators used in Microsoft Access database engine SQL expressions (except **[Between](https://msdn.microsoft.com/library/ff192436\(v=office.15\))**, **[In](https://msdn.microsoft.com/library/ff836369\(v=office.15\))**, and **[Like](https://msdn.microsoft.com/library/ff195752\(v=office.15\))**) are defined by the VBA expression service.</span></span> <span data-ttu-id="2aa90-108">Darüber hinaus bietet der VBA-Ausdrucks-Editor über 100 VBA-Funktionen, die Sie in SQL-Ausdrücken verwenden können.</span><span class="sxs-lookup"><span data-stu-id="2aa90-108">In addition, the VBA expression service offers over 100 VBA functions that you can use in SQL expressions.</span></span> <span data-ttu-id="2aa90-109">Angenommen, Sie können diese VBA-Funktionen verwenden, um eine SQL-Abfrage in der Entwurfsansicht des Microsoft Access-Abfrage zum Verfassen und außerdem können diese Funktionen in einer SQL-Abfrage in der DAO- **OpenRecordset** -Methode in Microsoft Visual C++, Microsoft Visual Basic und Microsoft Excel-Code.</span><span class="sxs-lookup"><span data-stu-id="2aa90-109">For example, you can use these VBA functions to compose an SQL query in the Microsoft Access query Design view, and you can also use these functions in an SQL query in the DAO **OpenRecordset** method in Microsoft Visual C++, Microsoft Visual Basic, and Microsoft Excel code.</span></span>

