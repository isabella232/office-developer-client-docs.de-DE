---
title: Umgang mit fehlgeschlagenen Updates
TOCTitle: Dealing with failed updates
ms:assetid: f6f4914d-59b3-f3f2-b986-218e07ce5a1d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250258(v=office.15)
ms:contentKeyID: 48548752
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9a44548fd8747428b12c03c24207f36d3871e349
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28725938"
---
# <a name="dealing-with-failed-updates"></a>Umgang mit fehlgeschlagenen Updates

**Betrifft**: Access 2013, Office 2013

## <a name="dealing-with-failed-updates"></a>Dealing with Failed Updates

Wenn eine Aktualisierung mit Fehlern endet, hängt es von der Art und dem Schweregrad der Fehler sowie der Logik Ihrer Anwendung ab, wie Sie die Fehler lösen. Wenn jedoch die Datenbank gemeinsam mit anderen Benutzern verwendet wird, gibt es den typischen Fehler, dass ein anderer Benutzer ein Feld vor Ihnen ändert. Diese Art von Fehler wird als *Konflikt* bezeichnet. ADO erkennt diese Situation und meldet einen Fehler.

Wenn Aktualisierungsfehler auftreten, werden sie in einer Fehlerbehandlungsroutine abgefangen. Filtern Sie das **Recordset** -Objekt mit der **adFilterConflictingRecords** -Konstante, damit nur die miteinander in Konflikt stehenden Zeilen angezeigt werden. In diesem Beispiel wird die Fehlerbehebung Strategie besteht lediglich Autor Drucken der vor- und Nachnamen (**au\_Fname** und **au\_Lname**).

Der Code, um den Benutzer auf den Aktualisierungskonflikt aufmerksam zu machen, sieht wie folgt aus:

```vb 
 
objRs.Filter = adFilterConflictingRecords 
objRs.MoveFirst 
Do While Not objRst.EOF 
   Debug.Print "Conflict: Name =  "; objRs!au_fname; " "; objRs!au_lname 
   objRs.MoveNext 
Loop 
```

