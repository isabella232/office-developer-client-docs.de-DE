---
title: IMAPIFormContainerResolveMultipleMessageClasses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.ResolveMultipleMessageCla
api_type:
- COM
ms.assetid: f18c2dd1-366f-48b4-b335-ebbc0651f467
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0730da9c3877985853e2cd0a55420e64fbd98e0c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412541"
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
  
> [in] Ein Zeiger auf ein Array, das die Namen der zu auflösende Nachrichtenklassen enthält. Nachrichtenklassennamen sind immer ANSI-Zeichenfolgen, nie Unicode.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie die Nachrichtenklassen aufgelöst werden. Das folgende Flag kann festgelegt werden:
    
MAPIFORM_EXACTMATCH 
  
> Es sollten nur Nachrichtenklassenzeichenfolgen aufgelöst werden, die eine genaue Übereinstimmung sind.
    
 _ppfrminfoarray_
  
> [out] Ein Zeiger auf einen Zeiger auf ein Array von Formularinformationsobjekten. Wenn eine Clientanwendung NULL im  _pMsgClassArray-Parameter_ übergibt, enthält der  _ppfrminfoarray-Parameter_ Formularinformationsobjekte für alle Formulare im Container. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Clientanwendungen rufen die **IMAPIFormContainer::ResolveMultipleMessageClasses-Methode** auf, um eine Gruppe von Nachrichtenklassen in Formulare innerhalb eines Formularcontainers zu auflösen. Das Array von Formularinformationsobjekten, die im  _ppfrminfoarray-Parameter_ zurückgegeben werden, bietet weiteren Zugriff auf die Eigenschaften der einzelnen Formulare. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um eine Gruppe von Nachrichtenklassen in Formulare zu auflösen, übergeben Sie ein Array von Nachrichtenklassennamen, die aufgelöst werden sollen. Um zu erzwingen, dass die Auflösung exakt ist (d. h. um die Auflösung einer Basisklasse der Nachrichtenklasse zu verhindern), kann das MAPIFORM_EXACTMATCH im  _ulFlags-Parameter übergeben_ werden. 
  
Wenn eine Nachrichtenklasse nicht in ein Formular aufgelöst werden kann, wird NULL für diese Nachrichtenklasse im Formularinformationsarray zurückgegeben. Gehen Sie daher nicht davon aus, dass alle Nachrichtenklassen erfolgreich aufgelöst wurden, auch wenn die Methode S_OK zurückgibt. Überprüfen Sie stattdessen die Werte im zurückgegebenen Array.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnResolveMultipleMessageClasses  <br/> |MFCMAPI verwendet die **IMAPIFormContainer::ResolveMultipleMessageClasses-Methode,** um ein Formular zu finden, das einem Satz von Nachrichtenklassen zugeordnet ist.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

