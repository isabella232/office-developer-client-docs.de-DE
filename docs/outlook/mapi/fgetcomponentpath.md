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
# <a name="fgetcomponentpath"></a><span data-ttu-id="f4748-103">FGetComponentPath</span><span class="sxs-lookup"><span data-stu-id="f4748-103">FGetComponentPath</span></span>

  
  
<span data-ttu-id="f4748-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4748-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4748-105">Gibt den Pfad zum privaten Mapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="f4748-105">Returns the path to the private Mapi32.dll.</span></span>
  
```cpp
BOOL FGetComponentPath(
  LPCSTR szComponent,
  LPSTR szQualifier,
  LPSTR szDllPath,
  DWORD cchBufferSize,
  BOOL fInstall
);
```

## <a name="parameters"></a><span data-ttu-id="f4748-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4748-106">Parameters</span></span>

 <span data-ttu-id="f4748-107">_szComponent_</span><span class="sxs-lookup"><span data-stu-id="f4748-107">_szComponent_</span></span>
  
> <span data-ttu-id="f4748-108">[in] Der MSIComponentID-Reg-Schlüssel, der unter [Mapi32.dll Stub registry Einstellungen](https://msdn.microsoft.com/library/dd162409.aspx).</span><span class="sxs-lookup"><span data-stu-id="f4748-108">[in] The MSIComponentID reg key described in [Mapi32.dll Stub Registry Settings](https://msdn.microsoft.com/library/dd162409.aspx).</span></span>
    
 <span data-ttu-id="f4748-109">_szQualifier_</span><span class="sxs-lookup"><span data-stu-id="f4748-109">_szQualifier_</span></span>
  
> <span data-ttu-id="f4748-110">[in] Der unter [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md)beschriebene Unterschlüssel MSIApplicationLCID oder MSIOfficeLCID.</span><span class="sxs-lookup"><span data-stu-id="f4748-110">[in] The MSIApplicationLCID or MSIOfficeLCID subkey described in [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span></span> <span data-ttu-id="f4748-111">Anrufer können **null übergeben,** wenn kein Qualifizierer vorlägig ist.</span><span class="sxs-lookup"><span data-stu-id="f4748-111">Callers can pass **null** if there is no qualifier.</span></span> 
    
 <span data-ttu-id="f4748-112">_szDllPath_</span><span class="sxs-lookup"><span data-stu-id="f4748-112">_szDllPath_</span></span>
  
> <span data-ttu-id="f4748-113">[in] Der Pfad zum privaten Mapi32.dll, der über vollständige MAPI-Funktionen verfügt (der gleiche Export wie der Mapi32.dll).</span><span class="sxs-lookup"><span data-stu-id="f4748-113">[in] The path to the private Mapi32.dll, which has full MAPI functionality (the same exports as the Mapi32.dll).</span></span>
    
 <span data-ttu-id="f4748-114">_cchBufferSize_</span><span class="sxs-lookup"><span data-stu-id="f4748-114">_cchBufferSize_</span></span>
  
> <span data-ttu-id="f4748-115">[in] Die Größe von  _szDllPath_ in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="f4748-115">[in] The size of  _szDllPath_, in characters.</span></span>
    
 <span data-ttu-id="f4748-116">_fInstall_</span><span class="sxs-lookup"><span data-stu-id="f4748-116">_fInstall_</span></span>
  
> <span data-ttu-id="f4748-117">[in] Weist MAPI an, die private Mapi32.dll zu installieren, wenn sie nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f4748-117">[in] Tells MAPI to install the private Mapi32.dll component if it is absent.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f4748-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f4748-118">Return value</span></span>

 <span data-ttu-id="f4748-119">**true**</span><span class="sxs-lookup"><span data-stu-id="f4748-119">**true**</span></span>
  
> <span data-ttu-id="f4748-120">Der Pfad wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="f4748-120">The path was found.</span></span>
    
 <span data-ttu-id="f4748-121">**false**</span><span class="sxs-lookup"><span data-stu-id="f4748-121">**false**</span></span>
  
> <span data-ttu-id="f4748-122">Der Pfad wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="f4748-122">The path was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f4748-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f4748-123">Remarks</span></span>

<span data-ttu-id="f4748-124">Verwenden Sie **die FGetComponentPath-Funktion,** wenn Sie den Pfad zum privaten Mapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="f4748-124">Use the **FGetComponentPath** function when you need to get the path to the private Mapi32.dll.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f4748-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4748-125">See also</span></span>



[<span data-ttu-id="f4748-126">Auswählen einer bestimmten Version der zu ladende MAPI</span><span class="sxs-lookup"><span data-stu-id="f4748-126">Choose a Specific Version of MAPI to Load</span></span>](how-to-choose-a-specific-version-of-mapi-to-load.md)


[<span data-ttu-id="f4748-127">Mapi32.dll stub Registry Einstellungen</span><span class="sxs-lookup"><span data-stu-id="f4748-127">Mapi32.dll Stub Registry Settings</span></span>](https://msdn.microsoft.com/library/dd162409.aspx)

