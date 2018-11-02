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
ms.openlocfilehash: 0eca4738d07c54b049073aaf5d4b802864761fa5
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920599"
---
# <a name="with-owneraccess-option-declaration-microsoft-access-sql"></a><span data-ttu-id="b9740-102">MIT OWNERACCESS OPTION-Deklaration (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="b9740-102">WITH OWNERACCESS OPTION declaration (Microsoft Access SQL)</span></span>


<span data-ttu-id="b9740-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b9740-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b9740-104">In einer Mehrbenutzerumgebung mit einer sicheren Arbeitsgruppe wird diese Deklaration mit einer Abfrage verwendet, um dem Benutzer, der die Abfrage ausführt, dieselben Berechtigungen zuzuweisen wie dem Besitzer der Abfrage.</span><span class="sxs-lookup"><span data-stu-id="b9740-104">In a multiuser environment with a secure workgroup, use this declaration with a query to give the user who runs the query the same permissions as the query's owner.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9740-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9740-105">Syntax</span></span>

<span data-ttu-id="b9740-106">*SQL-Anweisung* MIT OWNERACCESS OPTION</span><span class="sxs-lookup"><span data-stu-id="b9740-106">*sqlstatement* WITH OWNERACCESS OPTION</span></span>

## <a name="remarks"></a><span data-ttu-id="b9740-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b9740-107">Remarks</span></span>

<span data-ttu-id="b9740-108">Die WITH OWNERACCESS OPTION-Deklaration ist optional.</span><span class="sxs-lookup"><span data-stu-id="b9740-108">The WITH OWNERACCESS OPTION declaration is optional.</span></span>

<span data-ttu-id="b9740-109">Im folgenden Beispiel kann der Benutzer Gehaltsdaten anzeigen (selbst wenn der Benutzer normalerweise nicht über die Berechtigungen zum Anzeigen der Tabelle mit den Gehältern verfügt). Dies ist jedoch nur möglich, wenn der Besitzer der Abfrage über die entsprechende Berechtigung verfügt:</span><span class="sxs-lookup"><span data-stu-id="b9740-109">The following example enables the user to view salary information (even if the user does not otherwise have permission to view the Payroll table), provided that the query's owner does have that permission:</span></span>

``` sql
SELECT LastName, 
FirstName, Salary
FROM Employees 
ORDER BY LastName 
WITH OWNERACCESS OPTION;
```

<span data-ttu-id="b9740-110">Wenn ein Benutzer aus anderen Gründen keine Tabelle erstellen kann oder einer Tabelle keine Daten hinzufügen kann, können Sie WITH OWNERACCESS OPTION verwenden, damit der Benutzer eine Tabellenerstellungs- oder Anfügeabfrage ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="b9740-110">If a user is otherwise prevented from creating or adding to a table, you can use WITH OWNERACCESS OPTION to enable the user to run a make-table or append query.</span></span>

<span data-ttu-id="b9740-111">Wenn Sie die Sicherheitseinstellungen und Benutzerberechtigungen der Arbeitsgruppe durchsetzen möchten, sollten Sie die WITH OWNERACCESS OPTION-Deklaration nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="b9740-111">If you want to enforce workgroup security settings and users' permissions, do not include the WITH OWNERACCESS OPTION declaration.</span></span>

<span data-ttu-id="b9740-p101">Diese Option erfordert, dass Sie auf die mit der Datenbank verknüpfte Datei System.mdw zugreifen können. Dies ist nur in einer sicheren Mehrbenutzerimplementation sinnvoll.</span><span class="sxs-lookup"><span data-stu-id="b9740-p101">This option requires you to have access to the System.mdw file associated with the database. It is useful only in secured multiuser implementations.</span></span>

