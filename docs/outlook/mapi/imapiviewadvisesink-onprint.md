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
ms.openlocfilehash: 202d461d4acefe18e69b47db9319cb328c61406e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592318"
---
# <a name="imapiviewadvisesinkonprint"></a>IMAPIViewAdviseSink::OnPrint

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Benachrichtigt den Formular-Viewer des Status eines Formulars drucken.
  
```cpp
HRESULT OnPrint(
ULONG dwPageNumber,
HRESULT hrStatus
);
```

## <a name="parameters"></a>Parameter

 _dwPageNumber_
  
> [in] Nummer der letzten Seite gedruckt.
    
 _hrStatus_
  
> [in] Ein HRESULT-Wert, der den Status des Auftrags drucken. Die folgenden Werte sind möglich:
    
S_FALSE 
  
> Der Druckauftrag wurde erfolgreich abgeschlossen.
    
S_OK 
  
> Der Druckauftrag wird gerade durchgeführt.
    
FEHLER BEI 
  
> Der Druckauftrag wurde aufgrund eines Fehlers abgebrochen.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Benachrichtigung war erfolgreich.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche zum Abbrechen in einem Dialogfeld abgebrochen. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Formularobjekte Aufrufen die **IMAPIViewAdviseSink::OnPrint** -Methode beim Drucken um den Viewer drucken Fortschritt zu informieren. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn der Druckauftrag mehrere Seiten umfasst, können Sie **OnPrint** aufrufen, nachdem jeder Seite gedruckt wird. Legen Sie _DwPageNumber_ zur gegenwärtig gedruckte Seite und _HrStatus_ auf S_OK zurück. Wenn der Druckauftrag abgeschlossen ist, legen Sie Anruf festgelegten **OnPrint** mit _DwPageNumber_ auf die letzte Seite gedruckt und _HrStatus_ auf S_FALSE. 
  
Weitere Informationen zum Formular Benachrichtigungen finden Sie unter [Senden und Empfangen von Formular Benachrichtigungen](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

