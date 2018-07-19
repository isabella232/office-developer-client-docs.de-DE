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
ms.openlocfilehash: 14be41c21244abe8c54261a95a410828c973d66b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792386"
---
# <a name="imapisupportnewuid"></a><span data-ttu-id="c7165-103">IMAPISupport::NewUID</span><span class="sxs-lookup"><span data-stu-id="c7165-103">IMAPISupport::NewUID</span></span>

  
  
<span data-ttu-id="c7165-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c7165-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c7165-105">Erstellt eine neue [MAPIUID](mapiuid.md) -Struktur, die als eindeutiger Bezeichner verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c7165-105">Creates a new [MAPIUID](mapiuid.md) structure to be used as a unique identifier.</span></span> 
  
```cpp
HRESULT NewUID(
LPMAPIUID lpMuid
);
```

## <a name="parameters"></a><span data-ttu-id="c7165-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7165-106">Parameters</span></span>

 <span data-ttu-id="c7165-107">_lpMuid_</span><span class="sxs-lookup"><span data-stu-id="c7165-107">_lpMuid_</span></span>
  
> <span data-ttu-id="c7165-108">Ein Zeiger auf die neue **MAPIUID** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="c7165-108">A pointer to the new **MAPIUID** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c7165-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c7165-109">Return value</span></span>

<span data-ttu-id="c7165-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="c7165-110">S_OK</span></span> 
  
> <span data-ttu-id="c7165-111">Die neue **MAPIUID** Struktur erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="c7165-111">The new **MAPIUID** structure was created.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c7165-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7165-112">Remarks</span></span>

<span data-ttu-id="c7165-113">Die **IMAPISupport::NewUID** -Methode wird für alle Unterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="c7165-113">The **IMAPISupport::NewUID** method is implemented for all support objects.</span></span> <span data-ttu-id="c7165-114">Dienstanbieter und Message-Dienste aufrufen **NewUID** , wenn sie benötigen, um eine langfristige eindeutige ID zu generieren.</span><span class="sxs-lookup"><span data-stu-id="c7165-114">Service providers and message services call **NewUID** whenever they need to generate a long-term unique identifier.</span></span> <span data-ttu-id="c7165-115">Eine Nachricht Speicheranbieter, zum Beispiel, **NewUID** zum Abrufen einer **MAPIUID** in die **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))-Eigenschaft einer neu erstellten Nachricht platzieren aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="c7165-115">A message store provider, for example, might call **NewUID** to obtain a **MAPIUID** to put in the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property of a newly created message.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="c7165-116">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="c7165-116">Notes to callers</span></span>

<span data-ttu-id="c7165-117">Verwechseln Sie nicht die **MAPIUID** -Struktur, die Sie bei der Anmeldung mit den Strukturen **MAPIUID** registrieren, die die **NewUID** -Methode erstellt.</span><span class="sxs-lookup"><span data-stu-id="c7165-117">Do not confuse the **MAPIUID** structure that you register at logon time with the **MAPIUID** structures that the **NewUID** method creates.</span></span> <span data-ttu-id="c7165-118">Die **MAPIUID** -Struktur, die Sie registrieren, wenn Sie die [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) -Methode aufrufen, stellt Adressbuch oder Nachricht MAPI-Speicheranbieter und wird verwendet, um die Eintrags-IDs zu unterscheiden, die verschiedene Anbieter erstellen.</span><span class="sxs-lookup"><span data-stu-id="c7165-118">The **MAPIUID** structure that you register when you call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method represents your address book or message store provider to MAPI and is used to distinguish entry identifiers that different providers create.</span></span> <span data-ttu-id="c7165-119">Diese Struktur **MAPIUID** sollte hartcodierte und nicht durch einen Aufruf von **NewUID**abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c7165-119">This **MAPIUID** structure should be hard-coded and not obtained through a call to **NewUID**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c7165-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7165-120">See also</span></span>



[<span data-ttu-id="c7165-121">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="c7165-121">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="c7165-122">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c7165-122">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

