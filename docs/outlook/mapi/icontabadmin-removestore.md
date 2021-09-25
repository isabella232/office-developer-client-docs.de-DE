---
title: IContabAdminRemoveStore
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IContabAdmin.RemoveStore
api_type:
- COM
ms.assetid: 2a5fcf5c-8a5a-4774-b8c9-1ac1ff27947d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f92e562196f551bc6dca7be9f3fd5093d5f4cc03
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592445"
---
# <a name="icontabadminremovestore"></a>IContabAdmin::RemoveStore

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Entfernt das durch die angegebene Eintrags-ID angegebene Kontaktadressbuch (Contact Address Book, CAB) aus der Adressbuchhierarchie.
  
```cpp
HRESULT RemoveStore(
ULONG cbEntryID, 
LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parameter

 _cbEntryID_
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf den Eintragsbezeichner des zu öffnenden Objekts.
    

