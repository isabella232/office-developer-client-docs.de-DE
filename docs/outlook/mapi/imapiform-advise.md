---
title: IMAPIFormAdvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIForm.Advise
api_type:
- COM
ms.assetid: 961318d6-bebe-4f4b-98ff-921cafc68d24
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 398644605e3ad1020ce594bc8d74593fdede6ad4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567599"
---
# <a name="imapiformadvise"></a>IMAPIForm::Advise

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Registriert eine Formularanzeige für Benachrichtigungen zu Ereignissen, die sich auf das Formular auswirken.
  
```cpp
HRESULT Advise(
  LPMAPIVIEWADVISESINK pAdvise,
  ULONG FAR * pulConnection
);
```

## <a name="parameters"></a>Parameter

 _pAdvise_
  
> [in] Ein Zeiger auf eine Ansicht empfiehlt einem Senkenobjekt, die nachfolgenden Benachrichtigungen zu erhalten. 
    
 _pulConnection_
  
> [out] Ein Zeiger auf einen Wert ungleich Null, der eine erfolgreiche Benachrichtigungsregistrierung darstellt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Registrierung war erfolgreich.
    
E_OUTOFMEMORY 
  
> Die Registrierung war aufgrund unzureichenden Arbeitsspeichers nicht erfolgreich.
    
## <a name="remarks"></a>HinwBemerkungeneise

Formularviewer rufen die **IMAPIForm::Advise-Methode** eines Formulars auf, um sich für Benachrichtigungen zu registrieren, wenn Änderungen am Formular auftreten. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Behalten Sie eine Kopie der Ansicht raten Senkenzeiger in den  _Parameter pAdvise_ übergeben, damit Sie es verwenden können, um die entsprechende [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) -Methode aufzurufen, wenn ein Ereignis auftritt. Rufen Sie die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) der Ansicht auf, um den Zeiger beizubehalten, bis die Benachrichtigungsregistrierung abgebrochen wird. Legen Sie den Inhalt des  _pulConnection-Parameters_ auf eine Zahl ungleich Null fest. 
  
Viele Formulare implementieren ein Hilfsobjekt, um die Registrierung und nachfolgende Benachrichtigung über Ereignisse zu behandeln. 
  
Weitere Informationen zum Benachrichtigungsprozess im Allgemeinen finden Sie unter [Ereignisbenachrichtigung in MAPI.](event-notification-in-mapi.md) 
  
Weitere Informationen zu Benachrichtigungen und Formularen finden Sie unter [Senden und Empfangen von Formularbenachrichtigungen.](sending-and-receiving-form-notifications.md)
  
## <a name="see-also"></a>Siehe auch



[IMAPIForm::Unadvise](imapiform-unadvise.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md)
  
[Senden und Empfangen von Formularbenachrichtigungen](sending-and-receiving-form-notifications.md)

