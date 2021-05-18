---
title: Implementieren der FlushQueues-Methode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8719f8aa-a537-4253-b67d-c4d38c40472b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1e5c78c71f7fddb04d3517aca0a34efa151ece08
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411778"
---
# <a name="implementing-the-flushqueues-method"></a>Implementieren der FlushQueues-Methode

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der MAPI-Spooler verwendet die [IXPLogon::FlushQueues-Methode,](ixplogon-flushqueues.md) um ausstehende Nachrichten in und von einem Transportanbieter herunterzuladen und hochzuladen. In der Regel leeren die MAPI-Spooler die Warteschlangen für alle Transportanbieter, die an der Sitzung angemeldet sind, beginnend mit dem ersten Transportanbieter, wie im Abschnitt Transportreihenfolge des Benutzerprofils festgelegt. Das Leeren von Warteschlangen ist fast immer das Ergebnis einer direkten Anforderung durch den Benutzer, sodass das Senden und Empfangen von Nachrichten während des Leerens von Warteschlangen synchron mit dem MAPI-Spooler erfolgt. Da diese Anrufe synchron sind, sollte der Transportanbieter sie so schnell wie möglich verarbeiten. 
  
Transport provider must handle the **FlushQueues** call as described in the following sequence of steps to enable proper message processing and to enable external resources such as modems to be used by other transport providers as part of the MAPI spooler'spooler operation **FlushQueues.** 
  
|**Schritt**|**Komponente**|**Implementierung**|
|:-----|:-----|:-----|
|1.  <br/> |MAPI-Spooler  <br/> |Ruft die **FlushQueues-Methode** für den ersten Transportanbieter auf, der in der Transportreihenfolge des Benutzerprofils aufgeführt ist, und gibt die angeforderten Flags im  _ulFlags-Parameter_ weiter. **FlushQueues wird** einmal aufgerufen, und alle Flags sind für den gesamten Upload- und Downloadvorgang festgelegt.  <br/> |
|2.  <br/> |Transportanbieter  <br/> |Muss eine Reihe von Dingen vor der Rückgabe vom **FlushQueues-Anruf** tun. Wenn zuvor übermittelte Nachrichten zurückgestellt werden, sollte die [IMAPISupport::SpoolerNotify-Methode](imapisupport-spoolernotify.md) mit dem NOTIFY_SENT_DEFERRED aufgerufen werden. Beachten Sie, dass der MAPI-Spooler eine Nachricht abbrechen kann, die zurückgestellt wurde, bevor der Transportanbieter die Verarbeitung der Nachricht beenden kann.  <br/> Wenn der Transportanbieter eine externe Ressource wie ein Modem verwendet, sollte die Verbindung mit der externen Ressource hergestellt werden.  <br/> Das STATUS_OUTBOUND_FLUSH-Bit in der **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))-Eigenschaft der Statuszeile des Transportanbieters muss mithilfe der [IMAPISupport::ModifyStatusRow-Methode festgelegt](imapisupport-modifystatusrow.md) werden.  <br/> Der Transportanbieter sollte dann S_OK **FlushQueues-Anruf zurückgeben.**  <br/> |
|3.  <br/> |MAPI-Spooler  <br/> |Überprüft die Statuszeile des Transportanbieters auf das STATUS_OUTBOUND_FLUSH bit und ruft [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) für die erste Nachricht in der Warteschlange auf.  <br/> |
|4.  <br/> |Transportanbieter  <br/> |Verarbeitet die Nachricht und gibt vom **SubmitMessage-Aufruf** zurück.  <br/> |
|5.  <br/> |MAPI-Spooler  <br/> |Wenn der Transportanbieter S_OK von **SubmitMessage** zurückgibt, ruft der MAPI-Spooler [IXPLogon::EndMessage](ixplogon-endmessage.md) für die Nachricht auf, wie beim regulären Nachrichten senden.  <br/> Wenn der Transportanbieter einen anderen Wert als S_OK von **SubmitMessage** zurückgibt, behandelt der MAPI-Spooler den Wert entsprechend, bevor **EndMessage** oder **erneut SubmitMessage** aufruft.  <br/> |
|6.  <br/> |Transportanbieter  <br/> |Gibt von **EndMessage mit** dem Status der Nachrichtenverarbeitung im  _lpulFlags-Parameter_ zurück.  <br/> |
|7.  <br/> |MAPI-Spooler und Transportanbieter  <br/> |Die SubmitMessage-EndMessage-Schleife wird fortgesetzt, bis alle Nachrichten in der Warteschlange -   heruntergeladen wurden.  <br/> |
|8.  <br/> |MAPI-Spooler  <br/> |Benachrichtigt den Transportanbieter, dass der Download von Nachrichten abgeschlossen ist, indem er die [IXPLogon::TransportNotify-Methode](ixplogon-transportnotify.md) des Transportanbieters mit dem NOTIFY_END_OUTBOUND_FLUSH aufruft.  <br/> |
|9.  <br/> |Transportanbieter  <br/> |Gibt alle externen Ressourcen frei, die beim Senden ausgehender Nachrichten verwendet werden, damit sie von anderen Transportanbietern zum Leeren ihrer Warteschlangen verwendet werden können.  <br/> Das STATUS_INBOUND_FLUSH in der **PR_STATUS_CODE** der Statuszeile des Transportanbieters muss mithilfe von **ModifyStatusRow festgelegt werden.**  <br/> |
|10.  <br/> |MAPI-Spooler  <br/> |Überprüft die Statuszeile des Transportanbieters auf das STATUS_INBOUND_FLUSH Bit und ruft [IXPLogon::StartMessage](ixplogon-startmessage.md) auf, wenn es festgelegt ist.  <br/> |
|11.  <br/> |Transportanbieter  <br/> |Verarbeitet die Nachricht und gibt von **StartMessage zurück.** Wenn der Transportanbieter andere Nachrichten hochladen muss, sollte er **SpoolerNotify** mit dem NOTIFY_NEWMAIL aufrufen.  <br/> Wenn der Transportanbieter keine Nachrichten hochladen kann, sollte er [IMAPIProp::SaveChanges für](imapiprop-savechanges.md) die Nachricht aufrufen, die der MAPI-Spooler in **StartMessage** übergeben hat, und zurückgeben.  <br/> |
|12.  <br/> |MAPI-Spooler  <br/> |Ruft **startMessage weiterhin auf,** **bis SaveChanges** für eine Nachricht aufgerufen wird. Nachdem der Transportanbieter das Hochladen abgeschlossen hat, ruft der MAPI-Spooler **TransportNotify** mit dem NOTIFY_END_INBOUND_FLUSH auf.  <br/> |
|13.  <br/> |Transportanbieter  <br/> |Deaktiviert das STATUS_INBOUND_FLUSH-Bit in der **PR_STATUS_CODE-Eigenschaft** der Statuszeile mithilfe von **ModifyStatusRow** und gibt alle externen Ressourcen frei, sodass sie von anderen Transportanbietern verwendet werden können.  <br/> |
|14.  <br/> |MAPI-Spooler  <br/> |Ruft **FlushQueues** für den nächsten Transportanbieter auf, der in der Transportreihenfolge des Benutzerprofils aufgeführt ist.  <br/> |
   
