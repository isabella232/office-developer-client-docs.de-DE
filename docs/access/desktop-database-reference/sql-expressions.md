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
# <a name="sql-expressions"></a><span data-ttu-id="19c80-102">SQL-Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="19c80-102">SQL expressions</span></span>

<span data-ttu-id="19c80-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="19c80-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="19c80-p101">Ein SQL-Ausdruck ist eine Zeichenfolge, aus der eine SQL-Anweisung ganz oder teilweise besteht. Die **FindFirst** -Methode eines **Recordset** -Objekts verwendet beispielsweise einen SQL-Ausdruck, der aus den Auswahlkriterien besteht, die in einer SQL- [WHERE-Klausel](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="19c80-p101">An SQL expression is a string that makes up all or part of an SQL statement. For example, the **FindFirst** method on a **Recordset** object uses an SQL expression consisting of the selection criteria found in an SQL [WHERE clause](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql).</span></span>

<span data-ttu-id="19c80-106">Microsoft Access-Datenbankmodul verwendet die Microsoft Visual Basic für Applikationen (oder VBA) Ausdruck Service einfache arithmetische und Funktion Bewertung durchführen.</span><span class="sxs-lookup"><span data-stu-id="19c80-106">The Microsoft Access database engine uses the Microsoft Visual Basic for Applications (or VBA) expression service to perform simple arithmetic and function evaluation.</span></span> <span data-ttu-id="19c80-107">Alle Operatoren, die in Microsoft Access-Datenbank-Engine-SQL-Ausdrücke (mit Ausnahme von **[ **[zwischen](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/and-operator)**, und **[wie](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**)](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)** verwendet werden durch den VBA-Ausdrucks-Editor definiert.</span><span class="sxs-lookup"><span data-stu-id="19c80-107">All of the operators used in Microsoft Access database engine SQL expressions (except **[Between](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/and-operator)**, **[In](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)**, and **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**) are defined by the VBA expression service.</span></span> <span data-ttu-id="19c80-108">Darüber hinaus bietet der VBA-Ausdrucks-Editor über 100 VBA-Funktionen, die Sie in SQL-Ausdrücken verwenden können.</span><span class="sxs-lookup"><span data-stu-id="19c80-108">In addition, the VBA expression service offers over 100 VBA functions that you can use in SQL expressions.</span></span> <span data-ttu-id="19c80-109">Angenommen, Sie können diese VBA-Funktionen verwenden, um eine SQL-Abfrage in der Entwurfsansicht des Microsoft Access-Abfrage zum Verfassen und außerdem können diese Funktionen in einer SQL-Abfrage in der DAO- **OpenRecordset** -Methode in Microsoft Visual C++, Microsoft Visual Basic und Microsoft Excel-Code.</span><span class="sxs-lookup"><span data-stu-id="19c80-109">For example, you can use these VBA functions to compose an SQL query in the Microsoft Access query Design view, and you can also use these functions in an SQL query in the DAO **OpenRecordset** method in Microsoft Visual C++, Microsoft Visual Basic, and Microsoft Excel code.</span></span>

## <a name="see-also"></a><span data-ttu-id="19c80-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19c80-110">See also</span></span>

- [<span data-ttu-id="19c80-111">Access VBA Konzepte</span><span class="sxs-lookup"><span data-stu-id="19c80-111">Access VBA Concepts</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/concepts-access-vba-reference)