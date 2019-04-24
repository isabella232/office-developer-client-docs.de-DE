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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4865c1c867dd73514ab22ac4e8da628caf154ee7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339270"
---
# <a name="icontabadminremovestore"></a>IContabAdmin::RemoveStore

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Entfernt das von der angegebenen Eintrags-ID angegebene Kontakt Adressbuch (CAB) aus der Adressbuchhierarchie.
  
```cpp
HRESULT RemoveStore(
ULONG cbEntryID, 
LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parameter

 _cbEntryID_
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird. 
    
 _lpEntryID_
  
> in Ein Zeiger auf die Eintrags-ID des zu öffnenden Objekts.
    

