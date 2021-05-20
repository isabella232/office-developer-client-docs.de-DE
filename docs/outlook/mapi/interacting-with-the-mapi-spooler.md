---
title: Interagieren mit dem MAPI-Spooler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5cc1d0a8-ad23-4173-b220-b7c0169073fa
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: da94347dcb47e5fdbd4a6c1d404b795f4f7938ab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432149"
---
# <a name="interacting-with-the-mapi-spooler"></a>Interagieren mit dem MAPI-Spooler

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Methoden in [der IXPLogon : IUnknown-Schnittstelle](ixplogoniunknown.md) werden vom MAPI-Spooler beim Aufrufen des Transportanbieters verwendet. Die meisten Arten von Transportanbietern sollten die meisten dieser Methoden implementieren können, damit sie schnell zurückkehren. Dies ist wünschenswert, da eine Methode, die lange dauert, um zurückzukehren, durch Aufrufe an den MAPI-Spooler aufgebrochen werden sollte, um die CPU für andere Aufgaben frei zu geben. 
  
Der MAPI-Spooler führt seine Arbeit aus und ruft Transportanbieter auf, wenn sich Vordergrundanwendungen im Leerlauf befinden. Nach der optionalen Anzeige von Dialogfeldern, wenn der Transportanbieter zum ersten Mal angemeldet ist (geregelt durch Flags, die von MAPI an den Transportanbieter übergeben werden), arbeiten Transportanbieter im Hintergrund, es sei denn, der Client wird zum Leeren von Sende- und Empfangswarteschlangen aufgerufen. Das Leeren von Warteschlangen ist der einzige Zeitpunkt, zu dem ein Transportanbieter die CPU nicht los lassen muss, und dann nur, wenn der Benutzer darüber informiert wird, dass eine potenziell lange Aktion ausgeführt wird. Der MAPI-Spooler fordert in der Regel an, dass ein Transportanbieter seine Warteschlangen als Reaktion auf eine Benutzeraktion leert, sodass der Transportanbieter in der Regel nichts tun muss, um sicherzustellen, dass der Benutzer informiert wird.
  
Ein Transportanbieter kann unabhängig entscheiden, eine Warteschlange zu leeren und die **STATUS_INBOUND_FLUSH-** und STATUS_OUTBOUND_FLUSH-Bits in der PR_STATUS_CODE ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))-Eigenschaft seiner Statuszeile zu verwenden, um den #A0 darüber zu informieren, dass er Aufmerksamkeit möchte, damit er den Auftrag erledigen kann. Die Statuszeile wird mithilfe der [IMAPISupport::ModifyStatusRow-Methode](imapisupport-modifystatusrow.md) aktualisiert. In diesem Fall sollte der Transportanbieter wahrscheinlich eine Statusanzeige oder eine andere Schnittstelle anzeigen, um den Benutzer darüber zu informieren, dass eine lange Aktion ausgeführt wird. 
  
Da netzwerkaktivität häufig länger als 0,2 Sekunden dauert, sollten Transportanbieter nach Möglichkeit asynchrone Netzwerkanforderungen verwenden. Auf diese Weise können sie eine Anforderung initiieren, die CPU los, indem sie den MAPI-Spooler aufrufen und wenn der MAPI-Spooler ihnen erneut die Kontrolle übergibt, um zu überprüfen, ob ihre Netzwerkanforderung abgeschlossen wurde. Wenn sie noch nicht abgeschlossen ist, geben sie die CPU erneut frei, indem sie den MAPI-Spooler mit der [IMAPISupport::SpoolerYield-Methode](imapisupport-spooleryield.md) aufrufen. 
  
Während der Nachrichtenverarbeitung zwischen [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) und [IXPLogon::EndMessage](ixplogon-endmessage.md) und [während IXPLogon::StartMessage](ixplogon-startmessage.md)ruft der Transportanbieter in der Regel viele Objekte auf, die vom MAPI-Spooler verfügbar gemacht werden. Im Rahmen der Behandlung dieser Objekte hilft der MAPI-Spooler dem Transportanbieter dabei, sich entsprechend als Hintergrundprozess zu verhalten, indem er bei entsprechender Verwendung eigene Ergebnisse liefert. Ein Transportanbieter, der eine zeitkritische Verarbeitung erfordert, kann einen kritischen Abschnitt für den MAPI-Spooler mithilfe der [IMAPISupport::SpoolerNotify-Supportobjektmethode](imapisupport-spoolernotify.md) deklarieren. In diesem Fall wird die CPU nur für explizite **SpoolerYield-Aufrufe** des Transportanbieters freigegeben, bis der Transportanbieter die Kritische Abschnittsverarbeitung mit einem anderen Aufruf von **SpoolerNotify beendet.**
  
> [!NOTE]
> Dies ist nicht identisch mit einem kritischen Win32-Abschnitt. Dies sollte nur erfolgen, wenn der Transportanbieter die Echtzeitkontrolle externer Ressourcen benötigt, z. B. das Lesen eingehender Daten aus einer Faxleitung. Da dies die Priorität des MAPI-Spoolerprozesses erhöht und dazu führen kann, dass die Arbeitsstation für die Dauer des Vorgangs nicht reagiert, sollten Sie den Benutzer benachrichtigen, dass eine potenziell lange Aktion ausgeführt wird, und nach Möglichkeit einen Fortschrittsindikator bereitstellen. 
  

