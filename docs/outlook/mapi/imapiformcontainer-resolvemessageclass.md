---
title: IMAPIFormContainerResolveMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.ResolveMessageClass
api_type:
- COM
ms.assetid: 9ce13f11-5787-4ea5-a84f-b1e3824529ee
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c0954d6f8b14b4088ece2ac276b045b6c163ed98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408551"
---
# <a name="imapiformcontainerresolvemessageclass"></a>IMAPIFormContainer::ResolveMessageClass

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Löst eine Nachrichtenklasse in Ihrem Formular in einem Formular Container auf und gibt ein Formular Informationsobjekt für dieses Formular zurück.
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMessageClass,
  ULONG ulFlags,
  LPMAPIFORMINFO FAR * ppforminfo
);
```

## <a name="parameters"></a>Parameter

 _szMessageClass_
  
> in Eine Zeichenfolge, die die zu lösende Nachrichtenklasse benennt. Nachrichtenklassennamen sind immer ANSI-Zeichenfolgen, nie Unicode.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die die Auflösung der Nachrichtenklasse steuert. Das folgende Flag kann festgelegt werden:
    
MAPIFORM_EXACTMATCH 
  
> Nur Nachrichtenklassen Zeichenfolgen, die exakt übereinstimmen, sollten aufgelöst werden.
    
 _ppforminfo_
  
> Out Ein Zeiger auf einen Zeiger auf das zurückgegebene Formular Informationsobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NOT_FOUND 
  
> Die Nachrichtenklasse, die im _szMessageClass_ -Parameter übergeben wird, stimmt nicht mit der Nachrichtenklasse für alle Formulare im Formular Container überein. 
    
## <a name="remarks"></a>Bemerkungen

Client Anwendungen rufen die **IMAPIFormContainer:: ResolveMessageClass** -Methode auf, um eine Nachrichtenklasse in ein Formular in einem Formular Container aufzulösen. Das im _ppforminfo_ -Parameter zurückgegebene Formular Informationsobjekt bietet weiteren Zugriff auf die Eigenschaften des Formulars mit der angegebenen Nachrichtenklasse. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um eine Nachrichtenklasse in ein Formular aufzulösen, geben Sie den Namen der zu lösenden Nachrichtenklasse ein (beispielsweise `IPM.HelpDesk.Software`). Um die Genauigkeit der Auflösung zu erzwingen (das heißt, um eine Lösung für eine Basisklasse der Nachrichtenklasse zu verhindern), kann das MAPIFORM_EXACTMATCH-Flag im _ulFlags_ -Parameter übergeben werden. 
  
Der Klassenbezeichner für die aufgelöste Nachrichtenklasse wird als Teil des Form Information-Objekts zurückgegeben. Gehen Sie nicht davon aus, dass der Klassenbezeichner in der OLE-Bibliothek vorhanden ist, bis Sie die [IMAPIFormMgr::P repareform](imapiformmgr-prepareform.md) -oder [IMAPIFormMgr:: CreateForm](imapiformmgr-createform.md) -Methode aufgerufen haben. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FormContainerDlg. cpp  <br/> |CFormContainerDlg:: OnResolveMessageClass  <br/> |MFCMAPI verwendet die **IMAPIFormContainer:: ResolveMessageClass** -Methode, um ein Formular zu suchen, das einer Nachrichtenklasse zugeordnet ist.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

