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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321413"
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
  
> [in] Ein Zeiger auf ein Ansichtskontextobjekt.
    
 _prcPosRect_
  
> [in] Ein Zeiger auf eine [RECT-Struktur,](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) die die Fenstergröße und -position des aktuellen Formulars enthält. Das nächste angezeigte Formular verwendet auch dieses Fensterrechteck. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NO_SUPPORT 
  
> Der Vorgang wird von dieser Nachrichtenwebsite nicht unterstützt.
    
## <a name="remarks"></a>Hinweise

Ein Formularobjekt ruft die **IMAPIMessageSite::D eleteMessage-Methode** auf, um die Nachricht zu löschen, die derzeit im Formular angezeigt wird. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Nach der Rückgabe von **DeleteMessage** müssen Formularobjekte nach einer neuen Nachricht suchen und sich dann selbst schließen, wenn keine vorhanden ist. Um zu ermitteln, ob die Nachricht **DeleteMessage** gelöscht oder in einen Ordner "Gelöschte Elemente" verschoben wurde, kann ein Formularobjekt die [IMAPIMessageSite::GetSiteStatus-Methode](imapimessagesite-getsitestatus.md) aufrufen, um zu ermitteln, ob das DELETE_IS_MOVE-Flag zurückgegeben wurde.  
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn die Implementierung der **DeleteMessage-Methode** durch einen Formularanzeiger zur nächsten Nachricht wechselt, nachdem eine Nachricht gelöscht wurde, sollte die Implementierung die [IMAPIViewContext::ActivateNext-Methode](imapiviewcontext-activatenext.md) aufrufen und das flag VCDIR_DELETE übergeben, bevor der eigentliche Löschvorgang ausgeführt wird. Wenn die Implementierung von **DeleteMessage** durch einen Formularanzeiger die gelöschte Nachricht verschiebt (z. B. in einen Ordner **"Gelöschte** Elemente"), muss die Implementierung Änderungen an der Nachricht speichern, wenn die Nachricht geändert wurde. 
  
Eine typische Implementierung von **DeleteMessage führt** die folgenden Aufgaben aus: 
  
1. Wenn die Implementierung die Nachricht bewegt, ruft sie die [IPersistMessage::Save-Methode](ipersistmessage-save.md) auf, und übergeben **Null** im _pMessage-Parameter_ und **true** im _fSameAsLoad-Parameter._ 
    
2. Es ruft die **IMAPIViewContext::ActivateNext-Methode** auf und über VCDIR_DELETE im _ulDir-Parameter._ 
    
3. Wenn beim **ActivateNext-Aufruf** ein Fehler auftritt, wird er zurückgegeben. Wenn **ActivateNext** S_FALSE zurückgibt, wird die [IPersistMessage::HandsOffMessage-Methode](ipersistmessage-handsoffmessage.md) aufruft. 
    
4. Es löscht oder verschiebt die Nachricht.
    
Um die vom Formularfenster verwendete **RECT-Struktur** zu erhalten, rufen Sie die Windows [GetWindowRect-Funktion](https://msdn.microsoft.com/library/ms633519) auf. 
  
Eine Liste der Schnittstellen im Zusammenhang mit Formularservern finden Sie unter [MAPI Form Interfaces](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::D eleteMessage  <br/> |Nicht implementiert.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MAPI-Formularschnittstellen](mapi-form-interfaces.md)

