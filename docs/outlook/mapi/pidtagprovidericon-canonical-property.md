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
ms.openlocfilehash: 61dc61872e8d1ed525d5ac3c46c56ccc3e45ea5e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593697"
---
# <a name="pidtagprovidericon-canonical-property"></a><span data-ttu-id="405b0-103">PidTagProviderIcon (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="405b0-103">PidTagProviderIcon Canonical Property</span></span>

  
  
<span data-ttu-id="405b0-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="405b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="405b0-105">Enthält eine Unicodezeichenfolge, die ein benutzerdefiniertes Symbol oder Symbole für einen MAPI-Anbieter in der Statusleiste von Microsoft Office Outlook im online und offline Zustand anzuzeigende angibt.</span><span class="sxs-lookup"><span data-stu-id="405b0-105">Contains a Unicode string that specifies a custom icon or icons to be displayed for a MAPI provider in the Microsoft Office Outlook status bar in both online and offline states.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="405b0-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="405b0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="405b0-107">PR_PROVIDER_ICON PR_PROVIDER_ICON_W</span><span class="sxs-lookup"><span data-stu-id="405b0-107">PR_PROVIDER_ICON, PR_PROVIDER_ICON_W</span></span>  <br/> |
|<span data-ttu-id="405b0-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="405b0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="405b0-109">0x3417</span><span class="sxs-lookup"><span data-stu-id="405b0-109">0x3417</span></span>  <br/> |
|<span data-ttu-id="405b0-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="405b0-110">Data type:</span></span>  <br/> |<span data-ttu-id="405b0-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="405b0-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="405b0-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="405b0-112">Area:</span></span>  <br/> |<span data-ttu-id="405b0-113">MAPI-Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="405b0-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="405b0-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="405b0-114">Remarks</span></span>

<span data-ttu-id="405b0-115">Diese Eigenschaften geben Sie die Ressourcendatei, die ein benutzerdefiniertes Symbol enthält, die einen MAPI-Anbieter Status online, darstellt und optional ein anderes benutzerdefiniertes Symbol in den Offlinemodus.</span><span class="sxs-lookup"><span data-stu-id="405b0-115">These properties specify the resource file that contains a custom icon that represents a MAPI provider in an online state, and optionally, another custom icon in the offline state.</span></span> <span data-ttu-id="405b0-116">Outlook fordert immer diese Eigenschaften im Unicode-Darstellung.</span><span class="sxs-lookup"><span data-stu-id="405b0-116">Outlook always requests these properties in Unicode representation.</span></span> 
  
<span data-ttu-id="405b0-117">Beispielsweise weist die folgenden Eigenschaftswert Outlook Symbol-ID 1001 aus der mymod32.dll Modul zu laden, und verwenden Sie das Symbol für den Status online: `mymod32.dll,#1001`.</span><span class="sxs-lookup"><span data-stu-id="405b0-117">For example, the following property value instructs Outlook to load icon ID 1001 from the module mymod32.dll and use that icon for the online state:  `mymod32.dll,#1001`.</span></span> <span data-ttu-id="405b0-118">Da kein anbieterspezifische Symbol für den Status offline vorhanden ist, wird in diesem Fall das standard-Outlook-offline-Symbol in der Statusleiste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="405b0-118">Since there is no provider-specific icon for the offline state, in this case, the standard Outlook offline icon is used in the status bar.</span></span> 
  
<span data-ttu-id="405b0-119">Der Wert der folgenden-Eigenschaft weist Outlook zum Symbol-ID 1001 aus dem Modul mymod32.dll laden und verwenden Sie das Symbol für den Status online und Symbol-ID 1002 auch aus der gleichen Modul für die offline-Status zu verwendende geladen: `mymod32.dll,#1001,#1002`.</span><span class="sxs-lookup"><span data-stu-id="405b0-119">The following property value instructs Outlook to load icon ID 1001 from the module mymod32.dll and use that icon for the online state, and to also load icon ID 1002 from this same module to be used for the offline state:  `mymod32.dll,#1001,#1002`.</span></span> <span data-ttu-id="405b0-120">Kein Outlook-Symbol wird in der Statusleiste verwendet.</span><span class="sxs-lookup"><span data-stu-id="405b0-120">No Outlook icon is used in the status bar.</span></span> 
  
<span data-ttu-id="405b0-121">Standardmäßig wird der Anbieter keine benutzerdefinierten Symbolen angegeben, durch die Outlook-Standard-Symbole für den Status online und offline-Status dargestellt.</span><span class="sxs-lookup"><span data-stu-id="405b0-121">By default, if no custom icons are specified, the provider is represented by the Outlook default icons for the online state and the offline state.</span></span> <span data-ttu-id="405b0-122">Der Anbieter kann optional einen Anzeigenamen ein, in der Statusleiste neben dem Symbol angezeigt werden soll angeben.</span><span class="sxs-lookup"><span data-stu-id="405b0-122">The provider can optionally specify a display name to be shown adjacent to the icon in the status bar.</span></span> <span data-ttu-id="405b0-123">Weitere Informationen finden Sie unter **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="405b0-123">For more information, see **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="405b0-124">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="405b0-124">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="405b0-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="405b0-125">Header files</span></span>

<span data-ttu-id="405b0-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="405b0-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="405b0-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="405b0-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="405b0-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="405b0-128">Mapitags.h</span></span>
  
> <span data-ttu-id="405b0-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="405b0-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="405b0-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="405b0-130">See also</span></span>



[<span data-ttu-id="405b0-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="405b0-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="405b0-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="405b0-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="405b0-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="405b0-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="405b0-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="405b0-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

