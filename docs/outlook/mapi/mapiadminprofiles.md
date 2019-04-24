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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e5043a614ccd94994fe86838f15aa1a43f22733e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357330"
---
# <a name="mapiadminprofiles"></a><span data-ttu-id="36faf-103">MAPIAdminProfiles</span><span class="sxs-lookup"><span data-stu-id="36faf-103">MAPIAdminProfiles</span></span>

  
  
<span data-ttu-id="36faf-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36faf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36faf-105">Erstellt ein Profilverwaltungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="36faf-105">Creates a profile administration object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="36faf-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="36faf-106">Header file:</span></span>  <br/> |<span data-ttu-id="36faf-107">Mapix. h</span><span class="sxs-lookup"><span data-stu-id="36faf-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="36faf-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="36faf-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="36faf-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="36faf-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="36faf-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="36faf-110">Called by:</span></span>  <br/> |<span data-ttu-id="36faf-111">Client Anwendungen</span><span class="sxs-lookup"><span data-stu-id="36faf-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPIAdminProfiles(
  ULONG ulFlags,
  LPPROFADMIN FAR * lppProfAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="36faf-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="36faf-112">Parameters</span></span>

 <span data-ttu-id="36faf-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="36faf-113">_ulFlags_</span></span>
  
> <span data-ttu-id="36faf-114">in Bitmaske von Flags, die Optionen für die Dienst Eingabefunktion angeben.</span><span class="sxs-lookup"><span data-stu-id="36faf-114">[in] Bitmask of flags indicating options for the service entry function.</span></span> 
    
 <span data-ttu-id="36faf-115">_lppProfAdmin_</span><span class="sxs-lookup"><span data-stu-id="36faf-115">_lppProfAdmin_</span></span>
  
> <span data-ttu-id="36faf-116">Out Zeiger auf einen Zeiger auf das neue Profilverwaltungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="36faf-116">[out] Pointer to a pointer to the new profile administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="36faf-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="36faf-117">Return value</span></span>

<span data-ttu-id="36faf-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="36faf-118">S_OK</span></span> 
  
> <span data-ttu-id="36faf-119">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="36faf-119">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="36faf-120">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="36faf-120">MFCMAPI reference</span></span>

<span data-ttu-id="36faf-121">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="36faf-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="36faf-122">**Datei**</span><span class="sxs-lookup"><span data-stu-id="36faf-122">**File**</span></span>|<span data-ttu-id="36faf-123">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="36faf-123">**Function**</span></span>|<span data-ttu-id="36faf-124">**Comment**</span><span class="sxs-lookup"><span data-stu-id="36faf-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="36faf-125">MAPIObjects. cpp</span><span class="sxs-lookup"><span data-stu-id="36faf-125">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="36faf-126">CMapiObjects:: GetProfAdmin</span><span class="sxs-lookup"><span data-stu-id="36faf-126">CMapiObjects::GetProfAdmin</span></span>  <br/> |<span data-ttu-id="36faf-127">MFCMAPI verwendet die **MAPIAdminProfiles** -Methode, um das Profilverwaltungsobjekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="36faf-127">MFCMAPI uses the **MAPIAdminProfiles** method to get the profile administration object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="36faf-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36faf-128">See also</span></span>



[<span data-ttu-id="36faf-129">IProfAdmin::CreateProfile</span><span class="sxs-lookup"><span data-stu-id="36faf-129">IProfAdmin::CreateProfile</span></span>](iprofadmin-createprofile.md)


[<span data-ttu-id="36faf-130">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="36faf-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

