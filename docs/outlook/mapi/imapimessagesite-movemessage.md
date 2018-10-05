---
title: IMAPIMessageSiteMoveMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.MoveMessage
api_type:
- COM
ms.assetid: cd4d7b11-fad0-4f05-a99e-9567abcab45c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c68e4fbda661a119416918a2c35d1780f1deccda
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382372"
---
# <a name="imapimessagesitemovemessage"></a>IMAPIMessageSite::MoveMessage

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verschiebt die aktuelle Nachricht in einen Ordner.
  
```cpp
HRESULT MoveMessage(
  LPFOLDER pFolderDestination,
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a>Parameter

 _pFolderDestination_
  
> [in] Ein Zeiger auf den Ordner, in dem die Nachricht verschoben werden.
    
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

Formularobjekte Aufrufen die **IMAPIMessageSite::MoveMessage** -Methode, um die aktuelle Nachricht in einen neuen Ordner zu verschieben. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Ein Formular Viewer-Implementierung von **MoveMessage** muss die [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) -Methode und übergeben die Kennzeichen VCDIR_MOVE vor dem Verschieben tatsächlich der Nachricht in einen neuen Ordner aufrufen. Rufen Sie die Windows [GetWindowRect](https://msdn.microsoft.com/library/ms633519) -Funktion, um die **Rechteck** -Struktur, die von einem Formular zugrunde Fenster verwendet zu erhalten. 
  
Eine Liste der Schnittstellen im Zusammenhang mit der Formular-Servern finden Sie unter [MAPI-Formulars Schnittstellen](mapi-form-interfaces.md).
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Nach der Rückgabe von **MoveMessage**müssen Formulare für eine aktuelle Nachricht überprüfen und dann schließen, wenn keines vorhanden ist. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Kommentar**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::MoveMessage  <br/> |Nicht implementiert.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MAPI-Formularoberflächen](mapi-form-interfaces.md)

