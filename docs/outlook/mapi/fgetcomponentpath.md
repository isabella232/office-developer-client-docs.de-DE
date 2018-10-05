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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384500"
---
# <a name="fgetcomponentpath"></a><span data-ttu-id="85888-103">FGetComponentPath</span><span class="sxs-lookup"><span data-stu-id="85888-103">FGetComponentPath</span></span>

  
  
<span data-ttu-id="85888-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85888-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85888-105">Gibt den Pfad zu der privaten Mapi32.dll zurück.</span><span class="sxs-lookup"><span data-stu-id="85888-105">Returns the path to the private Mapi32.dll.</span></span>
  
```cpp
BOOL FGetComponentPath(
  LPCSTR szComponent,
  LPSTR szQualifier,
  LPSTR szDllPath,
  DWORD cchBufferSize,
  BOOL fInstall
);
```

## <a name="parameters"></a><span data-ttu-id="85888-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="85888-106">Parameters</span></span>

 <span data-ttu-id="85888-107">_szComponent_</span><span class="sxs-lookup"><span data-stu-id="85888-107">_szComponent_</span></span>
  
> <span data-ttu-id="85888-108">[in] Die MSIComponentID-Registrierungsschlüssel in [Mapi32.dll Stub Registrierungseinstellungen](https://msdn.microsoft.com/library/dd162409.aspx)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="85888-108">[in] The MSIComponentID reg key described in [Mapi32.dll Stub Registry Settings](https://msdn.microsoft.com/library/dd162409.aspx).</span></span>
    
 <span data-ttu-id="85888-109">_szQualifier_</span><span class="sxs-lookup"><span data-stu-id="85888-109">_szQualifier_</span></span>
  
> <span data-ttu-id="85888-110">[in] Die MSIApplicationLCID oder MSIOfficeLCID Unterschlüssel in [Wählen Sie eine bestimmte Version von MAPI auf Load](how-to-choose-a-specific-version-of-mapi-to-load.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="85888-110">[in] The MSIApplicationLCID or MSIOfficeLCID subkey described in [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span></span> <span data-ttu-id="85888-111">Anrufer können **null** übergeben, wenn kein Qualifizierer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="85888-111">Callers can pass **null** if there is no qualifier.</span></span> 
    
 <span data-ttu-id="85888-112">_szDllPath_</span><span class="sxs-lookup"><span data-stu-id="85888-112">_szDllPath_</span></span>
  
> <span data-ttu-id="85888-113">[in] Der Pfad zu der privaten Mapi32.dll, die vollständigen MAPI-Funktionalität (die gleichen Exporte als die Mapi32.dll) hat.</span><span class="sxs-lookup"><span data-stu-id="85888-113">[in] The path to the private Mapi32.dll, which has full MAPI functionality (the same exports as the Mapi32.dll).</span></span>
    
 <span data-ttu-id="85888-114">_cchBufferSize_</span><span class="sxs-lookup"><span data-stu-id="85888-114">_cchBufferSize_</span></span>
  
> <span data-ttu-id="85888-115">[in] Die Größe des _SzDllPath_in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="85888-115">[in] The size of  _szDllPath_, in characters.</span></span>
    
 <span data-ttu-id="85888-116">_fInstall_</span><span class="sxs-lookup"><span data-stu-id="85888-116">_fInstall_</span></span>
  
> <span data-ttu-id="85888-117">[in] Erfahren Sie mehr MAPI, um die private Mapi32.dll Komponente zu installieren, wenn es nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="85888-117">[in] Tells MAPI to install the private Mapi32.dll component if it is absent.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="85888-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="85888-118">Return value</span></span>

 <span data-ttu-id="85888-119">**"true"**</span><span class="sxs-lookup"><span data-stu-id="85888-119">**true**</span></span>
  
> <span data-ttu-id="85888-120">Der Pfad wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="85888-120">The path was found.</span></span>
    
 <span data-ttu-id="85888-121">**false**</span><span class="sxs-lookup"><span data-stu-id="85888-121">**false**</span></span>
  
> <span data-ttu-id="85888-122">Der Pfad wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="85888-122">The path was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="85888-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="85888-123">Remarks</span></span>

<span data-ttu-id="85888-124">Verwenden Sie die **FGetComponentPath** -Funktion, wenn Sie den Pfad der privaten Mapi32.dll abzurufen müssen.</span><span class="sxs-lookup"><span data-stu-id="85888-124">Use the **FGetComponentPath** function when you need to get the path to the private Mapi32.dll.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="85888-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85888-125">See also</span></span>



[<span data-ttu-id="85888-126">Auswählen einer bestimmten zu ladenden MAPI-Version</span><span class="sxs-lookup"><span data-stu-id="85888-126">Choose a Specific Version of MAPI to Load</span></span>](how-to-choose-a-specific-version-of-mapi-to-load.md)


[<span data-ttu-id="85888-127">Mapi32.dll Stub Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="85888-127">Mapi32.dll Stub Registry Settings</span></span>](https://msdn.microsoft.com/library/dd162409.aspx)

