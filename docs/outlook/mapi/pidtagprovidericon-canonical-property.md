---
title: Kanonische Pidtagprovidericon (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderIcon
api_type:
- COM
ms.assetid: 59c84b1f-13b5-484b-b703-2fb9fcc6c7eb
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 55e6c8fb013e544ae04740aeaeb23ac23949cffb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286460"
---
# <a name="pidtagprovidericon-canonical-property"></a><span data-ttu-id="9b33c-103">Kanonische Pidtagprovidericon (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9b33c-103">PidTagProviderIcon Canonical Property</span></span>

  
  
<span data-ttu-id="9b33c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b33c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b33c-105">Enthält eine Unicode-Zeichenfolge, die ein benutzerdefiniertes Symbol oder Symbole angibt, die für einen MAPI-Anbieter in der Microsoft Office Outlook-Statusleiste in Online-und Offline Zuständen angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9b33c-105">Contains a Unicode string that specifies a custom icon or icons to be displayed for a MAPI provider in the Microsoft Office Outlook status bar in both online and offline states.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9b33c-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="9b33c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9b33c-107">PR_PROVIDER_ICON, PR_PROVIDER_ICON_W</span><span class="sxs-lookup"><span data-stu-id="9b33c-107">PR_PROVIDER_ICON, PR_PROVIDER_ICON_W</span></span>  <br/> |
|<span data-ttu-id="9b33c-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="9b33c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9b33c-109">0x3417</span><span class="sxs-lookup"><span data-stu-id="9b33c-109">0x3417</span></span>  <br/> |
|<span data-ttu-id="9b33c-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="9b33c-110">Data type:</span></span>  <br/> |<span data-ttu-id="9b33c-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9b33c-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9b33c-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="9b33c-112">Area:</span></span>  <br/> |<span data-ttu-id="9b33c-113">MAPI-Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="9b33c-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b33c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b33c-114">Remarks</span></span>

<span data-ttu-id="9b33c-115">Diese Eigenschaften geben die Ressourcendatei an, die ein benutzerdefiniertes Symbol enthält, das einen MAPI-Anbieter in einem Onlinestatus darstellt, und optional ein weiteres benutzerdefiniertes Symbol im Offlinestatus.</span><span class="sxs-lookup"><span data-stu-id="9b33c-115">These properties specify the resource file that contains a custom icon that represents a MAPI provider in an online state, and optionally, another custom icon in the offline state.</span></span> <span data-ttu-id="9b33c-116">Diese Eigenschaften werden von Outlook immer in der Unicode-Darstellung angefordert.</span><span class="sxs-lookup"><span data-stu-id="9b33c-116">Outlook always requests these properties in Unicode representation.</span></span> 
  
<span data-ttu-id="9b33c-117">Der folgende Eigenschaftswert weist beispielsweise Outlook an, die Symbol-ID 1001 aus dem Modul mymod32. dll zu laden und dieses Symbol für den Online `mymod32.dll,#1001`Status zu verwenden:.</span><span class="sxs-lookup"><span data-stu-id="9b33c-117">For example, the following property value instructs Outlook to load icon ID 1001 from the module mymod32.dll and use that icon for the online state:  `mymod32.dll,#1001`.</span></span> <span data-ttu-id="9b33c-118">Da es kein anbieterspezifisches Symbol für den Offlinestatus gibt, wird in diesem Fall das Standardsymbol Outlook offline in der Statusleiste verwendet.</span><span class="sxs-lookup"><span data-stu-id="9b33c-118">Since there is no provider-specific icon for the offline state, in this case, the standard Outlook offline icon is used in the status bar.</span></span> 
  
<span data-ttu-id="9b33c-119">Der folgende Eigenschaftswert weist Outlook an, die Symbol-ID 1001 aus dem Modul mymod32. dll zu laden und dieses Symbol für den Onlinestatus zu verwenden und auch die Symbol-ID 1002 aus demselben Modul zu laden, das für `mymod32.dll,#1001,#1002`den Offlinestatus verwendet werden soll:.</span><span class="sxs-lookup"><span data-stu-id="9b33c-119">The following property value instructs Outlook to load icon ID 1001 from the module mymod32.dll and use that icon for the online state, and to also load icon ID 1002 from this same module to be used for the offline state:  `mymod32.dll,#1001,#1002`.</span></span> <span data-ttu-id="9b33c-120">In der Statusleiste wird kein Outlook-Symbol verwendet.</span><span class="sxs-lookup"><span data-stu-id="9b33c-120">No Outlook icon is used in the status bar.</span></span> 
  
<span data-ttu-id="9b33c-121">Wenn keine benutzerdefinierten Symbole angegeben werden, wird der Anbieter standardmäßig durch die Outlook-Standardsymbole für den Status Online und den Status Offline dargestellt.</span><span class="sxs-lookup"><span data-stu-id="9b33c-121">By default, if no custom icons are specified, the provider is represented by the Outlook default icons for the online state and the offline state.</span></span> <span data-ttu-id="9b33c-122">Der Anbieter kann optional einen Anzeigenamen angeben, der neben dem Symbol in der Statusleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b33c-122">The provider can optionally specify a display name to be shown adjacent to the icon in the status bar.</span></span> <span data-ttu-id="9b33c-123">Weitere Informationen finden Sie unter **PR_PROVIDER_DISPLAY_NAME_W** ([pidtagproviderdisplayname (](pidtagproviderdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9b33c-123">For more information, see **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9b33c-124">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9b33c-124">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9b33c-125">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="9b33c-125">Header files</span></span>

<span data-ttu-id="9b33c-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9b33c-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="9b33c-127">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="9b33c-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="9b33c-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="9b33c-128">Mapitags.h</span></span>
  
> <span data-ttu-id="9b33c-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="9b33c-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9b33c-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b33c-130">See also</span></span>



[<span data-ttu-id="9b33c-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9b33c-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9b33c-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9b33c-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9b33c-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="9b33c-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9b33c-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="9b33c-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

