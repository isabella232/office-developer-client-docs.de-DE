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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329484"
---
# <a name="imapiformadvise"></a>IMAPIForm::Advise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Registriert eine Formularanzeige für Benachrichtigungen über Ereignisse, die sich auf das Formular auswirken.
  
```cpp
HRESULT Advise(
  LPMAPIVIEWADVISESINK pAdvise,
  ULONG FAR * pulConnection
);
```

## <a name="parameters"></a>Parameter

 _pAdvise_
  
> [in] Ein Zeiger auf ein Ansichtssenkenobjekt rät zum Empfangen der nachfolgenden Benachrichtigungen. 
    
 _pulConnection_
  
> [out] Ein Zeiger auf einen Wert ungleich Null, der eine erfolgreiche Benachrichtigungsregistrierung darstellt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Registrierung war erfolgreich.
    
E_OUTOFMEMORY 
  
> Die Registrierung war aufgrund unzureichenden Arbeitsspeichers nicht erfolgreich.
    
## <a name="remarks"></a>Hinweise

Formularbetrachter rufen die **IMAPIForm::Advise-Methode** eines Formulars auf, um sich für Benachrichtigungen zu registrieren, wenn Änderungen am Formular vorgenommen werden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Bewahren Sie eine Kopie des im  _pAdvise-Parameter_ übergebenen Ansichtssenkenzeigers auf, damit Sie die entsprechende [IMAPIViewAdviseSink-Methode](imapiviewadvisesinkiunknown.md) aufrufen können, wenn ein Ereignis auftritt. Rufen Sie die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) der Ansichtssenke auf, um den Zeiger zu behalten, bis die Benachrichtigungsregistrierung abgebrochen wird. Legen Sie den Inhalt des  _Parameters pulConnection_ auf eine Zahl ungleich Null fest. 
  
Viele Formulare implementieren ein Hilfsobjekt, um die Registrierung und nachfolgende Benachrichtigung von Ereignissen zu verarbeiten. 
  
Weitere Informationen zum Benachrichtigungsprozess im Allgemeinen finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md). 
  
Weitere Informationen zu Benachrichtigungen und Formularen finden Sie unter Senden und Empfangen [von Formularbenachrichtigungen](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIForm::Unadvise](imapiform-unadvise.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md)
  
[Senden und Empfangen von Formularbenachrichtigungen](sending-and-receiving-form-notifications.md)

