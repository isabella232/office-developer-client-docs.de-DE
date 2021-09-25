---
title: Zurückstellen der Verarbeitung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a791b95f-56ad-493a-9ba5-fb4c7dd80e89
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 909e25601e572e3373883b83791f4d8a785fdbea
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588203"
---
# <a name="deferring-processing"></a>Zurückstellen der Verarbeitung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Übergeben Sie das MAPI_DEFERRED_ERRORS Flag so weit wie möglich an Methodenaufrufe. Viele der MAPI-Methodenaufrufe wurden für die Annahme dieses Flags optimiert, sodass der Anbieter die angeforderte Aufgabe verschieben kann, bis mehrere Aufgaben gleichzeitig ausgeführt werden können, oder Sie können nicht mehr auf die Ergebnisse warten.
  
Wenn Sie beispielsweise MAPI_DEFERRED_ERRORS an [IMsgStore::OpenEntry](imsgstore-openentry.md) übergeben, um einen Ordner zu öffnen, können das Öffnen des Ordners und ein möglicher Remoteaufruf verschoben werden, bis Sie einen weiteren Aufruf ausführen, z. B. einen Aufruf der **GetHierarchyTable-** oder **GetProps-Methoden des Ordners.** Sowohl **GetHierarchyTable** als **auch GetProps** erfordern die Rückgabe von Daten vom Dienstanbieter, eine Aufgabe, die sofort ausgeführt werden muss. 
  
Eine weitere Möglichkeit zum Zurückstellen der Verarbeitung besteht einfach nicht darin, einen Anruf zu tätigen. Wenn Sie sich des Benutzers bewusst sind und wenn der Benutzer ressourcen- oder verarbeitungsbedingt sein kann, können Sie ermitteln, wann es sinnvoll ist, Anrufe zu tätigen. Es besteht die Möglichkeit, die Leistung zu verbessern, indem Sie Aufrufe entweder zu einem Zeitpunkt tätigen, zu dem der Benutzer dies nicht bemerkt, oder indem sie überhaupt nicht ausgeführt werden.
  
Angenommen, Sie erhalten mehr als eine Benachrichtigung pro Sekunde aus einem Nachrichtenspeicher, der eine große Anzahl von Nachrichten verschiebt. Es wird eine Statusanzeige angezeigt, um den Prozentsatz des Abschlusses des Vorgangs anzugeben. Benutzer nehmen diesen Vorgang in der Regel erst als langsam wahr, wenn ein paar Sekunden vergangen sind. Wenn Sie die Statusanzeige aktualisieren, nehmen Sie daher erst vier Sekunden nach der Initiierung des Verschiebungsvorgangs Änderungen vor. Dies spart Zeit in den allgemeinen Fällen, wenn der Vorgang schnell ist, und informiert die Benutzer zeitnah, wenn der Vorgang langsam ist.
  

