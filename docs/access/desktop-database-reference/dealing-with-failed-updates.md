---
title: Umgang mit fehlgeschlagenen Updates
TOCTitle: Dealing with failed updates
ms:assetid: f6f4914d-59b3-f3f2-b986-218e07ce5a1d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250258(v=office.15)
ms:contentKeyID: 48548752
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 9e7d34ad96a44ba654f06f6b94d67a6dd3cf4cef
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585767"
---
# <a name="dealing-with-failed-updates"></a>Umgang mit fehlgeschlagenen Updates

**Gilt für**: Access 2013, Office 2013

## <a name="dealing-with-failed-updates"></a>Umgehen mit fehlgeschlagenen Aktualisierungen

Wenn eine Aktualisierung mit Fehlern endet, hängt es von der Art und dem Schweregrad der Fehler sowie der Logik Ihrer Anwendung ab, wie Sie die Fehler lösen. Wenn jedoch die Datenbank gemeinsam mit anderen Benutzern verwendet wird, gibt es den typischen Fehler, dass ein anderer Benutzer ein Feld vor Ihnen ändert. Diese Art von Fehler wird als *Konflikt* bezeichnet. ADO erkennt diese Situation und meldet einen Fehler.

Wenn Aktualisierungsfehler auftreten, werden sie in einer Fehlerbehandlungsroutine abgefangen. Filtern Sie das **Recordset**-Objekt mit der **adFilterConflictingRecords**-Konstante, damit nur die miteinander in Konflikt stehenden Zeilen angezeigt werden. In diesem Beispiel besteht die Fehlerauflösungsstrategie lediglich darin, den Vor- und Nachnamen des Autors (**au \_ fname** und **au \_ lname**) zu drucken.

Der Code, um den Benutzer auf den Aktualisierungskonflikt aufmerksam zu machen, sieht wie folgt aus:

```vb 
 
objRs.Filter = adFilterConflictingRecords 
objRs.MoveFirst 
Do While Not objRst.EOF 
   Debug.Print "Conflict: Name =  "; objRs!au_fname; " "; objRs!au_lname 
   objRs.MoveNext 
Loop 
```

