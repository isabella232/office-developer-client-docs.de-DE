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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7b2761e20444c51d08380aee01c41eee797733eb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396491"
---
# <a name="imapimessagesitedeletemessage"></a>IMAPIMessageSite::DeleteMessage

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
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
  
> [in] Ein Zeiger auf ein [Rechteck](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) -Struktur, die im Fenstergröße und Position des aktuellen Formulars enthält. Das nächste Formular angezeigt wird auch dieses Fenster Rechteck verwendet. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NO_SUPPORT 
  
> Der Vorgang wird von dieser Site Nachricht nicht unterstützt.
    
## <a name="remarks"></a>Hinweise

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
    
Rufen Sie die Windows [GetWindowRect](https://msdn.microsoft.com/library/ms633519) -Funktion, um die **Rechteck** -Struktur, die von einem Formular zugrunde Fenster verwendet zu erhalten. 
  
Eine Liste der Schnittstellen im Zusammenhang mit der Formular-Servern finden Sie unter [MAPI-Formulars Schnittstellen](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Kommentar**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::DeleteMessage  <br/> |Nicht implementiert.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MAPI-Formularoberflächen](mapi-form-interfaces.md)

