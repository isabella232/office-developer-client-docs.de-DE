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
  
Fordert an, dass die aktuelle Nachricht zur Zustellung in die Warteschlange eingereiht wird.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie eine Nachricht übermittelt wird. Das folgende Flag kann festgelegt werden:
    
FORCE_SUBMIT 
  
> MAPI sollte die Nachricht übermitteln, auch wenn sie möglicherweise nicht sofort gesendet wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Formularobjekte rufen die **IMAPIMessageSite::SubmitMessage-Methode** auf, um anzuerlangen, dass eine Nachricht zur Zustellung in die Warteschlange gestellt wird. Die Nachrichtenwebsite sollte die [IPersistMessage::HandsOffMessage-Methode](ipersistmessage-handsoffmessage.md) aufrufen, bevor die Nachricht übermittelt wird. Die Nachricht muss nicht zuvor gespeichert worden sein, da **SubmitMessage** dazu führen sollte, dass die Nachricht gespeichert wird, wenn die Nachricht geändert wurde. Nach der Rückgabe von **SubmitMessage** muss das Formular nach einer aktuellen Nachricht suchen und sich dann selbst schließen, wenn keine vorhanden ist. 
  
Eine Liste der Schnittstellen im Zusammenhang mit Formularservern finden Sie unter [MAPI Form Interfaces](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::SubmitMessage  <br/> |MFCMAPI verwendet die **IMAPIMessageSite::SubmitMessage-Methode,** um die Nachricht zu speichern. Zunächst wird die **IPersistMessage::HandsOffMessage-Methode** und dann **SubmitMessage aufruft.**  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MAPI-Formularschnittstellen](mapi-form-interfaces.md)

