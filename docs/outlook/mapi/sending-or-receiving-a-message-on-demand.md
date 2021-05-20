---
title: Senden oder Empfangen einer Nachricht nach Bedarf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 479404c5-4926-402a-aa12-75dd23276d75
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 15b9c8c5a56b6f37464d2469bd1d7b3e24596502
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436370"
---
# <a name="sending-or-receiving-a-message-on-demand"></a>Senden oder Empfangen einer Nachricht nach Bedarf
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clients verwenden in der Regel das MAPI-Subsystem – den MAPI-Spooler und die Dienstanbieter –, um den Zeitpunkt der Nachrichtenübermittlung und des Empfangs zu verarbeiten. Sie können diese Zeitplanung jedoch ändern, indem Sie das Statusobjekt des MAPI-Spoolers oder eines Transportanbieters verwenden.
  
Die [IMAPIStatus::FlushQueues-Methode](imapistatus-flushqueues.md) entfernt alle Nachrichten aus den ein- oder ausgehenden Warteschlangen eines oder mehreren Transportanbieters. In den folgenden Verfahren werden zwei Techniken zum Senden oder Empfangen von Nachrichten bei Bedarf beschrieben. Bei der ersten Prozedur wird das Statusobjekt des #A0 verwendet, um die Warteschlangen aller Transportanbieter im Profil zu leeren. Beim zweiten Verfahren wird die Warteschlange eines einzelnen Transportanbieters geleert. 
  
### <a name="to-flush-all-incoming-or-outgoing-queues-in-a-single-operation"></a>So leeren Sie alle eingehenden oder ausgehenden Warteschlangen in einem einzelnen Vorgang
  
1. Rufen [Sie IMAPISession::GetStatusTable auf,](imapisession-getstatustable.md) um auf die Statustabelle zu zugreifen. 
    
2. Rufen Sie die [IMAPITable::SetColumns-Methode](imapitable-setcolumns.md) der Statustabelle auf, um den Spaltensatz auf **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) und **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) zu beschränken.
    
3. Erstellen Sie eine Eigenschaftseinschränkung mithilfe einer [SPropertyRestriction-Struktur,](spropertyrestriction.md) um PR_RESOURCE_TYPE **mit** MAPI_SPOOLER. 
    
4. Rufen [Sie HrQueryAllRows auf,](hrqueryallrows.md)und übergeben Sie die **SPropertyRestriction-Struktur,** um die Zeile abzurufen, die den Status des MAPI-Spoolers darstellt. 
    
5. Übergeben Sie **PR_ENTRYID-Spalte** [an IMAPISession::OpenEntry,](imapisession-openentry.md) um das Statusobjekt des MAPI-Spoolers zu öffnen. 
    
6. Rufen Sie die [IMAPIStatus::FlushQueues-Methode](imapistatus-flushqueues.md) des MAPI-Spoolers auf, übergeben Sie das FLUSH_NO_UI-Flag, um die Benutzeroberfläche zu unterdrücken, und entweder das flag FLUSH_DOWNLOAD oder FLUSH_UPLOAD, um die ausgehenden oder eingehenden Warteschlangen zu leeren. 
    
7. Geben Sie das Statusobjekt und die Statustabelle sowie die [SRowSet-Struktur](srowset.md) frei, die der Tabelle zugeordnet ist. 
    
### <a name="to-flush-incoming-or-outgoing-queues-individually-by-transport-provider"></a>So leeren Sie eingehende oder ausgehende Warteschlangen einzeln nach Transportanbieter
  
1. Rufen [Sie IMAPISession::GetStatusTable auf,](imapisession-getstatustable.md) um auf die Statustabelle zu zugreifen. 
    
2. Rufen Sie die [IMAPITable::SetColumns-Methode](imapitable-setcolumns.md) der Statustabelle auf, um den Spaltensatz auf PR_ENTRYID **und** **PR_RESOURCE_TYPE.**
    
3. Erstellen Sie eine Eigenschaftseinschränkung mithilfe einer [SPropertyRestriction-Struktur,](spropertyrestriction.md) um PR_RESOURCE_TYPE **mit** MAPI_TRANSPORT_PROVIDER. 
    
4. Rufen [Sie HrQueryAllRows auf,](hrqueryallrows.md)und übergeben Sie die **SPropertyRestriction-Struktur,** um die Zeilen abzurufen, die von Transportanbietern bereitgestellt werden. 
    
5. Für jede Zeile, die von **HrQueryAllRows zurückgegeben wird:**
    
    1. Übergeben Sie **PR_ENTRYID-Spalte** an [IMAPISession::OpenEntry,](imapisession-openentry.md) um das Statusobjekt des Transportanbieters zu öffnen. 
        
    2. Überprüfen Sie, ob das Transportstatusobjekt die **FlushQueues-Methode** **unterstützt,** indem Sie überprüfen, ob die PR_RESOURCE_METHODS ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) -Eigenschaft über die STATUS_FLUSH_QUEUES verfügt. 
        
    3. Wenn unterstützt, rufen Sie [IMAPIStatus::FlushQueues auf.](imapistatus-flushqueues.md) Wenn dies nicht unterstützt wird, rufen Sie die **IMAPIStatus::FlushQueues-Methode** des MAPI-Spoolers auf, und übergeben Sie den Eintragsbezeichner des Transports im _lpTargetTransport-Parameter._ Anweisungen zum Zugriff auf das Statusobjekt des MAPI-Spoolers finden Sie im vorherigen Verfahren. Legen Sie das FLUSH_DOWNLOAD, um die ausgehenden Warteschlangen oder das FLUSH_UPLOAD zu leeren, um die eingehenden Warteschlangen zu leeren. 
        
    4. Geben Sie das Statusobjekt und die Statustabelle sowie die [SRowSet-Struktur](srowset.md) frei, die der Tabelle zugeordnet ist. 
    
Der MAPI-Spooler berücksichtigt das FLUSH_NO_UI wie die meisten LAN-Transportanbieter. Diese Kennzeichnung wird jedoch nicht von allen Transportanbietern berücksichtigt, insbesondere denen, die explizit ein Modem verwenden, und dem Remotezugriffsdienst (RAS). RAS wurde nicht so konzipiert, dass Clients die Benutzeroberfläche unterdrücken können. Es ist möglich, dass ein Client so konfiguriert wird, dass er eine Verbindung herstellen kann, ohne dass die Interaktion eines Benutzers erforderlich ist. Dies ist jedoch schwierig und erfordert intime Kenntnisse der Nachrichtendienste des Clients.
  

