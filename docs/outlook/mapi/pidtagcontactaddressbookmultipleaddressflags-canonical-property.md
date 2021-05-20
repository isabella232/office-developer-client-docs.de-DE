---
title: PidTagContactAddressBookMultipleAddressFlags (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookMultipleAddressFlags
api_type:
- HeaderDef
ms.assetid: ed3bc585-13f6-46a5-9e71-9c8513ddfc0a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ecd795490d953f1aa237dfbd77585ba79c8b3234
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429250"
---
# <a name="pidtagcontactaddressbookmultipleaddressflags-canonical-property"></a><span data-ttu-id="bf4a6-103">PidTagContactAddressBookMultipleAddressFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bf4a6-103">PidTagContactAddressBookMultipleAddressFlags Canonical Property</span></span>

  
  
<span data-ttu-id="bf4a6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf4a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf4a6-105">Enthält Kennzeichen, die angeben, ob die Anbieter mehrere E-Mail-Adressen pro Kontaktelement unterstützen.</span><span class="sxs-lookup"><span data-stu-id="bf4a6-105">Contains flags that indicating whether the providers will support multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bf4a6-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bf4a6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bf4a6-107">PR_CONTAB_MULTI_ADDR_FLAGS</span><span class="sxs-lookup"><span data-stu-id="bf4a6-107">PR_CONTAB_MULTI_ADDR_FLAGS</span></span>  <br/> |
|<span data-ttu-id="bf4a6-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="bf4a6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bf4a6-109">0x6625</span><span class="sxs-lookup"><span data-stu-id="bf4a6-109">0x6625</span></span>  <br/> |
|<span data-ttu-id="bf4a6-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bf4a6-110">Data type:</span></span>  <br/> |<span data-ttu-id="bf4a6-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="bf4a6-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="bf4a6-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bf4a6-112">Area:</span></span>  <br/> |<span data-ttu-id="bf4a6-113">Kontaktadressenbuch</span><span class="sxs-lookup"><span data-stu-id="bf4a6-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf4a6-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bf4a6-114">Remarks</span></span>

<span data-ttu-id="bf4a6-115">Wenn die Kennzeichen in dieser Eigenschaft TRUE sind, schließt der Anbieter keine Kontakte ohne E-Mail-Adressen ein.</span><span class="sxs-lookup"><span data-stu-id="bf4a6-115">If the flags in this property are TRUE, the provider does not include contacts without email addresses.</span></span> <span data-ttu-id="bf4a6-116">Nur die primäre E-Mail-Adresse wird berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="bf4a6-116">Only the primary email address will be honored.</span></span> <span data-ttu-id="bf4a6-117">Dies ist eine Eigenschaft in einem Abschnitt "Kontakt-Adressbuch".</span><span class="sxs-lookup"><span data-stu-id="bf4a6-117">This is a property on a Contact Address Book profile section.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bf4a6-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bf4a6-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="bf4a6-119">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="bf4a6-119">Header files</span></span>

<span data-ttu-id="bf4a6-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bf4a6-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="bf4a6-121">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="bf4a6-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="bf4a6-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bf4a6-122">Mapitags.h</span></span>
  
> <span data-ttu-id="bf4a6-123">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="bf4a6-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bf4a6-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf4a6-124">See also</span></span>



[<span data-ttu-id="bf4a6-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bf4a6-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bf4a6-126">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="bf4a6-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bf4a6-127">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bf4a6-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bf4a6-128">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bf4a6-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

