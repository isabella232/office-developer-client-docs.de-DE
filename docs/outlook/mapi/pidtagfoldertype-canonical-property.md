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
ms.openlocfilehash: 8d6167a7a3c983171f2ff9cb2a54c879a14dca0e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591415"
---
# <a name="pidtagfoldertype-canonical-property"></a><span data-ttu-id="7b77e-103">PidTagFolderType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7b77e-103">PidTagFolderType Canonical Property</span></span>

  
  
<span data-ttu-id="7b77e-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b77e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b77e-105">Enthält eine Konstante, die den Ordner angibt.</span><span class="sxs-lookup"><span data-stu-id="7b77e-105">Contains a constant that indicates the folder type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7b77e-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7b77e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7b77e-107">PR_FOLDER_TYPE</span><span class="sxs-lookup"><span data-stu-id="7b77e-107">PR_FOLDER_TYPE</span></span>  <br/> |
|<span data-ttu-id="7b77e-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="7b77e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7b77e-109">0x3601</span><span class="sxs-lookup"><span data-stu-id="7b77e-109">0x3601</span></span>  <br/> |
|<span data-ttu-id="7b77e-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7b77e-110">Data type:</span></span>  <br/> |<span data-ttu-id="7b77e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7b77e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7b77e-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7b77e-112">Area:</span></span>  <br/> |<span data-ttu-id="7b77e-113">MAPI-container</span><span class="sxs-lookup"><span data-stu-id="7b77e-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b77e-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="7b77e-114">Remarks</span></span>

<span data-ttu-id="7b77e-115">Diese Eigenschaft kann genau einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="7b77e-115">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="7b77e-116">FOLDER_GENERIC</span><span class="sxs-lookup"><span data-stu-id="7b77e-116">FOLDER_GENERIC</span></span> 
  
> <span data-ttu-id="7b77e-117">Eine generische Ordner, der Nachrichten und andere Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="7b77e-117">A generic folder that contains messages and other folders.</span></span>
    
<span data-ttu-id="7b77e-118">FOLDER_ROOT</span><span class="sxs-lookup"><span data-stu-id="7b77e-118">FOLDER_ROOT</span></span> 
  
> <span data-ttu-id="7b77e-119">Der Stammordner der Ordner Hierarchietabelle, d. h., einen Ordner, die über keinen übergeordneten Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="7b77e-119">The root folder of the folder hierarchy table, that is, a folder that has no parent folder.</span></span>
    
<span data-ttu-id="7b77e-120">FOLDER_SEARCH</span><span class="sxs-lookup"><span data-stu-id="7b77e-120">FOLDER_SEARCH</span></span> 
  
> <span data-ttu-id="7b77e-121">Dieser Ordner enthält die Ergebnisse einer Suche, in Form von Links zu Nachrichten, die Suchkriterien erfüllen.</span><span class="sxs-lookup"><span data-stu-id="7b77e-121">A folder that contains the results of a search, in the form of links to messages that meet search criteria.</span></span>
    
<span data-ttu-id="7b77e-122">Im Stammverzeichnis des eines Nachrichtenspeichers darf nicht mit dem Stamm der Teilstruktur zwischen Personen Nachricht (IPM) in diesem Speicher verwechselt werden.</span><span class="sxs-lookup"><span data-stu-id="7b77e-122">The root of a message store should not be confused with the root of the interpersonal message (IPM) subtree in that store.</span></span> <span data-ttu-id="7b77e-123">Das Store-Stammordner, ohne übergeordnetes Objekt ist, wird durch Aufrufen der [IMsgStore::OpenEntry](imsgstore-openentry.md) -Methode mit einem null-Eintrags-ID abgerufen.</span><span class="sxs-lookup"><span data-stu-id="7b77e-123">The store's root folder, which has no parent, is obtained by calling the [IMsgStore::OpenEntry](imsgstore-openentry.md) method with a null entry identifier.</span></span> <span data-ttu-id="7b77e-124">Stammordner der IPM-Unterstruktur, die ein übergeordnetes Element vorhanden ist, wird mit dem Wert der Eigenschaft **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) für den Anruf **OpenEntry** abgerufen.</span><span class="sxs-lookup"><span data-stu-id="7b77e-124">The IPM subtree's root folder, which does have a parent, is obtained by using the value of the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property for the **OpenEntry** call.</span></span> 
  
<span data-ttu-id="7b77e-125">MAPI kann nur eine Stammordner pro Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="7b77e-125">MAPI allows only one root folder per message store.</span></span> <span data-ttu-id="7b77e-126">Dieser Ordner enthält Nachrichten und andere Ordner.</span><span class="sxs-lookup"><span data-stu-id="7b77e-126">This folder contains messages and other folders.</span></span> <span data-ttu-id="7b77e-127">Im Stammordner **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))-Eigenschaft enthält die Eintrags-ID des Ordners.</span><span class="sxs-lookup"><span data-stu-id="7b77e-127">The root folder's **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) property contains the folder's own entry identifier.</span></span>
  
<span data-ttu-id="7b77e-128">Die Informationen in einem Suchergebnisse Ordner in seiner Inhaltstabelle, die enthält dieselben Spalten als Tabelle normalerweise sowie zwei zusätzliche Spalten Ermitteln des Ordners, in dem jede Nachricht wurde gefunden, in erster Linie gespeichert ist: **PR_PARENT_DISPLAY** ([ PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (Anzeigename, erforderlich), und diese Eigenschaft (Eintrags-ID, optional).</span><span class="sxs-lookup"><span data-stu-id="7b77e-128">The information in a search-results folder is mainly stored in its contents table, which contains the same columns as a typical contents table, as well as two extra columns identifying the folder in which each message was found: **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (display name, required) and this property (entry identifier, optional).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7b77e-129">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7b77e-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7b77e-130">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="7b77e-130">Protocol specifications</span></span>

<span data-ttu-id="7b77e-131">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b77e-131">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b77e-132">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="7b77e-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7b77e-133">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b77e-133">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b77e-134">Ordner Vorgänge behandelt.</span><span class="sxs-lookup"><span data-stu-id="7b77e-134">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7b77e-135">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="7b77e-135">Header files</span></span>

<span data-ttu-id="7b77e-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7b77e-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="7b77e-137">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="7b77e-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="7b77e-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7b77e-138">Mapitags.h</span></span>
  
> <span data-ttu-id="7b77e-139">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="7b77e-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7b77e-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b77e-140">See also</span></span>



[<span data-ttu-id="7b77e-141">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7b77e-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7b77e-142">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7b77e-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7b77e-143">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7b77e-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7b77e-144">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7b77e-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

