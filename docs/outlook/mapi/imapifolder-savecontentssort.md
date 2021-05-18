---
title: IMAPIFolderSaveContentsSort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SaveContentsSort
api_type:
- COM
ms.assetid: 5ae3fdf0-6193-4c1f-bd2e-d69c56d69773
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c142424bb050ae287f54a87ea8a5e0ea45acb12c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411617"
---
# <a name="imapifoldersavecontentssort"></a>IMAPIFolder::SaveContentsSort

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt die Standardsortreihenfolge für die Inhaltstabelle eines Ordners fest.
  
```cpp
HRESULT SaveContentsSort(
  LPSSortOrderSet lpSortCriteria,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpSortCriteria_
  
> [in] Ein Zeiger auf eine [SSortOrderSet-Struktur,](ssortorderset.md) die die Standardsortierungsreihenfolge enthält. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie die Standardsortreihenfolge festgelegt wird. Das folgende Flag kann festgelegt werden:
    
RECURSIVE_SORT 
  
> Der Standardmäßige Sortierreihenfolgensatz gilt für den angegebenen Ordner und für alle seine Unterordner.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Sortierreihenfolge wurde erfolgreich gespeichert.
    
MAPI_E_NO_SUPPORT 
  
> Der Nachrichtenspeicheranbieter unterstützt das Speichern einer Sortierreihenfolge für seine Ordnerinhaltstabellen nicht.
    
## <a name="remarks"></a>Hinweise

Die **IMAPIFolder::SaveContentsSort-Methode** richtet eine Standardsortierreihenfolge für die Inhaltstabelle eines Ordners ein. Das heißt, wenn ein Client die [IMAPIContainer::GetContentsTable-Methode](imapicontainer-getcontentstable.md) des Ordners aufruft, nachdem der Code **SaveContentsSort** aufgerufen hat, werden die Zeilen in der zurückgegebenen Inhaltstabelle in der von **SaveContentsSort** festgelegten Reihenfolge angezeigt.
  
Nicht alle Nachrichtenspeicheranbieter unterstützen **SaveContentsSort;** Es ist akzeptabel, dass Nachrichtenspeicheranbieter MAPI_E_NO_SUPPORT **saveContentsSort-Methode** zurückgeben. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

