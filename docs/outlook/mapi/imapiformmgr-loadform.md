---
title: IMAPIFormMgrLoadForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.LoadForm
api_type:
- COM
ms.assetid: 5ca500c3-c737-45a5-b0fc-473b75c1d68d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7e445646477ad1fc56b41141b541358d9b9f9616
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418785"
---
# <a name="imapiformmgrloadform"></a>IMAPIFormMgr::LoadForm

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Startet ein Formular zum Öffnen einer vorhandenen Nachricht.
  
```cpp
HRESULT LoadForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pmsg,
  LPMAPIVIEWCONTEXT pViewContext,
  REFIID riid,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Ein Handle zum übergeordneten Fenster des Statusindikators, das beim Öffnen des Formulars angezeigt wird. Der  _ulUIParam-Parameter_ wird ignoriert, es sei denn, das MAPI_DIALOG wird im  _ulFlags-Parameter_ festgelegt. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Formular geöffnet wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DIALOG 
  
> Zeigt eine Benutzeroberfläche an, um den Status zur Verfügung zu stellen, oder fordert den Benutzer auf, weitere Informationen zu erhalten. Wenn dieses Kennzeichen nicht festgelegt ist, wird keine Benutzeroberfläche angezeigt.
    
MAPIFORM_EXACTMATCH 
  
> Es sollten nur Nachrichtenklassenzeichenfolgen aufgelöst werden, die eine genaue Übereinstimmung sind.
    
 _lpszMessageClass_
  
> [in] Ein Zeiger auf eine Zeichenfolge, die die Nachrichtenklasse der zu ladenden Nachricht benennt. Wenn NULL im  _lpszMessageClass-Parameter_ übergeben wird, wird die Nachrichtenklasse anhand der Nachricht bestimmt, auf die der  _pmsg-Parameter_ verweist. 
    
 _ulMessageStatus_
  
> [in] Eine Bitmaske mit client- oder anbieterdefinierten **Flags,** die aus der PR_MSG_STATUS ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))-Eigenschaft der Nachricht kopiert wurden, die Informationen über den Status der Nachricht enthält. Der  _ulMessageStatus-Parameter_ muss festgelegt werden,  _wenn lpszMessageClass_ nicht NULL ist. Andernfalls  _wird ulMessageStatus_ ignoriert. 
    
 _ulMessageFlags_
  
> [in] Ein Zeiger auf eine Bitmaske von **Flags,** die aus der PR_MESSAGE_FLAGS ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft der Nachricht kopiert wurden, die den aktuellen Status der Nachricht angibt. Der  _ulMessageFlags-Parameter_ muss festgelegt werden,  _wenn lpszMessageClass_ nicht NULL ist. Andernfalls  _wird ulMessageFlags_ ignoriert. 
    
 _pFolderFocus_
  
> [in] Ein Zeiger auf den Ordner, der die Nachricht direkt enthält. Der  _pFolderFocus-Parameter_ kann NULL sein, wenn ein solcher Ordner nicht vorhanden ist (z. B. wenn die Nachricht in eine andere Nachricht eingebettet ist). 
    
 _pMessageSite_
  
> [in] Ein Zeiger auf die Nachrichtenwebsite der Nachricht.
    
 _pmsg_
  
> [in] Ein Zeiger auf die Nachricht.
    
 _pViewContext_
  
> [in] Ein Zeiger auf den Ansichtskontext für die Nachricht. Der  _pViewContext-Parameter_ kann NULL sein. 
    
 _riid_
  
> [in] Der Schnittstellenbezeichner (Interface Identifier, IID) der Schnittstelle, die für das zurückgegebene Formularobjekt verwendet werden soll. Der  _riid-Parameter_ darf nicht NULL sein. 
    
 _ppvObj_
  
> [out] Ein Zeiger auf einen Zeiger auf die zurückgegebene Schnittstelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NO_INTERFACE 
  
> Das Formular unterstützt die angeforderte Schnittstelle nicht.
    
MAPI_E_NOT_FOUND 
  
> Die in  _lpszMessageClass_ übergebene Nachrichtenklasse ist nicht mit der Nachrichtenklasse für ein Formular in der Formularbibliothek übereinstimmend. 
    
## <a name="remarks"></a>Hinweise

Formularbetrachter rufen die **IMAPIFormMgr::LoadForm-Methode** auf, um ein Formular für eine vorhandene Nachricht zu öffnen. **LoadForm** öffnet das Formularobjekt, lädt die Nachricht in das Formularobjekt, richtet gegebenenfalls den entsprechenden Ansichtskontext ein und gibt die angeforderte Schnittstelle für das Formularobjekt zurück. 
  
Der  _pFolderFocus-Parameter_ zeigt auf den Ordner, der die Nachricht enthält. Wenn die Nachricht in eine andere Nachricht eingebettet ist,  _sollte pFolderFocus_ NULL sein. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn NULL in  _lpszMessageClass_ übergeben wird, ruft die Implementierung die Nachrichtenklasse, den Status und die Flags der Nachricht aus den Eigenschaften **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** und PR_MESSAGE_FLAGS **der Nachricht** ab. Wenn eine Nachrichtenklassenzeichenfolge in _lpszMessageClass_ bereitgestellt wird, muss die Implementierung die Werte in _ulMessageStatus_ und _ulMessageFlags verwenden._
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal  <br/> |MFCMAPI verwendet die **IMAPIFormMgr::LoadForm-Methode,** um ein Formular zu laden, bevor es angezeigt wird.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[PidTagMessageClass (kanonische Eigenschaft)](pidtagmessageclass-canonical-property.md)
  
[PidTagMessageFlags (kanonische Eigenschaft)](pidtagmessageflags-canonical-property.md)
  
[PidTagMessageStatus (kanonische Eigenschaft)](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

