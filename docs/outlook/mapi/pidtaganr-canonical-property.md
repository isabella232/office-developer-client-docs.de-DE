---
title: PidTagAnr (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAnr
api_type:
- HeaderDef
ms.assetid: eca3d4ff-2e92-4d20-a498-98e0773c1962
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 94e83f4a93bac4ee144c5fbf94fd4b3fdb6c2f55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794072"
---
# <a name="pidtaganr-canonical-property"></a><span data-ttu-id="7c542-103">PidTagAnr (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7c542-103">PidTagAnr Canonical Property</span></span>

  
  
<span data-ttu-id="7c542-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7c542-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7c542-105">Einen String-Wert für die Verwendung in einer eigenschaftseinschränkung auf eine Adresse Adressbuch Container Inhaltstabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="7c542-105">Contains a string value for use in a property restriction on an address book container contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7c542-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7c542-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7c542-107">PR_ANR, PR_ANR_A, PR_ANR_W</span><span class="sxs-lookup"><span data-stu-id="7c542-107">PR_ANR, PR_ANR_A, PR_ANR_W</span></span>  <br/> |
|<span data-ttu-id="7c542-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="7c542-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7c542-109">0x360C</span><span class="sxs-lookup"><span data-stu-id="7c542-109">0x360C</span></span>  <br/> |
|<span data-ttu-id="7c542-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7c542-110">Data type:</span></span>  <br/> |<span data-ttu-id="7c542-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="7c542-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="7c542-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7c542-112">Area:</span></span>  <br/> |<span data-ttu-id="7c542-113">Adressbuch</span><span class="sxs-lookup"><span data-stu-id="7c542-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7c542-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c542-114">Remarks</span></span>

<span data-ttu-id="7c542-115">Diese Eigenschaften gehören nicht auf ein beliebiges Objekt; Es wird von adressbuchanbietern implementierte in [SPropertyRestriction](spropertyrestriction.md) Strukturen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="7c542-115">These properties do not belong to any object; it is furnished by address book providers in [SPropertyRestriction](spropertyrestriction.md) structures.</span></span> <span data-ttu-id="7c542-116">Diese Eigenschaft enthält eine Zeichenfolge der mehrdeutiger Name-Lösung (ANR), die ein Adressbuchcontainer Inhaltstabelle, entsprechende Empfänger der Nachricht erhalten verglichen werden kann.</span><span class="sxs-lookup"><span data-stu-id="7c542-116">This property contains an ambiguous name resolution (ANR) string that can be tested against an address book container's contents table to find corresponding message recipients.</span></span> 
  
<span data-ttu-id="7c542-117">Von adressbuchanbietern implementierte gleich dem Wert der **PR_ANR** und zugeordneten Eigenschaften für jeden Eintrag in der Inhaltstabelle mit einer vom Anbieter definiertes übereinstimmenden Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="7c542-117">Address book providers match the value of **PR_ANR** and associated properties against every entry in the contents table, using a provider-defined matching algorithm.</span></span> <span data-ttu-id="7c542-118">Die Spalte oder Spalten, die in diese Übereinstimmung verwendet werden, werden vom Anbieter als Teil des Algorithmus ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="7c542-118">The column or columns that are used in this match are chosen by the provider as part of the algorithm.</span></span> <span data-ttu-id="7c542-119">Die Spalte **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) ist die am häufigsten verwendet. die Spalte **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) ist auch nützlich, wenn sie den Namen des Benutzers e-Mail enthält.</span><span class="sxs-lookup"><span data-stu-id="7c542-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) column is the most commonly used; the **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) column is also useful when it contains the user's email name.</span></span> 
  
<span data-ttu-id="7c542-120">Weitere Informationen über die Auflösung nicht eindeutiger Namen finden Sie unter [Address Book Einschränkungen](address-book-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="7c542-120">For more information on ambiguous name resolution, see [Address Book Restrictions](address-book-restrictions.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7c542-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7c542-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7c542-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="7c542-122">Protocol specifications</span></span>

<span data-ttu-id="7c542-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7c542-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7c542-124">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="7c542-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7c542-125">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7c542-125">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7c542-126">Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="7c542-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7c542-127">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="7c542-127">Header files</span></span>

<span data-ttu-id="7c542-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7c542-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="7c542-129">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="7c542-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="7c542-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7c542-130">Mapitags.h</span></span>
  
> <span data-ttu-id="7c542-131">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="7c542-131">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7c542-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c542-132">See also</span></span>



[<span data-ttu-id="7c542-133">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="7c542-133">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
[<span data-ttu-id="7c542-134">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="7c542-134">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)


[<span data-ttu-id="7c542-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7c542-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7c542-136">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7c542-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7c542-137">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7c542-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7c542-138">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7c542-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

