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
ms.openlocfilehash: 1f3a876269868c30df48e0a0b62036cfdc199955
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792172"
---
# <a name="imapiformmgrloadform"></a>IMAPIFormMgr::LoadForm

  
  
**Betrifft**: Outlook 
  
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
  
> [in] Ein Handle für das übergeordnete Fenster der Statusanzeige, die angezeigt wird, während das Formular geöffnet wird. Der Parameter _UlUIParam_ wird ignoriert, es sei denn, das Flag MAPI_DIALOG im _UlFlags_ -Parameter festgelegt ist. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie das Formular geöffnet wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_DIALOG 
  
> Zeigt eine Benutzeroberfläche zum Bereitstellen von Status oder auffordern, Weitere Informationen. Wenn dieses Flag nicht festgelegt ist, wird keine Benutzeroberfläche angezeigt.
    
MAPIFORM_EXACTMATCH 
  
> Nur Nachricht Klasse Zeichenfolgen, die eine genaue Übereinstimmung sollten aufgelöst werden.
    
 _lpszMessageClass_
  
> [in] Ein Zeiger auf eine Zeichenfolge, die den Namen die Nachrichtenklasse der Nachricht geladen werden. Wenn NULL in der _LpszMessageClass_ -Parameter übergeben wird, wird die Nachrichtenklasse aus der Nachricht auf das durch den Parameter _Pmsg_ bestimmt. 
    
 _ulMessageStatus_
  
> [in] Eine Bitmaske vom Client definiert oder vom Anbieter definiertes Flags, kopiert aus der **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))-Eigenschaft der Nachricht bereitstellt, die Informationen zum Status der Nachricht. Der Parameter _UlMessageStatus_ muss festgelegt werden, wenn _LpszMessageClass_ ungleich NULL ist. Andernfalls wird _UlMessageStatus_ ignoriert. 
    
 _ulMessageFlags_
  
> [in] Ein Zeiger auf eine Bitmaske aus Flags, die von der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft der Nachricht, die angibt, den aktuellen Status der Nachricht kopiert. Der Parameter _UlMessageFlags_ muss festgelegt werden, wenn _LpszMessageClass_ ungleich NULL ist. Andernfalls wird _UlMessageFlags_ ignoriert. 
    
 _pFolderFocus_
  
> [in] Ein Zeiger auf den Ordner, der die Nachricht direkt enthält. Der Parameter _pFolderFocus_ kann NULL sein, wenn eine solche ein Ordner nicht vorhanden ist (z. B., wenn die Nachricht in eine andere Nachricht eingebettet ist). 
    
 _pMessageSite_
  
> [in] Ein Zeiger auf die Website Nachricht der Nachricht.
    
 _pmsg_
  
> [in] Ein Zeiger auf die Nachricht.
    
 _pViewContext_
  
> [in] Ein Zeiger auf den Ansichtskontext für die Nachricht. Der Parameter _pViewContext_ kann NULL sein. 
    
 _riid_
  
> [in] Die Schnittstelle Identifier (IID) der Schnittstelle für das zurückgegebene Form-Objekt verwendet werden soll. Der Parameter _Riid_ darf nicht NULL sein. 
    
 _ppvObj_
  
> [out] Ein Zeiger auf einen Zeiger auf die zurückgegebene Schnittstelle.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NO_INTERFACE 
  
> Das Formular unterstützt die angeforderte Schnittstelle nicht.
    
MAPI_E_NOT_FOUND 
  
> Die Nachrichtenklasse übergebenen _LpszMessageClass_ stimmt nicht mit die Nachrichtenklasse für jedes Formular in der Formularbibliothek überein. 
    
## <a name="remarks"></a>Bemerkungen

Formular Viewer rufen Sie die **IMAPIFormMgr::LoadForm** -Methode zum Öffnen eines Formulars für eine vorhandene Nachricht. **LoadForm** Öffnet das Form-Objekt, wird die Nachricht in das Form-Objekt geladen, richtet die entsprechenden Ansichtskontext bei Bedarf und die angeforderte Schnittstelle für das Form-Objekt zurückgibt. 
  
Der _pFolderFocus_ -Parameter verweist auf den Ordner, der die Nachricht enthält. Wenn die Nachricht in einer anderen Nachricht eingebettet ist, sollte _pFolderFocus_ NULL sein. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn NULL in _LpszMessageClass_übergeben wird, erhält die Implementierung der Nachricht Nachrichtenklasse, Status und Flags aus der Nachricht **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** und **PR_MESSAGE_FLAGS **Eigenschaften. Wenn eine Meldungszeichenfolge-Klasse in _LpszMessageClass_bereitgestellt wird, muss die Implementierung der Werte in _UlMessageStatus_ und _UlMessageFlags_verwenden.
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal  <br/> |MFCMAPI (engl.) verwendet die **IMAPIFormMgr::LoadForm** -Methode, um ein Formular zu laden, bevor es angezeigt.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[PidTagMessageClass (kanonische Eigenschaft)](pidtagmessageclass-canonical-property.md)
  
[PidTagMessageFlags (kanonische Eigenschaft)](pidtagmessageflags-canonical-property.md)
  
[PidTagMessageStatus (kanonische Eigenschaft)](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

