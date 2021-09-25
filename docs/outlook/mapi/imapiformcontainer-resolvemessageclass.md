---
title: IMAPIFormContainerResolveMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormContainer.ResolveMessageClass
api_type:
- COM
ms.assetid: 9ce13f11-5787-4ea5-a84f-b1e3824529ee
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 43273b0f725b962a51a38009aab0bd5592c5644b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630803"
---
# <a name="imapiformcontainerresolvemessageclass"></a>IMAPIFormContainer::ResolveMessageClass

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Löst eine Nachrichtenklasse in ihrem Formular in einem Formularcontainer auf und gibt ein Formularinformationsobjekt für dieses Formular zurück.
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMessageClass,
  ULONG ulFlags,
  LPMAPIFORMINFO FAR * ppforminfo
);
```

## <a name="parameters"></a>Parameter

 _szMessageClass_
  
> [in] Eine Zeichenfolge, die die aufgelöste Nachrichtenklasse benennt. Nachrichtenklassennamen sind immer ANSI-Zeichenfolgen, niemals Unicode.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie die Nachrichtenklasse aufgelöst wird. Das folgende Kennzeichen kann festgelegt werden:
    
MAPIFORM_EXACTMATCH 
  
> Nur Nachrichtenklassenzeichenfolgen, die eine genaue Übereinstimmung sind, sollten aufgelöst werden.
    
 _ppforminfo_
  
> [out] Ein Zeiger auf einen Zeiger auf das zurückgegebene Formularinformationsobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NOT_FOUND 
  
> Die im Parameter  _"szMessageClass"_ übergebene Nachrichtenklasse stimmt nicht mit der Nachrichtenklasse für ein Formular im Formularcontainer überein. 
    
## <a name="remarks"></a>Bemerkungen

Clientanwendungen rufen die **IMAPIFormContainer::ResolveMessageClass-Methode** auf, um eine Nachrichtenklasse in ein Formular in einem Formularcontainer aufzulösen. Das im  _Ppforminfo-Parameter_ zurückgegebene Formularinformationsobjekt bietet weiteren Zugriff auf die Eigenschaften des Formulars mit der angegebenen Nachrichtenklasse. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um eine Nachrichtenklasse in ein Formular aufzulösen, übergeben Sie den Namen der zu lösenden Nachrichtenklasse (z. B.  `IPM.HelpDesk.Software` ). Um zu erzwingen, dass die Auflösung genau ist (d. h. um die Auflösung für eine Basisklasse der Nachrichtenklasse zu verhindern), kann das flag MAPIFORM_EXACTMATCH im  _ulFlags-Parameter_ übergeben werden. 
  
Der Klassenbezeichner für die aufgelöste Nachrichtenklasse wird als Teil des Formularinformationsobjekts zurückgegeben. Gehen Sie erst nach dem Aufrufen der [IMAPIFormMgr::P repareForm-](imapiformmgr-prepareform.md) oder [IMAPIFormMgr::CreateForm-Methode](imapiformmgr-createform.md) davon aus, dass der Klassenbezeichner in der OLE-Bibliothek vorhanden ist. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnResolveMessageClass  <br/> |MFCMAPI verwendet die **IMAPIFormContainer::ResolveMessageClass-Methode,** um ein Formular zu suchen, das einer Nachrichtenklasse zugeordnet ist.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

