---
title: IMAPISupportSubscribe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.Subscribe
api_type:
- COM
ms.assetid: e6baaff1-446e-431a-a09b-9b529153382b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bc65b07ef27c0738a58ef5ef13cb699f4c23d32c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625399"
---
# <a name="imapisupportsubscribe"></a>IMAPISupport::Subscribe

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Registriert eine Empfehlungssenke, um Benachrichtigungen über MAPI zu erhalten.
  
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
  
> [in] Ein Zeiger auf einen Benachrichtigungsschlüssel, der das Empfehlungsquellobjekt darstellt. Der  _lpKey-Parameter_ darf nicht NULL sein. 
    
 _ulEventMask_
  
> [in] Eine Maske mit Werten, die die Typen von Benachrichtigungsereignissen angibt, an denen der Aufrufer interessiert ist, und die in die Registrierung einbezogen werden sollten. Die folgenden Werte sind gültig:
    
 _fnevCriticalError_
  
> Registriert Benachrichtigungen zu schwerwiegenden Fehlern, z. B. zu wenig Arbeitsspeicher.
    
 _fnevExtended_
  
> Registriert für Benachrichtigungen zu Ereignissen, die für den jeweiligen Adressbuch- oder Nachrichtenspeicheranbieter spezifisch sind.
    
 _fnevNewMail_
  
> Registriert sich für Benachrichtigungen über das Eintreffen neuer Nachrichten. 
    
 _fnevObjectCreated_
  
> Registriert Benachrichtigungen über die Erstellung eines neuen Objekts.
    
 _fnevObjectCopied_
  
> Registriert Benachrichtigungen über ein objekt, das kopiert wird.
    
 _fnevObjectDeleted_
  
> Registriert Benachrichtigungen über ein objekt, das gelöscht wird.
    
 _fnevObjectModified_
  
> Registriert Benachrichtigungen über ein Objekt, das geändert wird.
    
 _fnevObjectMoved_
  
> Registriert Benachrichtigungen über ein Objekt, das verschoben wird.
    
 _fnevSearchComplete_
  
> Registriert Benachrichtigungen über den Abschluss eines Suchvorgangs.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie die Benachrichtigung erfolgt. Das folgende Kennzeichen kann festgelegt werden:
    
NOTIFY_SYNC 
  
> Wenn der Aufrufer die [IMAPISupport::Notify-Methode](imapisupport-notify.md) aufruft, um Benachrichtigungen für diese Empfehlungssenke zu generieren, sollte **Notify** alle erforderlichen Aufrufe durchführen, um Senken vor der Rückgabe zu empfehlen. Wenn dieses Flag nicht festgelegt ist, ist die Benachrichtigung asynchron, und Rückrufe werden in die Warteschlange der Prozesse eingereiht, die abonniert und gestartet wurden, wenn diese Prozesse die Kontrolle über die CPU erhalten. 
    
 _lpAdviseSink_
  
> [in] Ein Zeiger auf ein Empfehlungssenkenobjekt. 
    
 _lpulConnection_
  
> [out] Ein Zeiger auf eine Nicht-Null-Verbindungsnummer, die die Registrierung darstellt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigungsregistrierung war erfolgreich.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport::Subscribe-Methode** wird für alle Supportobjekte des Dienstanbieters implementiert. Dienstanbieter rufen **Subscribe** von einer ihrer **"Advise"-Methoden** auf, damit MAPI die Benachrichtigungen verwalten kann. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um die MAPI-Unterstützungsmethoden für Benachrichtigungen zu verwenden, erstellen Sie einen Schlüssel für die Empfehlungsquelle des Objekts, zu dem Benachrichtigungen generiert werden sollen. Der Wert des Schlüssels muss eindeutig sein und sollte bei jeder Objektänderung leicht neu generiert werden. 
  
MAPI verwendet den Benachrichtigungsschlüssel, um nach rückruffunktionen zu suchen, die über die [HrAllocAdviseSink-Funktion](hrallocadvisesink.md) für die entsprechende Empfehlungsquelle registriert sind. Übergeben Sie diesen Schlüssel an **IMAPISupport::Notify,** wenn Sie eine Benachrichtigung für die entsprechende Empfehlungsquelle generieren müssen. 
  
Die NOTIFY_SYNC-Kennzeichnung wirkt sich auf den Vorgang nachfolgender Aufrufe von **Notify** aus. Wenn Sie NOTIFY_SYNC festlegen, wird **"Notify"** erst zurückgegeben, wenn alle erforderlichen Benachrichtigungen gesendet wurden. Wenn Sie NOTIFY_SYNC nicht festlegen, wird **Notify** asynchron ausgeführt und wird möglicherweise zurückgegeben, bevor alle Benachrichtigungen gesendet wurden. 
  
## <a name="see-also"></a>Siehe auch



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[Benachrichtigung](notification.md)
  
[NOTIFKEY](notifkey.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

