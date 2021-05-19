---
title: PidTagProviderIcon (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 55e6c8fb013e544ae04740aeaeb23ac23949cffb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425638"
---
# <a name="pidtagprovidericon-canonical-property"></a><span data-ttu-id="df7fe-103">PidTagProviderIcon (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="df7fe-103">PidTagProviderIcon Canonical Property</span></span>

  
  
<span data-ttu-id="df7fe-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df7fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df7fe-105">Enthält eine Unicode-Zeichenfolge, die ein benutzerdefiniertes Symbol oder ein benutzerdefiniertes Symbol angibt, das für einen MAPI-Anbieter in der Microsoft Office Outlook Statusleiste im Online- und Offlinestatus angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="df7fe-105">Contains a Unicode string that specifies a custom icon or icons to be displayed for a MAPI provider in the Microsoft Office Outlook status bar in both online and offline states.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="df7fe-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="df7fe-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="df7fe-107">PR_PROVIDER_ICON, PR_PROVIDER_ICON_W</span><span class="sxs-lookup"><span data-stu-id="df7fe-107">PR_PROVIDER_ICON, PR_PROVIDER_ICON_W</span></span>  <br/> |
|<span data-ttu-id="df7fe-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="df7fe-108">Identifier:</span></span>  <br/> |<span data-ttu-id="df7fe-109">0x3417</span><span class="sxs-lookup"><span data-stu-id="df7fe-109">0x3417</span></span>  <br/> |
|<span data-ttu-id="df7fe-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="df7fe-110">Data type:</span></span>  <br/> |<span data-ttu-id="df7fe-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="df7fe-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="df7fe-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="df7fe-112">Area:</span></span>  <br/> |<span data-ttu-id="df7fe-113">MAPI-Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="df7fe-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df7fe-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="df7fe-114">Remarks</span></span>

<span data-ttu-id="df7fe-115">Diese Eigenschaften geben die Ressourcendatei an, die ein benutzerdefiniertes Symbol enthält, das einen MAPI-Anbieter in einem Onlinestatus darstellt, und optional ein weiteres benutzerdefiniertes Symbol im Offlinestatus.</span><span class="sxs-lookup"><span data-stu-id="df7fe-115">These properties specify the resource file that contains a custom icon that represents a MAPI provider in an online state, and optionally, another custom icon in the offline state.</span></span> <span data-ttu-id="df7fe-116">Outlook fordert diese Eigenschaften immer in der Unicode-Darstellung an.</span><span class="sxs-lookup"><span data-stu-id="df7fe-116">Outlook always requests these properties in Unicode representation.</span></span> 
  
<span data-ttu-id="df7fe-117">Der folgende Eigenschaftswert z. B. anweisen Outlook Symbol-ID 1001 aus dem Modul mymod32.dll zu laden und dieses Symbol für den Onlinestatus zu verwenden: `mymod32.dll,#1001` .</span><span class="sxs-lookup"><span data-stu-id="df7fe-117">For example, the following property value instructs Outlook to load icon ID 1001 from the module mymod32.dll and use that icon for the online state:  `mymod32.dll,#1001`.</span></span> <span data-ttu-id="df7fe-118">Da es kein anbieterspezifisches Symbol für den Offlinestatus gibt, wird in diesem Fall das standard-Outlook-Offlinesymbol in der Statusleiste verwendet.</span><span class="sxs-lookup"><span data-stu-id="df7fe-118">Since there is no provider-specific icon for the offline state, in this case, the standard Outlook offline icon is used in the status bar.</span></span> 
  
<span data-ttu-id="df7fe-119">Der folgende Eigenschaftswert wies Outlook an, die Symbol-ID 1001 aus dem Modul mymod32.dll zu laden und dieses Symbol für den Onlinestatus zu verwenden und auch die Symbol-ID 1002 aus diesem Modul zu laden, das für den Offlinestatus verwendet werden soll: `mymod32.dll,#1001,#1002` .</span><span class="sxs-lookup"><span data-stu-id="df7fe-119">The following property value instructs Outlook to load icon ID 1001 from the module mymod32.dll and use that icon for the online state, and to also load icon ID 1002 from this same module to be used for the offline state:  `mymod32.dll,#1001,#1002`.</span></span> <span data-ttu-id="df7fe-120">Es Outlook in der Statusleiste kein Symbol verwendet.</span><span class="sxs-lookup"><span data-stu-id="df7fe-120">No Outlook icon is used in the status bar.</span></span> 
  
<span data-ttu-id="df7fe-121">Wenn keine benutzerdefinierten Symbole angegeben werden, wird der Anbieter standardmäßig durch die Outlook für den Onlinestatus und den Offlinestatus dargestellt.</span><span class="sxs-lookup"><span data-stu-id="df7fe-121">By default, if no custom icons are specified, the provider is represented by the Outlook default icons for the online state and the offline state.</span></span> <span data-ttu-id="df7fe-122">Der Anbieter kann optional einen Anzeigenamen angeben, der neben dem Symbol in der Statusleiste angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="df7fe-122">The provider can optionally specify a display name to be shown adjacent to the icon in the status bar.</span></span> <span data-ttu-id="df7fe-123">Weitere Informationen finden Sie **unter PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="df7fe-123">For more information, see **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="df7fe-124">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="df7fe-124">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="df7fe-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="df7fe-125">Header files</span></span>

<span data-ttu-id="df7fe-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="df7fe-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="df7fe-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="df7fe-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="df7fe-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="df7fe-128">Mapitags.h</span></span>
  
> <span data-ttu-id="df7fe-129">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="df7fe-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="df7fe-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df7fe-130">See also</span></span>



[<span data-ttu-id="df7fe-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="df7fe-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="df7fe-132">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="df7fe-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="df7fe-133">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="df7fe-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="df7fe-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="df7fe-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

