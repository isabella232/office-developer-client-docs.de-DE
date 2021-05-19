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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435418"
---
# <a name="icontabadminremovestore"></a><span data-ttu-id="3dbce-103">IContabAdmin::RemoveStore</span><span class="sxs-lookup"><span data-stu-id="3dbce-103">IContabAdmin::RemoveStore</span></span>

  
  
<span data-ttu-id="3dbce-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3dbce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3dbce-105">Entfernt das durch die angegebene Eintrags-ID angegebene Adressbuch (Contact Address Book, CAB) aus der Adressbuchhierarchie.</span><span class="sxs-lookup"><span data-stu-id="3dbce-105">Removes the Contact Address Book (CAB) specified by the given entry ID from the address book hierarchy.</span></span>
  
```cpp
HRESULT RemoveStore(
ULONG cbEntryID, 
LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="3dbce-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3dbce-106">Parameters</span></span>

 <span data-ttu-id="3dbce-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="3dbce-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="3dbce-108">[in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="3dbce-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="3dbce-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="3dbce-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="3dbce-110">[in] Ein Zeiger auf den Eintragsbezeichner des zu öffnende Objekts.</span><span class="sxs-lookup"><span data-stu-id="3dbce-110">[in] A pointer to the entry identifier of the object to open.</span></span>
    

