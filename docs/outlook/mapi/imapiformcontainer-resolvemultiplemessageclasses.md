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
  
Löst eine Gruppe von Nachrichtenklassen in Ihre Formulare in einem Formular Container auf und gibt ein Array von Formular Informationsobjekten für diese Formulare zurück.
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClassArray,
  ULONG ulFlags,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a>Parameter

 _pMsgClassArray_
  
> in Ein Zeiger auf ein Array, das die Namen der aufzulösenden Nachrichtenklassen enthält. Nachrichtenklassennamen sind immer ANSI-Zeichenfolgen, nie Unicode.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die die Auflösung der Nachrichtenklassen steuert. Das folgende Flag kann festgelegt werden:
    
MAPIFORM_EXACTMATCH 
  
> Nur Nachrichtenklassen Zeichenfolgen, die exakt übereinstimmen, sollten aufgelöst werden.
    
 _ppfrminfoarray_
  
> Out Ein Zeiger auf einen Zeiger auf ein Array von Formular Informationsobjekten. Wenn eine Clientanwendung im _pMsgClassArray_ -Parameter den Wert NULL übergibt, enthält der _ppfrminfoarray_ -parameterformular Informationsobjekte für alle Formulare im Container. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Bemerkungen

Client Anwendungen rufen die **IMAPIFormContainer:: ResolveMultipleMessageClasses** -Methode auf, um eine Gruppe von Nachrichtenklassen in Formulare in einem Formular Container aufzulösen. Das im _ppfrminfoarray_ -Parameter zurückgegebene Array von Formular Informationsobjekten bietet weiteren Zugriff auf die einzelnen Eigenschaften der Formulare. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um eine Gruppe von Nachrichtenklassen in Formulare aufzulösen, führen Sie ein Array von Nachrichtenklassennamen aus, die aufgelöst werden sollen. Um die Genauigkeit der Auflösung zu erzwingen (das heißt, um eine Lösung für eine Basisklasse der Nachrichtenklasse zu verhindern), kann das MAPIFORM_EXACTMATCH-Flag im _ulFlags_ -Parameter übergeben werden. 
  
Wenn eine Nachrichtenklasse nicht in ein Formular aufgelöst werden kann, wird für diese Nachrichtenklasse im Formular Informations Array NULL zurückgegeben. Daher sollten Sie nicht davon ausgehen, dass alle Nachrichtenklassen erfolgreich aufgelöst wurden, selbst wenn die Methode S_OK zurückgibt. Überprüfen Sie stattdessen die Werte im zurückgegebenen Array.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FormContainerDlg. cpp  <br/> |CFormContainerDlg:: OnResolveMultipleMessageClasses  <br/> |MFCMAPI verwendet die **IMAPIFormContainer:: ResolveMultipleMessageClasses** -Methode, um ein Formular zu suchen, das einer Gruppe von Nachrichtenklassen zugeordnet ist.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

