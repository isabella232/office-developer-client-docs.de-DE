---
title: IMAPIMessageSiteSubmitMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.SubmitMessage
api_type:
- COM
ms.assetid: 6b14c383-8bc6-4e86-bd92-0500272af40d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 496732e334d2d39672048dd1a02346aaee4b70e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417028"
---
# <a name="imapimessagesitesubmitmessage"></a>IMAPIMessageSite::SubmitMessage

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fordert an, dass die aktuelle Nachricht für die Übermittlung in die Warteschlange gestellt wird.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> in Eine Bitmaske von Flags, die die Übermittlung einer Nachricht steuert. Das folgende Flag kann festgelegt werden:
    
FORCE_SUBMIT 
  
> MAPI sollte die Nachricht auch dann übermitteln, wenn Sie nicht sofort gesendet werden kann.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Bemerkungen

Formularobjekte rufen die **IMAPIMessageSite:: SubmitMessage** -Methode auf, um anzufordern, dass eine Nachricht für die Übermittlung in die Warteschlange gestellt wird. Die Nachrichtenwebsite sollte vor dem Senden der Nachricht die [IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md) -Methode aufrufen. Die Nachricht muss nicht zuvor gespeichert worden sein, da **SubmitMessage** die Nachricht speichern sollte, wenn die Nachricht geändert wurde. Nach der Rückgabe von **SubmitMessage**muss das Formular nach einer aktuellen Nachricht suchen und sich dann selbst entlassen, wenn keine vorhanden ist. 
  
Eine Liste der Schnittstellen im Zusammenhang mit Formular Servern finden Sie unter [MAPI-Formular Schnittstellen](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: SubmitMessage  <br/> |MFCMAPI verwendet die **IMAPIMessageSite:: SubmitMessage** -Methode, um die Nachricht zu speichern. Zuerst wird die **IPersistMessage:: HandsOffMessage** -Methode aufgerufen, und anschließend wird **SubmitMessage**aufgerufen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MAPI-Formular Schnittstellen](mapi-form-interfaces.md)

