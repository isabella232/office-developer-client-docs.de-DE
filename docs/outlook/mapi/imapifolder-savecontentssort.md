---
title: IMAPIFolderSaveContentsSort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFolder.SaveContentsSort
api_type:
- COM
ms.assetid: 5ae3fdf0-6193-4c1f-bd2e-d69c56d69773
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1e16f14afda35ec67375f77371f7601f056e968f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596330"
---
# <a name="imapifoldersavecontentssort"></a>IMAPIFolder::SaveContentsSort

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt die Standardsortierreihenfolge für das Inhaltsverzeichnis eines Ordners fest.
  
```cpp
HRESULT SaveContentsSort(
  LPSSortOrderSet lpSortCriteria,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpSortCriteria_
  
> [in] Ein Zeiger auf eine [SSortOrderSet-Struktur,](ssortorderset.md) die die Standardsortierreihenfolge enthält. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie die Standardsortierreihenfolge festgelegt wird. Das folgende Kennzeichen kann festgelegt werden:
    
RECURSIVE_SORT 
  
> Der Standardsortierreihenfolgesatz gilt für den angegebenen Ordner und alle unteren Ordner.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Sortierreihenfolge wurde erfolgreich gespeichert.
    
MAPI_E_NO_SUPPORT 
  
> Das Speichern einer Sortierreihenfolge für die Ordnerinhaltstabellen wird vom Nachrichtenspeicheranbieter nicht unterstützt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPIFolder::SaveContentsSort-Methode** richtet eine Standardsortierreihenfolge für das Inhaltsverzeichnis eines Ordners ein. Das heißt, wenn ein Client die [IMAPIContainer::GetContentsTable-Methode](imapicontainer-getcontentstable.md) des Ordners aufruft, nachdem der Code **SaveContentsSort** aufgerufen hat, werden die Zeilen in der zurückgegebenen Inhaltstabelle in der von **SaveContentsSort** festgelegten Reihenfolge angezeigt.
  
Nicht alle Nachrichtenspeicheranbieter unterstützen **SaveContentsSort;** Es ist akzeptabel, dass Nachrichtenspeicheranbieter MAPI_E_NO_SUPPORT aus der **SaveContentsSort-Methode** zurückgeben. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

