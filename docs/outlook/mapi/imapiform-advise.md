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
  
Registriert einen Formular-Viewer für Benachrichtigungen zu Ereignissen, die das Formular betreffen.
  
```cpp
HRESULT Advise(
  LPMAPIVIEWADVISESINK pAdvise,
  ULONG FAR * pulConnection
);
```

## <a name="parameters"></a>Parameter

 _pAdvise_
  
> in Ein Zeiger auf eine Ansicht Advise Sink-Objekt, das die nachfolgenden Benachrichtigungen empfangen. 
    
 _pulConnection_
  
> Out Ein Zeiger auf einen Wert ungleich NULL, der eine erfolgreiche Benachrichtigungs Registrierung darstellt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Registrierung war erfolgreich.
    
E_OUTOFMEMORY 
  
> Die Registrierung war aufgrund unzureichenden Arbeitsspeichers nicht erfolgreich.
    
## <a name="remarks"></a>Bemerkungen

Formular Betrachter rufen die **IMAPIForm:: Advise** -Methode eines Formulars auf, um bei Änderungen am Formular eine Benachrichtigung zu registrieren. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Halten Sie eine Kopie des Ansichts-Advise-Senke-Zeigers im _pAdvise_ -Parameter übergeben, damit Sie Sie verwenden können, um die entsprechende [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) -Methode aufzurufen, wenn ein Ereignis eintritt. Rufen Sie die [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) -Methode der View-Advise-Senke auf, um den Zeiger beizubehalten, bis die Benachrichtigungs Registrierung abgebrochen wird. Legen Sie den Inhalt des _pulConnection_ -Parameters auf eine Zahl ungleich NULL fest. 
  
Viele Formulare implementieren ein Hilfsobjekt zur Behandlung der Registrierung und der nachfolgenden Benachrichtigung über Ereignisse. 
  
Weitere Informationen zum Benachrichtigungsprozess im Allgemeinen finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md). 
  
Weitere Informationen zu Benachrichtigungen und Formularen finden Sie unter [senden und empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIForm::Unadvise](imapiform-unadvise.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md)
  
[Senden und empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md)

