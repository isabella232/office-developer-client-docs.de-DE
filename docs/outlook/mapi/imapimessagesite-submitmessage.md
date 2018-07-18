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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 694ee8b12b9918502e60c0c6ea92992cc1062945
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792229"
---
# <a name="imapimessagesitesubmitmessage"></a>IMAPIMessageSite::SubmitMessage

  
  
**Betrifft**: Outlook 
  
Fordert, dass die aktuelle Nachricht für die Übermittlung in die Warteschlange gestellt werden.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie eine Nachricht gesendet wird. Das folgende Flag kann festgelegt werden:
    
FORCE_SUBMIT 
  
> MAPI sollten die Nachricht zu übermitteln, auch wenn es nicht sofort gesendet werden kann.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Formularobjekte Aufrufen die **IMAPIMessageSite::SubmitMessage** -Methode, um anzufordern, dass eine Nachricht für die Übermittlung in die Warteschlange gestellt werden. Die Nachricht Website sollten die [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) -Methode aufrufen, bevor die Nachricht zu übermitteln. Die Nachricht muss nicht zuvor gespeichert wurde, da **SubmitMessage** führen sollten die Nachricht gespeichert werden soll, wenn die Nachricht geändert wurde. Nach der Rückgabe von **SubmitMessage**muss das Formular für eine aktuelle Nachricht überprüfen und schließen selbst dann, wenn keines vorhanden ist. 
  
Eine Liste der Schnittstellen im Zusammenhang mit der Formular-Servern finden Sie unter [MAPI-Formulars Schnittstellen](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::SubmitMessage  <br/> |MFCMAPI (engl.) verwendet die **IMAPIMessageSite::SubmitMessage** -Methode, um die Nachricht zu speichern. Zunächst die **IPersistMessage::HandsOffMessage** -Methode aufgerufen, und ruft dann **SubmitMessage**.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MAPI-Formularoberflächen](mapi-form-interfaces.md)

