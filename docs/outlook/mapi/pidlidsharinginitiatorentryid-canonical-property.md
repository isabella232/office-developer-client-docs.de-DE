---
title: PidLidSharingInitiatorEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingInitiatorEntryId
api_type:
- COM
ms.assetid: 47f00706-83df-49cb-bda7-ef572d76a020
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bfe682fc3263278c6e1d02a29a8b6432f41ac79e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396407"
---
# <a name="pidlidsharinginitiatorentryid-canonical-property"></a><span data-ttu-id="0f749-103">PidLidSharingInitiatorEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0f749-103">PidLidSharingInitiatorEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="0f749-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f749-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0f749-105">Legt fest, wie eine eine Freigabenachricht-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="0f749-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0f749-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0f749-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0f749-107">dispidSharingInitiatorEid</span><span class="sxs-lookup"><span data-stu-id="0f749-107">dispidSharingInitiatorEid</span></span>  <br/> |
|<span data-ttu-id="0f749-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="0f749-108">Property set:</span></span>  <br/> |<span data-ttu-id="0f749-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="0f749-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="0f749-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="0f749-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0f749-111">0x00008A09</span><span class="sxs-lookup"><span data-stu-id="0f749-111">0x00008A09</span></span>  <br/> |
|<span data-ttu-id="0f749-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0f749-112">Data type:</span></span>  <br/> |<span data-ttu-id="0f749-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0f749-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0f749-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0f749-114">Area:</span></span>  <br/> |<span data-ttu-id="0f749-115">Freigabe</span><span class="sxs-lookup"><span data-stu-id="0f749-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0f749-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0f749-116">Remarks</span></span>

<span data-ttu-id="0f749-117">Diese Eigenschaft muss auf den Wert der Eigenschaft **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) für das Adressbuch des aktuell angemeldeten Benutzers festgelegt werden (siehe [[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)).</span><span class="sxs-lookup"><span data-stu-id="0f749-117">This property must be set to the value of the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property for the Address Book of the currently logged-on user (see [[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0f749-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0f749-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0f749-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0f749-119">Protocol specifications</span></span>

<span data-ttu-id="0f749-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f749-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f749-121">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="0f749-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0f749-122">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f749-122">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f749-123">Teilt Postfachordner zwischen Clients.</span><span class="sxs-lookup"><span data-stu-id="0f749-123">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0f749-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="0f749-124">Header files</span></span>

<span data-ttu-id="0f749-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0f749-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="0f749-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="0f749-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0f749-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f749-127">See also</span></span>



[<span data-ttu-id="0f749-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0f749-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0f749-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0f749-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0f749-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0f749-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0f749-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0f749-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

