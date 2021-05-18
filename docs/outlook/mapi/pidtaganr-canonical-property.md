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
ms.openlocfilehash: ce08ba971662b7f5060e6b24a6d2c5ee1a921d5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327965"
---
# <a name="pidtaganr-canonical-property"></a><span data-ttu-id="bbbb9-103">PidTagAnr (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bbbb9-103">PidTagAnr Canonical Property</span></span>

  
  
<span data-ttu-id="bbbb9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bbbb9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bbbb9-105">Enthält einen Zeichenfolgenwert für die Verwendung in einer Eigenschaftseinschränkung für eine Adressbuchcontainerinhaltstabelle.</span><span class="sxs-lookup"><span data-stu-id="bbbb9-105">Contains a string value for use in a property restriction on an address book container contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bbbb9-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bbbb9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bbbb9-107">PR_ANR, PR_ANR_A, PR_ANR_W</span><span class="sxs-lookup"><span data-stu-id="bbbb9-107">PR_ANR, PR_ANR_A, PR_ANR_W</span></span>  <br/> |
|<span data-ttu-id="bbbb9-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="bbbb9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bbbb9-109">0x360C</span><span class="sxs-lookup"><span data-stu-id="bbbb9-109">0x360C</span></span>  <br/> |
|<span data-ttu-id="bbbb9-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bbbb9-110">Data type:</span></span>  <br/> |<span data-ttu-id="bbbb9-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="bbbb9-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="bbbb9-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bbbb9-112">Area:</span></span>  <br/> |<span data-ttu-id="bbbb9-113">Adressbuch</span><span class="sxs-lookup"><span data-stu-id="bbbb9-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bbbb9-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bbbb9-114">Remarks</span></span>

<span data-ttu-id="bbbb9-115">Diese Eigenschaften gehören zu keinem Objekt. Es wird von Adressbuchanbietern in [SPropertyRestriction-Strukturen](spropertyrestriction.md) eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="bbbb9-115">These properties do not belong to any object; it is furnished by address book providers in [SPropertyRestriction](spropertyrestriction.md) structures.</span></span> <span data-ttu-id="bbbb9-116">Diese Eigenschaft enthält eine zeichenfolge mit mehrdeutiger Namensauflösung (ANR), die mit der Inhaltstabelle eines Adressbuchcontainers getestet werden kann, um nach entsprechenden Nachrichtenempfängern zu suchen.</span><span class="sxs-lookup"><span data-stu-id="bbbb9-116">This property contains an ambiguous name resolution (ANR) string that can be tested against an address book container's contents table to find corresponding message recipients.</span></span> 
  
<span data-ttu-id="bbbb9-117">Adressbuchanbieter entsprechen dem Wert der **PR_ANR** und zugeordneten Eigenschaften mit jedem Eintrag in der Inhaltstabelle, indem sie einen vom Anbieter definierten Abgleichsalgorithmus verwenden.</span><span class="sxs-lookup"><span data-stu-id="bbbb9-117">Address book providers match the value of **PR_ANR** and associated properties against every entry in the contents table, using a provider-defined matching algorithm.</span></span> <span data-ttu-id="bbbb9-118">Die spalte oder spalten, die in dieser Übereinstimmung verwendet werden, werden vom Anbieter als Teil des Algorithmus ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="bbbb9-118">The column or columns that are used in this match are chosen by the provider as part of the algorithm.</span></span> <span data-ttu-id="bbbb9-119">Die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) ist die am häufigsten verwendete Spalte. Die **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) ist auch hilfreich, wenn sie den E-Mail-Namen des Benutzers enthält.</span><span class="sxs-lookup"><span data-stu-id="bbbb9-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) column is the most commonly used; the **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) column is also useful when it contains the user's email name.</span></span> 
  
<span data-ttu-id="bbbb9-120">Weitere Informationen zur mehrdeutigen Namensauflösung finden Sie unter [Adressbucheinschränkungen](address-book-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="bbbb9-120">For more information on ambiguous name resolution, see [Address Book Restrictions](address-book-restrictions.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bbbb9-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bbbb9-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bbbb9-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="bbbb9-122">Protocol specifications</span></span>

<span data-ttu-id="bbbb9-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bbbb9-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bbbb9-124">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="bbbb9-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bbbb9-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bbbb9-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bbbb9-126">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="bbbb9-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bbbb9-127">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="bbbb9-127">Header files</span></span>

<span data-ttu-id="bbbb9-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bbbb9-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="bbbb9-129">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="bbbb9-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="bbbb9-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bbbb9-130">Mapitags.h</span></span>
  
> <span data-ttu-id="bbbb9-131">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="bbbb9-131">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bbbb9-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bbbb9-132">See also</span></span>



[<span data-ttu-id="bbbb9-133">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="bbbb9-133">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
[<span data-ttu-id="bbbb9-134">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="bbbb9-134">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)


[<span data-ttu-id="bbbb9-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bbbb9-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bbbb9-136">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="bbbb9-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bbbb9-137">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bbbb9-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bbbb9-138">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bbbb9-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

