---
title: IMAPIMessageSiteGetMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIMessageSite.GetMessage
api_type:
- COM
ms.assetid: 49d12c49-84f8-44ac-bc4a-2ee44a46f8c1
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1d334a273f0f454c59ea2c28b98e4e5bac6b809d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556623"
---
# <a name="imapimessagesitegetmessage"></a>IMAPIMessageSite::GetMessage

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die aktuelle Nachricht zurück.
  
```cpp
HRESULT GetMessage(
  LPMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a>Parameter

 _ppmsg_
  
> [out] Ein Zeiger auf einen Zeiger auf die zurückgegebene Schnittstelle für die Nachricht.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
S_FALSE 
  
> Für das aufrufende Formular ist derzeit keine Nachricht vorhanden.
    
## <a name="remarks"></a>HinwBemerkungeneise

Formulare rufen die **IMAPIMessageSite::GetMessage-Methode** auf, um eine Nachrichtenschnittstelle für die aktuelle Nachricht abzurufen. Die aktuelle Nachricht ist die gleiche Nachricht wie zuvor in der [IPersistMessage::InitNew](ipersistmessage-initnew.md)-, [IPersistMessage::Load](ipersistmessage-load.md)- oder [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) -Methode übergeben wurde. 
  
 **GetMessage** gibt S_FALSE zurück, wenn derzeit keine Nachricht vorhanden ist. Dieser Zustand kann nach Aufrufen der [IPersistMessage::HandsOffMessage-Methode](ipersistmessage-handsoffmessage.md) oder vor dem nächsten Aufruf von **IPersistMessage::Load** oder **IPersistMessage::SaveCompleted** auftreten. 
  
Eine Liste der Schnittstellen im Zusammenhang mit Formularservern finden Sie unter [MAPI-Formularschnittstellen.](mapi-form-interfaces.md)
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetSession  <br/> |MFCMAPI verwendet die **IMAPIMessageSite::GetMessage-Methode,** um den aktuell zwischengespeicherten Nachrichtenzeiger zurückzugeben, sofern verfügbar.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IPersistMessage::InitNew](ipersistmessage-initnew.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MAPI-Formularschnittstellen](mapi-form-interfaces.md)

