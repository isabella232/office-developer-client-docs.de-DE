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
ms.openlocfilehash: 03dd0553d0203585850ac5c4f8c91c86ef60236a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321280"
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
  
> Out Ein Zeiger auf einen Zeiger auf die zurückgegebene Schnittstelle für die Nachricht.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
S_FALSE 
  
> Für das Anruf Formular ist derzeit keine Nachricht vorhanden.
    
## <a name="remarks"></a>Bemerkungen

Formulare rufen die **IMAPIMessageSite:: getMessage** -Methode auf, um eine Nachrichten Schnittstelle für die aktuelle Nachricht abzurufen. Die aktuelle Nachricht ist dieselbe Nachricht, die zuvor in der [IPersistMessage:: InitNew](ipersistmessage-initnew.md), [IPersistMessage:: Laden](ipersistmessage-load.md)oder [IPersistMessage: SaveCompleted](ipersistmessage-savecompleted.md) -Methode übergeben wurde. 
  
 **GetMessage** gibt S_FALSE zurück, wenn keine Nachricht vorhanden ist. Dieser Zustand kann nach Aufrufen der [IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md) -Methode oder vor dem nächsten Aufruf von **IPersistMessage:: Laden** oder **IPersistMessage:: SaveCompleted** erfolgen. 
  
Eine Liste der Schnittstellen im Zusammenhang mit Formular Servern finden Sie unter [MAPI-Formular Schnittstellen](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: getSession  <br/> |MFCMAPI verwendet die **IMAPIMessageSite:: getMessage** -Methode, um den aktuell zwischengespeicherten Nachrichten Zeiger zurückzugeben, sofern dieser verfügbar ist.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IPersistMessage::InitNew](ipersistmessage-initnew.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MAPI-Formular Schnittstellen](mapi-form-interfaces.md)

