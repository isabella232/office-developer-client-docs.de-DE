---
title: PidTagFolderType (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderType
api_type:
- HeaderDef
ms.assetid: 2ab4681e-0013-4ba0-ba26-50517bbf3f5b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7cca884eae2111a94d87cc24a6d30542148ab845
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316317"
---
# <a name="pidtagfoldertype-canonical-property"></a><span data-ttu-id="28eb4-103">PidTagFolderType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="28eb4-103">PidTagFolderType Canonical Property</span></span>

  
  
<span data-ttu-id="28eb4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="28eb4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="28eb4-105">Enthält eine Konstante, die den Ordnertyp angibt.</span><span class="sxs-lookup"><span data-stu-id="28eb4-105">Contains a constant that indicates the folder type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="28eb4-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="28eb4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="28eb4-107">PR_FOLDER_TYPE</span><span class="sxs-lookup"><span data-stu-id="28eb4-107">PR_FOLDER_TYPE</span></span>  <br/> |
|<span data-ttu-id="28eb4-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="28eb4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="28eb4-109">0x3601</span><span class="sxs-lookup"><span data-stu-id="28eb4-109">0x3601</span></span>  <br/> |
|<span data-ttu-id="28eb4-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="28eb4-110">Data type:</span></span>  <br/> |<span data-ttu-id="28eb4-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="28eb4-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="28eb4-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="28eb4-112">Area:</span></span>  <br/> |<span data-ttu-id="28eb4-113">MAPI-Container</span><span class="sxs-lookup"><span data-stu-id="28eb4-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="28eb4-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="28eb4-114">Remarks</span></span>

<span data-ttu-id="28eb4-115">Diese Eigenschaft kann genau einen der folgenden Werte haben:</span><span class="sxs-lookup"><span data-stu-id="28eb4-115">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="28eb4-116">FOLDER_GENERIC</span><span class="sxs-lookup"><span data-stu-id="28eb4-116">FOLDER_GENERIC</span></span> 
  
> <span data-ttu-id="28eb4-117">Ein generischer Ordner, der Nachrichten und andere Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="28eb4-117">A generic folder that contains messages and other folders.</span></span>
    
<span data-ttu-id="28eb4-118">FOLDER_ROOT</span><span class="sxs-lookup"><span data-stu-id="28eb4-118">FOLDER_ROOT</span></span> 
  
> <span data-ttu-id="28eb4-119">Der Stammordner der Ordnerhierarchietabelle, d. h. ein Ordner ohne übergeordneten Ordner.</span><span class="sxs-lookup"><span data-stu-id="28eb4-119">The root folder of the folder hierarchy table, that is, a folder that has no parent folder.</span></span>
    
<span data-ttu-id="28eb4-120">FOLDER_SEARCH</span><span class="sxs-lookup"><span data-stu-id="28eb4-120">FOLDER_SEARCH</span></span> 
  
> <span data-ttu-id="28eb4-121">Ein Ordner, der die Ergebnisse einer Suche in Form von Links zu Nachrichten enthält, die Suchkriterien erfüllen.</span><span class="sxs-lookup"><span data-stu-id="28eb4-121">A folder that contains the results of a search, in the form of links to messages that meet search criteria.</span></span>
    
<span data-ttu-id="28eb4-122">Der Stamm eines Nachrichtenspeichers sollte nicht mit dem Stamm der Unterstruktur für zwischenpersonale Nachrichten (IPM) in diesem Speicher verwechselt werden.</span><span class="sxs-lookup"><span data-stu-id="28eb4-122">The root of a message store should not be confused with the root of the interpersonal message (IPM) subtree in that store.</span></span> <span data-ttu-id="28eb4-123">Der Stammordner des Speichers, der kein übergeordnetes Element besitzt, wird durch Aufrufen der [IMsgStore::OpenEntry-Methode](imsgstore-openentry.md) mit einem Nulleintragsbezeichner erhalten.</span><span class="sxs-lookup"><span data-stu-id="28eb4-123">The store's root folder, which has no parent, is obtained by calling the [IMsgStore::OpenEntry](imsgstore-openentry.md) method with a null entry identifier.</span></span> <span data-ttu-id="28eb4-124">Der Stammordner der #A0 mit einem übergeordneten Element wird mithilfe des Werts der **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))-Eigenschaft für den **OpenEntry-Aufruf** erhalten.</span><span class="sxs-lookup"><span data-stu-id="28eb4-124">The IPM subtree's root folder, which does have a parent, is obtained by using the value of the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property for the **OpenEntry** call.</span></span> 
  
<span data-ttu-id="28eb4-125">MAPI lässt pro Nachrichtenspeicher nur einen Stammordner zu.</span><span class="sxs-lookup"><span data-stu-id="28eb4-125">MAPI allows only one root folder per message store.</span></span> <span data-ttu-id="28eb4-126">Dieser Ordner enthält Nachrichten und andere Ordner.</span><span class="sxs-lookup"><span data-stu-id="28eb4-126">This folder contains messages and other folders.</span></span> <span data-ttu-id="28eb4-127">Die Eigenschaft PR_PARENT_ENTRYID **(** [PidTagParentEntryId](pidtagparententryid-canonical-property.md)) des Stammordners enthält den eigenen Eintragsbezeichner des Ordners.</span><span class="sxs-lookup"><span data-stu-id="28eb4-127">The root folder's **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) property contains the folder's own entry identifier.</span></span>
  
<span data-ttu-id="28eb4-128">Die Informationen in einem Suchergebnisordner werden hauptsächlich in der Inhaltstabelle gespeichert, die die gleichen Spalten wie eine typische Inhaltstabelle enthält, sowie zwei zusätzliche Spalten, die den Ordner identifizieren, in dem jede Nachricht gefunden wurde: **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (Anzeigename, erforderlich) und diese Eigenschaft (Eintrags-ID, optional).</span><span class="sxs-lookup"><span data-stu-id="28eb4-128">The information in a search-results folder is mainly stored in its contents table, which contains the same columns as a typical contents table, as well as two extra columns identifying the folder in which each message was found: **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (display name, required) and this property (entry identifier, optional).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="28eb4-129">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="28eb4-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="28eb4-130">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="28eb4-130">Protocol specifications</span></span>

<span data-ttu-id="28eb4-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="28eb4-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="28eb4-132">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="28eb4-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="28eb4-133">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="28eb4-133">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="28eb4-134">Verarbeitet Ordnervorgänge.</span><span class="sxs-lookup"><span data-stu-id="28eb4-134">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="28eb4-135">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="28eb4-135">Header files</span></span>

<span data-ttu-id="28eb4-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="28eb4-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="28eb4-137">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="28eb4-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="28eb4-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="28eb4-138">Mapitags.h</span></span>
  
> <span data-ttu-id="28eb4-139">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="28eb4-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="28eb4-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28eb4-140">See also</span></span>



[<span data-ttu-id="28eb4-141">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="28eb4-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="28eb4-142">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="28eb4-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="28eb4-143">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="28eb4-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="28eb4-144">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="28eb4-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

