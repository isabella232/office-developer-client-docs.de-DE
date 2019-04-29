---
title: Kanonische Pidtagcontactaddressbookmultipleaddressflag (-Eigenschaft
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
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a><span data-ttu-id="bcb6c-103">Kanonische Pidtagcontactaddressbookmultipleaddressflag (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bcb6c-103">PidTagContactAddressBookMultipleAddressFlag Canonical Property</span></span>

  
  
<span data-ttu-id="bcb6c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bcb6c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bcb6c-105">Enthält ein Flag, das TRUE ist, wenn der Anbieter mehrere e-Mail-Adressen pro Kontaktelement unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bcb6c-105">Contains a flag that is TRUE when the provider supports multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bcb6c-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bcb6c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bcb6c-107">PR_CONTAB_MULTI_ADDR_FLAG</span><span class="sxs-lookup"><span data-stu-id="bcb6c-107">PR_CONTAB_MULTI_ADDR_FLAG</span></span>  <br/> |
|<span data-ttu-id="bcb6c-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="bcb6c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bcb6c-109">0x6614</span><span class="sxs-lookup"><span data-stu-id="bcb6c-109">0x6614</span></span>  <br/> |
|<span data-ttu-id="bcb6c-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bcb6c-110">Data type:</span></span>  <br/> |<span data-ttu-id="bcb6c-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="bcb6c-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="bcb6c-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bcb6c-112">Area:</span></span>  <br/> |<span data-ttu-id="bcb6c-113">Kontakt Adressbuch</span><span class="sxs-lookup"><span data-stu-id="bcb6c-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bcb6c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bcb6c-114">Remarks</span></span>

<span data-ttu-id="bcb6c-115">Wenn diese Eigenschaft auf TRUE festgelegt ist, lässt der Anbieter keine Kontakte ohne e-Mail-Adressen zu.</span><span class="sxs-lookup"><span data-stu-id="bcb6c-115">If this property is TRUE, the provider does not allow contacts without email addresses.</span></span> <span data-ttu-id="bcb6c-116">Wenn FALSE, zeigt der Anbieter alle Kontakte an, ob er eine primäre e-Mail-Adresse hat oder nicht.</span><span class="sxs-lookup"><span data-stu-id="bcb6c-116">If FALSE, the provider shows all contacts whether or not they have a primary email address.</span></span> <span data-ttu-id="bcb6c-117">Es wird nur die primäre e-Mail-Adresse geehrt.</span><span class="sxs-lookup"><span data-stu-id="bcb6c-117">Only the primary email address will be honored.</span></span> <span data-ttu-id="bcb6c-118">Hierbei handelt es sich um eine Eigenschaft in einem Adressbuchcontainer des Kontakts und eine Spalte in der Tabelle mit Adressbuch Containern des Kontakts.</span><span class="sxs-lookup"><span data-stu-id="bcb6c-118">This is a property on a Contact Address Book container, and a column in the table of Contact Address Book containers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bcb6c-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bcb6c-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="bcb6c-120">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="bcb6c-120">Header files</span></span>

<span data-ttu-id="bcb6c-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="bcb6c-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="bcb6c-122">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="bcb6c-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="bcb6c-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="bcb6c-123">Mapitags.h</span></span>
  
> <span data-ttu-id="bcb6c-124">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="bcb6c-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bcb6c-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bcb6c-125">See also</span></span>



[<span data-ttu-id="bcb6c-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bcb6c-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bcb6c-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bcb6c-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bcb6c-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bcb6c-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bcb6c-129">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bcb6c-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

