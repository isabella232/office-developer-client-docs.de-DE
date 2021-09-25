---
title: IMAPIMessageSiteDeleteMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIMessageSite.DeleteMessage
api_type:
- COM
ms.assetid: 09955996-b904-4c0d-8ba5-954a8875c055
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0fa359f87ec9ea7797e20a33688d67df0bd0b834
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575974"
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
    
## <a name="remarks"></a>HinwBemerkungeneise

Ein Formularobjekt ruft die **IMAPIMessageSite::D eleteMessage-Methode** auf, um die Nachricht zu löschen, die das Formular derzeit anzeigt. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Nach der Rückgabe von **DeleteMessage** müssen Formularobjekte nach einer neuen Nachricht suchen und sich dann selbst schließen, wenn keine vorhanden ist. Um zu bestimmen, ob die Nachricht, für die **DeleteMessage** ausgeführt wurde, gelöscht oder in einen Ordner **"Gelöschte Elemente"** verschoben wurde, kann ein Formularobjekt die [IMAPIMessageSite::GetSiteStatus-Methode](imapimessagesite-getsitestatus.md) aufrufen, um zu bestimmen, ob das DELETE_IS_MOVE Flag zurückgegeben wurde. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn die Implementierung der **DeleteMessage-Methode** eines Formularviewers zur nächsten Nachricht wechselt, nachdem eine Nachricht gelöscht wurde, sollte die Implementierung die [IMAPIViewContext::ActivateNext-Methode](imapiviewcontext-activatenext.md) aufrufen und das VCDIR_DELETE Flag übergeben, bevor der tatsächliche Löschvorgang ausgeführt wird. Wenn die Implementierung von **DeleteMessage** durch eine Formularanzeige die gelöschte Nachricht verschiebt (z. B. in einen Ordner **"Gelöschte Elemente"),** muss die Implementierung Änderungen an der Nachricht speichern, wenn die Nachricht geändert wurde. 
  
Eine typische Implementierung von **DeleteMessage** führt die folgenden Aufgaben aus: 
  
1. Wenn die Implementierung die Nachricht verschiebt, ruft sie die [IPersistMessage::Save-Methode](ipersistmessage-save.md) auf und übergibt **null** im _pMessage-Parameter_ und **"true"** im _fSameAsLoad-Parameter._ 
    
2. Sie ruft die **IMAPIViewContext::ActivateNext-Methode** auf und übergibt das VCDIR_DELETE-Flag im _ulDir-Parameter._ 
    
3. Wenn der **ActivateNext-Aufruf** fehlschlägt, wird er zurückgegeben. Wenn **ActivateNext** S_FALSE zurückgibt, wird die [IPersistMessage::HandsOffMessage-Methode](ipersistmessage-handsoffmessage.md) aufgerufen. 
    
4. Die Nachricht wird gelöscht oder verschoben.
    
Rufen Sie die Windows [GetWindowRect-Funktion](https://msdn.microsoft.com/library/ms633519) auf, um die von einem Formularfenster verwendete **RECT-Struktur** abzurufen. 
  
Eine Liste der Schnittstellen im Zusammenhang mit Formularservern finden Sie unter [MAPI-Formularschnittstellen.](mapi-form-interfaces.md)
  
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

