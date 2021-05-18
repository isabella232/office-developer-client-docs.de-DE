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
ms.openlocfilehash: e5043a614ccd94994fe86838f15aa1a43f22733e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412352"
---
# <a name="mapiadminprofiles"></a><span data-ttu-id="a6cb3-103">MAPIAdminProfiles</span><span class="sxs-lookup"><span data-stu-id="a6cb3-103">MAPIAdminProfiles</span></span>

  
  
<span data-ttu-id="a6cb3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6cb3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6cb3-105">Erstellt ein Profilverwaltungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="a6cb3-105">Creates a profile administration object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a6cb3-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="a6cb3-106">Header file:</span></span>  <br/> |<span data-ttu-id="a6cb3-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="a6cb3-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="a6cb3-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="a6cb3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a6cb3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a6cb3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a6cb3-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="a6cb3-110">Called by:</span></span>  <br/> |<span data-ttu-id="a6cb3-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="a6cb3-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPIAdminProfiles(
  ULONG ulFlags,
  LPPROFADMIN FAR * lppProfAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="a6cb3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6cb3-112">Parameters</span></span>

 <span data-ttu-id="a6cb3-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a6cb3-113">_ulFlags_</span></span>
  
> <span data-ttu-id="a6cb3-114">[in] Bitmaske mit Flags, die Optionen für die Diensteingabefunktion angibt.</span><span class="sxs-lookup"><span data-stu-id="a6cb3-114">[in] Bitmask of flags indicating options for the service entry function.</span></span> 
    
 <span data-ttu-id="a6cb3-115">_lppProfAdmin_</span><span class="sxs-lookup"><span data-stu-id="a6cb3-115">_lppProfAdmin_</span></span>
  
> <span data-ttu-id="a6cb3-116">[out] Zeiger auf einen Zeiger auf das neue Profilverwaltungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="a6cb3-116">[out] Pointer to a pointer to the new profile administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a6cb3-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a6cb3-117">Return value</span></span>

<span data-ttu-id="a6cb3-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="a6cb3-118">S_OK</span></span> 
  
> <span data-ttu-id="a6cb3-119">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="a6cb3-119">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="a6cb3-120">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="a6cb3-120">MFCMAPI reference</span></span>

<span data-ttu-id="a6cb3-121">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a6cb3-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a6cb3-122">**Datei**</span><span class="sxs-lookup"><span data-stu-id="a6cb3-122">**File**</span></span>|<span data-ttu-id="a6cb3-123">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="a6cb3-123">**Function**</span></span>|<span data-ttu-id="a6cb3-124">**Comment**</span><span class="sxs-lookup"><span data-stu-id="a6cb3-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a6cb3-125">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="a6cb3-125">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="a6cb3-126">CMapiObjects::GetProfAdmin</span><span class="sxs-lookup"><span data-stu-id="a6cb3-126">CMapiObjects::GetProfAdmin</span></span>  <br/> |<span data-ttu-id="a6cb3-127">MFCMAPI verwendet die **MAPIAdminProfiles-Methode,** um das Profilverwaltungsobjekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a6cb3-127">MFCMAPI uses the **MAPIAdminProfiles** method to get the profile administration object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a6cb3-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6cb3-128">See also</span></span>



[<span data-ttu-id="a6cb3-129">IProfAdmin::CreateProfile</span><span class="sxs-lookup"><span data-stu-id="a6cb3-129">IProfAdmin::CreateProfile</span></span>](iprofadmin-createprofile.md)


[<span data-ttu-id="a6cb3-130">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="a6cb3-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

