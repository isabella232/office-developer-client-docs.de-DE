---
title: IMAPIFormMgrResolveMultipleMessageClasses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormMgr.ResolveMultipleMessageClasses
api_type:
- COM
ms.assetid: d3cc6658-e46d-42dd-b1ac-65c88cfef8ca
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fc19d017c2c0d8f06650bc889fb245fb22d2a805
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610545"
---
# <a name="imapiformmgrresolvemultiplemessageclasses"></a>IMAPIFormMgr::ResolveMultipleMessageClasses

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Löst eine Gruppe von Nachrichtenklassen in ihre Formulare in einem Formularcontainer auf und gibt ein Array von Formularinformationsobjekten für diese Formulare zurück.
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClasses,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a>Parameter

 _pMsgClasses_
  
> [in] Ein Zeiger auf ein Array, das die Namen der aufzulösenden Nachrichtenklassen enthält.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie die Nachrichtenklassen aufgelöst werden. Das folgende Kennzeichen kann festgelegt werden:
    
MAPIFORM_EXACTMATCH 
  
> Nur Nachrichtenklassenzeichenfolgen, die eine genaue Übereinstimmung sind, sollten aufgelöst werden.
    
MAPIFORM_LOCALONLY
  
> Fügen Sie keine zwischengespeicherten Formulare ein.
    
 _pFolderFocus_
  
> [in] Ein Zeiger auf den Ordner, der das Formular enthält, dessen Nachrichtenklasse aufgelöst wird. Der  _pFolderFocus-Parameter_ kann NULL sein. 
    
 _ppfrminfoarray_
  
> [out] Ein Zeiger auf einen Zeiger auf ein Array von Formularinformationsobjekten. Wenn ein Formularviewer im  _Parameter pMsgClasses_ NULL übergibt, enthält der  _Parameter ppfrminfoarray Formularinformationsobjekte_ für alle Formulare im Container. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>HinwBemerkungeneise

Formularviewer rufen die **IMAPIFormMgr::ResolveMultipleMessageClasses-Methode** auf, um eine Gruppe von Nachrichtenklassen in Formulare in einem Formularcontainer aufzulösen. Das array of form information objects returned in  _ppfrminfoarray_ provides further access to each of the forms' properties. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um eine Gruppe von Nachrichtenklassen in Formulare aufzulösen, übergibt ein Formularviewer ein Array von Nachrichtenklassennamen, die aufgelöst werden sollen. Um zu erzwingen, dass die Auflösung genau ist (d. h. um die Auflösung einer Basisklasse der Nachrichtenklasse zu verhindern, wenn kein exakt übereinstimmender Formularserver verfügbar ist), kann das MAPIFORM_EXACTMATCH Flag im  _ulFlags-Parameter_ übergeben werden. 
  
Nachrichtenklassennamen sind immer ANSI-Zeichenfolgen, niemals Unicode.
  
Wenn eine Nachrichtenklasse nicht in ein Formular aufgelöst werden kann, wird NULL für diese Nachrichtenklasse im Formularinformationsarray zurückgegeben. Selbst wenn die Methode S_OK zurückgibt, sollten Formularviewer daher nicht davon ausgehen, dass alle Nachrichtenklassen erfolgreich aufgelöst wurden. Stattdessen sollten Formularviewer die Werte im zurückgegebenen Array überprüfen.
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

