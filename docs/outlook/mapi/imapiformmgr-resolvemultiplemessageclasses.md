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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428018"
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
  
> [in] Ein Zeiger auf ein Array, das die Namen der zu auflösende Nachrichtenklassen enthält.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie die Nachrichtenklassen aufgelöst werden. Das folgende Flag kann festgelegt werden:
    
MAPIFORM_EXACTMATCH 
  
> Es sollten nur Nachrichtenklassenzeichenfolgen aufgelöst werden, die eine genaue Übereinstimmung sind.
    
MAPIFORM_LOCALONLY
  
> Schließen Sie keine zwischengespeicherten Formulare ein.
    
 _pFolderFocus_
  
> [in] Ein Zeiger auf den Ordner, der das Formular enthält, dessen Nachrichtenklasse aufgelöst wird. Der  _pFolderFocus-Parameter_ kann NULL sein. 
    
 _ppfrminfoarray_
  
> [out] Ein Zeiger auf einen Zeiger auf ein Array von Formularinformationsobjekten. Wenn ein Formularanzeiger NULL im  _pMsgClasses-Parameter_ übergibt, enthält der  _ppfrminfoarray-Parameter_ Formularinformationsobjekte für alle Formulare im Container. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Formularbetrachter rufen die **IMAPIFormMgr::ResolveMultipleMessageClasses-Methode** auf, um eine Gruppe von Nachrichtenklassen in Formulare innerhalb eines Formularcontainers zu auflösen. Das Array von Formularinformationsobjekten, die in  _ppfrminfoarray_ zurückgegeben werden, bietet weiteren Zugriff auf die Eigenschaften der einzelnen Formulare. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um eine Gruppe von Nachrichtenklassen in Formulare zu auflösen, übergibt eine Formularanzeige ein Array von Nachrichtenklassennamen, die aufgelöst werden sollen. Um zu erzwingen, dass die Auflösung exakt ist (d. h. um die Auflösung zu einer Basisklasse der Nachrichtenklasse zu verhindern, wenn kein exakt übereinstimmender Formularserver verfügbar ist), kann das MAPIFORM_EXACTMATCH-Flag im  _ulFlags-Parameter_ übergeben werden. 
  
Nachrichtenklassennamen sind immer ANSI-Zeichenfolgen, nie Unicode.
  
Wenn eine Nachrichtenklasse nicht in ein Formular aufgelöst werden kann, wird NULL für diese Nachrichtenklasse im Formularinformationsarray zurückgegeben. Daher sollten Formularanzeigen nicht unter der Annahme funktionieren, dass alle Nachrichtenklassen erfolgreich aufgelöst wurden, auch wenn die Methode S_OK zurückgibt. Stattdessen sollten Formularbetrachter die Werte im zurückgegebenen Array überprüfen.
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

