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
  
> [in] Gibt an, in welchem Ordner die Nachricht verfasst werden soll. Wenn die Variable FALSE ist, wird  _der pFolderFocus-Parameter_ ignoriert, und die Formularanzeige kann die Nachricht in einem beliebigen Ordner verfassen. Wenn die Variable TRUE ist und NULL im  _pFolderFocus-Parameter_ übergeben wird, wird die Nachricht im aktuellen Ordner verfasst. Wenn die Variable TRUE ist und ein Nicht-NULL-Wert in _pFolderFocus_ übergeben wird, wird die Nachricht in dem Ordner verfasst, auf den _pFolderFocus verweist._
    
 _pFolderFocus_
  
> [in] Ein Zeiger auf den Ordner, in dem die neue Nachricht erstellt wird.
    
 _pPersistMessage_
  
> [in] Ein Zeiger auf das Formularobjekt für das neue Formular.
    
 _ppMessage_
  
> [out] Ein Zeiger auf einen Zeiger auf die neue Nachricht.
    
 _ppMessageSite_
  
> [out] Ein Zeiger auf einen Zeiger auf ein Nachrichtenwebsiteobjekt für die neue Nachricht.
    
 _ppViewContext_
  
> [out] Ein Zeiger auf einen Zeiger auf einen Ansichtskontext, der für die Übergabe an ein neues Formular mit der neuen Nachricht geeignet ist. Wenn das Formular einen eigenen Ansichtskontext implementiert, kann NULL im  _ppViewContext-Parameter übergeben_ werden. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Formularobjekte rufen die **IMAPIMessageSite::NewMessage-Methode** auf, um eine neue Nachricht zu erstellen. Das Formular verwendet **NewMessage,** um eine neue Nachricht und die zugeordnete Nachrichtenwebsite aus der Ansicht zu erhalten. Anschließend kann die neue Nachricht geändert werden. 
  
Sie können auch einen zugeordneten Ansichtskontext abrufen, indem Sie einen Nicht-NULL-Wert im  _ppViewContext-Parameter_ übergeben. Dieser Ansichtskontext kann direkt verwendet oder aggregiert und an die neue Nachricht übergeben werden. Wenn eine vollständige Implementierung erforderlich ist, übergeben Sie NULL in  _ppViewContext_.
  
Eine Liste der Schnittstellen im Zusammenhang mit Formularservern finden Sie unter [MAPI Form Interfaces](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::NewMessage  <br/> |MFCMAPI verwendet die **IMAPIMessageSite::NewMessage-Methode,** um eine neue Nachricht zu erstellen, eine neue Formularanzeige zu instanziieren und **SetPersist** zum Festlegen der Nachricht in der Formularanzeige auf. Schließlich wird die Formularanzeige als Nachrichtenwebsite zurückgegeben.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MAPI-Formularschnittstellen](mapi-form-interfaces.md)

