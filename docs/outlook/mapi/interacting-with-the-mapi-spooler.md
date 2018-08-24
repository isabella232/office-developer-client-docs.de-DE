---
title: Interaktion mit dem MAPI-Spooler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5cc1d0a8-ad23-4173-b220-b7c0169073fa
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c8032172ef19fbb01af68058b2e0255e269183a8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587894"
---
# <a name="interacting-with-the-mapi-spooler"></a>Interaktion mit dem MAPI-Spooler

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Methoden in der [IXPLogon: IUnknown](ixplogoniunknown.md) Schnittstelle werden beim Aufrufen der Adressbuchhierarchie durch die MAPI-Warteschlange verwendet. Es sollte für die meisten Arten von Transportanbieter für die meisten dieser Methoden implementieren, sodass diese schnell zurückgeben möglich sein. Dies ist wünschenswert, da, wenn eine Methode zum Zurückgeben lange dauert dann es mit Aufrufen an die Warteschlange MAPI-Version die CPU für andere Aufgaben aufgeteilt werden sollte. 
  
Die MAPI-Warteschlange führt diese Aufgaben und seine Aufrufe der Anbieter Transport, wenn Vordergrund Applikationen im Leerlauf befinden. Nach dem Anzeigen von Dialogfeldern optional, wenn der Adressbuchhierarchie zuerst angemeldet ist (unterliegt von MAPI an der Adressbuchhierarchie übergebene Kennzeichen), Betrieb Transportanbieter im Hintergrund, wenn vom Client zum leeren senden und Empfangen von Warteschlangen aufgerufen. Das leeren Warteschlangen ist nur dann, dass ein Transportdienstes nicht die CPU freigeben muss und dann nur, wenn der Benutzer informiert wird, dass eine möglicherweise länger Aktion ausgeführt wird. Die MAPI-Warteschlange fordert, dass ein Transportdienstes leeren Warteschlangen als Antwort auf eine Benutzeraktion aus, damit der Adressbuchhierarchie in der Regel keine muss nichts, um sicherzustellen, dass der Benutzer informiert wird in der Regel an.
  
Ein Transportdienstes kann unabhängig voneinander leeren eine Warteschlange und die Bits STATUS_INBOUND_FLUSH und STATUS_OUTBOUND_FLUSH in der Statuszeile der **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))-Eigenschaft verwenden, um die MAPI-Warteschlange zu informieren, die dass die diesmal festlegen Aufmerksamkeit, damit das alles erledigt abrufen kann. Die Statuszeile wird mit der [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) -Methode aktualisiert. In diesem Fall sollte der Adressbuchhierarchie wahrscheinlich angezeigt werden, eine Statusanzeige oder andere-Schnittstelle für den Benutzer zu informieren, dass eine lange Aktion durchgeführt wird. 
  
Da Netzwerkaktivität oft mehr als 0,2 Sekunden dauert, sollten, Transportanbieter nach Möglichkeit asynchrones Netzwerkanfragen verwenden. So können sie eine Anforderung initiieren, Version CPU erneut, indem die MAPI-Warteschlange und wenn die MAPI-Warteschlange erneut sie bietet Kontrolle, überprüfen, um festzustellen, ob ihre Netzwerk-Anforderung abgeschlossen wurde. Wenn sie noch nicht abgeschlossen wurde, Version sie erneut die CPU Rückrufen an die MAPI-Warteschlange mit der [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) -Methode. 
  
Während der Verarbeitung, zwischen [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) und [IXPLogon::EndMessage](ixplogon-endmessage.md) und während der [IXPLogon::StartMessage](ixplogon-startmessage.md)sendet der Adressbuchhierarchie viele Aufrufe in der Regel auf Objekte, die die MAPI-Warteschlange ausgesetzt. Im Rahmen der Behandlung von dieser Objekte kann die MAPI-Warteschlange der Adressbuchhierarchie entsprechend als Hintergrundprozess steuern, indem Sie auf einem eigenen bei Bedarf zurückhalten. Ein Transportdienstes zeitlich bedingte verarbeitenden kann einen wichtigen Abschnitt aus, um die MAPI-Warteschlange mithilfe der [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) Support-Objekt-Methode deklarieren. In diesem Fall wird die CPU nur auf explizite **SpoolerYield** Aufrufe von freigegeben der Adressbuchhierarchie, bis der Adressbuchhierarchie kritischen Abschnitt mit einer anderen Aufruf **SpoolerNotify**Verarbeitung beendet.
  
> [!NOTE]
> Dies ist nicht identisch mit einem kritischen Win32-Abschnitt. Dies sollte nur geschehen, wenn der Adressbuchhierarchie Real-Time Control von externen Ressourcen wie Lesen von eingehenden Daten aus einer Zeile Fax benötigt. Da dies die Priorität des Prozesses MAPI-Warteschlange erhöht und kann dazu führen, dass die Arbeitsstation für die Dauer des Vorgangs nicht reagiert werden soll, ist es ratsam, benachrichtigt den Benutzer, den eine möglicherweise länger Aktion ausgeführt wird, und geben Sie nach Möglichkeit eine Statusanzeige. 
  

