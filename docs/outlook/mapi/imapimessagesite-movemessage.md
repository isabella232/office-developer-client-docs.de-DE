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
ms.openlocfilehash: c68e4fbda661a119416918a2c35d1780f1deccda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321365"
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
  
> in Ein Zeiger auf den Ordner, in den die Nachricht verschoben werden soll.
    
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

Formularobjekte rufen die **IMAPIMessageSite:: MoveMessage** -Methode auf, um die aktuelle Nachricht in einen neuen Ordner zu verschieben. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die Implementierung von **MoveMessage** durch einen Formular Betrachter muss die [IMAPIViewContext:: ActivateNext](imapiviewcontext-activatenext.md) -Methode aufrufen und das VCDIR_MOVE-Flag übergeben, bevor die Nachricht tatsächlich in einen neuen Ordner bewegt wird. Rufen Sie die Windows- [GetWindowRect](https://msdn.microsoft.com/library/ms633519) -Funktion auf, um die vom Fenster eines Formulars verwendete **Rect** -Struktur abzurufen. 
  
Eine Liste der Schnittstellen im Zusammenhang mit Formular Servern finden Sie unter [MAPI-Formular Schnittstellen](mapi-form-interfaces.md).
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Nach der Rückgabe von **MoveMessage**müssen Formulare nach einer aktuellen Nachricht suchen und sich dann selbst entlassen, wenn keine vorhanden ist. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: MoveMessage  <br/> |Nicht implementiert.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MAPI-Formular Schnittstellen](mapi-form-interfaces.md)

