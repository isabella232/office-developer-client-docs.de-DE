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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330198"
---
# <a name="imapisupportnewuid"></a><span data-ttu-id="d56b4-103">IMAPISupport::NewUID</span><span class="sxs-lookup"><span data-stu-id="d56b4-103">IMAPISupport::NewUID</span></span>

  
  
<span data-ttu-id="d56b4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d56b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d56b4-105">Erstellt eine neue [MAPIUID](mapiuid.md) -Struktur, die als eindeutiger Bezeichner verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d56b4-105">Creates a new [MAPIUID](mapiuid.md) structure to be used as a unique identifier.</span></span> 
  
```cpp
HRESULT NewUID(
LPMAPIUID lpMuid
);
```

## <a name="parameters"></a><span data-ttu-id="d56b4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d56b4-106">Parameters</span></span>

 <span data-ttu-id="d56b4-107">_lpMuid_</span><span class="sxs-lookup"><span data-stu-id="d56b4-107">_lpMuid_</span></span>
  
> <span data-ttu-id="d56b4-108">Ein Zeiger auf die neue **MAPIUID** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="d56b4-108">A pointer to the new **MAPIUID** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d56b4-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d56b4-109">Return value</span></span>

<span data-ttu-id="d56b4-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="d56b4-110">S_OK</span></span> 
  
> <span data-ttu-id="d56b4-111">Die neue **MAPIUID** -Struktur wurde erstellt.</span><span class="sxs-lookup"><span data-stu-id="d56b4-111">The new **MAPIUID** structure was created.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d56b4-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d56b4-112">Remarks</span></span>

<span data-ttu-id="d56b4-113">Die **IMAPISupport:: NewUID** -Methode wird für alle Support-Objekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="d56b4-113">The **IMAPISupport::NewUID** method is implemented for all support objects.</span></span> <span data-ttu-id="d56b4-114">Dienstanbieter und Nachrichtendienste rufen **NewUID** auf, wenn Sie einen langfristigen eindeutigen Bezeichner generieren müssen.</span><span class="sxs-lookup"><span data-stu-id="d56b4-114">Service providers and message services call **NewUID** whenever they need to generate a long-term unique identifier.</span></span> <span data-ttu-id="d56b4-115">Ein Nachrichtenspeicher Anbieter kann beispielsweise **NewUID** aufrufen, um eine **MAPIUID** abzurufen, die in die **PR_SEARCH_KEY** ([pidtagsearchkey (](pidtagsearchkey-canonical-property.md))-Eigenschaft einer neu erstellten Nachricht eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d56b4-115">A message store provider, for example, might call **NewUID** to obtain a **MAPIUID** to put in the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property of a newly created message.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="d56b4-116">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="d56b4-116">Notes to callers</span></span>

<span data-ttu-id="d56b4-117">Verwechseln Sie die **MAPIUID** -Struktur nicht, die Sie bei der Anmeldung mit den **MAPIUID** -Strukturen registrieren, die von der **NewUID** -Methode erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d56b4-117">Do not confuse the **MAPIUID** structure that you register at logon time with the **MAPIUID** structures that the **NewUID** method creates.</span></span> <span data-ttu-id="d56b4-118">Die **MAPIUID** -Struktur, die Sie beim Aufrufen der [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) -Methode registrieren, stellt das Adressbuch oder der Nachrichtenspeicher Anbieter in MAPI dar und dient zur Unterscheidung von Eintrags Bezeichnern, die von verschiedenen Anbietern erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d56b4-118">The **MAPIUID** structure that you register when you call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method represents your address book or message store provider to MAPI and is used to distinguish entry identifiers that different providers create.</span></span> <span data-ttu-id="d56b4-119">Diese **MAPIUID** -Struktur sollte hart codiert und nicht über einen Aufruf von **NewUID**abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d56b4-119">This **MAPIUID** structure should be hard-coded and not obtained through a call to **NewUID**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d56b4-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d56b4-120">See also</span></span>



[<span data-ttu-id="d56b4-121">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="d56b4-121">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="d56b4-122">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d56b4-122">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

