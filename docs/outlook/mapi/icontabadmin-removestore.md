---
title: IContabAdminRemoveStore
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IContabAdmin.RemoveStore
api_type:
- COM
ms.assetid: 2a5fcf5c-8a5a-4774-b8c9-1ac1ff27947d
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 868f38eaf52d3d0a3787623983a4a587de8fdc3b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792027"
---
# <a name="icontabadminremovestore"></a>IContabAdmin::RemoveStore

  
  
**Betrifft**: Outlook 
  
Entfernt den Kontakt Adresse Buch (CAB) mit der angegebenen Eintrags-ID aus der Adressbuchhierarchie angegeben.
  
```cpp
HRESULT RemoveStore(
ULONG cbEntryID, 
LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parameter

 _cbEntryID_
  
> [in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID des Objekts zu öffnen.
    

