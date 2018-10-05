---
title: IMAPIFormAdvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.Advise
api_type:
- COM
ms.assetid: 961318d6-bebe-4f4b-98ff-921cafc68d24
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2ed8bace97dee3842243ed835769e80e8aaf6b03
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387531"
---
# <a name="imapiformadvise"></a>IMAPIForm::Advise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Registriert einen Formular-Viewer für Benachrichtigungen über Ereignisse, die Einfluss auf das Formular.
  
```cpp
HRESULT Advise(
  LPMAPIVIEWADVISESINK pAdvise,
  ULONG FAR * pulConnection
);
```

## <a name="parameters"></a>Parameter

 _pAdvise_
  
> [in] Ein Zeiger auf eine Ansicht advise Empfängerobjekt, um nachfolgenden Benachrichtigungen zu erhalten. 
    
 _pulConnection_
  
> [out] Ein Zeiger auf einen Wert ungleich NULL, der eine erfolgreiche benachrichtigungsregistrierung darstellt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Registrierung erfolgreich war.
    
E_OUTOFMEMORY 
  
> Die Registrierung war nicht erfolgreich, da nicht genügend Arbeitsspeicher.
    
## <a name="remarks"></a>Hinweise

Formular Viewer Aufrufen eines Formulars **IMAPIForm::Advise** -Methode, um für die Benachrichtigung zu registrieren, falls sich das Formular. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Beibehalten einer Kopie der Ansicht advise-Empfängerzeiger im _pAdvise_ -Parameter übergeben werden, sodass Sie sie verwenden können, die entsprechende [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) -Methode aufrufen, wenn ein Ereignis auftritt. Aufruf der Ansicht Teilen des Empfängers [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) -Methode, die den Zeiger beibehalten werden, bis benachrichtigungsregistrierung abgebrochen wird. Legen Sie den Inhalt des Parameters _PulConnection_ auf eine Zahl ungleich NULL. 
  
Viele Formulare implementieren Sie ein Objekt, um die Registrierung und nachfolgende Benachrichtigung über Ereignisse behandelt werden sollen. 
  
Weitere Informationen zu den Benachrichtigungsprozess im Allgemeinen finden Sie unter [Event Notification in MAPI](event-notification-in-mapi.md). 
  
Weitere Informationen zu Benachrichtigungen und Formulare finden Sie unter [Senden und Empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIForm::Unadvise](imapiform-unadvise.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md)
  
[Senden und Empfangen von Formularbenachrichtigungen](sending-and-receiving-form-notifications.md)

