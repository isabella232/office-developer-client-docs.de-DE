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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7e445646477ad1fc56b41141b541358d9b9f9616
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321695"
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
  
> in Ein Handle für das übergeordnete Fenster der Statusanzeige, das angezeigt wird, während das Formular geöffnet wird. Der _ulUIParam_ -Parameter wird ignoriert, es sei denn, das MAPI_DIALOG-Flag wird im _ulFlags_ -Parameter festgelegt. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die steuert, wie das Formular geöffnet wird. Die folgenden Flags können festgelegt werden:
    
MAPI_DIALOG 
  
> Zeigt eine Benutzeroberfläche an, um den Status anzugeben oder den Benutzer aufzufordern, weitere Informationen zu erhalten. Wenn dieses Flag nicht festgelegt ist, wird keine Benutzeroberfläche angezeigt.
    
MAPIFORM_EXACTMATCH 
  
> Nur Nachrichtenklassen Zeichenfolgen, die exakt übereinstimmen, sollten aufgelöst werden.
    
 _lpszMessageClass_
  
> in Ein Zeiger auf eine Zeichenfolge, die die Nachrichtenklasse der zu ladenden Nachricht benennt. Wenn NULL im _lpszMessageClass_ -Parameter übergeben wird, wird die Nachrichtenklasse aus der Nachricht bestimmt, auf die durch den _pmsg_ -Parameter verwiesen wird. 
    
 _ulMessageStatus_
  
> in Eine Bitmaske von Client definierten oder Anbieter definierten Flags, die aus der **PR_MSG_STATUS** ([pidtagmessagestatus (](pidtagmessagestatus-canonical-property.md))-Eigenschaft der Nachricht kopiert wurden, die Informationen zum Status der Nachricht bereitstellt. Der Parameter _ulMessageStatus_ muss festgelegt werden, wenn _LPSZMESSAGECLASS_ ungleich NULL ist; Andernfalls wird _ulMessageStatus_ ignoriert. 
    
 _ulMessageFlags_
  
> in Ein Zeiger auf eine Bitmaske von Flags, die aus der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft der Nachricht kopiert werden, die den aktuellen Status der Nachricht angibt. Der Parameter _ulMessageFlags_ muss festgelegt werden, wenn _LPSZMESSAGECLASS_ ungleich NULL ist; Andernfalls wird _ulMessageFlags_ ignoriert. 
    
 _pFolderFocus_
  
> in Ein Zeiger auf den Ordner, der die Nachricht direkt enthält. Der _pFolderFocus_ -Parameter kann NULL sein, wenn ein solcher Ordner nicht vorhanden ist (beispielsweise, wenn die Nachricht in eine andere Nachricht eingebettet ist). 
    
 _pMessageSite_
  
> in Ein Zeiger auf die Nachrichtenwebsite der Nachricht.
    
 _pmsg_
  
> in Ein Zeiger auf die Nachricht.
    
 _pViewContext_
  
> in Ein Zeiger auf den Ansichtskontext für die Nachricht. Der _pViewContext_ -Parameter kann NULL sein. 
    
 _riid_
  
> in Der Schnittstellenbezeichner (IID) der Schnittstelle, die für das zurückgegebene Form-Objekt verwendet werden soll. Der _riid_ -Parameter darf nicht NULL sein. 
    
 _ppvObj_
  
> Out Ein Zeiger auf einen Zeiger auf die zurückgegebene Schnittstelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NO_INTERFACE 
  
> Die angeforderte Schnittstelle wird vom Formular nicht unterstützt.
    
MAPI_E_NOT_FOUND 
  
> Die Nachrichtenklasse, die in _lpszMessageClass_ übergeben wird, stimmt nicht mit der Nachrichtenklasse für ein Formular in der Formularbibliothek überein. 
    
## <a name="remarks"></a>Bemerkungen

Formular Betrachter rufen die **IMAPIFormMgr:: LoadForm** -Methode auf, um ein Formular für eine vorhandene Nachricht zu öffnen. **LoadForm** öffnet das Form-Objekt, lädt die Nachricht in das Form-Objekt, richtet gegebenenfalls den entsprechenden Ansichtskontext ein und gibt die angeforderte Schnittstelle für das Form-Objekt zurück. 
  
Der _pFolderFocus_ -Parameter zeigt auf den Ordner, der die Nachricht enthält. Wenn die Nachricht in eine andere Nachricht eingebettet ist, sollte _PFOLDERFOCUS_ NULL sein. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn NULL in _lpszMessageClass_übergeben wird, ruft die Implementierung die Nachrichtenklasse, den Status und die Flags der Nachricht aus **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** und **PR_MESSAGE_FLAGS **Eigenschaften. Wenn in _lpszMessageClass_eine Nachrichtenklassen Zeichenfolge bereitgestellt wird, muss die Implementierung die Werte in _ulMessageStatus_ und _ulMessageFlags_verwenden.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFormFunctions. cpp  <br/> |OpenMessageNonModal  <br/> |MFCMAPI verwendet die **IMAPIFormMgr:: LoadForm** -Methode, um ein Formular zu laden, bevor es angezeigt wird.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Kanonische PidTagMessageClass-Eigenschaft](pidtagmessageclass-canonical-property.md)
  
[Kanonische PidTagMessageFlags-Eigenschaft](pidtagmessageflags-canonical-property.md)
  
[Kanonische Pidtagmessagestatus (-Eigenschaft](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

