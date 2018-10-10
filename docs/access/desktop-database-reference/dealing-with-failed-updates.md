---
title: Umgehen mit fehlgeschlagenen Aktualisierungen
TOCTitle: Dealing with Failed Updates
ms:assetid: f6f4914d-59b3-f3f2-b986-218e07ce5a1d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250258(v=office.15)
ms:contentKeyID: 48548752
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6d3af3026052954ec74b10026e0cf288a6aa5249
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473032"
---
# <a name="dealing-with-failed-updates"></a><span data-ttu-id="ef044-102">Umgehen mit fehlgeschlagenen Aktualisierungen</span><span class="sxs-lookup"><span data-stu-id="ef044-102">Dealing with Failed Updates</span></span>


<span data-ttu-id="ef044-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ef044-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="dealing-with-failed-updates"></a><span data-ttu-id="ef044-104">Umgehen mit fehlgeschlagenen Aktualisierungen</span><span class="sxs-lookup"><span data-stu-id="ef044-104">Dealing with Failed Updates</span></span>

<span data-ttu-id="ef044-p101">Wenn eine Aktualisierung mit Fehlern endet, hängt es von der Art und dem Schweregrad der Fehler sowie der Logik Ihrer Anwendung ab, wie Sie die Fehler lösen. Wenn jedoch die Datenbank gemeinsam mit anderen Benutzern verwendet wird, gibt es den typischen Fehler, dass ein anderer Benutzer ein Feld vor Ihnen ändert. Diese Art von Fehler wird als *Konflikt* bezeichnet. ADO erkennt diese Situation und meldet einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="ef044-p101">When an update concludes with errors, how you resolve the errors depends on the nature and severity of the errors and the logic of your application. However, if the database is shared with other users, a typical error is that someone else modifies the field before you do. This type of error is called a *conflict.* ADO detects this situation and reports an error.</span></span>

<span data-ttu-id="ef044-109">Wenn Aktualisierungsfehler auftreten, werden sie in einer Fehlerbehandlungsroutine abgefangen.</span><span class="sxs-lookup"><span data-stu-id="ef044-109">If there are update errors, they will be trapped in an error-handling routine.</span></span> <span data-ttu-id="ef044-110">Filtern Sie das **Recordset** -Objekt mit der **adFilterConflictingRecords** -Konstante, damit nur die miteinander in Konflikt stehenden Zeilen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ef044-110">Filter the **Recordset** with the **adFilterConflictingRecords** constant so that only the conflicting rows are visible.</span></span> <span data-ttu-id="ef044-111">In diesem Beispiel wird die Fehlerbehebung Strategie besteht lediglich Autor Drucken der vor- und Nachnamen (**au\_Fname** und **au\_Lname**).</span><span class="sxs-lookup"><span data-stu-id="ef044-111">In this example, the error-resolution strategy is merely to print the author's first and last names (**au\_fname** and **au\_lname**).</span></span>

<span data-ttu-id="ef044-112">Der Code, um den Benutzer auf den Aktualisierungskonflikt aufmerksam zu machen, sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="ef044-112">The code to alert the user to the update conflict looks like this:</span></span>

```vb 
 
objRs.Filter = adFilterConflictingRecords 
objRs.MoveFirst 
Do While Not objRst.EOF 
   Debug.Print "Conflict: Name =  "; objRs!au_fname; " "; objRs!au_lname 
   objRs.MoveNext 
Loop 
```

