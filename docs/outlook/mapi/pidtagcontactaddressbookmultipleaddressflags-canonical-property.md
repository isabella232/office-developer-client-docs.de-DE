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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fbe955d3e7a509edf6ba10678e1e2538c9185193
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794185"
---
# <a name="pidtagcontactaddressbookmultipleaddressflags-canonical-property"></a><span data-ttu-id="26112-103">PidTagContactAddressBookMultipleAddressFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="26112-103">PidTagContactAddressBookMultipleAddressFlags Canonical Property</span></span>

  
  
<span data-ttu-id="26112-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="26112-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="26112-105">Flags, die pro Kontaktelement zurück, der angibt, ob der Anbieter mehrere e-Mail unterstützt-Adressen enthält.</span><span class="sxs-lookup"><span data-stu-id="26112-105">Contains flags that indicating whether the providers will support multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="26112-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="26112-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="26112-107">PR_CONTAB_MULTI_ADDR_FLAGS</span><span class="sxs-lookup"><span data-stu-id="26112-107">PR_CONTAB_MULTI_ADDR_FLAGS</span></span>  <br/> |
|<span data-ttu-id="26112-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="26112-108">Identifier:</span></span>  <br/> |<span data-ttu-id="26112-109">0x6625</span><span class="sxs-lookup"><span data-stu-id="26112-109">0x6625</span></span>  <br/> |
|<span data-ttu-id="26112-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="26112-110">Data type:</span></span>  <br/> |<span data-ttu-id="26112-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="26112-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="26112-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="26112-112">Area:</span></span>  <br/> |<span data-ttu-id="26112-113">Kontakt-Adressbuch</span><span class="sxs-lookup"><span data-stu-id="26112-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="26112-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26112-114">Remarks</span></span>

<span data-ttu-id="26112-115">Wenn die Kennzeichen in dieser Eigenschaft TRUE sind, ist der Anbieter nicht Kontakte ohne e-Mail-Adressen enthalten.</span><span class="sxs-lookup"><span data-stu-id="26112-115">If the flags in this property are TRUE, the provider does not include contacts without email addresses.</span></span> <span data-ttu-id="26112-116">Nur die primäre e-Mail-Adresse wird berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="26112-116">Only the primary email address will be honored.</span></span> <span data-ttu-id="26112-117">Dies ist eine Eigenschaft für einen Kontakt Adressbuch Profil.</span><span class="sxs-lookup"><span data-stu-id="26112-117">This is a property on a Contact Address Book profile section.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="26112-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="26112-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="26112-119">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="26112-119">Header files</span></span>

<span data-ttu-id="26112-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="26112-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="26112-121">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="26112-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="26112-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="26112-122">Mapitags.h</span></span>
  
> <span data-ttu-id="26112-123">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="26112-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="26112-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26112-124">See also</span></span>



[<span data-ttu-id="26112-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="26112-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="26112-126">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="26112-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="26112-127">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="26112-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="26112-128">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="26112-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

