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
ms.openlocfilehash: bf633a971f7e3077ce2f418021ef183a36db8cc8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411092"
---
# <a name="opening-a-message"></a>Öffnen einer Nachricht
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
### <a name="to-open-a-message"></a>So öffnen Sie eine Nachricht
  
1. Rufen Sie die Eintrags-ID der Nachricht aus einer der folgenden Quellen ab:
    
   - Die Zeile, die die Nachricht in der Inhaltstabelle des übergeordneten Ordners darstellt. Weitere Informationen zum Arbeiten mit einer Ordnerinhaltstabelle finden Sie unter [Inhaltstabellen](contents-tables.md).
    
   - Das **lpEntryID** -Element der [NEWMAIL_NOTIFICATION](newmail_notification.md) -Struktur, die mit einer neuen e-Mail-Benachrichtigung gesendet wird. Weitere Informationen zum empfangen und Verarbeiten von Benachrichtigungen finden Sie unter [Handling Notifications](handling-notifications.md).
    
   - Ein Aufruf der [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode der Nachricht, die die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft anfordert. 
    
2. Rufen Sie eine der folgenden **OpenEntry** -Methoden auf, um die Nachricht zu öffnen, und legen Sie _lpEntryID_ auf die Eintrags-ID der Nachricht fest: 
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
  Die schnellste Methode ist nur für eingehende Nachrichten nutzbar und umfasst das Aufrufen der **IMAPIFolder:: OpenEntry** -Methode des Empfänger Ordners. Die nächste schnellste Methode, die **IMsgStore:: OpenEntry** -Methode des Nachrichtenspeichers aufzurufen, ist für alle Nachrichten verwendbar, ebenso wie die langsamste Methode, indem **IMAPISession:: OpenEntry**aufgerufen wird.
    
> [!NOTE]
> Ordner und deren Inhaltstabellen können jederzeit geschlossen werden, ohne dass sich dies nachteilig auf die Nachrichten auswirkt, die in diesen geöffnet wurden. 
  
### <a name="to-open-a-message-that-has-been-saved-on-disk"></a>So öffnen Sie eine Nachricht, die auf dem Datenträger gespeichert wurde
  
1. Rufen Sie **StgOpenStorage** auf, um einen **IStorage** -Schnittstellenzeiger abzurufen, und übergeben Sie den Namen der Nachrichtendatei für den _pwcsName_ -Parameter. 
    
   ```cpp
    LPSTORAGE pStorage = NULL;
    HRESULT hr = StgOpenStorage (L"MESSAGE.MSG", NULL,
                                STGM_TRANSACTED |
                                STGM_READWRITE |
                                STGM_SHARE_EXCLUSIVE,
                                NULL, 0, &pStorage);
    
   ```

2. Aufrufen von **OpenIMsgOnIStg** zum Abrufen eines **IMessage** -Schnittstellenzeigers für den Zugriff auf die Nachricht. 
    
   ```cpp
    LPMESSAGE pMessage = NULL;
    LPMALLOC pMalloc = MAPIGetDefaultMalloc();
    hr = OpenIMsgOnIStg (NULL, MAPIAllocateBuffer, MAPIAllocateMore,
                        MAPIFreeBuffer, pMalloc, NULL, pStorage,
                        NULL, 0, 0, &pMessage);
    
   ```


