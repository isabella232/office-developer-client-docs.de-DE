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
ms.openlocfilehash: b783a624ef5358a69d65dd52785b285db1a70df7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588671"
---
# <a name="pidtagcontactaddressbookmultipleaddressflags-canonical-property"></a><span data-ttu-id="37de0-103">PidTagContactAddressBookMultipleAddressFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="37de0-103">PidTagContactAddressBookMultipleAddressFlags Canonical Property</span></span>

  
  
<span data-ttu-id="37de0-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37de0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37de0-105">Flags, die pro Kontaktelement zurück, der angibt, ob der Anbieter mehrere e-Mail unterstützt-Adressen enthält.</span><span class="sxs-lookup"><span data-stu-id="37de0-105">Contains flags that indicating whether the providers will support multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="37de0-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="37de0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="37de0-107">PR_CONTAB_MULTI_ADDR_FLAGS</span><span class="sxs-lookup"><span data-stu-id="37de0-107">PR_CONTAB_MULTI_ADDR_FLAGS</span></span>  <br/> |
|<span data-ttu-id="37de0-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="37de0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="37de0-109">0x6625</span><span class="sxs-lookup"><span data-stu-id="37de0-109">0x6625</span></span>  <br/> |
|<span data-ttu-id="37de0-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="37de0-110">Data type:</span></span>  <br/> |<span data-ttu-id="37de0-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="37de0-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="37de0-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="37de0-112">Area:</span></span>  <br/> |<span data-ttu-id="37de0-113">Kontakt-Adressbuch</span><span class="sxs-lookup"><span data-stu-id="37de0-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37de0-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="37de0-114">Remarks</span></span>

<span data-ttu-id="37de0-115">Wenn die Kennzeichen in dieser Eigenschaft TRUE sind, ist der Anbieter nicht Kontakte ohne e-Mail-Adressen enthalten.</span><span class="sxs-lookup"><span data-stu-id="37de0-115">If the flags in this property are TRUE, the provider does not include contacts without email addresses.</span></span> <span data-ttu-id="37de0-116">Nur die primäre e-Mail-Adresse wird berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="37de0-116">Only the primary email address will be honored.</span></span> <span data-ttu-id="37de0-117">Dies ist eine Eigenschaft für einen Kontakt Adressbuch Profil.</span><span class="sxs-lookup"><span data-stu-id="37de0-117">This is a property on a Contact Address Book profile section.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="37de0-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="37de0-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="37de0-119">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="37de0-119">Header files</span></span>

<span data-ttu-id="37de0-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="37de0-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="37de0-121">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="37de0-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="37de0-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="37de0-122">Mapitags.h</span></span>
  
> <span data-ttu-id="37de0-123">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="37de0-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="37de0-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37de0-124">See also</span></span>



[<span data-ttu-id="37de0-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="37de0-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="37de0-126">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="37de0-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="37de0-127">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="37de0-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="37de0-128">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="37de0-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

