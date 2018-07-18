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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6658f1c4bcfaf7557d9b53c5e70d87e124475580
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792448"
---
# <a name="imapisupportsubscribe"></a>IMAPISupport::Subscribe

  
  
**Betrifft**: Outlook 
  
Registriert ein Advise-Empfänger Erhalt von Benachrichtigungen über MAPI an.
  
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
  
> [in] Ein Zeiger auf eine Benachrichtigung-Schlüssel, der Advise-Source-Objekt darstellt. Der Parameter _LpKey_ darf nicht NULL sein. 
    
 _ulEventMask_
  
> [in] Eine Maske von Werten, mit die die Typen von Benachrichtigungsereignisse anzugeben, die dem Anrufer ist daran interessiert, und die Registrierung einbezogen werden soll. Die folgenden Werte sind gültig:
    
 _fnevCriticalError_
  
> Register für Benachrichtigungen zu schwerwiegenden Fehlern, beispielsweise nicht genügend Arbeitsspeicher.
    
 _fnevExtended_
  
> Speicheranbieter Register für Benachrichtigungen über Ereignisse, die speziell für die bestimmten Adressbuch oder einer Nachricht.
    
 _fnevNewMail_
  
> Register für die Benachrichtigung über den Empfang von neuen Nachrichten. 
    
 _fnevObjectCreated_
  
> Register für die Benachrichtigung über die Erstellung eines neuen Objekts.
    
 _fnevObjectCopied_
  
> Register für Benachrichtigungen zu einem Objekt kopiert wird.
    
 _fnevObjectDeleted_
  
> Register für Benachrichtigungen zu einem Objekt, das gelöscht wird.
    
 _fnevObjectModified_
  
> Register für Benachrichtigungen zu einem Objekt geändert wird.
    
 _fnevObjectMoved_
  
> Register für Benachrichtigungen zu einem Objekt verschoben wird.
    
 _fnevSearchComplete_
  
> Register für die Benachrichtigung über den Abschluss der Suchvorgang.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie die Benachrichtigung erfolgt. Das folgende Flag kann festgelegt werden:
    
NOTIFY_SYNC 
  
> Wenn der Anrufer die [IMAPISupport::Notify](imapisupport-notify.md) -Methode zum Generieren von Benachrichtigungen für diese Advise-Empfänger aufruft, sollten **Benachrichtigen** alle erforderlichen Aufrufe advise-senken, vor der Rückgabe. Wenn dieses Flag nicht festgelegt ist, Benachrichtigung ist asynchron und Rückrufe werden in der Warteschlange für die Prozesse, die sich dafür angemeldet haben und gestartet, wenn die Prozesse der CPU Kontrolle. 
    
 _lpAdviseSink_
  
> [in] Ein Zeiger auf eine Advise-Empfängerobjekt. 
    
 _lpulConnection_
  
> [out] Ein Zeiger auf eine Verbindung ungleich NULL-Zahl, die Registrierung darstellt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die benachrichtigungsregistrierung war erfolgreich.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport::Subscribe** -Methode wird für alle dienstanbieterobjekten Unterstützung implementiert. Dienstanbieter Aufrufen **Abonnieren** von einem ihrer **Advise** -Methoden, um MAPI, um die Benachrichtigungen verwalten zu ermöglichen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um die Methoden des MAPI-Unterstützung für die Benachrichtigung zu verwenden, erstellen Sie einen Product Key für die Advise-Quelle das Objekt über welche Benachrichtigungen generiert werden soll. Der Wert des Schlüssels muss eindeutig sein und auf einfache Weise neu generiert werden sollte jeder Änderung des Objekts. 
  
MAPI verwendet den Benachrichtigung Schlüssel um zu suchenden alle Callback-Funktionen, die über die [HrAllocAdviseSink](hrallocadvisesink.md) -Funktion für die entsprechenden Advise-Quelle registriert. Übergeben Sie dieser Schlüssel an **IMAPISupport::Notify** , wenn Sie eine Benachrichtigung für die entsprechenden Advise-Quelle erstellen müssen. 
  
Das Flag NOTIFY_SYNC wirkt sich auf den Betrieb von nachfolgende Aufrufe **benachrichtigt werden soll**. Wenn Sie NOTIFY_SYNC festlegen, gibt **Benachrichtigen** bis zum Abschluss aller erforderlichen Mitteilungen senden keine zurück. Wenn Sie nicht NOTIFY_SYNC festlegen, arbeitet **Benachrichtigen** asynchron möglicherweise zurückgeben, bevor alle die Benachrichtigungen gesendet wurden. 
  
## <a name="see-also"></a>Siehe auch



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[Benachrichtigung](notification.md)
  
[NOTIFKEY](notifkey.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

