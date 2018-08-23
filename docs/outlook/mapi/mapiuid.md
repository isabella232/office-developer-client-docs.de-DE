---
title: MAPIUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIUID
api_type:
- COM
ms.assetid: 63eac3ee-e59b-4a06-8bb9-f72764d84bda
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f7ec60768ab07c56969f538f196a1f9df5dbed17
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587166"
---
# <a name="mapiuid"></a><span data-ttu-id="fb789-103">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="fb789-103">MAPIUID</span></span>

  
  
<span data-ttu-id="fb789-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fb789-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fb789-105">Ein Byte-Reihenfolge unabhängige Version einer [GUID](guid.md) -Struktur, die verwendet wird, um einem Dienstanbieter eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="fb789-105">A byte-order independent version of a [GUID](guid.md) structure that is used to uniquely identify a service provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fb789-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="fb789-106">Header file:</span></span>  <br/> |<span data-ttu-id="fb789-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fb789-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="fb789-108">Verwandte Makro:</span><span class="sxs-lookup"><span data-stu-id="fb789-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="fb789-109">IsEqualMAPIUID</span><span class="sxs-lookup"><span data-stu-id="fb789-109">IsEqualMAPIUID</span></span>](isequalmapiuid.md) <br/> |
   
```cpp
typedef struct _MAPIUID
{
  BYTE ab[16];
} MAPIUID, FAR *LPMAPIUID;

```

## <a name="members"></a><span data-ttu-id="fb789-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="fb789-110">Members</span></span>

 <span data-ttu-id="fb789-111">**ab**</span><span class="sxs-lookup"><span data-stu-id="fb789-111">**ab**</span></span>
  
> <span data-ttu-id="fb789-112">Ein Array, das einen 16-Byte-Bezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="fb789-112">An array that contains a 16-byte identifier.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fb789-113">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="fb789-113">Remarks</span></span>

<span data-ttu-id="fb789-114">Eine **MAPIUID** -Struktur ist eine **GUID** -Struktur in Intel® Prozessor-Byte-Reihenfolge zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="fb789-114">A **MAPIUID** structure is a **GUID** structure put into Intel® processor byte order.</span></span> 
  
<span data-ttu-id="fb789-115">MAPI erstellt **MAPIUID** Strukturen in eine Möglichkeit, mit dem zwei verschiedene Elemente, die dieselbe ID äußerst selten kann.</span><span class="sxs-lookup"><span data-stu-id="fb789-115">MAPI creates **MAPIUID** structures in a way that makes it very rare for two different items to have the same identifier.</span></span> <span data-ttu-id="fb789-116">**MAPIUID** Strukturen können gespeichert werden, als binäre Eigenschaften oder als Dateien, ohne dabei die Anordnung der Bytes des Computers speichern oder den Zugriff auf die Informationen zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="fb789-116">**MAPIUID** structures can be stored as binary properties or as files, without regard to the byte ordering of the computer storing or accessing the information.</span></span> 
  
 <span data-ttu-id="fb789-117">**MAPIUID** Strukturen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="fb789-117">**MAPIUID** structures are used:</span></span> 
  
- <span data-ttu-id="fb789-118">Um einen Profilabschnitt zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="fb789-118">To identify a profile section.</span></span>
    
- <span data-ttu-id="fb789-119">In den Eintrag Bezeichner der Nachricht speichern und address Book-Objekten, um den verantwortlich Dienstanbieter zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="fb789-119">In the entry identifiers of message store and address book objects to identify the responsible service provider.</span></span>
    
- <span data-ttu-id="fb789-120">In der Eigenschaft **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) von Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="fb789-120">In the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property of messages.</span></span>
    
<span data-ttu-id="fb789-121">Um einen **MAPIUID** Bezeichner für eine Suche Schlüssel generiert werden soll, rufen Sie Dienstanbieter [IMAPISupport::NewUID](imapisupport-newuid.md).</span><span class="sxs-lookup"><span data-stu-id="fb789-121">To generate a **MAPIUID** identifier for a search key, service providers call [IMAPISupport::NewUID](imapisupport-newuid.md).</span></span>
  
<span data-ttu-id="fb789-122">Wenn ein Client über ein Netzwerk eine Nachricht sendet, sollte ein Protokoll oder Übertragung Format verwendet werden, die nicht die Bytereihenfolge **MAPIUID** Daten geändert wird.</span><span class="sxs-lookup"><span data-stu-id="fb789-122">When a client transmits a message across a network, it should use a protocol or transmission format that does not change the byte order of **MAPIUID** data.</span></span> 
  
<span data-ttu-id="fb789-123">Weitere Informationen dazu, wie **MAPIUID** Strukturen verwendet werden finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="fb789-123">For more information about how **MAPIUID** structures are used, see the following topics:</span></span> 
  
[<span data-ttu-id="fb789-124">Registrieren der eindeutigen Dienstanbieterbezeichner</span><span class="sxs-lookup"><span data-stu-id="fb789-124">Registering Service Provider Unique Identifiers</span></span>](registering-service-provider-unique-identifiers.md)
  
[<span data-ttu-id="fb789-125">Festlegen der Transportreihenfolge</span><span class="sxs-lookup"><span data-stu-id="fb789-125">Setting Transport Order</span></span>](setting-transport-order.md)
  
## <a name="see-also"></a><span data-ttu-id="fb789-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb789-126">See also</span></span>



[<span data-ttu-id="fb789-127">GUID</span><span class="sxs-lookup"><span data-stu-id="fb789-127">GUID</span></span>](guid.md)
  
[<span data-ttu-id="fb789-128">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="fb789-128">IMAPISession::OpenProfileSection</span></span>](imapisession-openprofilesection.md)
  
[<span data-ttu-id="fb789-129">IMAPISupport::NewUID</span><span class="sxs-lookup"><span data-stu-id="fb789-129">IMAPISupport::NewUID</span></span>](imapisupport-newuid.md)


[<span data-ttu-id="fb789-130">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="fb789-130">MAPI Structures</span></span>](mapi-structures.md)

