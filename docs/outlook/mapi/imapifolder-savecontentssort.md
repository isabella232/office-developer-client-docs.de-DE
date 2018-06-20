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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7c8ccada96b3e34372d488e16c85627e8b6b0cd7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792115"
---
# <a name="imapifoldersavecontentssort"></a>IMAPIFolder::SaveContentsSort

  
  
**Betrifft**: Outlook 
  
Legt die Standard-Sortierreihenfolge für einen Ordner Inhaltstabelle fest.
  
```cpp
HRESULT SaveContentsSort(
  LPSSortOrderSet lpSortCriteria,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpSortCriteria_
  
> [in] Ein Zeiger auf eine [SSortOrderSet](ssortorderset.md) -Struktur, die die Sortierreihenfolge enthält. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie die Sortierreihenfolge festgelegt wird. Das folgende Flag kann festgelegt werden:
    
RECURSIVE_SORT 
  
> Der Sortierung Reihenfolge Standardsatz gilt für den angegebenen Ordner und für alle Unterordner.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Sortierreihenfolge wurde erfolgreich gespeichert.
    
MAPI_E_NO_SUPPORT 
  
> Die Nachrichtenanbieter unterstützt keine Sortierreihenfolge für ihre Ordner Inhalt Tabellen speichern.
    
## <a name="remarks"></a>Hinweise

Die **IMAPIFolder::SaveContentsSort** -Methode stellt eine standardmäßige Sortierreihenfolge für einen Ordner Inhaltstabelle her. D. h., wenn ein Client nach der Code ruft **SaveContentsSort**den Ordner [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) -Methode aufruft, werden die Zeilen in der Inhaltstabelle zurückgegebene in der Reihenfolge von **SaveContentsSort**hergestellt angezeigt.
  
Nachricht nicht alle Anbieter unterstützen **SaveContentsSort**. Es ist akzeptabel für Nachricht Anbieter MAPI_E_NO_SUPPORT aus der **SaveContentsSort** -Methode zurückgegeben. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)

