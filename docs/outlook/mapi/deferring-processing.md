---
title: Zurückstellen der Verarbeitung
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
# <a name="deferring-processing"></a>Zurückstellen der Verarbeitung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Führen Sie das MAPI_DEFERRED_ERRORS-Flag so weit wie möglich an Methodenaufrufe weiter. Viele der MAPI-Methodenaufrufe wurden so optimiert, dass diese Kennzeichnung akzeptiert wird, sodass der Anbieter die angeforderte Aufgabe entweder verschiebt, bis mehrere Aufgaben gleichzeitig ausgeführt werden können, oder Sie können nicht mehr auf die Ergebnisse warten.
  
Wenn Sie beispielsweise MAPI_DEFERRED_ERRORS an [IMsgStore:: OpenEntry](imsgstore-openentry.md) weitergeben, um einen Ordner zu öffnen, kann das Öffnen des Ordners und ein möglicher Remoteaufruf verschoben werden, bis Sie einen weiteren Aufruf ausführen, beispielsweise einen Aufruf an **** die GetHierarchy-Datei des Ordners oder ** **GetProps-Methoden. Sowohl **** gethierarchyable als auch GetProps erfordern die Rückgabe von Daten vom Dienstanbieter, eine Aufgabe, die sofort ausgeführt werden muss. **** 
  
Eine andere Möglichkeit, die Verarbeitung zu verzögern, besteht darin, keinen Anruf zu tätigen. Wenn Sie den Benutzer erkennen und wenn der Benutzer die Ressourcen oder die Verarbeitungszeit ausleeren kann, können Sie bestimmen, wann es sinnvoll ist, Anrufe zu tätigen. Es besteht die Möglichkeit, die Leistung zu verbessern, indem Sie Anrufe entweder zu einem Zeitpunkt durchführen, zu dem der Benutzer Sie nicht bemerkt oder überhaupt nicht vornimmt.
  
Betrachten Sie beispielsweise die Situation, wenn Sie mehr als eine Benachrichtigung pro Sekunde aus einem Nachrichtenspeicher erhalten, der eine große Anzahl von Nachrichten verschiebt. Eine Statusanzeige wird angezeigt, um den Prozentsatz der Fertigstellung des Vorgangs anzugeben. Dieser Vorgang wird in der Regel erst nach einigen Sekunden verlangsamt. Wenn Sie also die Statusanzeige aktualisieren, nehmen Sie keine Änderungen vor, bevor Sie mindestens vier Sekunden nach dem Initiieren des Verschiebevorgangs beginnen. Dies spart Zeit in den häufig verwendeten Fällen, wenn der Vorgang schnell ausgeführt wird und die Benutzerrecht zeitig informiert werden, wenn der Vorgang langsam ist.
  

