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
  
Löst eine Nachrichtenklasse in ihr Formular in einem Formularcontainer auf und gibt ein Formularinformationsobjekt für dieses Formular zurück.
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMessageClass,
  ULONG ulFlags,
  LPMAPIFORMINFO FAR * ppforminfo
);
```

## <a name="parameters"></a>Parameter

 _szMessageClass_
  
> [in] Eine Zeichenfolge, die die aufgelöste Nachrichtenklasse benennt. Nachrichtenklassennamen sind immer ANSI-Zeichenfolgen, nie Unicode.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie die Nachrichtenklasse aufgelöst wird. Das folgende Flag kann festgelegt werden:
    
MAPIFORM_EXACTMATCH 
  
> Es sollten nur Nachrichtenklassenzeichenfolgen aufgelöst werden, die eine genaue Übereinstimmung sind.
    
 _ppforminfo_
  
> [out] Ein Zeiger auf einen Zeiger auf das zurückgegebene Formularinformationsobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NOT_FOUND 
  
> Die im  _szMessageClass-Parameter_ übergebene Nachrichtenklasse ist nicht mit der Nachrichtenklasse für ein Formular im Formularcontainer übereinstimmend. 
    
## <a name="remarks"></a>Hinweise

Clientanwendungen rufen die **IMAPIFormContainer::ResolveMessageClass-Methode** auf, um eine Nachrichtenklasse in ein Formular innerhalb eines Formularcontainers zu auflösen. Das im  _ppforminfo-Parameter_ zurückgegebene Formularinformationsobjekt bietet weiteren Zugriff auf die Eigenschaften des Formulars mit der angegebenen Nachrichtenklasse. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um eine Nachrichtenklasse in ein Formular zu auflösen, übergeben Sie den Namen der nachrichtenklasse, die aufgelöst werden soll (z. B.  `IPM.HelpDesk.Software` ). Um zu erzwingen, dass die Auflösung exakt ist (d. h. um die Auflösung einer Basisklasse der Nachrichtenklasse zu verhindern), kann das MAPIFORM_EXACTMATCH im  _ulFlags-Parameter übergeben_ werden. 
  
Der Klassenbezeichner für die aufgelöste Nachrichtenklasse wird als Teil des Formularinformationsobjekts zurückgegeben. Gehen Sie erst nach dem Aufruf der [IMAPIFormMgr::P repareForm-](imapiformmgr-prepareform.md) oder [IMAPIFormMgr::CreateForm-Methode](imapiformmgr-createform.md) davon aus, dass der Klassenbezeichner in der OLE-Bibliothek vorhanden ist. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnResolveMessageClass  <br/> |MFCMAPI verwendet die **IMAPIFormContainer::ResolveMessageClass-Methode,** um ein Formular zu finden, das einer Nachrichtenklasse zugeordnet ist.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

