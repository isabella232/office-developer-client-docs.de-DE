---
title: IMAPIFormMgrResolveMessageClass
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.ResolveMessageClass
api_type:
- COM
ms.assetid: c2af7516-3a97-4422-874d-b1e3a0d4f316
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e99cff77fe872018722395c53c605e4d8fabfdde
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426394"
---
# <a name="imapiformmgrresolvemessageclass"></a>IMAPIFormMgr::ResolveMessageClass

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Löst eine Nachrichtenklasse in ihr Formular in einem Formularcontainer auf und gibt ein Formularinformationsobjekt für dieses Formular zurück.
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMsgClass,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIFORMINFO FAR * ppResult
);
```

## <a name="parameters"></a>Parameter

 _szMsgClass_
  
> [in] Eine Zeichenfolge, die die aufgelöste Nachrichtenklasse benennt.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie die Nachrichtenklasse aufgelöst wird. Das folgende Flag kann festgelegt werden:
    
MAPIFORM_EXACTMATCH 
  
> Es sollten nur Nachrichtenklassenzeichenfolgen aufgelöst werden, die eine genaue Übereinstimmung sind.
    
 _pFolderFocus_
  
> [in] Ein Zeiger auf den Ordner, der die aufgelöste Nachricht enthält. Der  _pFolderFocus-Parameter_ kann NULL sein. 
    
 _ppResult_
  
> [out] Ein Zeiger auf einen Zeiger auf ein zurückgegebenes Formularinformationsobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NOT_FOUND 
  
> Die im  _szMsgClass-Parameter_ übergebene Nachrichtenklasse ist nicht mit der Nachrichtenklasse für ein Formular in der Formularbibliothek übereinstimmend. 
    
## <a name="remarks"></a>Hinweise

Formularbetrachter rufen die **IMAPIFormMgr::ResolveMessageClass-Methode** auf, um eine Nachrichtenklasse in ihr Formular innerhalb eines Formularcontainers zu auflösen. Das im  _ppResult-Parameter_ zurückgegebene Formularinformationsobjekt bietet weiteren Zugriff auf die Eigenschaften des Formulars mit der angegebenen Nachrichtenklasse. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um eine Nachrichtenklasse in ein Formular zu auflösen, übergibt eine Formularanzeige den Namen der zu auflösenden Nachrichtenklasse, z. B. " `IPM.HelpDesk.Software` ". Um zu erzwingen, dass die Auflösung exakt ist (d. h. um die Auflösung zu einer Basisklasse der Nachrichtenklasse zu verhindern, wenn kein exakt übereinstimmender Formularserver verfügbar ist), kann das MAPIFORM_EXACTMATCH-Flag im  _ulFlags-Parameter_ übergeben werden. Wenn der  _pFolderFocus-Parameter_ NULL ist, durchsucht der Nachrichtenklassenauflösungsprozess keinen Ordnercontainer. 
  
Die Reihenfolge der durchsuchten Container hängt von der Implementierung des Formularbibliotheksanbieters ab. Der Standardmäßige Formularbibliotheksanbieter durchsucht zuerst den lokalen Container, dann den Ordnercontainer für den übergebenen Ordner, den persönlichen Formularcontainer und schließlich den Organisationscontainer.
  
Nachrichtenklassennamen sind immer ANSI-Zeichenfolgen, nie Unicode.
  
Der Klassenbezeichner für die aufgelöste Nachrichtenklasse wird als Teil des Formularinformationsobjekts zurückgegeben. Eine Formularanzeige sollte erst dann in der Annahme funktionieren, dass der Klassenbezeichner in der OLE-Bibliothek vorhanden ist, nachdem die Formularanzeige entweder die [IMAPIFormMgr::P repareForm-Methode](imapiformmgr-prepareform.md) oder die [IMAPIFormMgr::CreateForm-Methode](imapiformmgr-createform.md) aufgerufen hat. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

