---
title: IMAPIViewAdviseSinkOnPrint
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnPrint
api_type:
- COM
ms.assetid: d16219a0-268c-428d-9f02-4f06eb5b6d7d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e66315042f8b5cd5aff0e4aa076588c9f312376a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406171"
---
# <a name="imapiviewadvisesinkonprint"></a>IMAPIViewAdviseSink::OnPrint

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Benachrichtigt den Formular Betrachter über den Druckstatus eines Formulars.
  
```cpp
HRESULT OnPrint(
ULONG dwPageNumber,
HRESULT hrStatus
);
```

## <a name="parameters"></a>Parameter

 _dwPageNumber_
  
> in Die Nummer der letzten Seite, die gedruckt wurde.
    
 _hrStatus_
  
> in Ein HRESULT-Wert, der den Status des Druckauftrags angibt. Die folgenden Werte sind möglich:
    
S_FALSE 
  
> Der Druckauftrag wurde erfolgreich abgeschlossen.
    
S_OK 
  
> Der Druckauftrag wird ausgeführt.
    
NICHT 
  
> Der Druckauftrag wurde aufgrund eines Fehlers abgebrochen.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigung wurde erfolgreich ausgeführt.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, indem er in einem Dialogfeld auf die Schaltfläche Abbrechen geklickt hat. 
    
## <a name="remarks"></a>Bemerkungen

Formularobjekte rufen beim Drucken die **IMAPIViewAdviseSink:: OnPrint** -Methode auf, um den Betrachter über den Druckfortschritt zu informieren. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn der Druckauftrag mehrere Seiten umfasst, können Sie **OnPrint** aufrufen, nachdem jede Seite gedruckt wurde. Legen Sie _dwPageNumber_ auf die Seite fest, die derzeit gedruckt wird, und _hrStatus_ auf S_OK. Wenn der Druckauftrag abgeschlossen ist, rufen **** Sie OnPrint mit _dwPageNumber_ auf die letzte Seite gedruckt festgelegt und _hrStatus_ auf S_FALSE festgelegt. 
  
Weitere Informationen zu Formular Benachrichtigungen finden Sie unter [senden und empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

