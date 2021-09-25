---
title: Implementieren der FlushQueues-Methode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 8719f8aa-a537-4253-b67d-c4d38c40472b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a2e2476582f4b8ca5b9e0ee819f5eb610344ae4a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575666"
---
# <a name="implementing-the-flushqueues-method"></a>Implementieren der FlushQueues-Methode

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der MAPI-Spooler verwendet die [IXPLogon::FlushQueues-Methode,](ixplogon-flushqueues.md) um alle ausstehenden Nachrichten in und von einem Transportanbieter herunterzuladen und hochzuladen. In der Regel leert der MAPI-Spooler die Warteschlangen für alle Transportanbieter, die an der Sitzung angemeldet sind, beginnend mit dem ersten Transportanbieter, wie im Abschnitt zur Transportreihenfolge des Benutzerprofils festgelegt. Das Leeren von Warteschlangen ist fast immer das Ergebnis einer direkten Anforderung durch den Benutzer, sodass das Senden und Empfangen von Nachrichten, während Warteschlangen geleert werden, synchron mit dem MAPI-Spooler ist. Da diese Aufrufe synchron sind, sollte der Transportanbieter sie so schnell wie möglich verarbeiten. 
  
Transportanbieter müssen den **FlushQueues-Aufruf** wie in der folgenden Schritte beschrieben verarbeiten, um eine ordnungsgemäße Nachrichtenverarbeitung zu ermöglichen und externe Ressourcen wie Modems von anderen Transportanbietern als Teil des **FlushQueues-Vorgangs** des MAPI-Spoolers zu verwenden. 
  
|**Schritt**|**Komponente**|**Implementierung**|
|:-----|:-----|:-----|
|1.  <br/> |MAPI-Spooler  <br/> |Ruft die **FlushQueues-Methode** für den ersten Transportanbieter auf, der in der Transportreihenfolge des Benutzerprofils aufgeführt ist, und übergibt die angeforderten Flags im _ulFlags-Parameter._ **FlushQueues** wird einmal aufgerufen, wobei alle Flags für den gesamten Upload- und Downloadvorgang festgelegt sind.  <br/> |
|2.  <br/> |Transportanbieter  <br/> |Es muss eine Reihe von Aktionen ausgeführt werden, bevor der **FlushQueues-Aufruf** zurückgegeben wird. Wenn zuvor gesendete Nachrichten zurückgestellt werden, sollte die [IMAPISupport::SpoolerNotify-Methode](imapisupport-spoolernotify.md) aufgerufen werden, wobei das NOTIFY_SENT_DEFERRED Flag festgelegt ist. Beachten Sie, dass der MAPI-Spooler eine Nachricht abbrechen kann, die zurückgestellt wurde, bevor der Transportanbieter die Verarbeitung der Nachricht beenden kann.  <br/> Wenn der Transportanbieter eine externe Ressource wie z. B. ein Modem verwendet, sollte die Verbindung mit der externen Ressource hergestellt werden.  <br/> Das STATUS_OUTBOUND_FLUSH Bit in der **eigenschaft PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) der Statuszeile des Transportanbieters muss mithilfe der [IMAPISupport::ModifyStatusRow-Methode](imapisupport-modifystatusrow.md) festgelegt werden.  <br/> Der Transportanbieter sollte dann S_OK für den **FlushQueues-Aufruf** zurückgeben.  <br/> |
|3.  <br/> |MAPI-Spooler  <br/> |Überprüft die Statuszeile des Transportanbieters auf das STATUS_OUTBOUND_FLUSH Bit und ruft [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) für die erste Nachricht in der Warteschlange auf.  <br/> |
|4.  <br/> |Transportanbieter  <br/> |Behandelt die Nachricht und gibt vom **SubmitMessage-Aufruf** zurück.  <br/> |
|5.  <br/> |MAPI-Spooler  <br/> |Wenn der Transportanbieter S_OK von **SubmitMessage zurückgibt,** ruft der MAPI-Spooler [IXPLogon::EndMessage](ixplogon-endmessage.md) für die Nachricht auf wie beim regulären Senden von Nachrichten.  <br/> Wenn der Transportanbieter einen anderen Wert als S_OK von **SubmitMessage zurückgibt,** verarbeitet der MAPI-Spooler den Wert entsprechend vor dem Aufrufen von **EndMessage** oder vor dem erneuten Aufrufen von **SubmitMessage.**  <br/> |
|6.  <br/> |Transportanbieter  <br/> |Gibt von **EndMessage** mit dem Status der Nachrichtenverarbeitung im  _lpulFlags-Parameter_ zurück.  <br/> |
|7.  <br/> |MAPI-Spooler und Transportanbieter  <br/> |Die **SubmitMessage** -  **EndMessage-Schleife** wird fortgesetzt, bis alle Nachrichten in der Warteschlange heruntergeladen wurden.  <br/> |
|8.  <br/> |MAPI-Spooler  <br/> |Benachrichtigt den Transportanbieter, dass das Herunterladen von Nachrichten beendet wurde, indem die [IXPLogon::TransportNotify-Methode](ixplogon-transportnotify.md) des Transportanbieters aufgerufen wird, wobei das NOTIFY_END_OUTBOUND_FLUSH Flag festgelegt ist.  <br/> |
|9.  <br/> |Transportanbieter  <br/> |Gibt alle externen Ressourcen frei, die zum Senden ausgehender Nachrichten verwendet werden, damit sie von anderen Transportanbietern zum Leeren ihrer Warteschlangen verwendet werden können.  <br/> Das STATUS_INBOUND_FLUSH Bit in der **PR_STATUS_CODE** Eigenschaft der Statuszeile des Transportanbieters muss mit **modifyStatusRow** festgelegt werden.  <br/> |
|10.  <br/> |MAPI-Spooler  <br/> |Überprüft die Statuszeile des Transportanbieters auf das STATUS_INBOUND_FLUSH Bit und ruft [IXPLogon::StartMessage auf,](ixplogon-startmessage.md) wenn es festgelegt ist.  <br/> |
|11.  <br/> |Transportanbieter  <br/> |Verarbeitet die Nachricht und gibt von **StartMessage** zurück. Wenn der Transportanbieter über andere hochzuladende Nachrichten verfügt, sollte **SpoolerNotify** aufgerufen werden, wobei das NOTIFY_NEWMAIL Flag festgelegt ist.  <br/> Wenn der Transportanbieter keine hochzuladenden Nachrichten hat, sollte er [IMAPIProp::SaveChanges](imapiprop-savechanges.md) für die Nachricht aufrufen, die der MAPI-Spooler in **StartMessage** übergeben und zurückgegeben hat.  <br/> |
|12.  <br/> |MAPI-Spooler  <br/> |Setzt den Aufruf von **StartMessage** fort, bis **SaveChanges** für eine Nachricht aufgerufen wird. Nachdem der Upload des Transportanbieters abgeschlossen ist, ruft der MAPI-Spooler **TransportNotify** auf, wobei das NOTIFY_END_INBOUND_FLUSH Flag festgelegt ist.  <br/> |
|13.  <br/> |Transportanbieter  <br/> |Löscht das STATUS_INBOUND_FLUSH Bit in der **PR_STATUS_CODE** Eigenschaft der Statuszeile mit **modifyStatusRow** und gibt alle externen Ressourcen frei, damit sie von anderen Transportanbietern verwendet werden können.  <br/> |
|14.  <br/> |MAPI-Spooler  <br/> |Ruft **FlushQueues** für den nächsten Transportanbieter auf, der in der Transportreihenfolge des Benutzerprofils aufgeführt ist.  <br/> |
   
