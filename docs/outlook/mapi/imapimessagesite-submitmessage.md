---
title: IMAPIMessageSiteSubmitMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIMessageSite.SubmitMessage
api_type:
- COM
ms.assetid: 6b14c383-8bc6-4e86-bd92-0500272af40d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fce66a5c7a306df2d116f473458e7155739eb750
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630698"
---
# <a name="imapimessagesitesubmitmessage"></a>IMAPIMessageSite::SubmitMessage

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fordert an, dass die aktuelle Nachricht zur Zustellung in die Warteschlange gestellt wird.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie eine Nachricht gesendet wird. Das folgende Kennzeichen kann festgelegt werden:
    
FORCE_SUBMIT 
  
> Die MAPI sollte die Nachricht auch dann übermitteln, wenn sie möglicherweise nicht sofort gesendet wird.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Bemerkungen

Formularobjekte rufen die **IMAPIMessageSite::SubmitMessage-Methode** auf, um anzufordern, dass eine Nachricht zur Zustellung in die Warteschlange gestellt wird. Die Nachrichtenwebsite sollte die [IPersistMessage::HandsOffMessage-Methode](ipersistmessage-handsoffmessage.md) vor dem Senden der Nachricht aufrufen. Die Nachricht muss nicht zuvor gespeichert worden sein, da **SubmitMessage** dazu führen sollte, dass die Nachricht gespeichert wird, wenn die Nachricht geändert wurde. Nach der Rückgabe von **SubmitMessage** muss das Formular nach einer aktuellen Nachricht suchen und sich dann selbst schließen, wenn keine vorhanden ist. 
  
Eine Liste der Schnittstellen im Zusammenhang mit Formularservern finden Sie unter [MAPI-Formularschnittstellen.](mapi-form-interfaces.md)
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::SubmitMessage  <br/> |MFCMAPI verwendet die **IMAPIMessageSite::SubmitMessage-Methode,** um die Nachricht zu speichern. Zuerst wird die **IPersistMessage::HandsOffMessage-Methode** und dann **SubmitMessage** aufgerufen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MAPI-Formularschnittstellen](mapi-form-interfaces.md)

