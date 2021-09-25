---
title: IMAPIViewAdviseSinkOnPrint
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIViewAdviseSink.OnPrint
api_type:
- COM
ms.assetid: d16219a0-268c-428d-9f02-4f06eb5b6d7d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 69f560903ef0fa1430007818cc364752fd9eaeae
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556482"
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

 _wetterPageNumber_
  
> [in] Die Nummer der letzten gedruckten Seite.
    
 _hrStatus_
  
> [in] Ein HRESULT-Wert, der den Status des Druckauftrags angibt. Die folgenden Werte sind möglich:
    
S_FALSE 
  
> Der Druckauftrag wurde erfolgreich abgeschlossen.
    
S_OK 
  
> Der Druckauftrag wird gerade ausgeführt.
    
FEHLGESCHLAGEN 
  
> Der Druckauftrag wurde aufgrund eines Fehlers beendet.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigung war erfolgreich.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die Schaltfläche Abbrechen in einem Dialogfeld. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Formularobjekte rufen die **IMAPIViewAdviseSink::OnPrint-Methode** beim Drucken auf, um den Betrachter über den Druckfortschritt zu informieren. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn der Druckauftrag mehrere Seiten umfasst, können Sie **OnPrint** aufrufen, nachdem jede Seite gedruckt wurde. Legen Sie  _"wetterPageNumber"_ auf die seite fest, die gerade gedruckt wird, und  _"hrStatus"_ auf S_OK. Wenn der Druckauftrag abgeschlossen ist, rufen **Sie "OnPrint"** auf, wobei  _"wetterPageNumber"_ auf die letzte gedruckte Seite und  _"hrStatus"_ auf S_FALSE festgelegt ist. 
  
Weitere Informationen zu Formularbenachrichtigungen finden Sie unter [Senden und Empfangen von Formularbenachrichtigungen.](sending-and-receiving-form-notifications.md)
  
## <a name="see-also"></a>Siehe auch



[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