Wenn eine Clientanwendung [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) für das Statusobjekt eines Transportanbieters aufruft, sollte der Transportanbieter das entsprechende Bit in seiner Statuszeile mit **ModifyStatusRow festlegen.** Der MAPI-Spooler ruft dann die **IXPLogon::FlushQueues-Methode** des Transportanbieters auf, um den MAPI-Spooler zu nutzen. Wenn die **IXPLogon::FlushQueues-Methode** des Transportanbieters als Ergebnis des **IMAPIStatus::FlushQueues-Aufrufs** einer Clientanwendung aufgerufen wird, erfolgt der Vorgang asynchron für die Clientanwendung. Andernfalls **funktioniert IXPLogon::FlushQueues** synchron mit dem MAPI-Spooler. 
  
Aus Leistungsgründen wird die **FlushQueues-Methode** eines Transportanbieters vom MAPI-Spooler nur dann aufruft, wenn die Flags STATUS_INBOUND_FLUSH und STATUS_OUTBOUND_FLUSH in der Statuszeile des Transportanbieters festgelegt sind. Daher kann ein Transportanbieter den **FlushQueues-Vorgang** jederzeit beenden, indem die STATUS_OUTBOUND_FLUSH und STATUS_INBOUND_FLUSH in der Statuszeile entfernt werden. Wenn der MAPI-Spooler heruntergefahren wird und den **FlushQueues-Vorgang** beenden muss, wird **TransportNotify** mit den festgelegten NOTIFY_END_INBOUND_FLUSH- und NOTIFY_END_OUTBOUND_FLUSH aufruft. Der Transportanbieter sollte alle externen Ressourcen frei geben und zurückgeben. 
  

