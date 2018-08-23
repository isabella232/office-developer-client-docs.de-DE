---
title: PidTagPstPathHint (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 9cb4af50-3735-4029-a608-a6e7927019dd
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6b71feb6d5967eab3aa490a256825a2803381f40
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569092"
---
# <a name="pidtagpstpathhint-canonical-property"></a><span data-ttu-id="0b1b9-103">PidTagPstPathHint (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0b1b9-103">PidTagPstPathHint Canonical Property</span></span>

  
  
<span data-ttu-id="0b1b9-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0b1b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0b1b9-105">Enthält den Namen der persönlicher Speicher-Tabelle (PST-Datei), die der Benutzer bearbeiten können, für das Dialogfeld Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0b1b9-105">Provides the personal storage table (.pst file) name, which the user can edit, for the configuration dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0b1b9-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0b1b9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0b1b9-107">PR_PST_PATH_HINT, PR_PST_PATH_HINT_A, PR_PST_PATH_HINT_W</span><span class="sxs-lookup"><span data-stu-id="0b1b9-107">PR_PST_PATH_HINT, PR_PST_PATH_HINT_A, PR_PST_PATH_HINT_W</span></span>  <br/> |
|<span data-ttu-id="0b1b9-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="0b1b9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0b1b9-109">0x6771</span><span class="sxs-lookup"><span data-stu-id="0b1b9-109">0x6771</span></span>  <br/> |
|<span data-ttu-id="0b1b9-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0b1b9-110">Data type:</span></span>  <br/> |<span data-ttu-id="0b1b9-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0b1b9-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0b1b9-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0b1b9-112">Area:</span></span>  <br/> |<span data-ttu-id="0b1b9-113">Persönlicher Speicher-Tabelle (. pst) interne</span><span class="sxs-lookup"><span data-stu-id="0b1b9-113">Personal storage table (.pst) internal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b1b9-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="0b1b9-114">Remarks</span></span>

<span data-ttu-id="0b1b9-115">Wenn Sie stattdessen die **PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md))-Eigenschaft verwendet wird, im Dialogfeld Konfiguration wird geöffnet, aber der Benutzer kann nicht den Pfad und viele andere Eigenschaften bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="0b1b9-115">If the **PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)) property is used instead, the configuration dialog box will open, but the user will not be allowed to edit the path and many other properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0b1b9-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0b1b9-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0b1b9-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0b1b9-117">Protocol specifications</span></span>

<span data-ttu-id="0b1b9-118">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="0b1b9-118">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="0b1b9-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="0b1b9-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0b1b9-120">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="0b1b9-120">Header files</span></span>

<span data-ttu-id="0b1b9-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0b1b9-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="0b1b9-122">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="0b1b9-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="0b1b9-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0b1b9-123">Mapitags.h</span></span>
  
> <span data-ttu-id="0b1b9-124">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="0b1b9-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0b1b9-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b1b9-125">See also</span></span>



[<span data-ttu-id="0b1b9-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0b1b9-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0b1b9-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0b1b9-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0b1b9-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0b1b9-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0b1b9-129">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0b1b9-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

