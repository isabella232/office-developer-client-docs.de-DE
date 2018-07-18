---
title: IMAPIMessageSiteDeleteMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.DeleteMessage
api_type:
- COM
ms.assetid: 09955996-b904-4c0d-8ba5-954a8875c055
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: da6de94342c8d8bbd378a3cde2fb065c97632291
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792205"
---
# <a name="imapimessagesitedeletemessage"></a>IMAPIMessageSite::DeleteMessage

  
  
**Betrifft**: Outlook 
  
Löscht die aktuelle Nachricht.
  
```cpp
HRESULT DeleteMessage(
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a>Parameter

 _pViewContext_
  
> [in] Ein Zeiger auf eine Ansicht Context-Objekt.
    
 _prcPosRect_
  
> [in] Ein Zeiger auf ein [Rechteck](http://msdn.microsoft.com/en-us/library/dd162897%28VS.85%29.aspx) -Struktur, die im Fenstergröße und Position des aktuellen Formulars enthält. Das nächste Formular angezeigt wird auch dieses Fenster Rechteck verwendet. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NO_SUPPORT 
  
> Der Vorgang wird von dieser Site Nachricht nicht unterstützt.
    
## <a name="remarks"></a>Bemerkungen

Ein Form-Objekt die **IMAPIMessageSite::DeleteMessage** -Methode aufgerufen, um die Nachricht zu löschen, die das Formular derzeit angezeigt wird. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Nach der Rückgabe von **DeleteMessage**müssen Formular-Objekte für eine neue Nachricht überprüfen und anschließend schließen, wenn keines vorhanden ist. Um zu bestimmen, ob die Nachricht, der **DeleteMessage** reagiert in einen Ordner **Gelöschte Objekte** verschoben oder gelöscht wurde, kann ein Form-Objekt rufen Sie die [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) -Methode, um zu bestimmen, ob das Flag DELETE_IS_MOVE zurückgegeben wurde. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn ein Formular Viewer Implementierung der **DeleteMessage** -Methode auf die nächste Nachricht verschiebt, nachdem sie eine Nachricht gelöscht, sollten die Implementierung rufen Sie die [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) -Methode und übergeben die Kennzeichen VCDIR_DELETE vor dem Ausführen das tatsächliche löschen. Wenn ein Formular Viewer Implementierung der **DeleteMessage** gelöschte Nachricht (beispielsweise in einem Ordner **Gelöschte Elemente** ) verschoben wird, muss die Implementierung der Nachricht speichern, wenn die Nachricht geändert wurde. 
  
**DeleteMessage** eine normale Implementierung werden die folgenden Aufgaben ausgeführt: 
  
1. Wenn die Implementierung die Nachricht verschoben wird, wird die [IPersistMessage::Save](ipersistmessage-save.md) -Methode **null** im _pMessage_ -Parameter und **true** im _fSameAsLoad_ -Parameter übergeben. 
    
2. Sie ruft die **IMAPIViewContext::ActivateNext** -Methode, die das VCDIR_DELETE-Flag in der _UlDir_ -Parameter übergeben. 
    
3. Wenn der **ActivateNext** -Aufruf fehlschlägt, wird zurückgegeben. Wenn **ActivateNext** S_FALSE zurückgibt, wird die [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) -Methode. 
    
4. Löscht oder verschiebt die Nachricht.
    
Rufen Sie die Windows [GetWindowRect](http://msdn.microsoft.com/en-us/library/ms633519) -Funktion, um die **Rechteck** -Struktur, die von einem Formular zugrunde Fenster verwendet zu erhalten. 
  
Eine Liste der Schnittstellen im Zusammenhang mit der Formular-Servern finden Sie unter [MAPI-Formulars Schnittstellen](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::DeleteMessage  <br/> |Nicht implementiert.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MAPI-Formularoberflächen](mapi-form-interfaces.md)

