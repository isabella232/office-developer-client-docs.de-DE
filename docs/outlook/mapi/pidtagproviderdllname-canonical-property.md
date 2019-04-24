---
title: Kanonische Pidtagproviderdllname (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderDllName
api_type:
- COM
ms.assetid: 9ddb38eb-9a32-4dbe-b42c-6ea9db98acd2
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 57fdc754ed4be29dbdd50a198707d8f39a14b3d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286488"
---
# <a name="pidtagproviderdllname-canonical-property"></a><span data-ttu-id="c9476-103">Kanonische Pidtagproviderdllname (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c9476-103">PidTagProviderDllName Canonical Property</span></span>

  
  
<span data-ttu-id="c9476-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9476-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9476-105">Enthält den Namen der Basisdatei der DLL (Dynamic-Link Library) des MAPI-Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="c9476-105">Contains the base file name of the MAPI service provider dynamic-link library (DLL).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c9476-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c9476-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c9476-107">PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W</span><span class="sxs-lookup"><span data-stu-id="c9476-107">PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="c9476-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="c9476-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c9476-109">0x300A</span><span class="sxs-lookup"><span data-stu-id="c9476-109">0x300A</span></span>  <br/> |
|<span data-ttu-id="c9476-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c9476-110">Data type:</span></span>  <br/> |<span data-ttu-id="c9476-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c9476-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c9476-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c9476-112">Area:</span></span>  <br/> |<span data-ttu-id="c9476-113">MAPI allgemein</span><span class="sxs-lookup"><span data-stu-id="c9476-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9476-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9476-114">Remarks</span></span>

<span data-ttu-id="c9476-115">MAPI verwendet eine Benennungskonvention für DLL-Dateien.</span><span class="sxs-lookup"><span data-stu-id="c9476-115">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="c9476-116">Sie fügt die Zeichenfolge 32 an den Basis-DLL-Namen an, um die Version zu identifizieren, die auf 32-Bit-Plattformen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c9476-116">It appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="c9476-117">Wenn beispielsweise der Name "MAPI" lautet. DLL angegeben ist, erstellt MAPI den Namen MAPI32. DLL zur Darstellung der entsprechenden 32-Bit-Version der DLL.</span><span class="sxs-lookup"><span data-stu-id="c9476-117">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="c9476-118">Diese Eigenschaften sollten den Basisnamen angeben.</span><span class="sxs-lookup"><span data-stu-id="c9476-118">These properties should specify the base name.</span></span> <span data-ttu-id="c9476-119">MAPI fügt die Zeichenfolge 32 entsprechend an.</span><span class="sxs-lookup"><span data-stu-id="c9476-119">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="c9476-120">Das Einschließen der Zeichenfolge 32 als Teil dieser Eigenschaft führt zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="c9476-120">Including the string 32 as part of this property results in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c9476-121">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c9476-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c9476-122">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="c9476-122">Header files</span></span>

<span data-ttu-id="c9476-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c9476-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="c9476-124">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="c9476-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="c9476-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="c9476-125">Mapitags.h</span></span>
  
> <span data-ttu-id="c9476-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="c9476-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c9476-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9476-127">See also</span></span>



[<span data-ttu-id="c9476-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c9476-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c9476-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c9476-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c9476-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c9476-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c9476-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c9476-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

