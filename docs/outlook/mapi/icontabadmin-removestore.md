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
ms.openlocfilehash: 868f38eaf52d3d0a3787623983a4a587de8fdc3b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792027"
---
# <a name="icontabadminremovestore"></a><span data-ttu-id="aaf2c-103">IContabAdmin::RemoveStore</span><span class="sxs-lookup"><span data-stu-id="aaf2c-103">IContabAdmin::RemoveStore</span></span>

  
  
<span data-ttu-id="aaf2c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aaf2c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aaf2c-105">Entfernt den Kontakt Adresse Buch (CAB) mit der angegebenen Eintrags-ID aus der Adressbuchhierarchie angegeben.</span><span class="sxs-lookup"><span data-stu-id="aaf2c-105">Removes the Contact Address Book (CAB) specified by the given entry ID from the address book hierarchy.</span></span>
  
```cpp
HRESULT RemoveStore(
ULONG cbEntryID, 
LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="aaf2c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aaf2c-106">Parameters</span></span>

 <span data-ttu-id="aaf2c-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="aaf2c-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="aaf2c-108">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="aaf2c-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="aaf2c-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="aaf2c-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="aaf2c-110">[in] Ein Zeiger auf die Eintrags-ID des Objekts zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="aaf2c-110">[in] A pointer to the entry identifier of the object to open.</span></span>
    