Wenn eine Clientanwendung [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) für das Statusobjekt eines Transportanbieters aufruft, sollte der Transportanbieter das entsprechende Bit in der Statuszeile mit **ModifyStatusRow** festlegen. Der MAPI-Spooler ruft dann die **IXPLogon::FlushQueues-Methode** des Transportanbieters aus Gründen der Benutzerfreundlichkeit des MAPI-Spoolers auf. Wenn die **IXPLogon::FlushQueues-Methode** des Transportanbieters als Ergebnis des **IMAPIStatus::FlushQueues-Aufrufs** einer Clientanwendung aufgerufen wird, erfolgt der Vorgang asynchron für die Clientanwendung. Andernfalls funktioniert **IXPLogon::FlushQueues** synchron mit dem MAPI-Spooler. 
  
Aus Leistungsgründen ruft der MAPI-Spooler nur die **FlushQueues-Methode** eines Transportanbieters auf, wenn die flags STATUS_INBOUND_FLUSH und STATUS_OUTBOUND_FLUSH in der Statuszeile des Transportanbieters festgelegt sind. Daher kann ein Transportanbieter den **FlushQueues-Vorgang** jederzeit beenden, indem er die STATUS_OUTBOUND_FLUSH löscht und flags in der Statuszeile STATUS_INBOUND_FLUSH. Wenn der MAPI-Spooler heruntergefahren wird und den **FlushQueues-Vorgang** beenden muss, wird **TransportNotify** aufgerufen, wobei sowohl die NOTIFY_END_INBOUND_FLUSH als auch NOTIFY_END_OUTBOUND_FLUSH Flags festgelegt sind. Der Transportanbieter sollte alle externen Ressourcen freigeben und zurückgeben. 
  

