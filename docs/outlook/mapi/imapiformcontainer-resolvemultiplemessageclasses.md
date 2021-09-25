---
title: IMAPIFormContainerResolveMultipleMessageClasses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormContainer.ResolveMultipleMessageCla
api_type:
- COM
ms.assetid: f18c2dd1-366f-48b4-b335-ebbc0651f467
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f83ac53c78f822e345e1c68e7255e5342ffd287a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551387"
---
# <a name="imapiformcontainerresolvemultiplemessageclasses"></a>IMAPIFormContainer::ResolveMultipleMessageClasses

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Löst eine Gruppe von Nachrichtenklassen in ihre Formulare in einem Formularcontainer auf und gibt ein Array von Formularinformationsobjekten für diese Formulare zurück.
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClassArray,
  ULONG ulFlags,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a>Parameter

 _pMsgClassArray_
  
> [in] Ein Zeiger auf ein Array, das die Namen der aufzulösenden Nachrichtenklassen enthält. Nachrichtenklassennamen sind immer ANSI-Zeichenfolgen, niemals Unicode.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie die Nachrichtenklassen aufgelöst werden. Das folgende Kennzeichen kann festgelegt werden:
    
MAPIFORM_EXACTMATCH 
  
> Nur Nachrichtenklassenzeichenfolgen, die eine genaue Übereinstimmung sind, sollten aufgelöst werden.
    
 _ppfrminfoarray_
  
> [out] Ein Zeiger auf einen Zeiger auf ein Array von Formularinformationsobjekten. Wenn eine Clientanwendung NULL im  _Parameter pMsgClassArray_ übergibt, enthält der  _Parameter ppfrminfoarray Formularinformationsobjekte_ für alle Formulare im Container. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>HinwBemerkungeneise

Clientanwendungen rufen die **IMAPIFormContainer::ResolveMultipleMessageClasses-Methode** auf, um eine Gruppe von Nachrichtenklassen in Formulare in einem Formularcontainer aufzulösen. Das array of form information objects returned in the  _ppfrminfoarray_ parameter provides further access to each of the forms' properties. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um eine Gruppe von Nachrichtenklassen in Formulare aufzulösen, übergeben Sie ein Array von Nachrichtenklassennamen, die aufgelöst werden sollen. Um zu erzwingen, dass die Auflösung genau ist (d. h. um die Auflösung für eine Basisklasse der Nachrichtenklasse zu verhindern), kann das flag MAPIFORM_EXACTMATCH im  _ulFlags-Parameter_ übergeben werden. 
  
Wenn eine Nachrichtenklasse nicht in ein Formular aufgelöst werden kann, wird NULL für diese Nachrichtenklasse im Formularinformationsarray zurückgegeben. Gehen Sie daher auch dann nicht davon aus, dass alle Nachrichtenklassen erfolgreich aufgelöst wurden, auch wenn die Methode S_OK zurückgibt. Überprüfen Sie stattdessen die Werte im zurückgegebenen Array.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnResolveMultipleMessageClasses  <br/> |MFCMAPI verwendet die **IMAPIFormContainer::ResolveMultipleMessageClasses-Methode,** um ein Formular zu suchen, das einem Satz von Nachrichtenklassen zugeordnet ist.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

