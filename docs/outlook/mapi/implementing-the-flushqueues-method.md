---
title: Implementieren der FlushQueues-Methode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8719f8aa-a537-4253-b67d-c4d38c40472b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: baafd8b6437f4febaee9420b274c20ba3242cae6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792586"
---
# <a name="implementing-the-flushqueues-method"></a>Implementieren der FlushQueues-Methode

  
  
**Betrifft**: Outlook 
  
Die MAPI-Warteschlange verwendet die [IXPLogon::FlushQueues](ixplogon-flushqueues.md) Methode herunterladen und Hochladen von ausstehenden Nachrichten zu und von eines Transportdienstes. In der Regel wird die MAPI-Warteschlange leeren Warteschlangen für alle Transportanbieter, die an der Sitzung angemeldeten beginnend mit der ersten Adressbuchhierarchie wie im Abschnitt Reihenfolge Transport Profil des Benutzers festgelegt. Das leeren Warteschlangen ist fast immer das Ergebnis einer direkten Anforderung durch den Benutzer, damit das Senden und Empfangen von Nachrichten, während das Warteschlangen leeren werden an die Warteschlange MAPI synchron ist. Da diese Aufrufe synchron sind, sollte der Adressbuchhierarchie sie so schnell wie möglich verarbeiten. 
  
Transportanbieter müssen **FlushQueues** Anruf gemäß der Beschreibung in der folgenden Schrittfolge um zum Aktivieren der Verarbeitung der richtige Meldung und die externe Ressourcen wie Modems von anderen Anbietern Transport verwendet werden, als Teil der MAPI-Warteschlange aktivieren behandeln. **FlushQueues** Vorgang. 
  
|**Schritt**|**Komponente**|**Implementierung**|
|:-----|:-----|:-----|
|1.  <br/> |MAPI-Warteschlange  <br/> |Ruft die **FlushQueues** -Methode für den ersten Transportanbieter in der Reihenfolge Transport die Benutzerprofils aufgeführt, die die angeforderten Kennzeichen im _UlFlags_ -Parameter übergeben. **FlushQueues** wird einmal mit alle Flags für den gesamten Upload und Download-Operation aufgerufen.  <br/> |
|2.  <br/> |Transportdienst  <br/> |Eine Reihe von Aufgaben vor der Rückgabe des Aufrufs **FlushQueues** ausführen muss. Wenn zuvor übermittelt, dass Nachrichten werden zurückgestellt wird, sollte die [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) -Methode mit dem Flag NOTIFY_SENT_DEFERRED aufgerufen werden. Beachten Sie, dass es möglich, dass die MAPI-Warteschlange abbrechen eine Nachricht, die vor der Adressbuchhierarchie zurückgestellte hat die Möglichkeit, die Nachricht verarbeitet.  <br/> Wenn der Adressbuchhierarchie eine externe Ressource wie ein Modem verwendet wird, sollte die Verbindung zu externen Ressource hergestellt werden.  <br/> Die STATUS_OUTBOUND_FLUSH bit in der Statuszeile des Transportdienstes-Eigenschaft **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) muss mit der [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) -Methode festgelegt werden.  <br/> Der Transportdienst sollte dann S_OK für den Anruf **FlushQueues** zurückgegeben.  <br/> |
|3.  <br/> |MAPI-Warteschlange  <br/> |Der Adressbuchhierarchie Statuszeile für das Bit STATUS_OUTBOUND_FLUSH überprüft und ruft [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) für die erste Meldung in der Warteschlange.  <br/> |
|4.  <br/> |Transportdienst  <br/> |Verarbeitet die Nachricht, und gibt den Anruf **SubmitMessage** zurück.  <br/> |
|5.  <br/> |MAPI-Warteschlange  <br/> |Wenn der Adressbuchhierarchie **SubmitMessage**S_OK zurückgibt, ruft die MAPI-Warteschlange [IXPLogon::EndMessage](ixplogon-endmessage.md) für die Nachricht wie bei regulären Nachricht senden.  <br/> Wenn der Adressbuchhierarchie **SubmitMessage**einen anderen Wert als S_OK zurückgibt, verarbeitet die MAPI-Warteschlange den Wert entsprechend vor dem Aufruf von **EndMessage**oder vor dem Aufruf von **SubmitMessage** erneut.  <br/> |
|6.  <br/> |Transportdienst  <br/> |Wird von **EndMessage** mit dessen Status im _LpulFlags_ -Parameter die Verarbeitung der Nachricht.  <br/> |
|7.  <br/> |MAPI-Warteschlange und Transport-Anbieter  <br/> |Die **SubmitMessage**- **EndMessage** Schleife wird fortgesetzt, bis alle Nachrichten in der Warteschlange übertragen worden sind.  <br/> |
|8.  <br/> |MAPI-Warteschlange  <br/> |Der Adressbuchhierarchie benachrichtigt, dass Nachrichten durch Aufrufen der Adressbuchhierarchie [IXPLogon::TransportNotify](ixplogon-transportnotify.md) -Methode mit dem Flag NOTIFY_END_OUTBOUND_FLUSH Download abgeschlossen ist.  <br/> |
|9.  <br/> |Transportdienst  <br/> |Gibt alle ausgehende Nachrichten senden, damit sie von anderen Anbietern Transport verwendet werden können, um ihre Warteschlangen zu leeren verwendeten externen Ressourcen frei.  <br/> Das bit in der Statuszeile des Transportdienstes-Eigenschaft **PR_STATUS_CODE** STATUS_INBOUND_FLUSH müssen mit **ModifyStatusRow**festgelegt werden.  <br/> |
|10.  <br/> |MAPI-Warteschlange  <br/> |Der Adressbuchhierarchie Statuszeile für das Bit STATUS_INBOUND_FLUSH überprüft und [IXPLogon::StartMessage](ixplogon-startmessage.md) aufgerufen, wenn sie festgelegt ist.  <br/> |
|11.  <br/> |Transportdienst  <br/> |Verarbeitet die Nachricht, und gibt **StartMessage**zurück. Weist der Adressbuchhierarchie anderen Nachrichten hochladen, muss sie mit dem Flag NOTIFY_NEWMAIL **SpoolerNotify** aufrufen.  <br/> Weist der Adressbuchhierarchie keine Nachrichten hochladen, muss sie [IMAPIProp::SaveChanges](imapiprop-savechanges.md) aufrufen, für die Nachricht die MAPI-Warteschlange in **StartMessage** übergeben, und zurückgeben.  <br/> |
|12.  <br/> |MAPI-Warteschlange  <br/> |Ruft weiterhin **StartMessage** bis auf eine Nachricht **SaveChanges** aufgerufen wird. Nachdem der Adressbuchhierarchie hochladen beendet wurde, ruft die MAPI-Warteschlange **TransportNotify** mit der NOTIFY_END_INBOUND_FLUSH-Flag.  <br/> |
|13.  <br/> |Transportdienst  <br/> |Löscht das bit in der **PR_STATUS_CODE** -Eigenschaft der Statuszeile mit **ModifyStatusRow** und Versionen verwenden Sie alle externe Ressourcen, damit sie für verfügbar sind von anderen Anbietern Transport STATUS_INBOUND_FLUSH.  <br/> |
|14.  <br/> |MAPI-Warteschlange  <br/> |Ruft **FlushQueues** für den nächsten Transportanbieter in der Reihenfolge Transport, der das Profil des Benutzers aufgeführt.  <br/> |
   
