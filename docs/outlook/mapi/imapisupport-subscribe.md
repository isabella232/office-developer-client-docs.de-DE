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
  
Registriert eine Advise-Senke, um Benachrichtigungen über MAPI zu empfangen.
  
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
  
> in Ein Zeiger auf einen Benachrichtigungs Schlüssel, der das Advise-Quellobjekt darstellt. Der _lpKey_ -Parameter darf nicht NULL sein. 
    
 _ulEventMask_
  
> in Eine Maske mit Werten, die die Typen von Benachrichtigungsereignissen angibt, an denen der Anrufer interessiert ist, und die in die Registrierung aufgenommen werden sollen. Die folgenden Werte sind gültig:
    
 _fnevCriticalError_
  
> Registriert Benachrichtigungen zu schwerwiegenden Fehlern, beispielsweise unzureichenden Arbeitsspeicher.
    
 _fnevExtended_
  
> Registriert Benachrichtigungen zu Ereignissen, die spezifisch für das jeweilige Adressbuch oder den Nachrichtenspeicher Anbieter sind.
    
 _Uleventmaskfnevnewmail_
  
> Registriert Benachrichtigungen über das Eintreffen neuer Nachrichten. 
    
 _fnevObjectCreated_
  
> Registriert Benachrichtigungen über die Erstellung eines neuen Objekts.
    
 _fnevObjectCopied_
  
> Registriert Benachrichtigungen zu einem kopierten Objekt.
    
 _fnevObjectDeleted_
  
> Registriert Benachrichtigungen zu einem Objekt, das gelöscht wird.
    
 _fnevObjectModified_
  
> Registriert Benachrichtigungen zu einem Objekt, das geändert wird.
    
 _fnevObjectMoved_
  
> Registriert Benachrichtigungen zu einem Objekt, das verschoben wird.
    
 _fnevSearchComplete_
  
> Registriert Benachrichtigungen über den Abschluss eines Suchvorgangs.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die die Art der Benachrichtigung steuert. Das folgende Flag kann festgelegt werden:
    
NOTIFY_SYNC 
  
> Wenn der Anrufer die [IMAPISupport:: notify](imapisupport-notify.md) -Methode zum Generieren von Benachrichtigungen für diese Advise-Senke aufruft, sollte notify alle erforderlichen Aufrufe für Advise-Empfänger durchführen, bevor **Sie** zurückkehren. Wenn dieses Flag nicht festgelegt ist, ist die Benachrichtigung asynchron, und die Rückrufe werden in die Warteschlange aufgenommen, wenn diese Prozesse die Steuerung der CPU erhalten haben. 
    
 _lpAdviseSink_
  
> in Ein Zeiger auf ein Advise-Senke-Objekt. 
    
 _lpulConnection_
  
> Out Ein Zeiger auf eine Verbindungsnummer ungleich NULL, die die Registrierung darstellt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigungs Registrierung war erfolgreich.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport:: subscribe** -Methode wird für alle Support Objekte des Dienstanbieters implementiert. Dienstanbieter rufen **subscribe** aus einer Ihrer **Advise** -Methoden auf, damit MAPI die Benachrichtigungen verwalten kann. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um die MAPI-Supportmethoden für die Benachrichtigung zu verwenden, erstellen Sie einen Schlüssel für die Advise-Quelle das Objekt, über das Benachrichtigungen generiert werden sollen. Der Wert des Schlüssels muss eindeutig sein und bei jeder Änderung des Objekts leicht neu generiert werden. 
  
MAPI verwendet den Benachrichtigungs Schlüssel, um nach beliebigen Rückruffunktionen zu suchen, die über die [HrAllocAdviseSink](hrallocadvisesink.md) -Funktion für die entsprechende Advise-Quelle registriert sind. Geben Sie diesen Schlüssel an **IMAPISupport:: notify** , wenn Sie eine Benachrichtigung für die entsprechende Advise-Quelle generieren müssen. 
  
Das NOTIFY_SYNC-Flag wirkt sich auf den Vorgang der nachfolgenden Aufrufe von **Notify**aus. Wenn Sie NOTIFY_SYNC festlegen, wird **Notify** erst zurückgegeben, wenn alle erforderlichen Benachrichtigungen gesendet wurden. Wenn Sie NOTIFY_SYNC nicht festlegen, wird **Notify** asynchron ausgeführt, und möglicherweise wird zurückgegeben, bevor alle Benachrichtigungen gesendet wurden. 
  
## <a name="see-also"></a>Siehe auch



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[Benachrichtigung](notification.md)
  
[NOTIFKEY](notifkey.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

