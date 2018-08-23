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
ms.openlocfilehash: 968be38e794793405aac15340a92ccd6d680498d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571696"
---
# <a name="imapiformmgrresolvemultiplemessageclasses"></a>IMAPIFormMgr::ResolveMultipleMessageClasses

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Eine Gruppe von Nachrichtenklassen in ihre Formulare in einem Formular Container aufgelöst wird, und gibt ein Array von Formular Informationen Objekte für diese Formulare.
  
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
  
> [in] Ein Zeiger auf ein Array, das die Namen der Nachrichtenklassen aufzulösende enthält.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie die Nachrichtenklassen aufgelöst werden. Das folgende Flag kann festgelegt werden:
    
MAPIFORM_EXACTMATCH 
  
> Nur Nachricht Klasse Zeichenfolgen, die eine genaue Übereinstimmung sollten aufgelöst werden.
    
MAPIFORM_LOCALONLY
  
> Schließen Sie nicht zwischengespeicherte Formulare.
    
 _pFolderFocus_
  
> [in] Ein Zeiger auf den Ordner, der das Formular enthält, deren Nachrichtenklasse aufgelöst wird. Der Parameter _pFolderFocus_ kann NULL sein. 
    
 _ppfrminfoarray_
  
> [out] Ein Zeiger auf einen Zeiger auf ein Array von Formular Informationen-Objekten. Wenn ein Formular Viewer NULL im Parameter _pMsgClasses_ übergibt, enthält der Parameter _Ppfrminfoarray_ Formular Informationen-Objekte für alle Formulare im Container. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Formular Viewer rufen Sie die **IMAPIFormMgr::ResolveMultipleMessageClasses** -Methode, um eine Gruppe von Nachrichtenklassen für Formulare innerhalb eines Containers Formular zu beheben. Das Array von Formular Informationen-Objekten, die in _Ppfrminfoarray_ zurückgegeben ermöglicht den Zugriff auf die Formulare Eigenschaften weiter. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um eine Gruppe von Nachrichtenklassen in Formularen aufzulösen, übergibt ein Formular Viewer in einem Array von Nachrichtenklassennamen aufgelöst werden. So erzwingen Sie die Auflösung genau sein (d. h., um auf eine Basisklasse der Nachrichtenklasse, wenn ein Formular genau übereinstimmenden Lösung zu verhindern Server ist nicht verfügbar) das Flag MAPIFORM_EXACTMATCH im _UlFlags_ -Parameter übergeben werden kann. 
  
Nachrichtenklassennamen sind immer noch nie Unicode-ANSI-Zeichenfolgen.
  
Wenn eine Nachrichtenklasse in einem Formular aufgelöst werden kann, wird NULL für die Nachrichtenklasse in das Formular Informationen Array zurückgegeben. Aus diesem Grund, auch wenn die Methode gibt S_OK zurück, sollte Formular Viewer funktioniert nicht auf der Annahme, dass alle Nachrichtenklassen erfolgreich behoben wurden. Formular Viewer sollten Sie stattdessen die Werte im zurückgegebenen Array überprüfen.
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

