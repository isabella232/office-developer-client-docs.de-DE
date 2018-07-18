---
title: Senden oder Empfangen einer Nachricht bei Bedarf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 479404c5-4926-402a-aa12-75dd23276d75
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ece5340497f83862b711f076c8c6346e14ec9355
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795498"
---
# <a name="sending-or-receiving-a-message-on-demand"></a>Senden oder Empfangen einer Nachricht bei Bedarf
  
**Betrifft**: Outlook 
  
Clients greifen in der Regel auf das MAPI-Subsystem – die MAPI-Warteschlange und die-Dienstanbieter – den Zeitpunkt der Nachrichtenübermittlung und Empfang von Nachrichten zu behandeln. Jedoch können Sie diese Zeitdauer ändern, mithilfe des Objekts Status, der die MAPI-Warteschlange oder eines Transportdienstes.
  
Die [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) -Methode entfernt alle Nachrichten aus Warteschlangen für eine oder mehrere Adressbuchhierarchie eingehend oder ausgehend. Die folgenden Verfahren werden zwei Verfahren zum Senden oder Empfangen von Nachrichten bei Bedarf beschrieben. Die erste Prozedur verwendet die MAPI-Warteschlange Status-Objekt zum Leeren der Warteschlangen aller Transport Provider im Profil. im zweite Verfahren leert die Warteschlange eines einzigen Anbieters. 
  
### <a name="to-flush-all-incoming-or-outgoing-queues-in-a-single-operation"></a>Um alle ein- oder ausgehenden Warteschlangen in einem einzigen Vorgang zu leeren.
  
1. Rufen Sie [IMAPISession::GetStatusTable](imapisession-getstatustable.md) Zugriff auf die Statustabelle. 
    
2. Rufen Sie die Statustabelle [IMAPITable::SetColumns](imapitable-setcolumns.md) -Methode zum Beschränken der Spalte **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) und **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) festgelegt.
    
3. Erstellen Sie eine eigenschaftseinschränkung mithilfe der Struktur einer [SPropertyRestriction](spropertyrestriction.md) **PR_RESOURCE_TYPE** mit MAPI_SPOOLER übereinstimmen. 
    
4. Rufen Sie [HrQueryAllRows](hrqueryallrows.md), indem Sie in der Struktur **SPropertyRestriction** übergeben, um die Zeile abzurufen, die den Status der Warteschlange MAPI darstellt. 
    
5. Übergeben Sie die Spalte **PR_ENTRYID** an [IMAPISession::OpenEntry](imapisession-openentry.md) , um die MAPI-Warteschlange Statusobjekt zu öffnen. 
    
6. Rufen Sie die MAPI-Warteschlange [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) -Methode übergeben Sie FLUSH_NO_UI Flag unterdrückt die Benutzeroberfläche und die FLUSH_DOWNLOAD oder FLUSH_UPLOAD Flag zum Leeren der Warteschlangen ausgehenden oder eingehenden. 
    
7. Lassen Sie die Status-Objekts und der Tabelle "Status" als auch die [SRowSet](srowset.md) -Struktur, die für die Tabelle zugeordnet ist. 
    
### <a name="to-flush-incoming-or-outgoing-queues-individually-by-transport-provider"></a>Zum ein- oder ausgehende Warteschlangen einzeln durch Adressbuchhierarchie leeren
  
1. Rufen Sie [IMAPISession::GetStatusTable](imapisession-getstatustable.md) Zugriff auf die Statustabelle. 
    
2. Rufen Sie die Statustabelle [IMAPITable::SetColumns](imapitable-setcolumns.md) -Methode zum Beschränken der Spalte **PR_ENTRYID** und **PR_RESOURCE_TYPE**festgelegt.
    
3. Erstellen Sie eine eigenschaftseinschränkung mithilfe der Struktur einer [SPropertyRestriction](spropertyrestriction.md) **PR_RESOURCE_TYPE** mit MAPI_TRANSPORT_PROVIDER übereinstimmen. 
    
4. Rufen Sie [HrQueryAllRows](hrqueryallrows.md), indem Sie in der Struktur **SPropertyRestriction** übergeben, um die Zeilen abrufen, die vom Transportanbieter für bereitgestellt werden. 
    
5. Für jede Zeile aus **HrQueryAllRows**zurückgegeben:
    
    1. Übergeben Sie die Spalte **PR_ENTRYID** [IMAPISession::OpenEntry](imapisession-openentry.md) zum Öffnen der Adressbuchhierarchie Status-Objekts. 
        
    2. Überprüfen Sie, dass der Status Transportobjekt die **FlushQueues** -Methode unterstützt überprüfen, dass dessen **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))-Eigenschaft der STATUS_FLUSH_QUEUES hat flag festgelegt. 
        
    3. Wenn unterstützt, rufen Sie [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md). Wenn nicht unterstützt, rufen Sie die MAPI-Warteschlange **IMAPIStatus::FlushQueues** -Methode, die Eintrags-ID des Transports im _LpTargetTransport_ -Parameter übergeben. Finden Sie im vorherige Verfahren Anweisungen zum Zugreifen auf die MAPI-Warteschlange Status-Objekt. Legen Sie das Kennzeichen FLUSH_DOWNLOAD zum Leeren der ausgehenden Warteschlangen oder FLUSH_UPLOAD-Flag, um die eingehenden Warteschlangen zu leeren. 
        
    4. Lassen Sie die Status-Objekts und der Tabelle "Status" als auch die [SRowSet](srowset.md) -Struktur, die für die Tabelle zugeordnet ist. 
    
Die MAPI-Warteschlange berücksichtigt das Flag FLUSH_NO_UI, wie die meisten LAN-Transport-Anbieter. Nicht alle Transportanbieter für berücksichtigt jedoch dieses Flag, insbesondere solche, die ein Modem explizit verwenden und Remote Access Service (RAS). RAS wurde nicht entwickelt, damit Clients die Benutzeroberfläche installieren können. Es ist möglich, damit ein Client konfiguriert werden, damit es verbinden kann, ohne die Interaktion eines Benutzers, aber es ist schwierig und erfordert sehr gute Kenntnisse über den Client Message-Dienste.
  

