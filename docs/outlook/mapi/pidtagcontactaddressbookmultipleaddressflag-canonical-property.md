---
title: PidTagContactAddressBookMultipleAddressFlag (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookMultipleAddressFlag
api_type:
- HeaderDef
ms.assetid: aefc34c5-1beb-44cf-a455-90f466e157ce
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6fabb03d552f195c200b0ecbd8fd69f470c0e1fd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431568"
---
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a><span data-ttu-id="f5f9b-103">PidTagContactAddressBookMultipleAddressFlag (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f5f9b-103">PidTagContactAddressBookMultipleAddressFlag Canonical Property</span></span>

  
  
<span data-ttu-id="f5f9b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5f9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5f9b-105">Enthält ein Flag, das TRUE ist, wenn der Anbieter mehrere E-Mail-Adressen pro Kontaktelement unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f5f9b-105">Contains a flag that is TRUE when the provider supports multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f5f9b-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f5f9b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f5f9b-107">PR_CONTAB_MULTI_ADDR_FLAG</span><span class="sxs-lookup"><span data-stu-id="f5f9b-107">PR_CONTAB_MULTI_ADDR_FLAG</span></span>  <br/> |
|<span data-ttu-id="f5f9b-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="f5f9b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f5f9b-109">0x6614</span><span class="sxs-lookup"><span data-stu-id="f5f9b-109">0x6614</span></span>  <br/> |
|<span data-ttu-id="f5f9b-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f5f9b-110">Data type:</span></span>  <br/> |<span data-ttu-id="f5f9b-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f5f9b-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f5f9b-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f5f9b-112">Area:</span></span>  <br/> |<span data-ttu-id="f5f9b-113">Kontaktadressenbuch</span><span class="sxs-lookup"><span data-stu-id="f5f9b-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5f9b-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f5f9b-114">Remarks</span></span>

<span data-ttu-id="f5f9b-115">Wenn diese Eigenschaft TRUE ist, lässt der Anbieter keine Kontakte ohne E-Mail-Adressen zu.</span><span class="sxs-lookup"><span data-stu-id="f5f9b-115">If this property is TRUE, the provider does not allow contacts without email addresses.</span></span> <span data-ttu-id="f5f9b-116">Bei FALSE zeigt der Anbieter alle Kontakte an, unabhängig davon, ob sie über eine primäre E-Mail-Adresse verfügen.</span><span class="sxs-lookup"><span data-stu-id="f5f9b-116">If FALSE, the provider shows all contacts whether or not they have a primary email address.</span></span> <span data-ttu-id="f5f9b-117">Nur die primäre E-Mail-Adresse wird berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="f5f9b-117">Only the primary email address will be honored.</span></span> <span data-ttu-id="f5f9b-118">Dies ist eine Eigenschaft für einen Contact Address Book-Container und eine Spalte in der Tabelle der Kontaktadressenbuchcontainer.</span><span class="sxs-lookup"><span data-stu-id="f5f9b-118">This is a property on a Contact Address Book container, and a column in the table of Contact Address Book containers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f5f9b-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f5f9b-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f5f9b-120">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="f5f9b-120">Header files</span></span>

<span data-ttu-id="f5f9b-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f5f9b-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="f5f9b-122">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f5f9b-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="f5f9b-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f5f9b-123">Mapitags.h</span></span>
  
> <span data-ttu-id="f5f9b-124">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="f5f9b-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f5f9b-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5f9b-125">See also</span></span>



[<span data-ttu-id="f5f9b-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f5f9b-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f5f9b-127">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="f5f9b-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f5f9b-128">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f5f9b-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f5f9b-129">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f5f9b-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

