---
title: IMAPIFormMgrLoadForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormMgr.LoadForm
api_type:
- COM
ms.assetid: 5ca500c3-c737-45a5-b0fc-473b75c1d68d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0ecdf85aa388a183b3adc34004f0ed1cc78ee77f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576009"
---
# <a name="imapiformmgrloadform"></a>IMAPIFormMgr::LoadForm

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Startet ein Formular, um eine vorhandene Nachricht zu öffnen.
  
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
  
> [in] Ein Handle für das übergeordnete Fenster der Statusanzeige, die beim Öffnen des Formulars angezeigt wird. Der  _ulUIParam-Parameter_ wird ignoriert, es sei denn, das flag MAPI_DIALOG im  _UlFlags-Parameter_ festgelegt ist. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Formular geöffnet wird. Die folgenden Flags können festgelegt werden:
    
MAPI_DIALOG 
  
> Zeigt eine Benutzeroberfläche an, um den Status bereitzustellen oder den Benutzer zur Eingabe weiterer Informationen aufzufordern. Wenn dieses Kennzeichen nicht festgelegt ist, wird keine Benutzeroberfläche angezeigt.
    
MAPIFORM_EXACTMATCH 
  
> Nur Nachrichtenklassenzeichenfolgen, die eine genaue Übereinstimmung sind, sollten aufgelöst werden.
    
 _lpszMessageClass_
  
> [in] Ein Zeiger auf eine Zeichenfolge, die die Nachrichtenklasse der zu ladenden Nachricht benennt. Wenn NULL im  _LpszMessageClass-Parameter_ übergeben wird, wird die Nachrichtenklasse anhand der Nachricht bestimmt, auf die durch den  _Parameter "pmsg"_ verwiesen wird. 
    
 _ulMessageStatus_
  
> [in] Eine Bitmaske von clientdefinierten oder vom Anbieter definierten Flags, die aus der **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) -Eigenschaft der Nachricht kopiert wurden, die Informationen zum Status der Nachricht bereitstellt. Der  _ulMessageStatus-Parameter_ muss festgelegt werden, wenn  _lpszMessageClass_ ungleich NULL ist. andernfalls wird  _ulMessageStatus_ ignoriert. 
    
 _ulMessageFlags_
  
> [in] Ein Zeiger auf eine Bitmaske mit Flags, die aus der **eigenschaft PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) der Nachricht kopiert wurden, die den aktuellen Status der Nachricht angibt. Der  _ulMessageFlags-Parameter_ muss festgelegt werden, wenn  _lpszMessageClass_ ungleich NULL ist. andernfalls wird  _ulMessageFlags_ ignoriert. 
    
 _pFolderFocus_
  
> [in] Ein Zeiger auf den Ordner, der die Nachricht direkt enthält. Der  _pFolderFocus-Parameter_ kann NULL sein, wenn ein solcher Ordner nicht vorhanden ist (z. B. wenn die Nachricht in eine andere Nachricht eingebettet ist). 
    
 _pMessageSite_
  
> [in] Ein Zeiger auf die Nachrichtenwebsite der Nachricht.
    
 _pmsg_
  
> [in] Ein Zeiger auf die Nachricht.
    
 _pViewContext_
  
> [in] Ein Zeiger auf den Ansichtskontext für die Nachricht. Der  _pViewContext-Parameter_ kann NULL sein. 
    
 _Riid_
  
> [in] Der Schnittstellenbezeichner (IID) der Schnittstelle, die für das zurückgegebene Formularobjekt verwendet werden soll. Der  _riid-Parameter_ darf nicht NULL sein. 
    
 _ppvObj_
  
> [out] Ein Zeiger auf einen Zeiger auf die zurückgegebene Schnittstelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NO_INTERFACE 
  
> Das Formular unterstützt die angeforderte Schnittstelle nicht.
    
MAPI_E_NOT_FOUND 
  
> Die in  _lpszMessageClass_ übergebene Nachrichtenklasse stimmt nicht mit der Nachrichtenklasse für ein Formular in der Formularbibliothek überein. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Formularviewer rufen die **IMAPIFormMgr::LoadForm-Methode** auf, um ein Formular für eine vorhandene Nachricht zu öffnen. **LoadForm** öffnet das Formularobjekt, lädt die Nachricht in das Formularobjekt, richtet ggf. den entsprechenden Ansichtskontext ein und gibt die angeforderte Schnittstelle für das Formularobjekt zurück. 
  
Der  _pFolderFocus-Parameter_ verweist auf den Ordner, der die Nachricht enthält. Wenn die Nachricht in eine andere Nachricht eingebettet ist, sollte  _pFolderFocus_ NULL sein. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn NULL in  _lpszMessageClass_ übergeben wird, ruft die Implementierung die Nachrichtenklasse, den Status und die Flags der Nachricht aus den Eigenschaften **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** und **PR_MESSAGE_FLAGS** der Nachricht ab. Wenn eine Nachrichtenklassenzeichenfolge in  _lpszMessageClass_ bereitgestellt wird, muss die Implementierung die Werte in  _ulMessageStatus_ und  _ulMessageFlags_ verwenden.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal  <br/> |MFCMAPI verwendet die **IMAPIFormMgr::LoadForm-Methode,** um ein Formular zu laden, bevor es angezeigt wird.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Kanonische PidTagMessageClass-Eigenschaft](pidtagmessageclass-canonical-property.md)
  
[PidTagMessageFlags (kanonische Eigenschaft)](pidtagmessageflags-canonical-property.md)
  
[PidTagMessageStatus (kanonische Eigenschaft)](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

