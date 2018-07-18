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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e4bce7f122522532023d18b43fe4bfdeda84af9b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791668"
---
# <a name="fgetcomponentpath"></a><span data-ttu-id="c0b46-103">FGetComponentPath</span><span class="sxs-lookup"><span data-stu-id="c0b46-103">FGetComponentPath</span></span>

  
  
<span data-ttu-id="c0b46-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c0b46-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c0b46-105">Gibt den Pfad zu der privaten Mapi32.dll zurück.</span><span class="sxs-lookup"><span data-stu-id="c0b46-105">Returns the path to the private Mapi32.dll.</span></span>
  
```cpp
BOOL FGetComponentPath(
  LPCSTR szComponent,
  LPSTR szQualifier,
  LPSTR szDllPath,
  DWORD cchBufferSize,
  BOOL fInstall
);
```

## <a name="parameters"></a><span data-ttu-id="c0b46-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0b46-106">Parameters</span></span>

 <span data-ttu-id="c0b46-107">_szComponent_</span><span class="sxs-lookup"><span data-stu-id="c0b46-107">_szComponent_</span></span>
  
> <span data-ttu-id="c0b46-108">[in] Die MSIComponentID-Registrierungsschlüssel in [Mapi32.dll Stub Registrierungseinstellungen](http://msdn.microsoft.com/en-us/library/dd162409.aspx)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c0b46-108">[in] The MSIComponentID reg key described in [Mapi32.dll Stub Registry Settings](http://msdn.microsoft.com/en-us/library/dd162409.aspx).</span></span>
    
 <span data-ttu-id="c0b46-109">_szQualifier_</span><span class="sxs-lookup"><span data-stu-id="c0b46-109">_szQualifier_</span></span>
  
> <span data-ttu-id="c0b46-110">[in] Die MSIApplicationLCID oder MSIOfficeLCID Unterschlüssel in [Wählen Sie eine bestimmte Version von MAPI auf Load](how-to-choose-a-specific-version-of-mapi-to-load.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c0b46-110">[in] The MSIApplicationLCID or MSIOfficeLCID subkey described in [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span></span> <span data-ttu-id="c0b46-111">Anrufer können **null** übergeben, wenn kein Qualifizierer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c0b46-111">Callers can pass **null** if there is no qualifier.</span></span> 
    
 <span data-ttu-id="c0b46-112">_szDllPath_</span><span class="sxs-lookup"><span data-stu-id="c0b46-112">_szDllPath_</span></span>
  
> <span data-ttu-id="c0b46-113">[in] Der Pfad zu der privaten Mapi32.dll, die vollständigen MAPI-Funktionalität (die gleichen Exporte als die Mapi32.dll) hat.</span><span class="sxs-lookup"><span data-stu-id="c0b46-113">[in] The path to the private Mapi32.dll, which has full MAPI functionality (the same exports as the Mapi32.dll).</span></span>
    
 <span data-ttu-id="c0b46-114">_cchBufferSize_</span><span class="sxs-lookup"><span data-stu-id="c0b46-114">_cchBufferSize_</span></span>
  
> <span data-ttu-id="c0b46-115">[in] Die Größe des _SzDllPath_in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="c0b46-115">[in] The size of  _szDllPath_, in characters.</span></span>
    
 <span data-ttu-id="c0b46-116">_fInstall_</span><span class="sxs-lookup"><span data-stu-id="c0b46-116">_fInstall_</span></span>
  
> <span data-ttu-id="c0b46-117">[in] Erfahren Sie mehr MAPI, um die private Mapi32.dll Komponente zu installieren, wenn es nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c0b46-117">[in] Tells MAPI to install the private Mapi32.dll component if it is absent.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c0b46-118">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="c0b46-118">Return value</span></span>

 <span data-ttu-id="c0b46-119">**"true"**</span><span class="sxs-lookup"><span data-stu-id="c0b46-119">**true**</span></span>
  
> <span data-ttu-id="c0b46-120">Der Pfad wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="c0b46-120">The path was found.</span></span>
    
 <span data-ttu-id="c0b46-121">**false**</span><span class="sxs-lookup"><span data-stu-id="c0b46-121">**false**</span></span>
  
> <span data-ttu-id="c0b46-122">Der Pfad wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="c0b46-122">The path was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c0b46-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0b46-123">Remarks</span></span>

<span data-ttu-id="c0b46-124">Verwenden Sie die **FGetComponentPath** -Funktion, wenn Sie den Pfad der privaten Mapi32.dll abzurufen müssen.</span><span class="sxs-lookup"><span data-stu-id="c0b46-124">Use the **FGetComponentPath** function when you need to get the path to the private Mapi32.dll.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c0b46-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0b46-125">See also</span></span>



[<span data-ttu-id="c0b46-126">Auswählen einer bestimmten zu ladenden MAPI-Version</span><span class="sxs-lookup"><span data-stu-id="c0b46-126">Choose a Specific Version of MAPI to Load</span></span>](how-to-choose-a-specific-version-of-mapi-to-load.md)


[<span data-ttu-id="c0b46-127">Mapi32.dll Stub Registrierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="c0b46-127">Mapi32.dll Stub Registry Settings</span></span>](http://msdn.microsoft.com/en-us/library/dd162409.aspx)

