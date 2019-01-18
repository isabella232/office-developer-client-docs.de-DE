---
title: MIT OWNERACCESS OPTION-Deklaration (Microsoft Access SQL)
TOCTitle: WITH OWNERACCESS OPTION declaration (Microsoft Access SQL)
ms:assetid: 82e51071-12b2-e97e-07b4-27ffceda831e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196724(v=office.15)
ms:contentKeyID: 48545993
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277584
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0882f143f13f6bd6d66c894f242a9cd50ebf9489
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718868"
---
# <a name="with-owneraccess-option-declaration-microsoft-access-sql"></a><span data-ttu-id="ae5be-102">MIT OWNERACCESS OPTION-Deklaration (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="ae5be-102">WITH OWNERACCESS OPTION declaration (Microsoft Access SQL)</span></span>


<span data-ttu-id="ae5be-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ae5be-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ae5be-104">In einer Mehrbenutzerumgebung mit einer sicheren Arbeitsgruppe wird diese Deklaration mit einer Abfrage verwendet, um dem Benutzer, der die Abfrage ausführt, dieselben Berechtigungen zuzuweisen wie dem Besitzer der Abfrage.</span><span class="sxs-lookup"><span data-stu-id="ae5be-104">In a multiuser environment with a secure workgroup, use this declaration with a query to give the user who runs the query the same permissions as the query's owner.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae5be-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae5be-105">Syntax</span></span>

<span data-ttu-id="ae5be-106">*SQL-Anweisung* MIT OWNERACCESS OPTION</span><span class="sxs-lookup"><span data-stu-id="ae5be-106">*sqlstatement* WITH OWNERACCESS OPTION</span></span>

## <a name="remarks"></a><span data-ttu-id="ae5be-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ae5be-107">Remarks</span></span>

<span data-ttu-id="ae5be-108">Die WITH OWNERACCESS OPTION-Deklaration ist optional.</span><span class="sxs-lookup"><span data-stu-id="ae5be-108">The WITH OWNERACCESS OPTION declaration is optional.</span></span>

<span data-ttu-id="ae5be-109">Im folgenden Beispiel kann der Benutzer Gehaltsdaten anzeigen (selbst wenn der Benutzer normalerweise nicht über die Berechtigungen zum Anzeigen der Tabelle mit den Gehältern verfügt). Dies ist jedoch nur möglich, wenn der Besitzer der Abfrage über die entsprechende Berechtigung verfügt:</span><span class="sxs-lookup"><span data-stu-id="ae5be-109">The following example enables the user to view salary information (even if the user does not otherwise have permission to view the Payroll table), provided that the query's owner does have that permission:</span></span>

``` sql
SELECT LastName, 
FirstName, Salary
FROM Employees 
ORDER BY LastName 
WITH OWNERACCESS OPTION;
```

<span data-ttu-id="ae5be-110">Wenn ein Benutzer aus anderen Gründen keine Tabelle erstellen kann oder einer Tabelle keine Daten hinzufügen kann, können Sie WITH OWNERACCESS OPTION verwenden, damit der Benutzer eine Tabellenerstellungs- oder Anfügeabfrage ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="ae5be-110">If a user is otherwise prevented from creating or adding to a table, you can use WITH OWNERACCESS OPTION to enable the user to run a make-table or append query.</span></span>

<span data-ttu-id="ae5be-111">Wenn Sie die Sicherheitseinstellungen und Benutzerberechtigungen der Arbeitsgruppe durchsetzen möchten, sollten Sie die WITH OWNERACCESS OPTION-Deklaration nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="ae5be-111">If you want to enforce workgroup security settings and users' permissions, do not include the WITH OWNERACCESS OPTION declaration.</span></span>

<span data-ttu-id="ae5be-p101">Diese Option erfordert, dass Sie auf die mit der Datenbank verknüpfte Datei System.mdw zugreifen können. Dies ist nur in einer sicheren Mehrbenutzerimplementation sinnvoll.</span><span class="sxs-lookup"><span data-stu-id="ae5be-p101">This option requires you to have access to the System.mdw file associated with the database. It is useful only in secured multiuser implementations.</span></span>

