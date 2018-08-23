---
title: MAPIAdminProfiles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAdminProfiles
api_type:
- HeaderDef
ms.assetid: 82a9e379-39e4-4257-8cba-a6758f431cdc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 843eed06f30dcca530cf4306c9e03bbffbb05af5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581286"
---
# <a name="mapiadminprofiles"></a><span data-ttu-id="a8fff-103">MAPIAdminProfiles</span><span class="sxs-lookup"><span data-stu-id="a8fff-103">MAPIAdminProfiles</span></span>

  
  
<span data-ttu-id="a8fff-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8fff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8fff-105">Erstellt ein Profil Administration-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a8fff-105">Creates a profile administration object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a8fff-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="a8fff-106">Header file:</span></span>  <br/> |<span data-ttu-id="a8fff-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="a8fff-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="a8fff-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="a8fff-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a8fff-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a8fff-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a8fff-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="a8fff-110">Called by:</span></span>  <br/> |<span data-ttu-id="a8fff-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="a8fff-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPIAdminProfiles(
  ULONG ulFlags,
  LPPROFADMIN FAR * lppProfAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="a8fff-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8fff-112">Parameters</span></span>

 <span data-ttu-id="a8fff-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a8fff-113">_ulFlags_</span></span>
  
> <span data-ttu-id="a8fff-114">[in] Bitmaske aus Flags, die Optionen für die Funktion Eintrag angibt.</span><span class="sxs-lookup"><span data-stu-id="a8fff-114">[in] Bitmask of flags indicating options for the service entry function.</span></span> 
    
 <span data-ttu-id="a8fff-115">_lppProfAdmin_</span><span class="sxs-lookup"><span data-stu-id="a8fff-115">_lppProfAdmin_</span></span>
  
> <span data-ttu-id="a8fff-116">[out] Zeiger auf einen Zeiger auf das neue Profil Administration-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a8fff-116">[out] Pointer to a pointer to the new profile administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a8fff-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="a8fff-117">Return value</span></span>

<span data-ttu-id="a8fff-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="a8fff-118">S_OK</span></span> 
  
> <span data-ttu-id="a8fff-119">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="a8fff-119">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="a8fff-120">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="a8fff-120">MFCMAPI reference</span></span>

<span data-ttu-id="a8fff-121">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a8fff-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a8fff-122">**Datei**</span><span class="sxs-lookup"><span data-stu-id="a8fff-122">**File**</span></span>|<span data-ttu-id="a8fff-123">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="a8fff-123">**Function**</span></span>|<span data-ttu-id="a8fff-124">**Comment**</span><span class="sxs-lookup"><span data-stu-id="a8fff-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a8fff-125">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="a8fff-125">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="a8fff-126">CMapiObjects::GetProfAdmin</span><span class="sxs-lookup"><span data-stu-id="a8fff-126">CMapiObjects::GetProfAdmin</span></span>  <br/> |<span data-ttu-id="a8fff-127">MFCMAPI (engl.) verwendet die **"MAPIAdminProfiles"** -Methode, um das Profil Administration-Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a8fff-127">MFCMAPI uses the **MAPIAdminProfiles** method to get the profile administration object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a8fff-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8fff-128">See also</span></span>



[<span data-ttu-id="a8fff-129">IProfAdmin::CreateProfile</span><span class="sxs-lookup"><span data-stu-id="a8fff-129">IProfAdmin::CreateProfile</span></span>](iprofadmin-createprofile.md)


[<span data-ttu-id="a8fff-130">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="a8fff-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

