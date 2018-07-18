---
title: IMsgStoreNotifyNewMail
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.NotifyNewMail
api_type:
- COM
ms.assetid: d0d003b0-f12f-4422-b71f-26886169461f
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bdda950cd1fab66db46590e0b9141bb3d2a75221
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792624"
---
# <a name="imsgstorenotifynewmail"></a>IMsgStore::NotifyNewMail

  
  
**Betrifft**: Outlook 
  
Informiert den Nachrichtenspeicher, den eine neue Nachricht empfangen hat. Diese Methode ist nur durch die MAPI-Warteschlange aufgerufen.
  
```cpp
HRESULT NotifyNewMail(
  LPNOTIFICATION lpNotification
);
```

## <a name="parameters"></a>Parameter

 _lpNotification_
  
> [in] Ein Zeiger auf eine [Benachrichtigung](notification.md) -Struktur, die Benachrichtigung �ber eine neue Nachricht beschreibt. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Nachrichtenspeicher wurde erfolgreich benachrichtigt.
    
## <a name="remarks"></a>Hinweise

Die **IMsgStore::NotifyNewMail** -Methode wird aufgerufen, durch die MAPI-Warteschlange, um dem Nachrichtenspeicher zu informieren, dass eine Nachricht f�r die �bermittlung bereit ist. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn **NotifyNewMail** aufgerufen wird, senden Sie eine neue e-Mail-Benachrichtigung an alle registrierten Clients. Sie k�nnen die Benachrichtigung durch Aufrufen von [IMAPISupport::Notify](imapisupport-notify.md), wenn Sie die Methoden des Support-Objekts verwenden oder eine eigene Implementierung mit senden. Ein registrierter Clients ist eine [IMsgStore::Advise](imsgstore-advise.md) aufgerufen hat, und legen Sie den  _lpEntryID_ -Parameter auf NULL und der Parameter  _ulEventMask_ _fnevNewMail_. 
  
Nicht �ndern oder den Speicher f�r die [Benachrichtigung](notification.md) -Struktur, die neue e-Mail-Benachrichtigung beschreibt, frei. Kopieren Sie die Struktur **NOTIFICATION** durch Aufrufen der Dienstprogrammfunktion [ScCopyNotifications](sccopynotifications.md) t�tigen Informationen in seine Member verwenden. 
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport::Subscribe](imapisupport-subscribe.md)
  
[IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)
  
[Benachrichtigung](notification.md)
  
[ScCopyNotifications](sccopynotifications.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

