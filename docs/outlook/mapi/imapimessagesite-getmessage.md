---
title: IMAPIMessageSiteGetMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetMessage
api_type:
- COM
ms.assetid: 49d12c49-84f8-44ac-bc4a-2ee44a46f8c1
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b3cdd9994de3e2a02a5302068881abce57a632a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792209"
---
# <a name="imapimessagesitegetmessage"></a>IMAPIMessageSite::GetMessage

  
  
**Betrifft**: Outlook 
  
Gibt die aktuelle Nachricht zurück.
  
```cpp
HRESULT GetMessage(
  LPMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a>Parameter

 _ppmsg_
  
> [out] Ein Zeiger auf einen Zeiger auf die zurückgegebene Schnittstelle für die Nachricht.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
S_FALSE 
  
> Keine Meldung, die derzeit für das aufrufende Formular vorhanden ist.
    
## <a name="remarks"></a>Bemerkungen

Formulare rufen Sie die **IMAPIMessageSite::GetMessage** -Methode, um eine Nachricht-Schnittstelle für die aktuelle Nachricht zu erhalten. Die aktuelle Nachricht ist die gleiche Nachricht an, wie zuvor in der [IPersistMessage::InitNew](ipersistmessage-initnew.md), [IPersistMessage::Load](ipersistmessage-load.md)oder [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) -Methode übergeben wurde. 
  
 **GetMessage** gibt S_FALSE zurück, wenn derzeit keine Meldung befindet. Dieser Status kann auftreten, nach dem Anrufe an die [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) -Methode oder vor dem nächsten Aufruf von **IPersistMessage::Load** oder **IPersistMessage::SaveCompleted** erfolgt. 
  
Eine Liste der Schnittstellen im Zusammenhang mit der Formular-Servern finden Sie unter [MAPI-Formulars Schnittstellen](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetSession  <br/> |MFCMAPI (engl.) verwendet die **IMAPIMessageSite::GetMessage** -Methode den Zeiger aktuell zwischengespeicherten Meldung zurückgegeben, sofern es vorhanden ist.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IPersistMessage::InitNew](ipersistmessage-initnew.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MAPI-Formularoberflächen](mapi-form-interfaces.md)

