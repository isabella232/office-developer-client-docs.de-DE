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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356476"
---
# <a name="sending-or-receiving-a-message-on-demand"></a>Senden oder Empfangen einer Nachricht nach Bedarf
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clients verwenden in der Regel das MAPI-Subsystem, die MAPI-Warteschlange und die Dienstanbieter, um den Zeitpunkt der Nachrichtenübermittlung und des Empfangs zu behandeln. Sie können dieses Timing jedoch ändern, indem Sie das Status-Objekt entweder des MAPI-Spoolers oder eines Transportanbieters verwenden.
  
Mit der [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) -Methode werden alle Nachrichten aus den eingehenden oder ausgehenden Warteschlangen eines oder mehrerer Transportanbieter entfernt. In den folgenden Verfahren werden zwei Techniken zum Senden oder empfangen von Nachrichten bei Bedarf beschrieben. Das erste Verfahren verwendet das Status-Objekt des MAPI-Spoolers, um die Warteschlangen aller Transportanbieter im Profil zu leeren. bei der zweiten Prozedur wird die Warteschlange eines einzelnen Transportanbieters geleert. 
  
### <a name="to-flush-all-incoming-or-outgoing-queues-in-a-single-operation"></a>So leeren Sie alle eingehenden oder ausgehenden Warteschlangen in einem einzelnen Vorgang
  
1. Rufen Sie [IMAPISession::](imapisession-getstatustable.md) getstatusable auf, um auf die Statustabelle zuzugreifen. 
    
2. Rufen Sie die [IMAPITable::](imapitable-setcolumns.md) SetColumns-Methode der Statustabelle auf, um den Spaltensatz auf **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) und **PR_RESOURCE_TYPE** ([pidtagresourcetype (](pidtagresourcetype-canonical-property.md)) einzuschränken.
    
3. Erstellen Sie eine Eigenschaftseinschränkung mithilfe einer [SPropertyRestriction](spropertyrestriction.md) -Struktur, um **PR_RESOURCE_TYPE** mit MAPI_SPOOLER zu vergleichen. 
    
4. Rufen Sie [HrQueryAllRows](hrqueryallrows.md)auf, und übergeben Sie die **SPropertyRestriction** -Struktur, um die Zeile abzurufen, die den Status des MAPI-Spoolers darstellt. 
    
5. Führen Sie die **PR_ENTRYID** -Spalte an [IMAPISession:: OpenEntry](imapisession-openentry.md) , um das Statusobjekt des MAPI-Spoolers zu öffnen. 
    
6. Rufen Sie die [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) -Methode des MAPI-Spoolers auf, und übergeben Sie das FLUSH_NO_UI-Flag, um die Benutzeroberfläche und das FLUSH_DOWNLOAD-oder FLUSH_UPLOAD-Flag zum leeren der ausgehenden oder eingehenden Warteschlangen zu unterdrücken. 
    
7. Geben Sie das Status-und die Status-Tabelle sowie die [SRowSet](srowset.md) -Struktur frei, die für die Tabelle reserviert ist. 
    
### <a name="to-flush-incoming-or-outgoing-queues-individually-by-transport-provider"></a>So leeren Sie eingehende oder ausgehende Warteschlangen einzeln über den Transportanbieter
  
1. Rufen Sie [IMAPISession::](imapisession-getstatustable.md) getstatusable auf, um auf die Statustabelle zuzugreifen. 
    
2. Rufen Sie die [IMAPITable::](imapitable-setcolumns.md) SetColumns-Methode der Statustabelle auf, um den Spaltensatz auf **PR_ENTRYID** und **PR_RESOURCE_TYPE**zu begrenzen.
    
3. Erstellen Sie eine Eigenschaftseinschränkung mithilfe einer [SPropertyRestriction](spropertyrestriction.md) -Struktur, um **PR_RESOURCE_TYPE** mit MAPI_TRANSPORT_PROVIDER zu vergleichen. 
    
4. Rufen Sie [HrQueryAllRows](hrqueryallrows.md)auf, und übergeben Sie die **SPropertyRestriction** -Struktur, um die Zeilen abzurufen, die von Transportanbietern bereitgestellt werden. 
    
5. Für jede Zeile, die von **HrQueryAllRows**zurückgegeben wird:
    
    1. Führen Sie die **PR_ENTRYID** -Spalte an [IMAPISession:: OpenEntry](imapisession-openentry.md) , um das Status-Objekt des Transportanbieters zu öffnen. 
        
    2. Überprüfen Sie, ob das Transportstatus Objekt die **FlushQueues** -Methode unterstützt, indem Sie überprüfen, ob die **PR_RESOURCE_METHODS** ([PIDTAGRESOURCEMETHODS (](pidtagresourcemethods-canonical-property.md))-Eigenschaft das STATUS_FLUSH_QUEUES-Flag festgelegt ist. 
        
    3. Wenn unterstützt, rufen Sie [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md). Wenn diese nicht unterstützt wird, rufen Sie die **IMAPIStatus:: FlushQueues** -Methode des MAPI-Spoolers auf, und übergeben Sie den Eintragsbezeichner des Transports im _lpTargetTransport_ -Parameter. Im vorherigen Verfahren finden Sie Anweisungen für den Zugriff auf das Statusobjekt des MAPI-Spoolers. Legen Sie das FLUSH_DOWNLOAD-Flag so fest, dass die ausgehenden Warteschlangen oder das FLUSH_UPLOAD-Flag geleert werden. 
        
    4. Geben Sie das Status-und die Status-Tabelle sowie die [SRowSet](srowset.md) -Struktur frei, die für die Tabelle reserviert ist. 
    
Der MAPI-Spooler würdigt das FLUSH_NO_UI-Flag wie die meisten LAN-Transportanbieter. Nicht alle Transportanbieter Ehren dieses Flag, insbesondere solche, die explizit ein Modem verwenden, und den RAS-Dienst. RAS wurde nicht entwickelt, um Clients das Unterdrücken der Benutzeroberfläche zu ermöglichen. Es ist möglich, dass ein Client so konfiguriert ist, dass er eine Verbindung herstellen kann, ohne die Interaktion eines Benutzers zu erfordern, aber es ist schwierig und erfordert eine genaue Kenntnis der Nachrichtendienste des Clients.
  

