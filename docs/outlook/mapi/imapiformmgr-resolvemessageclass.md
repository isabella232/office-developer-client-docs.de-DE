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
  
Löst eine Nachrichtenklasse in Ihrem Formular innerhalb eines Formular Containers auf und gibt ein Formular Informationsobjekt für dieses Formular zurück.
  
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
  
> in Eine Zeichenfolge, die die zu lösende Nachrichtenklasse benennt.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die die Auflösung der Nachrichtenklasse steuert. Das folgende Flag kann festgelegt werden:
    
MAPIFORM_EXACTMATCH 
  
> Nur Nachrichtenklassen Zeichenfolgen, die exakt übereinstimmen, sollten aufgelöst werden.
    
 _pFolderFocus_
  
> in Ein Zeiger auf den Ordner, der die zu bearbeitende Nachricht enthält. Der _pFolderFocus_ -Parameter kann NULL sein. 
    
 _ppResult_
  
> Out Ein Zeiger auf einen Zeiger auf ein zurückgegebenes Formular Informationsobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NOT_FOUND 
  
> Die Nachrichtenklasse, die im _szMsgClass_ -Parameter übergeben wird, stimmt nicht mit der Nachrichtenklasse für ein Formular in der Formularbibliothek überein. 
    
## <a name="remarks"></a>Bemerkungen

Formular Betrachter rufen die **IMAPIFormMgr:: ResolveMessageClass** -Methode auf, um eine Nachrichtenklasse in Ihr Formular innerhalb eines Formular Containers aufzulösen. Das im _ppResult_ -Parameter zurückgegebene Formular Informationsobjekt bietet weiteren Zugriff auf die Eigenschaften des Formulars, das über die angegebene Nachrichtenklasse verfügt. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um eine Nachrichtenklasse in ein Formular aufzulösen, übergibt ein Formular Betrachter den Namen der zu lösenden Nachrichtenklasse, beispielsweise " `IPM.HelpDesk.Software`". Um die Auflösung genau zu erzwingen (das heißt, um die Auflösung einer Basisklasse der Nachrichtenklasse zu verhindern, wenn ein genau übereinstimmender Formularserver nicht verfügbar ist), kann das MAPIFORM_EXACTMATCH-Flag im _ulFlags_ -Parameter übergeben werden. Wenn der _pFolderFocus_ -Parameter NULL ist, durchsucht der Prozess der Nachrichtenklassen Auflösung keinen Ordner Container. 
  
Die Reihenfolge der gesuchten Container hängt von der Implementierung des Formularbibliothek Anbieters ab. Der Standardanbieter für Formularbibliotheken durchsucht zuerst den lokalen Container, dann den Ordner Container für den übergebenen Ordner, den persönlichen Formular Container und schließlich den Organisationscontainer.
  
Nachrichtenklassennamen sind immer ANSI-Zeichenfolgen, nie Unicode.
  
Der Klassenbezeichner für die aufgelöste Nachrichtenklasse wird als Teil des Form Information-Objekts zurückgegeben. Ein Formular Betrachter sollte nicht davon ausgehen, dass der Klassenbezeichner in der OLE-Bibliothek vorhanden ist, bis die [IMAPIFormMgr::P repareform](imapiformmgr-prepareform.md) -Methode oder die [IMAPIFormMgr:: CreateForm](imapiformmgr-createform.md) -Methode aufgerufen wurde. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

