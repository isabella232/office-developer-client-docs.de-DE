---
title: Öffnen einer Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 142c4975-08df-4501-9996-557aa44eafb3
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e0701e64469576a8241002a6ff11299d1c343556
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582980"
---
# <a name="opening-a-message"></a>Öffnen einer Nachricht
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
### <a name="to-open-a-message"></a>Öffnen eine Nachricht
  
1. Abrufen von Eintrags-ID der Nachricht aus einer der folgenden Quellen:
    
   - Die Zeile, die die Nachricht in der Inhaltstabelle des übergeordneten Ordners darstellt. Weitere Informationen zum Arbeiten mit einem Ordner Inhaltstabelle finden Sie unter [Inhalt Tabellen](contents-tables.md).
    
   - Der **LpEntryID** Member der [NEWMAIL_NOTIFICATION](newmail_notification.md) -Struktur, die mit einer neuen e-Mail-Benachrichtigung gesendet wird. Weitere Informationen zu empfangen und Behandlung Benachrichtigungen finden Sie unter [Behandeln von Benachrichtigungen](handling-notifications.md).
    
   - Anruf an die Nachricht [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode, die Eigenschaft **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) anfordert. 
    
2. Rufen Sie eine der folgenden Methoden **OpenEntry** zum Öffnen der Nachricht, die Einstellung _LpEntryID_ an die Nachricht Eintrags-ID: 
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
  Die schnellste Methode kann nur für eingehende Nachrichten verwendet werden und umfasst den Empfangsordner **IMAPIFolder::OpenEntry** -Methode aufrufen. Die nächste schnellste Methode aufrufen der Nachrichtenspeicher **IMsgStore::OpenEntry** -Methode kann für alle Nachrichten verwendet werden, wie die langsamste-Methode aufrufen **IMAPISession::OpenEntry**ist.
    
> [!NOTE]
> Ordner und deren Inhalt Tabellen können geschlossen werden können Sie jederzeit ohne Beeinträchtigung der keines der Nachrichten, die darin enthaltenen aus geöffnet wurden. 
  
### <a name="to-open-a-message-that-has-been-saved-on-disk"></a>Um eine Nachricht zu öffnen, die auf dem Datenträger gespeichert wurde
  
1. Rufen Sie **StgOpenStorage** zum Abrufen eines **IStorage** Schnittstelle Zeigers, übergeben Sie den Namen der Nachrichtendatei für den Parameter _PwcsName_ . 
    
   ```cpp
    LPSTORAGE pStorage = NULL;
    HRESULT hr = StgOpenStorage (L"MESSAGE.MSG", NULL,
                                STGM_TRANSACTED |
                                STGM_READWRITE |
                                STGM_SHARE_EXCLUSIVE,
                                NULL, 0, &pStorage);
    
   ```

2. Rufen Sie **OpenIMsgOnIStg** zum Abrufen eines **IMessage** -Schnittstelle Zeigers Zugriff auf die Nachricht. 
    
   ```cpp
    LPMESSAGE pMessage = NULL;
    LPMALLOC pMalloc = MAPIGetDefaultMalloc();
    hr = OpenIMsgOnIStg (NULL, MAPIAllocateBuffer, MAPIAllocateMore,
                        MAPIFreeBuffer, pMalloc, NULL, pStorage,
                        NULL, 0, 0, &pMessage);
    
   ```


