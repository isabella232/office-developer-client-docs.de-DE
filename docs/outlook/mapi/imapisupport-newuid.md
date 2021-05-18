---
title: IMAPISupportNewUID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.NewUID
api_type:
- COM
ms.assetid: 7994477d-5207-4335-b538-69c98782d52d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a38f7ea475f8a5cbad4f1cc295c3e2550ea8cd66
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406997"
---
# <a name="imapisupportnewuid"></a><span data-ttu-id="3bd2b-103">IMAPISupport::NewUID</span><span class="sxs-lookup"><span data-stu-id="3bd2b-103">IMAPISupport::NewUID</span></span>

  
  
<span data-ttu-id="3bd2b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3bd2b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3bd2b-105">Erstellt eine neue [MAPIUID-Struktur,](mapiuid.md) die als eindeutiger Bezeichner verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3bd2b-105">Creates a new [MAPIUID](mapiuid.md) structure to be used as a unique identifier.</span></span> 
  
```cpp
HRESULT NewUID(
LPMAPIUID lpMuid
);
```

## <a name="parameters"></a><span data-ttu-id="3bd2b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3bd2b-106">Parameters</span></span>

 <span data-ttu-id="3bd2b-107">_lpMuid_</span><span class="sxs-lookup"><span data-stu-id="3bd2b-107">_lpMuid_</span></span>
  
> <span data-ttu-id="3bd2b-108">Ein Zeiger auf die neue **MAPIUID-Struktur.**</span><span class="sxs-lookup"><span data-stu-id="3bd2b-108">A pointer to the new **MAPIUID** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3bd2b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3bd2b-109">Return value</span></span>

<span data-ttu-id="3bd2b-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="3bd2b-110">S_OK</span></span> 
  
> <span data-ttu-id="3bd2b-111">Die neue **MAPIUID-Struktur** wurde erstellt.</span><span class="sxs-lookup"><span data-stu-id="3bd2b-111">The new **MAPIUID** structure was created.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3bd2b-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3bd2b-112">Remarks</span></span>

<span data-ttu-id="3bd2b-113">Die **IMAPISupport::NewUID-Methode** wird für alle Supportobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="3bd2b-113">The **IMAPISupport::NewUID** method is implemented for all support objects.</span></span> <span data-ttu-id="3bd2b-114">Dienstanbieter und Nachrichtendienste rufen **NewUID** auf, wenn sie einen langfristigen eindeutigen Bezeichner generieren müssen.</span><span class="sxs-lookup"><span data-stu-id="3bd2b-114">Service providers and message services call **NewUID** whenever they need to generate a long-term unique identifier.</span></span> <span data-ttu-id="3bd2b-115">Ein Nachrichtenspeicheranbieter kann beispielsweise **NewUID** aufrufen, um eine **MAPIUID** zu erhalten, die in der **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))-Eigenschaft einer neu erstellten Nachricht gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3bd2b-115">A message store provider, for example, might call **NewUID** to obtain a **MAPIUID** to put in the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property of a newly created message.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="3bd2b-116">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="3bd2b-116">Notes to callers</span></span>

<span data-ttu-id="3bd2b-117">Verwechseln Sie nicht die **MAPIUID-Struktur,** die Sie bei der Anmeldung registrieren, mit den **MAPIUID-Strukturen,** die die **NewUID-Methode** erstellt.</span><span class="sxs-lookup"><span data-stu-id="3bd2b-117">Do not confuse the **MAPIUID** structure that you register at logon time with the **MAPIUID** structures that the **NewUID** method creates.</span></span> <span data-ttu-id="3bd2b-118">Die **MAPIUID-Struktur,** die Sie beim Aufrufen der [IMAPISupport::SetProviderUID-Methode](imapisupport-setprovideruid.md) registrieren, stellt Ihren Adressbuch- oder Nachrichtenspeicheranbieter für MAPI dar und wird verwendet, um Eintragsbezeichner zu unterscheiden, die von verschiedenen Anbietern erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="3bd2b-118">The **MAPIUID** structure that you register when you call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method represents your address book or message store provider to MAPI and is used to distinguish entry identifiers that different providers create.</span></span> <span data-ttu-id="3bd2b-119">Diese **MAPIUID-Struktur** sollte hart codiert sein und nicht über einen Aufruf von **NewUID erhalten werden.**</span><span class="sxs-lookup"><span data-stu-id="3bd2b-119">This **MAPIUID** structure should be hard-coded and not obtained through a call to **NewUID**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3bd2b-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3bd2b-120">See also</span></span>



[<span data-ttu-id="3bd2b-121">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="3bd2b-121">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="3bd2b-122">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="3bd2b-122">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

