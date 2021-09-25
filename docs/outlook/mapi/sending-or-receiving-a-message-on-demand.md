---
title: Senden oder Empfangen einer Nachricht nach Bedarf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 479404c5-4926-402a-aa12-75dd23276d75
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3f239b996d157ba5d15c5f2af22b4ea585d09d47
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609481"
---
# <a name="sending-or-receiving-a-message-on-demand"></a>Senden oder Empfangen einer Nachricht nach Bedarf
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clients verlassen sich in der Regel auf das MAPI-Subsystem – den MAPI-Spooler und die Dienstanbieter – um den Zeitpunkt der Nachrichtenübertragung und des Empfangs zu verarbeiten. Sie können diesen Zeitpunkt jedoch mithilfe des Statusobjekts des MAPI-Spoolers oder eines Transportanbieters ändern.
  
Die [IMAPIStatus::FlushQueues-Methode](imapistatus-flushqueues.md) entfernt alle Nachrichten aus den ein- oder ausgehenden Warteschlangen eines oder mehrerer Transportanbieter. In den folgenden Verfahren werden zwei Verfahren zum Senden oder Empfangen von Nachrichten bei Bedarf beschrieben. Die erste Prozedur verwendet das Statusobjekt des MAPI-Poolers, um die Warteschlangen jedes Transportanbieters im Profil zu leeren. Die zweite Prozedur leert die Warteschlange eines einzelnen Transportanbieters. 
  
### <a name="to-flush-all-incoming-or-outgoing-queues-in-a-single-operation"></a>So leeren Sie alle ein- oder ausgehenden Warteschlangen in einem einzigen Vorgang
  
1. Rufen Sie [IMAPISession::GetStatusTable](imapisession-getstatustable.md) auf, um auf die Statustabelle zuzugreifen. 
    
2. Rufen Sie die [IMAPITable::SetColumns-Methode](imapitable-setcolumns.md) der Statustabelle auf, um den Spaltensatz auf **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) und **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) zu beschränken.
    
3. Erstellen Sie eine Eigenschaftseinschränkung mithilfe einer [SPropertyRestriction-Struktur,](spropertyrestriction.md) um **PR_RESOURCE_TYPE** mit MAPI_SPOOLER übereinzuordnen. 
    
4. Rufen Sie [HrQueryAllRows](hrqueryallrows.md)auf, und übergeben Sie die **SPropertyRestriction-Struktur,** um die Zeile abzurufen, die den Status des MAPI-Spoolers darstellt. 
    
5. Übergeben Sie die **PR_ENTRYID** Spalte an [IMAPISession::OpenEntry,](imapisession-openentry.md) um das Statusobjekt des MAPI-Spoolers zu öffnen. 
    
6. Rufen Sie die [IMAPIStatus::FlushQueues-Methode](imapistatus-flushqueues.md) des MAPI-Spoolers auf, und übergeben Sie das flag FLUSH_NO_UI, um die Benutzeroberfläche zu unterdrücken, und entweder das FLUSH_DOWNLOAD oder FLUSH_UPLOAD Flag, um die ausgehenden oder eingehenden Warteschlangen zu leeren. 
    
7. Geben Sie das Statusobjekt und die Statustabelle sowie die [SRowSet-Struktur](srowset.md) frei, die für die Tabelle zugeordnet ist. 
    
### <a name="to-flush-incoming-or-outgoing-queues-individually-by-transport-provider"></a>So leeren Sie eingehende oder ausgehende Warteschlangen einzeln nach Transportanbieter
  
1. Rufen Sie [IMAPISession::GetStatusTable](imapisession-getstatustable.md) auf, um auf die Statustabelle zuzugreifen. 
    
2. Rufen Sie die [IMAPITable::SetColumns-Methode](imapitable-setcolumns.md) der Statustabelle auf, um den Spaltensatz auf **PR_ENTRYID** und **PR_RESOURCE_TYPE** zu beschränken.
    
3. Erstellen Sie eine Eigenschaftseinschränkung mithilfe einer [SPropertyRestriction-Struktur,](spropertyrestriction.md) um **PR_RESOURCE_TYPE** mit MAPI_TRANSPORT_PROVIDER übereinzuordnen. 
    
4. Rufen Sie [HrQueryAllRows](hrqueryallrows.md)auf, und übergeben Sie die **SPropertyRestriction-Struktur,** um die Zeilen abzurufen, die von Transportanbietern bereitgestellt werden. 
    
5. Für jede von **HrQueryAllRows zurückgegebene** Zeile:
    
    1. Übergeben Sie die **spalte PR_ENTRYID** an [IMAPISession::OpenEntry,](imapisession-openentry.md) um das Statusobjekt des Transportanbieters zu öffnen. 
        
    2. Überprüfen Sie, ob das Transportstatusobjekt die **FlushQueues-Methode** unterstützt, indem Sie überprüfen, ob für die **eigenschaft PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) das STATUS_FLUSH_QUEUES Flag festgelegt ist. 
        
    3. Wenn dies unterstützt wird, rufen Sie [IMAPIStatus::FlushQueues auf.](imapistatus-flushqueues.md) Wenn dies nicht unterstützt wird, rufen Sie die **IMAPIStatus::FlushQueues-Methode** des MAPI-Spoolers auf, und übergeben Sie den Eintragsbezeichner des Transports im _LpTargetTransport-Parameter._ Anweisungen zum Zugriff auf das Statusobjekt des MAPI-Spoolers finden Sie im vorherigen Verfahren. Legen Sie das flag FLUSH_DOWNLOAD fest, um die ausgehenden Warteschlangen zu leeren, oder das flag FLUSH_UPLOAD, um die eingehenden Warteschlangen zu leeren. 
        
    4. Geben Sie das Statusobjekt und die Statustabelle sowie die [SRowSet-Struktur](srowset.md) frei, die für die Tabelle zugeordnet ist. 
    
Der MAPI-Spooler berücksichtigt das FLUSH_NO_UI Flag wie die meisten LAN-Transportanbieter. Dieses Kennzeichen wird jedoch nicht von allen Transportanbietern beachtet, insbesondere bei denen, die explizit ein Modem und den RAS (Remote Access Service) verwenden. RAS wurde nicht so konzipiert, dass Clients die Benutzeroberfläche unterdrücken können. Es ist möglich, dass ein Client so konfiguriert wird, dass er eine Verbindung herstellen kann, ohne dass die Interaktion eines Benutzers erforderlich ist. Dies ist jedoch schwierig und erfordert fundierte Kenntnisse der Nachrichtendienste des Clients.
  

