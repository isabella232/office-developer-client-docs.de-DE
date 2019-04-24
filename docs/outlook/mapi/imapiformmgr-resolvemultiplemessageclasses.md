---
title: IMAPIFormMgrResolveMultipleMessageClasses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.ResolveMultipleMessageClasses
api_type:
- COM
ms.assetid: d3cc6658-e46d-42dd-b1ac-65c88cfef8ca
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 515061c6c208008c4752e5ff2f23933a4c259c00
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321868"
---
# <a name="imapiformmgrresolvemultiplemessageclasses"></a>IMAPIFormMgr::ResolveMultipleMessageClasses

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Löst eine Gruppe von Nachrichtenklassen in Ihre Formulare innerhalb eines Formular Containers auf und gibt ein Array von Formular Informationsobjekten für diese Formulare zurück.
  
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
  
> in Ein Zeiger auf ein Array, das die Namen der aufzulösenden Nachrichtenklassen enthält.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die die Auflösung der Nachrichtenklassen steuert. Das folgende Flag kann festgelegt werden:
    
MAPIFORM_EXACTMATCH 
  
> Nur Nachrichtenklassen Zeichenfolgen, die exakt übereinstimmen, sollten aufgelöst werden.
    
MAPIFORM_LOCALONLY
  
> Verwenden Sie keine zwischengespeicherten Formulare.
    
 _pFolderFocus_
  
> in Ein Zeiger auf den Ordner, der das Formular enthält, dessen Nachrichtenklasse aufgelöst wird. Der _pFolderFocus_ -Parameter kann NULL sein. 
    
 _ppfrminfoarray_
  
> Out Ein Zeiger auf einen Zeiger auf ein Array von Formular Informationsobjekten. Wenn ein Formular-Viewer im _pMsgClasses_ -Parameter den Wert NULL übergibt, enthält der _ppfrminfoarray_ -parameterformular Informationsobjekte für alle Formulare im Container. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Bemerkungen

Formular Betrachter rufen die **IMAPIFormMgr:: ResolveMultipleMessageClasses** -Methode auf, um eine Gruppe von Nachrichtenklassen in Formulare in einem Formular Container aufzulösen. Das Array der in _ppfrminfoarray_ zurückgegebenen Formular Informationsobjekte bietet weiteren Zugriff auf die einzelnen Eigenschaften der Formulare. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um eine Gruppe von Nachrichtenklassen in Formulare aufzulösen, übergibt ein Formular Betrachter ein Array von Nachrichtenklassennamen, die aufgelöst werden sollen. Um die Auflösung genau zu erzwingen (das heißt, um die Auflösung einer Basisklasse der Nachrichtenklasse zu verhindern, wenn ein genau übereinstimmender Formularserver nicht verfügbar ist), kann das MAPIFORM_EXACTMATCH-Flag im _ulFlags_ -Parameter übergeben werden. 
  
Nachrichtenklassennamen sind immer ANSI-Zeichenfolgen, nie Unicode.
  
Wenn eine Nachrichtenklasse nicht in ein Formular aufgelöst werden kann, wird für diese Nachrichtenklasse im Formular Informations Array NULL zurückgegeben. Selbst wenn die Methode S_OK zurückgibt, sollten die Formular Betrachter daher nicht davon ausgehen, dass alle Nachrichtenklassen erfolgreich aufgelöst wurden. Stattdessen sollten Formular Betrachter die Werte im zurückgegebenen Array überprüfen.
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

