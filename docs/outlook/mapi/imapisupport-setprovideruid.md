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
ms.openlocfilehash: a60ac0d7ab139f77aea87080e1ce37fee870e97b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437539"
---
# <a name="imapisupportsetprovideruid"></a><span data-ttu-id="043c0-103">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="043c0-103">IMAPISupport::SetProviderUID</span></span>

  
  
<span data-ttu-id="043c0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="043c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="043c0-105">Registriert eine [MAPIUID](mapiuid.md) -Struktur, die den Dienstanbieter eindeutig darstellt.</span><span class="sxs-lookup"><span data-stu-id="043c0-105">Registers a [MAPIUID](mapiuid.md) structure that uniquely represents the service provider.</span></span> 
  
```cpp
HRESULT SetProviderUID(
LPMAPIUID lpProviderID,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="043c0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="043c0-106">Parameters</span></span>

 <span data-ttu-id="043c0-107">_lpProviderID_</span><span class="sxs-lookup"><span data-stu-id="043c0-107">_lpProviderID_</span></span>
  
> <span data-ttu-id="043c0-108">in Ein Zeiger auf die **MAPIUID** -Struktur, die das Adressbuch oder den Nachrichtenspeicher Anbieter identifiziert.</span><span class="sxs-lookup"><span data-stu-id="043c0-108">[in] A pointer to the **MAPIUID** structure that identifies the address book or message store provider.</span></span> 
    
 <span data-ttu-id="043c0-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="043c0-109">_ulFlags_</span></span>
  
> <span data-ttu-id="043c0-110">Reserviert muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="043c0-110">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="043c0-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="043c0-111">Return value</span></span>

<span data-ttu-id="043c0-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="043c0-112">S_OK</span></span> 
  
> <span data-ttu-id="043c0-113">Die **MAPIUID** -Struktur wurde erfolgreich registriert.</span><span class="sxs-lookup"><span data-stu-id="043c0-113">The **MAPIUID** structure was successfully registered.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="043c0-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="043c0-114">Remarks</span></span>

<span data-ttu-id="043c0-115">Die **IMAPISupport:: SetProviderUID** -Methode wird für Support Objekte des Adressbuchs und des Nachrichtenspeichers implementiert.</span><span class="sxs-lookup"><span data-stu-id="043c0-115">The **IMAPISupport::SetProviderUID** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="043c0-116">Diese Anbieter rufen **SetProviderUID** auf, um einen eindeutigen Bezeichner zu registrieren, der in der **MAPIUID** -Struktur beschrieben ist, auf die von _lpProviderID_verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="043c0-116">These providers call **SetProviderUID** to register a unique identifier described in the **MAPIUID** structure that is pointed to by  _lpProviderID_.</span></span> <span data-ttu-id="043c0-117">Anbieter schließen diesen Bezeichner in alle Eintrags-IDs ein, die Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="043c0-117">Providers include this identifier in all of the entry identifiers that they create.</span></span> 
  
<span data-ttu-id="043c0-118">MAPI verwendet die **MAPIUID** -Struktur beim Senden ausgehender Nachrichten an den MAPI-Spooler und zum Bestimmen des geeigneten Anbieters für die Verarbeitung von Clientanforderungen.</span><span class="sxs-lookup"><span data-stu-id="043c0-118">MAPI uses the **MAPIUID** structure when it sends outbound messages to the MAPI spooler and to determine the appropriate provider for handling client requests.</span></span> <span data-ttu-id="043c0-119">Wenn ein Client beispielsweise die [IMAPISession:: OpenEntry](imapisession-openentry.md) -Methode aufruft, untersucht MAPI **den MAPIUID** -Teil der Eintrags-ID, ordnet ihn dem Anbieter zu, der ihn an **SetProviderUID**übergeben hat, und ruft den OpenEntry- **Eintrag** des Anbieters auf. .</span><span class="sxs-lookup"><span data-stu-id="043c0-119">For example, when a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method, MAPI examines the **MAPIUID** portion of the entry identifier, maps it to the provider that passed it to **SetProviderUID**, and calls that provider's **OpenEntry**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="043c0-120">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="043c0-120">Notes to callers</span></span>

<span data-ttu-id="043c0-121">Rufen Sie **SetProviderUID** bei der Anmeldung auf, um Ihre **MAPIUID** -Struktur zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="043c0-121">Call **SetProviderUID** at logon time to register your **MAPIUID** structure.</span></span> <span data-ttu-id="043c0-122">MAPI ermöglicht es Adressbuch-und Nachrichtenspeicher Anbietern, mehrere Bezeichner zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="043c0-122">MAPI allows address book and message store providers to register multiple identifiers.</span></span> <span data-ttu-id="043c0-123">Wenn Sie mehrere Aufrufe an **SetProviderUID**durchführen, wird die **MAPIUID** -Struktur immer dem Satz von **MAPIUID** -Strukturen des Anbieters hinzugefügt, auch wenn die **MAPIUID** ein Duplikat ist.</span><span class="sxs-lookup"><span data-stu-id="043c0-123">When you make multiple calls to **SetProviderUID**, it always adds the **MAPIUID** structure to the provider's set of **MAPIUID** structures, even if the **MAPIUID** is a duplicate.</span></span> <span data-ttu-id="043c0-124">**SetProviderUID** kann keine **MAPIUID**entfernen.</span><span class="sxs-lookup"><span data-stu-id="043c0-124">**SetProviderUID** cannot remove a **MAPIUID**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="043c0-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="043c0-125">See also</span></span>



[<span data-ttu-id="043c0-126">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="043c0-126">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="043c0-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="043c0-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

