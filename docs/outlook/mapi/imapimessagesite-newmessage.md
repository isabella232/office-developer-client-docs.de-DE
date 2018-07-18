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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7062e0b73d2d70be12fb9cead6813ef9c36fdd43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792224"
---
# <a name="imapimessagesitenewmessage"></a>IMAPIMessageSite::NewMessage

  
  
**Betrifft**: Outlook 
  
Erstellt eine neue Nachricht an.
  
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
  
> [in] Gibt an, in welchem Ordner die Nachricht verfasst werden sollte. Wenn die Variable auf false festgelegt ist, der _pFolderFocus_ -Parameter wird ignoriert, und der Formular-Viewer kann Verfassen Sie die Nachricht in einem Ordner. Wenn die Variable auf true festgelegt ist und NULL im _pFolderFocus_ -Parameter übergeben wird, besteht die Nachricht im aktuellen Ordner. Wenn die Variable TRUE ist und _pFolderFocus_ein NULL-Wert übergeben wird, besteht die Nachricht im Ordner auf _pFolderFocus_zeigt.
    
 _pFolderFocus_
  
> [in] Ein Zeiger auf den Ordner, in dem die neue Nachricht erstellt wird.
    
 _pPersistMessage_
  
> [in] Ein Zeiger auf das Form-Objekt für das neue Formular.
    
 _ppMessage_
  
> [out] Ein Zeiger auf einen Zeiger auf die neue Nachricht.
    
 _ppMessageSite_
  
> [out] Ein Zeiger auf einen Zeiger auf ein Objekt "Message" Website für die neue Nachricht.
    
 _ppViewContext_
  
> [out] Ein Zeiger auf einen Zeiger auf ein Ansichtskontext, die für die Übergabe an ein neues Formular mit der neuen Nachricht geeignet ist. Wenn das Formular eine eigene Ansichtskontext implementiert, kann der NULL im _PpViewContext_ -Parameter übergeben werden. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Formularobjekte Aufrufen die **IMAPIMessageSite::NewMessage** -Methode zum Erstellen einer neuen Nachricht. Das Formular wird mit **NewMessage** eine neue Nachricht und die Website für die zugehörige Nachricht aus der Ansicht abgerufen. Sie können dann die neue Nachricht ändern. 
  
Sie können auch einen Kontext für die zugeordnete Ansicht durch die Übergabe eines nicht-NULL-Werts im Parameter _PpViewContext_ abrufen. In diesem Ansichtskontext direkt verwendet werden kann, oder aggregiert und an die neue Nachricht übergeben werden kann. Wenn eine vollständige Implementierung erforderlich ist, übergeben Sie NULL _PpViewContext_.
  
Eine Liste der Schnittstellen im Zusammenhang mit der Formular-Servern finden Sie unter [MAPI-Formulars Schnittstellen](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::NewMessage  <br/> |MFCMAPI (engl.) wird die **IMAPIMessageSite::NewMessage** -Methode verwendet, um eine neue Nachricht erstellen, instanziieren Sie einen neues Formular Viewer und Aufrufen von **SetPersist** , um die Nachricht auf dem Formular Viewer festzulegen. Schließlich gibt den Formular-Viewer als Website für die Nachricht zurück.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MAPI-Formularoberflächen](mapi-form-interfaces.md)

