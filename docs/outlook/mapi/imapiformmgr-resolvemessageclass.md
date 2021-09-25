---
title: IMAPIFormMgrResolveMessageClass
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormMgr.ResolveMessageClass
api_type:
- COM
ms.assetid: c2af7516-3a97-4422-874d-b1e3a0d4f316
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8ea8a07c8b299c254fbbb8fd914838c916c5684f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596207"
---
# <a name="imapiformmgrresolvemessageclass"></a>IMAPIFormMgr::ResolveMessageClass

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Löst eine Nachrichtenklasse in ihrem Formular in einem Formularcontainer auf und gibt ein Formularinformationsobjekt für dieses Formular zurück.
  
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
  
> [in] Eine Bitmaske mit Flags, die steuert, wie die Nachrichtenklasse aufgelöst wird. Das folgende Kennzeichen kann festgelegt werden:
    
MAPIFORM_EXACTMATCH 
  
> Nur Nachrichtenklassenzeichenfolgen, die eine genaue Übereinstimmung sind, sollten aufgelöst werden.
    
 _pFolderFocus_
  
> [in] Ein Zeiger auf den Ordner, der die aufgelöste Nachricht enthält. Der  _pFolderFocus-Parameter_ kann NULL sein. 
    
 _ppResult_
  
> [out] Ein Zeiger auf einen Zeiger auf ein zurückgegebenes Formularinformationsobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NOT_FOUND 
  
> Die im Parameter  _"szMsgClass"_ übergebene Nachrichtenklasse stimmt nicht mit der Nachrichtenklasse für ein Formular in der Formularbibliothek überein. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Formularviewer rufen die **IMAPIFormMgr::ResolveMessageClass-Methode** auf, um eine Nachrichtenklasse in ihr Formular innerhalb eines Formularcontainers aufzulösen. Das im  _PpResult-Parameter_ zurückgegebene Formularinformationsobjekt bietet weiteren Zugriff auf die Eigenschaften des Formulars, das über die angegebene Nachrichtenklasse verfügt. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um eine Nachrichtenklasse in ein Formular aufzulösen, übergibt eine Formularanzeige den Namen der zu lösenden Nachrichtenklasse, `IPM.HelpDesk.Software` z. B. " ". Um zu erzwingen, dass die Auflösung genau ist (d. h. um die Auflösung einer Basisklasse der Nachrichtenklasse zu verhindern, wenn kein exakt übereinstimmender Formularserver verfügbar ist), kann das MAPIFORM_EXACTMATCH Flag im  _ulFlags-Parameter_ übergeben werden. Wenn der  _pFolderFocus-Parameter_ NULL ist, durchsucht der Auflösungsprozess der Nachrichtenklasse keinen Ordnercontainer. 
  
Die Reihenfolge der durchsuchten Container hängt von der Implementierung des Formularbibliotheksanbieters ab. Der Standardmäßige Formularbibliotheksanbieter durchsucht zuerst den lokalen Container, dann den Ordnercontainer für den übergebenen Ordner, den persönlichen Formularcontainer und schließlich den Organisationscontainer.
  
Nachrichtenklassennamen sind immer ANSI-Zeichenfolgen, niemals Unicode.
  
Der Klassenbezeichner für die aufgelöste Nachrichtenklasse wird als Teil des Formularinformationsobjekts zurückgegeben. Ein Formularviewer sollte erst funktionieren, wenn der Klassenbezeichner in der OLE-Bibliothek vorhanden ist, nachdem der Formularviewer entweder die [IMAPIFormMgr::P repareForm-Methode](imapiformmgr-prepareform.md) oder die [IMAPIFormMgr::CreateForm-Methode](imapiformmgr-createform.md) aufgerufen hat. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

