---
title: Öffnen einer Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 142c4975-08df-4501-9996-557aa44eafb3
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d74e26f2968758f31a410a428bd75b70803e5141
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555951"
---
# <a name="opening-a-message"></a>Öffnen einer Nachricht
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
### <a name="to-open-a-message"></a>So öffnen Sie eine Nachricht
  
1. Rufen Sie den Eintragsbezeichner der Nachricht aus einer der folgenden Quellen ab:
    
   - Die Zeile, die die Nachricht im Inhaltsverzeichnis des übergeordneten Ordners darstellt. Weitere Informationen zum Arbeiten mit einem Ordnerinhaltsverzeichnis finden Sie unter [Inhaltstabellen.](contents-tables.md)
    
   - Das **lpEntryID-Mitglied** der [NEWMAIL_NOTIFICATION](newmail_notification.md) Struktur, die mit einer neuen E-Mail-Benachrichtigung gesendet wird. Weitere Informationen zum Empfangen und Behandeln von Benachrichtigungen finden Sie unter ["Behandeln von Benachrichtigungen".](handling-notifications.md)
    
   - Ein Aufruf der [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) der Nachricht, die die **eigenschaft PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) anfordert. 
    
2. Rufen Sie eine der folgenden **OpenEntry-Methoden** auf, um die Nachricht zu öffnen, und legen Sie  _lpEntryID_ auf den Eintragsbezeichner der Nachricht fest: 
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
  Die schnellste Methode kann nur für eingehende Nachrichten verwendet werden und umfasst den Aufruf der **IMAPIFolder::OpenEntry-Methode** des Empfangsordners. Die nächstschnellste Methode, die **IMsgStore::OpenEntry-Methode** des Nachrichtenspeichers aufzurufen, kann für alle Nachrichten verwendet werden, ebenso wie die langsamste Methode, die **IMAPISession::OpenEntry aufruft.**
    
> [!NOTE]
> Ordner und ihre Inhaltstabellen können jederzeit geschlossen werden, ohne dass sich dies negativ auf die Nachrichten auswirkt, die von ihnen aus geöffnet wurden. 
  
### <a name="to-open-a-message-that-has-been-saved-on-disk"></a>So öffnen Sie eine Nachricht, die auf dem Datenträger gespeichert wurde
  
1. Rufen Sie **StgOpenStorage** auf, um einen **IStorage-Schnittstellenzeiger** abzurufen, und übergeben Sie dabei den Namen der Nachrichtendatei für den _pwcsName-Parameter._ 
    
   ```cpp
    LPSTORAGE pStorage = NULL;
    HRESULT hr = StgOpenStorage (L"MESSAGE.MSG", NULL,
                                STGM_TRANSACTED |
                                STGM_READWRITE |
                                STGM_SHARE_EXCLUSIVE,
                                NULL, 0, &pStorage);
    
   ```

2. Rufen Sie **OpenIMsgOnIStg** auf, um einen **IMessage-Schnittstellenzeiger** abzurufen, um auf die Nachricht zuzugreifen. 
    
   ```cpp
    LPMESSAGE pMessage = NULL;
    LPMALLOC pMalloc = MAPIGetDefaultMalloc();
    hr = OpenIMsgOnIStg (NULL, MAPIAllocateBuffer, MAPIAllocateMore,
                        MAPIFreeBuffer, pMalloc, NULL, pStorage,
                        NULL, 0, 0, &pMessage);
    
   ```


