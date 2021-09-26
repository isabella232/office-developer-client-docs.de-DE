---
title: Interagieren mit dem MAPI-Spooler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 5cc1d0a8-ad23-4173-b220-b7c0169073fa
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bb620bc68239e5353d30b99cc9e76e907343c37b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620604"
---
# <a name="interacting-with-the-mapi-spooler"></a>Interagieren mit dem MAPI-Spooler

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Methoden in der [IXPLogon : IUnknown-Schnittstelle](ixplogoniunknown.md) werden vom MAPI-Spooler beim Aufrufen des Transportanbieters verwendet. Es sollte für die meisten Arten von Transportanbietern möglich sein, die meisten dieser Methoden zu implementieren, damit sie schnell zurückgegeben werden. Dies ist wünschenswert, da eine Methode, deren Rückgabe lange dauert, durch Aufrufe an den MAPI-Spooler aufgeteilt werden sollte, um die CPU für andere Aufgaben freizugeben. 
  
Der MAPI-Spooler führt seine Arbeit aus und ruft Transportanbieter auf, wenn sich Vordergrundanwendungen im Leerlauf befinden. Nach dem optionalen Anzeigen von Dialogfeldern bei der ersten Anmeldung des Transportanbieters (gesteuert durch Flags, die von der MAPI an den Transportanbieter übergeben werden), arbeiten Transportanbieter im Hintergrund, es sei denn, sie werden vom Client aufgerufen, um Sende- und Empfangswarteschlangen zu leeren. Das Leeren von Warteschlangen ist die einzige Zeit, zu der ein Transportanbieter die CPU nicht freigeben muss, und dann nur, wenn der Benutzer informiert wird, dass eine potenziell lange Aktion ausgeführt wird. Der MAPI-Spooler fordert in der Regel an, dass ein Transportanbieter seine Warteschlangen als Reaktion auf eine Benutzeraktion leert, sodass der Transportanbieter in der Regel nichts unternehmen muss, um sicherzustellen, dass der Benutzer informiert wird.
  
Ein Transportanbieter kann unabhängig voneinander eine Warteschlange leeren und die STATUS_INBOUND_FLUSH und STATUS_OUTBOUND_FLUSH Bits in der **Eigenschaft PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) seiner Statuszeile verwenden, um den MAPI-Spooler darüber zu informieren, dass er Aufmerksamkeit möchte, damit er die Aufgabe erledigen kann. Die Statuszeile wird mithilfe der [IMAPISupport::ModifyStatusRow-Methode](imapisupport-modifystatusrow.md) aktualisiert. In diesem Fall sollte der Transportanbieter wahrscheinlich eine Statusanzeige oder eine andere Benutzeroberfläche anzeigen, um den Benutzer darüber zu informieren, dass eine lange Aktion ausgeführt wird. 
  
Da die Netzwerkaktivität häufig mehr als 0,2 Sekunden dauert, sollten Transportanbieter nach Möglichkeit asynchrone Netzwerkanforderungen verwenden. Dadurch können sie eine Anforderung initiieren, die CPU freigeben, indem sie an den MAPI-Spooler zurückrufen, und wenn der MAPI-Spooler ihnen erneut die Kontrolle übergibt, um zu überprüfen, ob ihre Netzwerkanforderung abgeschlossen wurde. Wenn sie noch nicht abgeschlossen ist, geben sie erneut die CPU frei, indem sie den MAPI-Spooler mit der [IMAPISupport::SpoolerYield-Methode](imapisupport-spooleryield.md) aufrufen. 
  
Während der Nachrichtenverarbeitung, zwischen [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) und [IXPLogon::EndMessage](ixplogon-endmessage.md) und während [IXPLogon::StartMessage](ixplogon-startmessage.md)führt der Transportanbieter in der Regel viele Aufrufe für Objekte durch, die ihm vom MAPI-Spooler verfügbar gemacht werden. Im Rahmen der Verarbeitung dieser Objekte hilft der MAPI-Spooler dem Transportanbieter, sich angemessen als Hintergrundprozess zu verhalten, indem er bei Bedarf eigenständig nachgibt. Ein Transportanbieter, der eine zeitkritische Verarbeitung erfordert, kann einen kritischen Abschnitt für den MAPI-Spooler mithilfe der [IMAPISupport::SpoolerNotify-Unterstützungsobjektmethode](imapisupport-spoolernotify.md) deklarieren. In diesem Fall wird die CPU nur bei expliziten **SpoolerYield-Aufrufen** durch den Transportanbieter freigegeben, bis der Transportanbieter die Verarbeitung wichtiger Abschnitte mit einem anderen Aufruf von **SpoolerNotify** beendet.
  
> [!NOTE]
> Dies ist nicht identisch mit einem kritischen Win32-Abschnitt. Dies sollte nur erfolgen, wenn der Transportanbieter die Echtzeitsteuerung externer Ressourcen benötigt, z. B. das Lesen eingehender Daten aus einer Faxzeile. Da dadurch die Priorität des MAPI-Spoolerprozesses erhöht wird und die Arbeitsstation während der Dauer des Vorgangs nicht mehr reagiert, sollten Sie den Benutzer benachrichtigen, dass eine potenziell lange Aktion ausgeführt wird, und nach Möglichkeit eine Statusanzeige bereitstellen. 
  

