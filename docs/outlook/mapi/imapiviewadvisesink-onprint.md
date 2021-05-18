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
  
Benachrichtigt die Formularanzeige über den Druckstatus eines Formulars.
  
```cpp
HRESULT OnPrint(
ULONG dwPageNumber,
HRESULT hrStatus
);
```

## <a name="parameters"></a>Parameter

 _dwPageNumber_
  
> [in] Die Nummer der letzten gedruckten Seite.
    
 _hrStatus_
  
> [in] Ein HRESULT-Wert, der den Status des Druckauftrags angibt. Die folgenden Werte sind möglich:
    
S_FALSE 
  
> Der Druckauftrag wurde erfolgreich abgeschlossen.
    
S_OK 
  
> Der Druckauftrag wird ausgeführt.
    
FAILED 
  
> Der Druckauftrag wurde aufgrund eines Fehlers beendet.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigung ist erfolgreich.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die Schaltfläche Abbrechen in einem Dialogfeld. 
    
## <a name="remarks"></a>Hinweise

Formularobjekte rufen die **IMAPIViewAdviseSink::OnPrint-Methode** beim Drucken auf, um den Betrachter über den Druckfortschritt zu informieren. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn der Druckauftrag mehrere Seiten umfasst, können Sie **OnPrint** aufrufen, nachdem jede Seite gedruckt wurde. Legen  _Sie dwPageNumber_ auf die Seite, die gerade gedruckt wird, und  _hrStatus_ auf S_OK. Wenn der Druckauftrag abgeschlossen ist, rufen Sie **OnPrint** auf,  _während dwPageNumber_ auf die letzte gedruckte Seite festgelegt ist, und  _hrStatus_ auf S_FALSE. 
  
Weitere Informationen zu Formularbenachrichtigungen finden Sie unter Senden und Empfangen [von Formularbenachrichtigungen](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

