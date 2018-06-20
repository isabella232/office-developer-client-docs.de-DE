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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a84698ccc132c750cbd071c05160117c40e352a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792210"
---
# <a name="imapiformmgrresolvemessageclass"></a>IMAPIFormMgr::ResolveMessageClass

  
  
**Betrifft**: Outlook 
  
Eine Nachrichtenklasse in seiner Form innerhalb eines Containers Formular aufgelöst wird, und gibt ein Formular Informationen-Objekt für das Formular zurück.
  
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
  
> [in] Eine Zeichenfolge, die den Namen die Nachrichtenklasse aufgelöst wird.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie die Nachrichtenklasse aufgelöst wird. Das folgende Flag kann festgelegt werden:
    
MAPIFORM_EXACTMATCH 
  
> Nur Nachricht Klasse Zeichenfolgen, die eine genaue Übereinstimmung sollten aufgelöst werden.
    
 _pFolderFocus_
  
> [in] Ein Zeiger auf den Ordner mit der Nachricht aufgelöst wird. Der Parameter _pFolderFocus_ kann NULL sein. 
    
 _ppResult_
  
> [out] Ein Zeiger auf einen Zeiger auf ein Formular zurückgegebenen Informationen-Objekt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NOT_FOUND 
  
> Die Nachrichtenklasse in der _SzMsgClass_ -Parameter übergeben stimmt nicht mit die Nachrichtenklasse für jedes Formular in der Formularbibliothek überein. 
    
## <a name="remarks"></a>Hinweise

Formular Viewer rufen Sie die **IMAPIFormMgr::ResolveMessageClass** -Methode, um auf die Form in einem Formular Container eine Nachrichtenklasse zu beheben. Das Formular Informationen-Objekt zurückgegeben, die im Parameter _PpResult_ bietet weitere Zugriff auf die Eigenschaften des Formulars, das die angegebenen Nachrichtenklasse hat. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um eine Nachrichtenklasse zu einem Formular zu beheben, ein Formular Viewer übergibt den Namen der Nachrichtenklasse aufgelöst, z. B. " `IPM.HelpDesk.Software`". So erzwingen Sie die Auflösung genau sein (d. h., um auf eine Basisklasse der Nachrichtenklasse, wenn ein Formular genau übereinstimmenden Lösung zu verhindern Server ist nicht verfügbar), die Kennzeichen MAPIFORM_EXACTMATCH im _UlFlags_ -Parameter übergeben werden können. Wenn der Parameter _pFolderFocus_ NULL ist, führt der Nachrichtenklasse Auflösungsprozess keine Ordnercontainer Suche. 
  
Die Reihenfolge der Container durchsucht, hängt von der Implementierung des Anbieters Bibliothek Formular ab. Der Formular Bibliothek Standardanbieter sucht zunächst den lokalen Container, und klicken Sie dann auf den Ordnercontainer für die übergebenen Ordner, den persönlichen Formular Container und schließlich Organisations-Container.
  
Nachrichtenklassennamen sind immer noch nie Unicode-ANSI-Zeichenfolgen.
  
Die Klassen-ID für die Nachrichtenklasse aufgelöst wird als Teil des Formulars Informationen-Objekts zurückgegeben. Ein Formular Viewer sollte nicht auf der Annahme verwendet werden, dass die Klassen-ID in der OLE-Bibliothek erst vorhanden ist, nachdem der Formular-Viewer die [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) -Methode oder die [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) -Methode aufgerufen hat. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormMgr: IUnknown](imapiformmgriunknown.md)

