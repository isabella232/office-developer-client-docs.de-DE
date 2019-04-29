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
  
Der MAPI-Spooler verwendet die [IXPLogon:: FlushQueues](ixplogon-flushqueues.md) -Methode zum herunterladen und hochladen ausstehender Nachrichten an einen und von einem Transportanbieter. In der Regel werden die Warteschlangen für alle Transportanbieter geleert, die bei der Sitzung angemeldet sind, beginnend mit dem ersten Transportanbieter, der im Abschnitt Transportauftrag des Benutzerprofils festgelegt ist. Das Leeren von Warteschlangen ist fast immer das Ergebnis einer direkten Anforderung des Benutzers, sodass das Senden und empfangen von Nachrichten während der leeren Warteschlangen synchron mit dem MAPI-Spooler erfolgt. Da diese Anrufe synchron sind, sollte der Transportanbieter Sie so schnell wie möglich verarbeiten. 
  
Transport Anbieter müssen den **FlushQueues** -Aufruf wie in der folgenden Abfolge von Schritten beschrieben behandeln, um die ordnungsgemäße Nachrichtenverarbeitung zu aktivieren und um zu ermöglichen, dass externe Ressourcen wie Modems von anderen Transportanbietern als Teil der MAPI-Warteschlangen verwendet werden. **FlushQueues** -Vorgang. 
  
