---
title: IMAPISupportSubscribe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Subscribe
api_type:
- COM
ms.assetid: e6baaff1-446e-431a-a09b-9b529153382b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5a8c288e877078ece6ab2da8c6494d96e1714ad7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419926"
---
# <a name="imapisupportsubscribe"></a>IMAPISupport::Subscribe

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Registriert eine Ratensenke, um Benachrichtigungen über MAPI zu erhalten.
  
```cpp
HRESULT Subscribe(
LPNOTIFKEY lpKey,
ULONG ulEventMask,
ULONG ulFlags,
LPMAPIADVISESINK lpAdviseSink,
ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a>Parameter

 _lpKey_
  
> [in] Ein Zeiger auf einen Benachrichtigungsschlüssel, der das advise-Quellobjekt darstellt. Der  _lpKey-Parameter_ darf nicht NULL sein. 
    
 _ulEventMask_
  
> [in] Eine Maske mit Werten, die die Arten von Benachrichtigungsereignissen angibt, die der Anrufer interessiert und in die Registrierung einbezogen werden sollte. Die folgenden Werte sind gültig:
    
 _fnevCriticalError_
  
> Registriert für Benachrichtigungen über schwerwiegende Fehler, z. B. unzureichenden Arbeitsspeicher.
    
 _fnevExtended_
  
> Registriert für Benachrichtigungen über Ereignisse, die für den jeweiligen Adressbuch- oder Nachrichtenspeicheranbieter spezifisch sind.
    
 _fnevNewMail_
  
> Registriert für Benachrichtigungen über das Eintreffen neuer Nachrichten. 
    
 _fnevObjectCreated_
  
> Registriert für Benachrichtigungen über die Erstellung eines neuen Objekts.
    
 _fnevObjectCopied_
  
> Registriert für Benachrichtigungen über ein objekt, das kopiert wird.
    
 _fnevObjectDeleted_
  
> Registriert für Benachrichtigungen über ein zu löschendes Objekt.
    
 _fnevObjectModified_
  
> Registriert für Benachrichtigungen über ein zu änderndes Objekt.
    
 _fnevObjectMoved_
  
> Registriert für Benachrichtigungen über ein verschobenes Objekt.
    
 _fnevSearchComplete_
  
> Registriert für Benachrichtigungen über den Abschluss eines Suchvorgangs.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie die Benachrichtigung erfolgt. Das folgende Flag kann festgelegt werden:
    
NOTIFY_SYNC 
  
> Wenn der Aufrufer die [IMAPISupport::Notify-Methode](imapisupport-notify.md) aufruft, um Benachrichtigungen für diese Absenke zu generieren, sollte **Notify** alle erforderlichen Aufrufe zur Beratung von Senken vor der Rückgabe machen. Wenn dieses Flag nicht festgelegt ist, ist die Benachrichtigung asynchron, und Rückrufe werden in die Warteschlange der Prozesse eingereiht, die abonniert und gestartet wurden, wenn diese Prozesse die Kontrolle über die CPU erlangen. 
    
 _lpAdviseSink_
  
> [in] Ein Zeiger auf ein Advise Sink-Objekt. 
    
 _lpulConnection_
  
> [out] Ein Zeiger auf eine Verbindungsnummer ungleich Null, die die Registrierung darstellt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigungsregistrierung war erfolgreich.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::Subscribe-Methode** ist für alle Dienstanbieterunterstützungsobjekte implementiert. Dienstanbieter rufen **Subscribe über** eine ihrer **Advise-Methoden** auf, damit MAPI die Benachrichtigungen verwalten kann. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um die MAPI-Supportmethoden für die Benachrichtigung zu verwenden, erstellen Sie einen Schlüssel für die Quelle des Hinweises, über den Benachrichtigungen generiert werden sollen. Der Wert des Schlüssels muss eindeutig sein und sollte bei jeder Änderung des Objekts problemlos neu generiert werden. 
  
MAPI verwendet den Benachrichtigungsschlüssel, um nach Rückruffunktionen zu suchen, die über die [HrAllocAdviseSink-Funktion](hrallocadvisesink.md) für die entsprechende Advise-Quelle registriert sind. Übergeben Sie diesen Schlüssel **an IMAPISupport::Notify,** wenn Sie eine Benachrichtigung für die entsprechende Ratenquelle generieren müssen. 
  
Das NOTIFY_SYNC wirkt sich auf den Betrieb nachfolgender Aufrufe von **Notify aus.** Wenn Sie NOTIFY_SYNC, wird **Notify** erst dann angezeigt, wenn alle erforderlichen Benachrichtigungen gesendet wurden. Wenn Sie keine NOTIFY_SYNC, wird **Notify** asynchron betrieben und möglicherweise vor dem Senden aller Benachrichtigungen zurückgeschickt. 
  
## <a name="see-also"></a>Siehe auch



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[Benachrichtigung](notification.md)
  
[NOTIFKEY](notifkey.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