Wenn eine Client-Anwendung anrufen [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) eines Transportdienstes Status Objekt sollten der Adressbuchhierarchie das entsprechende Bit in der Statuszeile mit **ModifyStatusRow**festlegen. Die MAPI-Warteschlange ruft dann der Adressbuchhierarchie **IXPLogon::FlushQueues** -Methode die MAPI-Warteschlange Ermessen. Wenn als Ergebnis einer Clientanwendung **IMAPIStatus::FlushQueues** Anruf, der Adressbuchhierarchie **IXPLogon::FlushQueues** -Methode aufgerufen wird die Verarbeitung erfolgt asynchron an die Clientanwendung. Andernfalls funktioniert **IXPLogon::FlushQueues** synchron mit der MAPI-Warteschlange. 
  
Aus Leistungsgründen wird die MAPI-Warteschlange nur eines Transportdienstes **FlushQueues** -Methode aufrufen, wenn die Flags STATUS_INBOUND_FLUSH und STATUS_OUTBOUND_FLUSH in der Adressbuchhierarchie Statuszeile festgelegt sind. Daher kann ein Transportdienstes den **FlushQueues** Vorgang können Sie jederzeit durch die Flags STATUS_OUTBOUND_FLUSH und STATUS_INBOUND_FLUSH in der Statuszeile clearing beenden. Wenn die MAPI-Warteschlange heruntergefahren wird und muss den **FlushQueues** Vorgang zu beenden, wird mit der NOTIFY_END_INBOUND_FLUSH und die NOTIFY_END_OUTBOUND_FLUSH Flags **TransportNotify** . Der Transportdienst sollte alle externe Ressourcen freizugeben und zurückzugeben. 
  