|**Schritt**|**Komponente**|**Implementierung**|
|:-----|:-----|:-----|
|1.  <br/> |MAPI-Spooler  <br/> |Ruft die **FlushQueues** -Methode für den ersten Transportanbieter auf, der in der Transport Reihenfolge des Benutzerprofils aufgeführt ist, und übergibt die angeforderten Flags im _ulFlags_ -Parameter. **FlushQueues** wird einmal aufgerufen, wenn alle Flags für den gesamten Upload-und Downloadvorgang festgelegt sind.  <br/> |
|2.  <br/> |Transport Anbieter  <br/> |Vor der Rückgabe vom **FlushQueues** -Aufruf muss eine Reihe von Aufgaben ausgeführt werden. Wenn zuvor übermittelte Nachrichten verzögert werden, sollte die [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) -Methode mit dem NOTIFY_SENT_DEFERRED-Flag-Satz aufgerufen werden. Beachten Sie, dass es dem MAPI-Spooler möglich ist, eine Nachricht abzubrechen, die verzögert wurde, bevor der Transportanbieter die Verarbeitung der Nachricht abschließen kann.  <br/> Wenn der Transportanbieter eine externe Ressource wie ein Modem verwendet, sollte die Verbindung mit der externen Ressource hergestellt werden.  <br/> Das STATUS_OUTBOUND_FLUSH-Bit in der **PR_STATUS_CODE** ([pidtagstatuscode (](pidtagstatuscode-canonical-property.md))-Eigenschaft der Status Zeile des Transportanbieters muss mithilfe der [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) -Methode festgelegt werden.  <br/> Der Transportanbieter sollte dann S_OK für den **FlushQueues** -Aufruf zurückgeben.  <br/> |
|3.  <br/> |MAPI-Spooler  <br/> |Überprüft die Statuszeile des Transportanbieters für das STATUS_OUTBOUND_FLUSH-Bit und ruft [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) für die erste Nachricht in der Warteschlange auf.  <br/> |
|4.  <br/> |Transport Anbieter  <br/> |Verarbeitet die Nachricht und gibt den **SubmitMessage** -Aufruf zurück.  <br/> |
|5.  <br/> |MAPI-Spooler  <br/> |Wenn der Transportanbieter S_OK von **SubmitMessage**zurückgibt, ruft der MAPI-Spooler [IXPLogon:: EndMessage](ixplogon-endmessage.md) für die Nachricht auf, wie beim regulären Senden von Nachrichten.  <br/> Wenn der Transportanbieter einen anderen Wert als S_OK aus **SubmitMessage**zurückgibt, verarbeitet der MAPI-Spooler den Wert vor dem Aufruf von **EndMessage**oder vor dem Aufruf von **SubmitMessage** .  <br/> |
|6.  <br/> |Transport Anbieter  <br/> |Gibt von **EndMessage** mit dem Status der Nachrichtenverarbeitung im Parameter _lpulFlags_ zurück.  <br/> |
|7.  <br/> |MAPI-Spooler und Transportanbieter  <br/> |Die **SubmitMessage**- -**EndMessage** -Schleife wird fortgesetzt, bis alle Nachrichten in der Warteschlange heruntergeladen wurden.  <br/> |
|8.  <br/> |MAPI-Spooler  <br/> |Benachrichtigt den Transportanbieter, dass das Herunterladen von Nachrichten beendet wurde, indem die [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) -Methode des Transportanbieters mit dem NOTIFY_END_OUTBOUND_FLUSH-Flagsatz aufgerufen wird.  <br/> |
|9.  <br/> |Transport Anbieter  <br/> |Gibt externe Ressourcen frei, die beim Senden ausgehender Nachrichten verwendet werden, damit Sie von anderen Transportanbietern zum leeren der Warteschlangen verwendet werden können.  <br/> Das STATUS_INBOUND_FLUSH-Bit in der **PR_STATUS_CODE** -Eigenschaft der Status Zeile des Transportanbieters muss mithilfe von **ModifyStatusRow**festgelegt werden.  <br/> |
|10.  <br/> |MAPI-Spooler  <br/> |Überprüft die Statuszeile des Transportanbieters für das STATUS_INBOUND_FLUSH-Bit und ruft [IXPLogon:: StartMessage](ixplogon-startmessage.md) auf, wenn es festgelegt ist.  <br/> |
|11.  <br/> |Transport Anbieter  <br/> |Verarbeitet die Nachricht und gibt von **StartMessage**zurück. Wenn der Transportanbieter andere Nachrichten hochladen muss, sollte er **SpoolerNotify** mit dem NOTIFY_NEWMAIL-Flag-Satz aufrufen.  <br/> Wenn der Transportanbieter keine Nachrichten hochladen kann, sollte er [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) für die Nachricht aufrufen, die der MAPI-Spooler in **StartMessage** übergeben hat, und zurückgeben.  <br/> |
|12.  <br/> |MAPI-Spooler  <br/> |Der Aufruf von **StartMessage** wird fortgesetzt, bis **SaveChanges** für eine Nachricht aufgerufen wird. Nachdem der Transportanbieter das Hochladen beendet hat, ruft der MAPI-Spooler **TransportNotify** mit dem NOTIFY_END_INBOUND_FLUSH-Kennzeichen Satz auf.  <br/> |
|13.  <br/> |Transport Anbieter  <br/> |Löscht das STATUS_INBOUND_FLUSH-Bit in der **PR_STATUS_CODE** -Eigenschaft seiner Status Zeile mithilfe von **ModifyStatusRow** und gibt alle externen Ressourcen frei, damit Sie von anderen Transportanbietern zur Verfügung stehen.  <br/> |
|14.  <br/> |MAPI-Spooler  <br/> |Ruft **FlushQueues** für den nächsten Transportanbieter auf, der in der Transport Reihenfolge des Benutzerprofils aufgeführt ist.  <br/> |
   
Wenn eine Clientanwendung [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) für das Statusobjekt eines Transportanbieters aufruft, sollte der Transportanbieter das entsprechende Bit in der Statuszeile mit **ModifyStatusRow**festlegen. Der MAPI-Spooler ruft dann die **IXPLogon:: FlushQueues** -Methode des Transportanbieters an der Bequemlichkeit des MAPI-Spoolers auf. Wenn die **IXPLogon:: FlushQueues** -Methode des Transportanbieters als Ergebnis eines Aufrufs von **IMAPIStatus:: FlushQueues** einer Clientanwendung aufgerufen wird, wird der Vorgang asynchron für die Clientanwendung ausgeführt. Andernfalls **IXPLogon:: FlushQueues** arbeitet synchron mit dem MAPI-Spooler. 
  
Aus Leistungsgründen ruft der MAPI-Spooler nur die **FlushQueues** -Methode eines Transportanbieters auf, wenn die Flags STATUS_INBOUND_FLUSH und STATUS_OUTBOUND_FLUSH in der Status Zeile des Transportanbieters festgelegt sind. Daher kann ein Transportanbieter den **FlushQueues** -Vorgang jederzeit beenden, indem die Flags STATUS_OUTBOUND_FLUSH und STATUS_INBOUND_FLUSH in der Status Zeile gelöscht werden. Wenn der MAPI-Spooler heruntergefahren wird und den **FlushQueues** -Vorgang beenden muss, wird **TransportNotify** sowohl mit der NOTIFY_END_INBOUND_FLUSH-als auch der NOTIFY_END_OUTBOUND_FLUSH-Flags-Gruppe aufgerufen. Der Transportanbieter sollte alle externen Ressourcen freigeben und zurückgeben. 
  

