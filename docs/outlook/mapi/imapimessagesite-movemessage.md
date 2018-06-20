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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0451d8635848705ef912b9a575d6390898251f4f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792220"
---
# <a name="imapimessagesitemovemessage"></a>IMAPIMessageSite::MoveMessage

  
  
**Betrifft**: Outlook 
  
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
  
> [in] Ein Zeiger auf ein [Rechteck](http://msdn.microsoft.com/en-us/library/dd162897%28VS.85%29.aspx) -Struktur, die im Fenstergröße und Position des aktuellen Formulars enthält. Das nächste Formular angezeigt wird auch dieses Fenster Rechteck verwendet. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NO_SUPPORT 
  
> Der Vorgang wird von dieser Site Nachricht nicht unterstützt.
    
## <a name="remarks"></a>Hinweise

Formularobjekte Aufrufen die **IMAPIMessageSite::MoveMessage** -Methode, um die aktuelle Nachricht in einen neuen Ordner zu verschieben. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Ein Formular Viewer-Implementierung von **MoveMessage** muss die [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) -Methode und übergeben die Kennzeichen VCDIR_MOVE vor dem Verschieben tatsächlich der Nachricht in einen neuen Ordner aufrufen. Rufen Sie die Windows [GetWindowRect](http://msdn.microsoft.com/en-us/library/ms633519) -Funktion, um die **Rechteck** -Struktur, die von einem Formular zugrunde Fenster verwendet zu erhalten. 
  
Eine Liste der Schnittstellen im Zusammenhang mit der Formular-Servern finden Sie unter [MAPI-Formulars Schnittstellen](mapi-form-interfaces.md).
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Nach der Rückgabe von **MoveMessage**müssen Formulare für eine aktuelle Nachricht überprüfen und dann schließen, wenn keines vorhanden ist. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::MoveMessage  <br/> |Nicht implementiert.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MAPI-Formulars Schnittstellen](mapi-form-interfaces.md)

