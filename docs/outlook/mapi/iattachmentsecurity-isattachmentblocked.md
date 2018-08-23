---
title: IAttachmentSecurityIsAttachmentBlocked
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttachmentSecurity.IsAttachmentBlocked
api_type:
- COM
ms.assetid: 6986d27a-9602-e44a-0797-4c47f2184ef7
description: 'Letzte Änderung: Montag, 25. Juni 2012'
ms.openlocfilehash: ff13866139bf422f071eaba2c146aa1140ccd1ab
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565046"
---
# <a name="iattachmentsecurityisattachmentblocked"></a><span data-ttu-id="ea733-103">IAttachmentSecurity::IsAttachmentBlocked</span><span class="sxs-lookup"><span data-stu-id="ea733-103">IAttachmentSecurity::IsAttachmentBlocked</span></span>

  
  
<span data-ttu-id="ea733-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ea733-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ea733-105">Überprüft, ob eine angegebene Anlage zum Anzeigen und Indizieren von Microsoft Outlook 2010 oder Microsoft Outlook 2013 ausgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="ea733-105">Checks if a specified attachment is blocked by Microsoft Outlook 2010 or Microsoft Outlook 2013 for viewing and indexing.</span></span>
  
```cpp
HRESULT IAttachmentSecurity::IsAttachmentBlocked( 
    LPCWSTR pwszFileName,  
    BOOL *pfBlocked 
);
```

## <a name="parameters"></a><span data-ttu-id="ea733-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea733-106">Parameters</span></span>

 <span data-ttu-id="ea733-107">_pwszFileName_</span><span class="sxs-lookup"><span data-stu-id="ea733-107">_pwszFileName_</span></span>
  
> <span data-ttu-id="ea733-108">[in] Zeiger auf den Dateinamen der Anlage.</span><span class="sxs-lookup"><span data-stu-id="ea733-108">[in] Pointer to the filename of an attachment.</span></span>
    
 <span data-ttu-id="ea733-109">_pfBlocked_</span><span class="sxs-lookup"><span data-stu-id="ea733-109">_pfBlocked_</span></span>
  
> <span data-ttu-id="ea733-110">[out] Zeiger auf einen Wert angibt, **true,** Wenn die angegebene Anlage blockiert wird; anderenfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="ea733-110">[out] Pointer to a value indicating **true** if the specified attachment is blocked; otherwise, **false**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ea733-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea733-111">See also</span></span>



[<span data-ttu-id="ea733-112">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="ea733-112">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="ea733-113">Überprüfen, ob eine Anlage blockiert ist</span><span class="sxs-lookup"><span data-stu-id="ea733-113">Verify an Attachment is Blocked</span></span>](how-to-verify-an-attachment-is-blocked.md)

