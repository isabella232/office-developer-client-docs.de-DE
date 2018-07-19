---
title: PidTagDefaultViewEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultViewEntryId
api_type:
- HeaderDef
ms.assetid: 1b4e82ed-c207-4828-8a5b-0ef312962355
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0db245efdd8aad73b0c094c35079f50925ca4478
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794292"
---
# <a name="pidtagdefaultviewentryid-canonical-property"></a><span data-ttu-id="51596-103">PidTagDefaultViewEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="51596-103">PidTagDefaultViewEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="51596-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="51596-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="51596-105">Enthält die Eintrags-ID der Standardansicht für einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="51596-105">Contains the entry identifier of a folder's default view.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="51596-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="51596-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="51596-107">PR_DEFAULT_VIEW_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="51596-107">PR_DEFAULT_VIEW_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="51596-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="51596-108">Identifier:</span></span>  <br/> |<span data-ttu-id="51596-109">0x3616</span><span class="sxs-lookup"><span data-stu-id="51596-109">0x3616</span></span>  <br/> |
|<span data-ttu-id="51596-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="51596-110">Data type:</span></span>  <br/> |<span data-ttu-id="51596-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="51596-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="51596-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="51596-112">Area:</span></span>  <br/> |<span data-ttu-id="51596-113">MAPI-container</span><span class="sxs-lookup"><span data-stu-id="51596-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51596-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51596-114">Remarks</span></span>

<span data-ttu-id="51596-115">Diese Eigenschaft ist die Eintrags-ID der Ordneransicht, die als Standardansicht festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="51596-115">This property is the entry identifier of the folder view that should be set as the initial view.</span></span> <span data-ttu-id="51596-116">Die Eigenschaft muss nicht festgelegt werden, wenn die Ansicht "Normal" als Standardansicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51596-116">The property need not be set if the "Normal" view is to be used as the initial view.</span></span>
  
<span data-ttu-id="51596-117">Eine Clientanwendung diese Eigenschaft zum Zeitpunkt geöffnet wird den Ordner abrufen und erhebliche Leistungsvorteile erzielt.</span><span class="sxs-lookup"><span data-stu-id="51596-117">A client application can obtain this property at the time it opens the folder and realize significant performance gains.</span></span> <span data-ttu-id="51596-118">Diese Eigenschaft kann als eine Verknüpfung zum Abrufen der Standardansicht, anstatt die zugeordneten Inhaltstabelle öffnen, und senden Sie eine Einschränkung von verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51596-118">This property can be used as a shortcut to obtain the default view, instead of opening the associated contents table and submitting a restriction.</span></span>
  
<span data-ttu-id="51596-119">Die Implementierung einer Service Provider der [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) -Methode kann diese Eigenschaft kopieren, wenn Ordner kopiert.</span><span class="sxs-lookup"><span data-stu-id="51596-119">A service provider implementation of the [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) method can copy this property when it copies folders.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="51596-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="51596-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="51596-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="51596-121">Protocol specifications</span></span>

<span data-ttu-id="51596-122">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51596-122">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51596-123">Ordner Vorgänge behandelt.</span><span class="sxs-lookup"><span data-stu-id="51596-123">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="51596-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="51596-124">Header files</span></span>

<span data-ttu-id="51596-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="51596-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="51596-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="51596-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="51596-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="51596-127">Mapitags.h</span></span>
  
> <span data-ttu-id="51596-128">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="51596-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="51596-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51596-129">See also</span></span>



[<span data-ttu-id="51596-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51596-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="51596-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51596-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="51596-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="51596-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="51596-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="51596-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

