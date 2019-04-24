---
title: FGetComponentPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FGetComponentPath
api_type:
- COM
ms.assetid: 2a303458-3283-409a-bc3b-b891f3fcfc22
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3456d81935a0a94bc2158eefd321da968dda9983
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335210"
---
# <a name="fgetcomponentpath"></a><span data-ttu-id="2bf00-103">FGetComponentPath</span><span class="sxs-lookup"><span data-stu-id="2bf00-103">FGetComponentPath</span></span>

  
  
<span data-ttu-id="2bf00-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2bf00-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2bf00-105">Gibt den Pfad zur privaten Mapi32. dll zurück.</span><span class="sxs-lookup"><span data-stu-id="2bf00-105">Returns the path to the private Mapi32.dll.</span></span>
  
```cpp
BOOL FGetComponentPath(
  LPCSTR szComponent,
  LPSTR szQualifier,
  LPSTR szDllPath,
  DWORD cchBufferSize,
  BOOL fInstall
);
```

## <a name="parameters"></a><span data-ttu-id="2bf00-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2bf00-106">Parameters</span></span>

 <span data-ttu-id="2bf00-107">_szComponent_</span><span class="sxs-lookup"><span data-stu-id="2bf00-107">_szComponent_</span></span>
  
> <span data-ttu-id="2bf00-108">in Der MSIComponentID reg-Schlüssel, der in den [Mapi32. dll-Registrierungseinstellungen](https://msdn.microsoft.com/library/dd162409.aspx)beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="2bf00-108">[in] The MSIComponentID reg key described in [Mapi32.dll Stub Registry Settings](https://msdn.microsoft.com/library/dd162409.aspx).</span></span>
    
 <span data-ttu-id="2bf00-109">_szQualifier_</span><span class="sxs-lookup"><span data-stu-id="2bf00-109">_szQualifier_</span></span>
  
> <span data-ttu-id="2bf00-110">in Der Unterschlüssel MSIApplicationLCID oder MSIOfficeLCID, der in [Wählen Sie eine bestimmte Version von MAPI zum Laden](how-to-choose-a-specific-version-of-mapi-to-load.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2bf00-110">[in] The MSIApplicationLCID or MSIOfficeLCID subkey described in [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span></span> <span data-ttu-id="2bf00-111">Aufrufer können **null** , wenn kein Qualifizierer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2bf00-111">Callers can pass **null** if there is no qualifier.</span></span> 
    
 <span data-ttu-id="2bf00-112">_szDllPath_</span><span class="sxs-lookup"><span data-stu-id="2bf00-112">_szDllPath_</span></span>
  
> <span data-ttu-id="2bf00-113">in Der Pfad zur privaten Mapi32. dll, die vollständige MAPI-Funktionalität aufweist (derselbe Export wie der Mapi32. dll).</span><span class="sxs-lookup"><span data-stu-id="2bf00-113">[in] The path to the private Mapi32.dll, which has full MAPI functionality (the same exports as the Mapi32.dll).</span></span>
    
 <span data-ttu-id="2bf00-114">_cchBufferSize_</span><span class="sxs-lookup"><span data-stu-id="2bf00-114">_cchBufferSize_</span></span>
  
> <span data-ttu-id="2bf00-115">in Die Größe von _szDllPath_in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="2bf00-115">[in] The size of  _szDllPath_, in characters.</span></span>
    
 <span data-ttu-id="2bf00-116">_fInstall_</span><span class="sxs-lookup"><span data-stu-id="2bf00-116">_fInstall_</span></span>
  
> <span data-ttu-id="2bf00-117">in Weist MAPI an, die private Mapi32. dll-Komponente zu installieren, wenn Sie nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2bf00-117">[in] Tells MAPI to install the private Mapi32.dll component if it is absent.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2bf00-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2bf00-118">Return value</span></span>

 <span data-ttu-id="2bf00-119">**true**</span><span class="sxs-lookup"><span data-stu-id="2bf00-119">**true**</span></span>
  
> <span data-ttu-id="2bf00-120">Der Pfad wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="2bf00-120">The path was found.</span></span>
    
 <span data-ttu-id="2bf00-121">**false**</span><span class="sxs-lookup"><span data-stu-id="2bf00-121">**false**</span></span>
  
> <span data-ttu-id="2bf00-122">Der Pfad wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="2bf00-122">The path was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2bf00-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2bf00-123">Remarks</span></span>

<span data-ttu-id="2bf00-124">Verwenden Sie die **FGetComponentPath** -Funktion, wenn Sie den Pfad zur privaten Mapi32. dll abrufen müssen.</span><span class="sxs-lookup"><span data-stu-id="2bf00-124">Use the **FGetComponentPath** function when you need to get the path to the private Mapi32.dll.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2bf00-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2bf00-125">See also</span></span>



[<span data-ttu-id="2bf00-126">Auswählen einer bestimmten zu ladenden MAPI-Version</span><span class="sxs-lookup"><span data-stu-id="2bf00-126">Choose a Specific Version of MAPI to Load</span></span>](how-to-choose-a-specific-version-of-mapi-to-load.md)


[<span data-ttu-id="2bf00-127">Mapi32. dll-Stub-Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="2bf00-127">Mapi32.dll Stub Registry Settings</span></span>](https://msdn.microsoft.com/library/dd162409.aspx)

