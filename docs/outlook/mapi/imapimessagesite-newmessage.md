---
title: IMAPIMessageSiteNewMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.NewMessage
api_type:
- COM
ms.assetid: ce6b6e6c-7f22-43c2-8182-90cf6db93844
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f51dd1fe533d0577996e6e1be185302f2dc972fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438771"
---
# <a name="imapimessagesitenewmessage"></a>IMAPIMessageSite::NewMessage

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine neue Nachricht.
  
```cpp
HRESULT NewMessage(
  ULONG fComposeInFolder,
  LPMAPIFOLDER pFolderFocus,
  LPPERSISTMESSAGE pPersistMessage,
  LPMESSAGE FAR * ppMessage,
  LPMAPIMESSAGESITE FAR * ppMessageSite,
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a>Parameter

 _fComposeInFolder_
  
> in Gibt an, in welchem Ordner die Nachricht erstellt werden soll. Wenn die Variable auf FALSE festgelegt ist, wird der _pFolderFocus_ -Parameter ignoriert, und der Formular Betrachter kann die Nachricht in einem beliebigen Ordner verfassen. Wenn die Variable auf TRUE festgelegt ist und im _pFolderFocus_ -Parameter NULL übergeben wird, wird die Nachricht im aktuellen Ordner zusammengefasst. Wenn die Variable auf TRUE festgelegt ist und ein Wert ungleich NULL in _pFolderFocus_übergeben wird, wird die Nachricht in dem Ordner zusammengestellt, auf den von _pFolderFocus_verwiesen wird.
    
 _pFolderFocus_
  
> in Ein Zeiger auf den Ordner, in dem die neue Nachricht erstellt wird.
    
 _pPersistMessage_
  
> in Ein Zeiger auf das Form-Objekt für das neue Formular.
    
 _ppMessage_
  
> Out Ein Zeiger auf einen Zeiger auf die neue Nachricht.
    
 _ppMessageSite_
  
> Out Ein Zeiger auf einen Zeiger auf ein Nachrichtenwebsite Objekt für die neue Nachricht.
    
 _ppViewContext_
  
> Out Ein Zeiger auf einen Zeiger auf einen Ansichtskontext, der für die Übergabe an ein neues Formular mit der neuen Nachricht geeignet ist. Wenn das Formular einen eigenen Ansichtskontext implementiert, kann im _ppViewContext_ -Parameter NULL übergeben werden. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Bemerkungen

Formularobjekte rufen die **IMAPIMessageSite:: PostMessage** -Methode auf, um eine neue Nachricht zu erstellen. Das Formular verwendet **** eine neumeldung, um eine neue Nachricht und die zugehörige Nachrichtenwebsite aus ihrer Ansicht abzurufen. Anschließend kann die neue Nachricht geändert werden. 
  
Sie können auch einen zugeordneten Ansichtskontext abrufen, indem Sie einen Wert ungleich NULL im _ppViewContext_ -Parameter übergeben. Dieser Ansichtskontext kann direkt verwendet werden, oder er kann aggregiert und an die neue Nachricht übergeben werden. Wenn eine vollständige Implementierung erforderlich ist, müssen Sie in _ppViewContext_den Wert NULL überschreiten.
  
Eine Liste der Schnittstellen im Zusammenhang mit Formular Servern finden Sie unter [MAPI-Formular Schnittstellen](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: neuNachricht  <br/> |MFCMAPI verwendet die **IMAPIMessageSite:: PostMessage** -Methode, um eine neue Nachricht zu erstellen, einen neuen Formular Betrachter zu **** instanziieren und setpersist aufzurufen, um die Nachricht im Formular-Viewer festzulegen. Schließlich wird der Formular Betrachter als Nachrichtenwebsite zurückgegeben.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MAPI-Formular Schnittstellen](mapi-form-interfaces.md)

