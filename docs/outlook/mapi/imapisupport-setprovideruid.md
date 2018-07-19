---
title: IMAPISupportSetProviderUID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SetProviderUID
api_type:
- COM
ms.assetid: 58855843-9a2b-4e5d-9332-b1bfad8b45e4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2182ec71c54c81e9a43a34973e005292ddccdfff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792415"
---
# <a name="imapisupportsetprovideruid"></a><span data-ttu-id="df831-103">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="df831-103">IMAPISupport::SetProviderUID</span></span>

  
  
<span data-ttu-id="df831-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="df831-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="df831-105">Registriert eine [MAPIUID](mapiuid.md) -Struktur, die den Dienstanbieter eindeutig darstellt.</span><span class="sxs-lookup"><span data-stu-id="df831-105">Registers a [MAPIUID](mapiuid.md) structure that uniquely represents the service provider.</span></span> 
  
```cpp
HRESULT SetProviderUID(
LPMAPIUID lpProviderID,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="df831-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="df831-106">Parameters</span></span>

 <span data-ttu-id="df831-107">_lpProviderID_</span><span class="sxs-lookup"><span data-stu-id="df831-107">_lpProviderID_</span></span>
  
> <span data-ttu-id="df831-108">[in] Ein Zeiger auf die **MAPIUID** -Struktur, die den Anbieter Address Book oder einer Nachricht Store identifiziert.</span><span class="sxs-lookup"><span data-stu-id="df831-108">[in] A pointer to the **MAPIUID** structure that identifies the address book or message store provider.</span></span> 
    
 <span data-ttu-id="df831-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="df831-109">_ulFlags_</span></span>
  
> <span data-ttu-id="df831-110">Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="df831-110">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="df831-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="df831-111">Return value</span></span>

<span data-ttu-id="df831-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="df831-112">S_OK</span></span> 
  
> <span data-ttu-id="df831-113">Die Struktur **MAPIUID** wurde erfolgreich registriert.</span><span class="sxs-lookup"><span data-stu-id="df831-113">The **MAPIUID** structure was successfully registered.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="df831-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="df831-114">Remarks</span></span>

<span data-ttu-id="df831-115">Die **IMAPISupport::SetProviderUID** -Methode wird für Adresse Adressbuch und Nachricht Store Anbieter Unterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="df831-115">The **IMAPISupport::SetProviderUID** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="df831-116">Diese Anbieter Aufrufen **SetProviderUID** zum Registrieren eines eindeutigen Bezeichners beschrieben in der **MAPIUID** -Struktur, die mit _LpProviderID_gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="df831-116">These providers call **SetProviderUID** to register a unique identifier described in the **MAPIUID** structure that is pointed to by  _lpProviderID_.</span></span> <span data-ttu-id="df831-117">Anbieter: Dieser Bezeichner in allen den Eintrag-IDs, die sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="df831-117">Providers include this identifier in all of the entry identifiers that they create.</span></span> 
  
<span data-ttu-id="df831-118">MAPI verwendet die **MAPIUID** -Struktur beim Senden ausgehender Nachrichten die Warteschlange MAPI und den entsprechenden Anbieter für die Verarbeitung von Clientanforderungen bestimmen.</span><span class="sxs-lookup"><span data-stu-id="df831-118">MAPI uses the **MAPIUID** structure when it sends outbound messages to the MAPI spooler and to determine the appropriate provider for handling client requests.</span></span> <span data-ttu-id="df831-119">Beispiel: Wenn ein Client die [IMAPISession::OpenEntry](imapisession-openentry.md) -Methode aufruft, MAPI untersucht den **MAPIUID** Teil des Eintrags-ID, ordnet sie den Anbieter, der sie **SetProviderUID**übergeben, und ruft diesen Anbieter **OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="df831-119">For example, when a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method, MAPI examines the **MAPIUID** portion of the entry identifier, maps it to the provider that passed it to **SetProviderUID**, and calls that provider's **OpenEntry**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="df831-120">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="df831-120">Notes to callers</span></span>

<span data-ttu-id="df831-121">Rufen Sie **SetProviderUID** bei der Anmeldung die **MAPIUID** -Struktur zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="df831-121">Call **SetProviderUID** at logon time to register your **MAPIUID** structure.</span></span> <span data-ttu-id="df831-122">MAPI ermöglicht Adresse Adressbuch und Nachricht Speicheranbieter mehrere Bezeichner registriert.</span><span class="sxs-lookup"><span data-stu-id="df831-122">MAPI allows address book and message store providers to register multiple identifiers.</span></span> <span data-ttu-id="df831-123">Wenn Sie mehrere Aufrufe von **SetProviderUID**vornehmen, hinzugefügt immer die **MAPIUID** -Struktur des Anbieters Satz von **MAPIUID** -Strukturen, auch wenn die **MAPIUID** ein Duplikat ist.</span><span class="sxs-lookup"><span data-stu-id="df831-123">When you make multiple calls to **SetProviderUID**, it always adds the **MAPIUID** structure to the provider's set of **MAPIUID** structures, even if the **MAPIUID** is a duplicate.</span></span> <span data-ttu-id="df831-124">**SetProviderUID** kann keiner **MAPIUID**entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="df831-124">**SetProviderUID** cannot remove a **MAPIUID**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="df831-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df831-125">See also</span></span>



[<span data-ttu-id="df831-126">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="df831-126">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="df831-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="df831-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

