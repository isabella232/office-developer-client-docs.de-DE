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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c1da292943d6e4d9625c6ce37019c630471e200b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792157"
---
# <a name="imapiformcontainerresolvemultiplemessageclasses"></a>IMAPIFormContainer::ResolveMultipleMessageClasses

  
  
**Betrifft**: Outlook 
  
Eine Gruppe von Nachrichtenklassen in Formularen in einem Formular Container aufgelöst wird, und gibt ein Array von Formular Informationen Objekte für diese Formulare.
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClassArray,
  ULONG ulFlags,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a>Parameter

 _pMsgClassArray_
  
> [in] Ein Zeiger auf ein Array, das die Namen der Nachrichtenklassen aufzulösende enthält. Nachrichtenklassennamen sind immer noch nie Unicode-ANSI-Zeichenfolgen.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie die Nachrichtenklassen aufgelöst werden. Das folgende Flag kann festgelegt werden:
    
MAPIFORM_EXACTMATCH 
  
> Nur Nachricht Klasse Zeichenfolgen, die eine genaue Übereinstimmung sollten aufgelöst werden.
    
 _ppfrminfoarray_
  
> [out] Ein Zeiger auf einen Zeiger auf ein Array von Formular Informationen-Objekten. Wenn eine Clientanwendung NULL im Parameter _pMsgClassArray_ übergibt, enthält der Parameter _Ppfrminfoarray_ Formular Informationen-Objekte für alle Formulare im Container. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Clientanwendungen rufen Sie die **IMAPIFormContainer::ResolveMultipleMessageClasses** -Methode, um eine Gruppe von Nachrichtenklassen für Formulare innerhalb eines Containers Formular zu beheben. Das Objektarray Formular Informationen zurückgegeben, die im Parameter _Ppfrminfoarray_ bietet weitere Zugriff auf jede der Forms-Eigenschaften. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um eine Gruppe von Nachrichtenklassen für Formulare zu beheben, übergeben Sie ein Array von Nachrichtenklassennamen aufgelöst werden. So erzwingen Sie die Auflösung genau sein (d. h., um auf eine Basisklasse der Nachrichtenklasse Lösung zu verhindern), die Kennzeichen MAPIFORM_EXACTMATCH im _UlFlags_ -Parameter übergeben werden können. 
  
Wenn eine Nachrichtenklasse in einem Formular aufgelöst werden kann, wird NULL für die Nachrichtenklasse in das Formular Informationen Array zurückgegeben. Aus diesem Grund, auch wenn die Methode S_OK zurückgegeben wird, gehen Sie nicht, dass alle Nachrichtenklassen erfolgreich behoben wurden. Überprüfen Sie stattdessen die Werte in das zurückgegebene Array.
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnResolveMultipleMessageClasses  <br/> |MFCMAPI (engl.) verwendet die **IMAPIFormContainer::ResolveMultipleMessageClasses** -Methode, um ein Formular zu suchen, die eine Reihe von Nachrichtenklassen zugeordnet ist.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md)
  
[IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

