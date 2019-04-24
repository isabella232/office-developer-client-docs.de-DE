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
  
> in Ein Zeiger auf ein View-Kontextobjekt.
    
 _prcPosRect_
  
> in Ein Zeiger auf eine [Rect](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) -Struktur, die die Größe und Position des aktuellen Formulars enthält. Das nächste Formular wird auch dieses Fensterrechteck verwendet. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NO_SUPPORT 
  
> Der Vorgang wird von dieser Nachrichtenwebsite nicht unterstützt.
    
## <a name="remarks"></a>Bemerkungen

Ein Form-Objekt ruft die **IMAPIMessageSite::D eletemessage** -Methode auf, um die Nachricht zu löschen, die vom Formular derzeit angezeigt wird. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Nach der Rückgabe von **DeleteMessage**müssen Formularobjekte nach einer neuen Nachricht suchen und dann selbst entlassen werden, wenn keine vorhanden ist. Um zu ermitteln, ob die Nachricht, auf die **DeleteMessage** gehandelt wurde, gelöscht oder in einen Ordner " **Gelöschte Elemente** " verschoben wurde, kann ein Form-Objekt die [IMAPIMessageSite:: GetSiteStatus](imapimessagesite-getsitestatus.md) -Methode aufrufen, um zu bestimmen, ob das DELETE_IS_MOVE-Flag zurückgegeben wurde. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn die Implementierung der **DeleteMessage** -Methode eines Formular Viewers zur nächsten Nachricht wechselt, nachdem eine Nachricht gelöscht wurde, sollte die Implementierung die [IMAPIViewContext:: ActivateNext](imapiviewcontext-activatenext.md) -Methode aufrufen und das VCDIR_DELETE-Flag vor dem Ausführen von der tatsächliche Löschvorgang. Wenn die **DeleteMessage** -Implementierung eines Formular Viewers die gelöschte Nachricht (beispielsweise in einen Ordner " **Gelöschte Elemente** ") verschiebt, muss die Implementierung Änderungen an der Nachricht speichern, wenn die Nachricht geändert wurde. 
  
Eine typische Implementierung von **DeleteMessage** führt die folgenden Aufgaben aus: 
  
1. Wenn die Implementierung die Nachricht verschiebt, ruft Sie die [IPersistMessage:: Save](ipersistmessage-save.md) -Methode auf und **übergibt NULL** im _pMessage_ -Parameter und **true** im _fSameAsLoad_ -Parameter. 
    
2. Die **IMAPIViewContext:: ActivateNext** -Methode wird aufgerufen, und das VCDIR_DELETE-Flag wird im _ulDir_ -Parameter übergeben. 
    
3. Wenn der **ActivateNext** -Aufruf fehlschlägt, wird zurückgegeben. Wenn **ActivateNext** den Wert S_FALSE zurückgibt, wird die [IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md) -Methode aufgerufen. 
    
4. Die Nachricht wird gelöscht oder verschoben.
    
Rufen Sie die Windows- [GetWindowRect](https://msdn.microsoft.com/library/ms633519) -Funktion auf, um die vom Fenster eines Formulars verwendete **Rect** -Struktur abzurufen. 
  
Eine Liste der Schnittstellen im Zusammenhang mit Formular Servern finden Sie unter [MAPI-Formular Schnittstellen](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer::D eleteMessage  <br/> |Nicht implementiert.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MAPI-Formular Schnittstellen](mapi-form-interfaces.md)

