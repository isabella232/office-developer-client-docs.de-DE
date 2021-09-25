---
title: IMsgStoreNotifyNewMail
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgStore.NotifyNewMail
api_type:
- COM
ms.assetid: d0d003b0-f12f-4422-b71f-26886169461f
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ddc2af722a6cf0535236a2b78d5c01488973bfb0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575686"
---
# <a name="imsgstorenotifynewmail"></a>IMsgStore::NotifyNewMail

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Informiert den Nachrichtenspeicher, den eine neue Nachricht empfangen hat. Diese Methode ist nur durch die MAPI-Warteschlange aufgerufen.
  
```cpp
HRESULT NotifyNewMail(
  LPNOTIFICATION lpNotification
);
```

## <a name="parameters"></a>Parameter

 _lpNotification_
  
> [in] Ein Zeiger auf eine [Benachrichtigung](notification.md) -Struktur, die Benachrichtigung �ber eine neue Nachricht beschreibt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Nachrichtenspeicher wurde erfolgreich benachrichtigt.
    
## <a name="remarks"></a>HinwBemerkungeneise

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

