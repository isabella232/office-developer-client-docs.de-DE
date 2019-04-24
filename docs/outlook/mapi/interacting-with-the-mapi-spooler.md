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
ms.openlocfilehash: da94347dcb47e5fdbd4a6c1d404b795f4f7938ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317206"
---
# <a name="interacting-with-the-mapi-spooler"></a>Interaktion mit dem MAPI-Spooler

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Methoden in der [IXPLogon: IUnknown](ixplogoniunknown.md) -Schnittstelle werden vom MAPI-Spooler beim Aufrufen des Transportanbieters verwendet. Die meisten Typen von Transportanbietern sollten die meisten dieser Methoden implementieren können, damit Sie schnell zurückkehren. Dies ist wünschenswert, denn wenn eine Methode eine lange Zeit benötigt, um zurückzukehren, sollte Sie mit Aufrufen zurück an den MAPI-Spooler aufgebrochen werden, um die CPU für andere Aufgaben freizugeben. 
  
Der MAPI-Spooler funktioniert und ruft seine Anrufe an Transportanbieter ab, wenn vordergrundanwendungen im Leerlauf sind. Nachdem optional Dialogfelder angezeigt werden, wenn der Transportanbieter zum ersten Mal angemeldet ist (gesteuert von Flags, die von MAPI an den Transportanbieter übergeben werden), werden Transportanbieter im Hintergrund ausgeführt, es sei denn, der Client wird zum leeren von Sende-und Empfangs Warteschlangen aufgerufen. Das Leeren von Warteschlangen ist der einzige Zeitpunkt, an dem ein Transportanbieter die CPU nicht freigeben muss, und dann nur dann, wenn der Benutzer darüber informiert wird, dass eine potenziell lange Aktion ausgeführt wird. Der MAPI-Spooler fordert in der Regel an, dass ein Transportanbieter seine Warteschlangen als Reaktion auf eine Benutzeraktion leert, sodass der Transportanbieter normalerweise keine weiteren Schritte Unternehmen muss, um sicherzustellen, dass der Benutzer informiert wird.
  
Ein Transportanbieter kann unabhängig davon entscheiden, eine Warteschlange zu leeren und die STATUS_INBOUND_FLUSH-und STATUS_OUTBOUND_FLUSH-Bits in der **PR_STATUS_CODE** ([pidtagstatuscode (](pidtagstatuscode-canonical-property.md))-Eigenschaft der Status Zeile zu verwenden, um die gewünschte MAPI-spoolerin zu informieren. Aufmerksamkeit, damit Sie den Auftrag erledigen kann. Die Statuszeile wird mithilfe der [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) -Methode aktualisiert. In diesem Fall sollte der Transportanbieter wahrscheinlich eine Statusanzeige oder eine andere Schnittstelle anzeigen, um dem Benutzer mitzuteilen, dass eine lange Aktion stattfindet. 
  
Da die Netzwerkaktivität häufig mehr als 0,2 Sekunden dauert, sollten Transportanbieter, wann immer möglich, asynchrone Netzwerkanforderungen verwenden. Dadurch können Sie eine Anforderung initiieren, die CPU freigeben, indem Sie den MAPI-Spooler aufrufen und wenn der MAPI-Spooler Sie erneut steuert, um zu überprüfen, ob die Netzwerkanforderung abgeschlossen wurde. Wenn es noch nicht abgeschlossen ist, wird die CPU erneut durch Aufrufen des MAPI-Spoolers mit der [IMAPISupport:: SpoolerYield](imapisupport-spooleryield.md) -Methode freigegeben. 
  
Während der Nachrichtenverarbeitung zwischen [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) und [IXPLogon:: EndMessage](ixplogon-endmessage.md) und während [IXPLogon:: StartMessage](ixplogon-startmessage.md)führt der Transportanbieter in der Regel viele Aufrufe für Objekte durch, die vom MAPI-Spooler angezeigt werden. Im Rahmen der Verarbeitung dieser Objekte hilft der MAPI-Spooler dem Transportanbieter, sich entsprechend als Hintergrundprozess zu Verhalten, indem er eigenständig nachgibt. Ein Transportanbieter, der zeitkritische Verarbeitung erfordert, kann mithilfe der [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) -Support Objektmethode einen kritischen Abschnitt für den MAPI-Spooler deklarieren. In diesem Fall wird die CPU nur für explizite **SpoolerYield** -Aufrufe des Transportanbieters freigegeben, bis der Transportanbieter die Verarbeitung kritischer Abschnitte mit einem weiteren Aufruf von **SpoolerNotify**beendet hat.
  
> [!NOTE]
> Dies ist nicht identisch mit einem kritischen Win32-Abschnitt. Dies sollte nur erfolgen, wenn der Transportanbieter die Echtzeitsteuerung externer Ressourcen wie das Lesen eingehender Daten aus einer Faxnachricht benötigt. Da dadurch die Priorität des MAPI-Spooler-Prozesses erhöht wird und die Arbeitsstation für die Dauer des Vorgangs nicht mehr reagiert, empfiehlt es sich, dem Benutzer mitzuteilen, dass eine potenziell lange Aktion ausgeführt wird und wenn möglich eine Statusanzeige bereitzustellen. 
  

