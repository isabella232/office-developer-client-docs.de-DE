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
ms.openlocfilehash: da314205f7d2dd746b72aa7e2b5ff2a13bb0c21b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432205"
---
# <a name="mapiuid"></a><span data-ttu-id="0e13f-103">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="0e13f-103">MAPIUID</span></span>

  
  
<span data-ttu-id="0e13f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e13f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e13f-105">Eine unabhängige Bytereihenfolge einer [GUID-Struktur,](guid.md) die zum eindeutigen Identifizieren eines Dienstanbieters verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0e13f-105">A byte-order independent version of a [GUID](guid.md) structure that is used to uniquely identify a service provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0e13f-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="0e13f-106">Header file:</span></span>  <br/> |<span data-ttu-id="0e13f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0e13f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0e13f-108">Verwandtes Makro:</span><span class="sxs-lookup"><span data-stu-id="0e13f-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="0e13f-109">IsEqualMAPIUID</span><span class="sxs-lookup"><span data-stu-id="0e13f-109">IsEqualMAPIUID</span></span>](isequalmapiuid.md) <br/> |
   
```cpp
typedef struct _MAPIUID
{
  BYTE ab[16];
} MAPIUID, FAR *LPMAPIUID;

```

## <a name="members"></a><span data-ttu-id="0e13f-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="0e13f-110">Members</span></span>

 <span data-ttu-id="0e13f-111">**ab**</span><span class="sxs-lookup"><span data-stu-id="0e13f-111">**ab**</span></span>
  
> <span data-ttu-id="0e13f-112">Ein Array, das einen 16-Byte-Bezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="0e13f-112">An array that contains a 16-byte identifier.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0e13f-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0e13f-113">Remarks</span></span>

<span data-ttu-id="0e13f-114">Eine **MAPIUID-Struktur** ist eine **GUID-Struktur,** die in intel® Prozessor-Bytereihenfolge geordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0e13f-114">A **MAPIUID** structure is a **GUID** structure put into Intel® processor byte order.</span></span> 
  
<span data-ttu-id="0e13f-115">MAPI erstellt **MAPIUID-Strukturen** so, dass es sehr selten ist, dass zwei unterschiedliche Elemente denselben Bezeichner haben.</span><span class="sxs-lookup"><span data-stu-id="0e13f-115">MAPI creates **MAPIUID** structures in a way that makes it very rare for two different items to have the same identifier.</span></span> <span data-ttu-id="0e13f-116">**MAPIUID-Strukturen** können als binäre Eigenschaften oder als Dateien gespeichert werden, unabhängig von der Bytereihenfolge des Computers, der die Informationen speichert oder auf diese zu zugegriffen hat.</span><span class="sxs-lookup"><span data-stu-id="0e13f-116">**MAPIUID** structures can be stored as binary properties or as files, without regard to the byte ordering of the computer storing or accessing the information.</span></span> 
  
 <span data-ttu-id="0e13f-117">**Es werden MAPIUID-Strukturen** verwendet:</span><span class="sxs-lookup"><span data-stu-id="0e13f-117">**MAPIUID** structures are used:</span></span> 
  
- <span data-ttu-id="0e13f-118">So identifizieren Sie einen Profilabschnitt.</span><span class="sxs-lookup"><span data-stu-id="0e13f-118">To identify a profile section.</span></span>
    
- <span data-ttu-id="0e13f-119">In den Eintragsbezeichnern von Nachrichtenspeicher- und Adressbuchobjekten, um den zuständigen Dienstanbieter zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="0e13f-119">In the entry identifiers of message store and address book objects to identify the responsible service provider.</span></span>
    
- <span data-ttu-id="0e13f-120">In der **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) -Eigenschaft von Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="0e13f-120">In the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property of messages.</span></span>
    
<span data-ttu-id="0e13f-121">Zum Generieren eines **MAPIUID-Bezeichners** für einen Suchschlüssel rufen Dienstanbieter [IMAPISupport::NewUID auf.](imapisupport-newuid.md)</span><span class="sxs-lookup"><span data-stu-id="0e13f-121">To generate a **MAPIUID** identifier for a search key, service providers call [IMAPISupport::NewUID](imapisupport-newuid.md).</span></span>
  
<span data-ttu-id="0e13f-122">Wenn ein Client eine Nachricht über ein Netzwerk überträgt, sollte er ein Protokoll- oder Übertragungsformat verwenden, das die Bytereihenfolge von **MAPIUID-Daten nicht** ändert.</span><span class="sxs-lookup"><span data-stu-id="0e13f-122">When a client transmits a message across a network, it should use a protocol or transmission format that does not change the byte order of **MAPIUID** data.</span></span> 
  
<span data-ttu-id="0e13f-123">Weitere Informationen zur Verwendung von **MAPIUID-Strukturen** finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="0e13f-123">For more information about how **MAPIUID** structures are used, see the following topics:</span></span> 
  
[<span data-ttu-id="0e13f-124">Registrieren eindeutiger Bezeichner des Dienstanbieters</span><span class="sxs-lookup"><span data-stu-id="0e13f-124">Registering Service Provider Unique Identifiers</span></span>](registering-service-provider-unique-identifiers.md)
  
[<span data-ttu-id="0e13f-125">Festlegen der Transportreihenfolge</span><span class="sxs-lookup"><span data-stu-id="0e13f-125">Setting Transport Order</span></span>](setting-transport-order.md)
  
## <a name="see-also"></a><span data-ttu-id="0e13f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e13f-126">See also</span></span>



[<span data-ttu-id="0e13f-127">GUID</span><span class="sxs-lookup"><span data-stu-id="0e13f-127">GUID</span></span>](guid.md)
  
[<span data-ttu-id="0e13f-128">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="0e13f-128">IMAPISession::OpenProfileSection</span></span>](imapisession-openprofilesection.md)
  
[<span data-ttu-id="0e13f-129">IMAPISupport::NewUID</span><span class="sxs-lookup"><span data-stu-id="0e13f-129">IMAPISupport::NewUID</span></span>](imapisupport-newuid.md)


[<span data-ttu-id="0e13f-130">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="0e13f-130">MAPI Structures</span></span>](mapi-structures.md)

