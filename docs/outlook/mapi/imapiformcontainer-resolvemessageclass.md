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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 713a177d5ceddf5fd4d97a0e35d87b2250748faf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792152"
---
# <a name="imapiformcontainerresolvemessageclass"></a>IMAPIFormContainer::ResolveMessageClass

  
  
**Betrifft**: Outlook 
  
Löst eine Nachrichtenklasse in seiner Form in einem Formular Container und ein Formular Informationen-Objekt für dieses Formular zurückgegeben.
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMessageClass,
  ULONG ulFlags,
  LPMAPIFORMINFO FAR * ppforminfo
);
```

## <a name="parameters"></a>Parameter

 _szMessageClass_
  
> [in] Eine Zeichenfolge, die den Namen die Nachrichtenklasse aufgelöst wird. Nachrichtenklassennamen sind immer noch nie Unicode-ANSI-Zeichenfolgen.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie die Nachrichtenklasse aufgelöst wird. Das folgende Flag kann festgelegt werden:
    
MAPIFORM_EXACTMATCH 
  
> Nur Nachricht Klasse Zeichenfolgen, die eine genaue Übereinstimmung sollten aufgelöst werden.
    
 _ppforminfo_
  
> [out] Ein Zeiger auf einen Zeiger auf das zurückgegebene Informationen Formularobjekt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NOT_FOUND 
  
> Die Nachrichtenklasse in der _SzMessageClass_ -Parameter übergeben entspricht nicht die Nachrichtenklasse für jedes Formular im Formular-Container. 
    
## <a name="remarks"></a>Bemerkungen

Clientanwendungen rufen Sie die **IMAPIFormContainer::ResolveMessageClass** -Methode, um eine Nachrichtenklasse zu einem Formular in einem Formular Container zu beheben. Das Formular Informationen-Objekt zurückgegeben, die im Parameter _Ppforminfo_ bietet weitere Zugriff auf die Eigenschaften des Formulars mit der angegebenen Nachrichtenklasse. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um eine Nachrichtenklasse zu einem Formular zu beheben, übergeben Sie den Namen der Nachrichtenklasse aufgelöst werden (beispielsweise `IPM.HelpDesk.Software`). So erzwingen Sie die Auflösung genau sein (d. h., um auf eine Basisklasse der Nachrichtenklasse Lösung zu verhindern), die Kennzeichen MAPIFORM_EXACTMATCH im _UlFlags_ -Parameter übergeben werden können. 
  
Die Klassen-ID für die Nachrichtenklasse aufgelöst wird als Teil des Formulars Informationen-Objekts zurückgegeben. Nehmen Sie nicht an, dass die Klassen-ID in der OLE-Bibliothek erst vorhanden ist, nachdem Sie die [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) oder [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) -Methode aufgerufen haben. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnResolveMessageClass  <br/> |MFCMAPI (engl.) verwendet die **IMAPIFormContainer::ResolveMessageClass** -Methode, um ein Formular zu suchen, die mit einer Nachrichtenklasse zugeordnet ist.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

