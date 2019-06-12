---
title: SQL-Ausdrücke (Access-Desktopdatenbankreferenz)
TOCTitle: SQL expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 06/13/2019
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: f38932ed4744e5479c523446f9ab77065f4eb203
ms.sourcegitcommit: d0e1ce095a478d90411abb8c147eb9efe19ffa5f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/12/2019
ms.locfileid: "34870864"
---
# <a name="sql-expressions"></a><span data-ttu-id="d5a49-102">SQL-Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="d5a49-102">SQL expressions</span></span>

<span data-ttu-id="d5a49-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d5a49-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d5a49-p101">Ein SQL-Ausdruck ist eine Zeichenfolge, aus der eine SQL-Anweisung ganz oder teilweise besteht. Die **FindFirst** -Methode eines **Recordset** -Objekts verwendet beispielsweise einen SQL-Ausdruck, der aus den Auswahlkriterien besteht, die in einer SQL- [WHERE-Klausel](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="d5a49-p101">An SQL expression is a string that makes up all or part of an SQL statement. For example, the **FindFirst** method on a **Recordset** object uses an SQL expression consisting of the selection criteria found in an SQL [WHERE clause](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql).</span></span>

<span data-ttu-id="d5a49-106">Das Microsoft Access-Datenbankmodul verwendet den VBA-Ausdrucksdienst (Microsoft Visual Basic for Applications) für einfache Arithmetik und Funktionsauswertungen.</span><span class="sxs-lookup"><span data-stu-id="d5a49-106">The Microsoft Access database engine uses the Microsoft Visual Basic for Applications (or VBA) expression service to perform simple arithmetic and function evaluation.</span></span> <span data-ttu-id="d5a49-107">Alle in SQL-Ausdrücken des Microsoft Access-Datenbankmoduls verwendeten Operatoren (außer **[Between](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/between-and-operator)**, **[In](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)** und **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**) werden vom VBA-Ausdrucksdienst definiert.</span><span class="sxs-lookup"><span data-stu-id="d5a49-107">All of the operators used in Microsoft Access database engine SQL expressions (except **[Between](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/between-and-operator)**, **[In](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)**, and **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**) are defined by the VBA expression service.</span></span> 

<span data-ttu-id="d5a49-108">Darüber hinaus bietet der VBA-Ausdrucksdienst über 100 VBA-Funktionen, die Sie in SQL-Ausdrücken verwenden können.</span><span class="sxs-lookup"><span data-stu-id="d5a49-108">In addition, the VBA expression service offers over 100 VBA functions that you can use in SQL expressions.</span></span> <span data-ttu-id="d5a49-109">Beispielsweise können Sie diese VBA-Funktionen verwenden, um eine SQL-Abfrage in der Abfrageentwurfsansicht von Microsoft Access zu erstellen. Sie können diese Funktionen auch in einer SQL-Abfrage in der DAO-Methode **OpenRecordset** in Microsoft Visual C++-, Microsoft Visual Basic- und Microsoft Excel-Code verwenden.</span><span class="sxs-lookup"><span data-stu-id="d5a49-109">For example, you can use these VBA functions to compose an SQL query in the Microsoft Access query Design view, and you can also use these functions in an SQL query in the DAO **OpenRecordset** method in Microsoft Visual C++, Microsoft Visual Basic, and Microsoft Excel code.</span></span>

## <a name="see-also"></a><span data-ttu-id="d5a49-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5a49-110">See also</span></span>

- [<span data-ttu-id="d5a49-111">VBA-Konzepte in Access</span><span class="sxs-lookup"><span data-stu-id="d5a49-111">Access VBA Concepts</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/concepts-access-vba-reference)
