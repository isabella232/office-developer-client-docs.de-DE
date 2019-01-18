---
title: SQL-Ausdrücke (Access PC-Datenbank-Referenz)
TOCTitle: SQL expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 5bbe9718bfb18ced5f09d2a9396e1e0829d0d81b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710545"
---
# <a name="sql-expressions"></a><span data-ttu-id="219b9-102">SQL-Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="219b9-102">SQL expressions</span></span>

<span data-ttu-id="219b9-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="219b9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="219b9-p101">Ein SQL-Ausdruck ist eine Zeichenfolge, aus der eine SQL-Anweisung ganz oder teilweise besteht. Die **FindFirst** -Methode eines **Recordset** -Objekts verwendet beispielsweise einen SQL-Ausdruck, der aus den Auswahlkriterien besteht, die in einer SQL- [WHERE-Klausel](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="219b9-p101">An SQL expression is a string that makes up all or part of an SQL statement. For example, the **FindFirst** method on a **Recordset** object uses an SQL expression consisting of the selection criteria found in an SQL [WHERE clause](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql).</span></span>

<span data-ttu-id="219b9-106">Microsoft Access-Datenbankmodul verwendet die Microsoft Visual Basic für Applikationen (oder VBA) Ausdruck Service einfache arithmetische und Funktion Bewertung durchführen.</span><span class="sxs-lookup"><span data-stu-id="219b9-106">The Microsoft Access database engine uses the Microsoft Visual Basic for Applications (or VBA) expression service to perform simple arithmetic and function evaluation.</span></span> <span data-ttu-id="219b9-107">Alle Operatoren, die in Microsoft Access-Datenbank-Engine-SQL-Ausdrücke (mit Ausnahme von **[ **[zwischen](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/and-operator)**, und **[wie](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**)](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)** verwendet werden durch den VBA-Ausdrucks-Editor definiert.</span><span class="sxs-lookup"><span data-stu-id="219b9-107">All of the operators used in Microsoft Access database engine SQL expressions (except **[Between](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/and-operator)**, **[In](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)**, and **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**) are defined by the VBA expression service.</span></span> <span data-ttu-id="219b9-108">Darüber hinaus bietet der VBA-Ausdrucks-Editor über 100 VBA-Funktionen, die Sie in SQL-Ausdrücken verwenden können.</span><span class="sxs-lookup"><span data-stu-id="219b9-108">In addition, the VBA expression service offers over 100 VBA functions that you can use in SQL expressions.</span></span> <span data-ttu-id="219b9-109">Angenommen, Sie können diese VBA-Funktionen verwenden, um eine SQL-Abfrage in der Entwurfsansicht des Microsoft Access-Abfrage zum Verfassen und außerdem können diese Funktionen in einer SQL-Abfrage in der DAO- **OpenRecordset** -Methode in Microsoft Visual C++, Microsoft Visual Basic und Microsoft Excel-Code.</span><span class="sxs-lookup"><span data-stu-id="219b9-109">For example, you can use these VBA functions to compose an SQL query in the Microsoft Access query Design view, and you can also use these functions in an SQL query in the DAO **OpenRecordset** method in Microsoft Visual C++, Microsoft Visual Basic, and Microsoft Excel code.</span></span>

## <a name="see-also"></a><span data-ttu-id="219b9-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="219b9-110">See also</span></span>

- [<span data-ttu-id="219b9-111">Access VBA Konzepte</span><span class="sxs-lookup"><span data-stu-id="219b9-111">Access VBA Concepts</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/concepts-access-vba-reference)
