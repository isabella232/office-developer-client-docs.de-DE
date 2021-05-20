---
title: Zurückdringen der Verarbeitung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a791b95f-56ad-493a-9ba5-fb4c7dd80e89
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2d3fbf8f7a725f121579066001715fb0bc6beba0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430931"
---
# <a name="deferring-processing"></a>Zurückdringen der Verarbeitung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Übergeben Sie MAPI_DEFERRED_ERRORS-Flag an Methodenaufrufe so weit wie möglich. Viele aufrufe der MAPI-Methode wurden für die Annahme dieses Kennzeichens optimiert, sodass der Anbieter die angeforderte Aufgabe entweder verschieben kann, bis mehrere Aufgaben gleichzeitig ausgeführt werden können, oder Sie können nicht mehr auf die Ergebnisse warten.
  
Wenn Sie z. B. MAPI_DEFERRED_ERRORS an [IMsgStore::OpenEntry](imsgstore-openentry.md) übergeben, um einen Ordner zu öffnen, können das Öffnen des Ordners und ein möglicher Remoteaufruf verschoben werden, bis Sie einen weiteren Aufruf wie z. B. einen Aufruf der **GetHierarchyTable-** oder **GetProps-Methoden** des Ordners machen. Sowohl **GetHierarchyTable** als auch **GetProps** erfordern die Rückgabe von Daten vom Dienstanbieter, eine Aufgabe, die sofort ausgeführt werden muss. 
  
Eine weitere Möglichkeit zum Aufschub der Verarbeitung ist einfach, keinen Anruf zu machen. Wenn Sie sich des Benutzers bewusst sind und wann der Benutzer ressourcen- oder verarbeitungszeitablaufend wahrgenommen werden kann, können Sie bestimmen, wann es sinnvoll ist, Anrufe zu machen. Es besteht die Möglichkeit, die Leistung zu verbessern, indem Sie anrufe entweder zu einem Zeitpunkt, zu dem der Benutzer sie nicht bemerkt oder gar nicht macht.
  
Berücksichtigen Sie beispielsweise die Situation, dass Sie mehr als eine Benachrichtigung pro Sekunde von einem Nachrichtenspeicher erhalten, der eine große Anzahl von Nachrichten bewegt. Es wird ein Fortschrittsindikator angezeigt, der den Prozentsatz des Abschlusses des Vorgangs angibt. Benutzer sehen diesen Vorgang in der Regel erst langsam, wenn einige Sekunden vergangen sind. Wenn Sie die Statusanzeige aktualisieren, nehmen Sie daher erst mindestens vier Sekunden nach Beginn des Verschiebens Änderungen vor. Dies spart zeit in den häufigen Fällen, in denen der Vorgang schnell ist, und informiert benutzer zeitnah, wenn der Vorgang langsam ist.
  

