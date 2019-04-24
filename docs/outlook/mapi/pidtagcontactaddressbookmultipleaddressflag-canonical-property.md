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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6fabb03d552f195c200b0ecbd8fd69f470c0e1fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344891"
---
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a><span data-ttu-id="e4c88-103">Kanonische Pidtagcontactaddressbookmultipleaddressflag (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e4c88-103">PidTagContactAddressBookMultipleAddressFlag Canonical Property</span></span>

  
  
<span data-ttu-id="e4c88-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4c88-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4c88-105">Enthält ein Flag, das TRUE ist, wenn der Anbieter mehrere e-Mail-Adressen pro Kontaktelement unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e4c88-105">Contains a flag that is TRUE when the provider supports multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e4c88-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e4c88-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e4c88-107">PR_CONTAB_MULTI_ADDR_FLAG</span><span class="sxs-lookup"><span data-stu-id="e4c88-107">PR_CONTAB_MULTI_ADDR_FLAG</span></span>  <br/> |
|<span data-ttu-id="e4c88-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e4c88-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e4c88-109">0x6614</span><span class="sxs-lookup"><span data-stu-id="e4c88-109">0x6614</span></span>  <br/> |
|<span data-ttu-id="e4c88-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e4c88-110">Data type:</span></span>  <br/> |<span data-ttu-id="e4c88-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e4c88-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="e4c88-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e4c88-112">Area:</span></span>  <br/> |<span data-ttu-id="e4c88-113">Kontakt Adressbuch</span><span class="sxs-lookup"><span data-stu-id="e4c88-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e4c88-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4c88-114">Remarks</span></span>

<span data-ttu-id="e4c88-115">Wenn diese Eigenschaft auf TRUE festgelegt ist, lässt der Anbieter keine Kontakte ohne e-Mail-Adressen zu.</span><span class="sxs-lookup"><span data-stu-id="e4c88-115">If this property is TRUE, the provider does not allow contacts without email addresses.</span></span> <span data-ttu-id="e4c88-116">Wenn FALSE, zeigt der Anbieter alle Kontakte an, ob er eine primäre e-Mail-Adresse hat oder nicht.</span><span class="sxs-lookup"><span data-stu-id="e4c88-116">If FALSE, the provider shows all contacts whether or not they have a primary email address.</span></span> <span data-ttu-id="e4c88-117">Es wird nur die primäre e-Mail-Adresse geehrt.</span><span class="sxs-lookup"><span data-stu-id="e4c88-117">Only the primary email address will be honored.</span></span> <span data-ttu-id="e4c88-118">Hierbei handelt es sich um eine Eigenschaft in einem Adressbuchcontainer des Kontakts und eine Spalte in der Tabelle mit Adressbuch Containern des Kontakts.</span><span class="sxs-lookup"><span data-stu-id="e4c88-118">This is a property on a Contact Address Book container, and a column in the table of Contact Address Book containers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e4c88-119">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e4c88-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e4c88-120">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="e4c88-120">Header files</span></span>

<span data-ttu-id="e4c88-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e4c88-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="e4c88-122">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="e4c88-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="e4c88-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="e4c88-123">Mapitags.h</span></span>
  
> <span data-ttu-id="e4c88-124">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="e4c88-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e4c88-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4c88-125">See also</span></span>



[<span data-ttu-id="e4c88-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e4c88-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e4c88-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e4c88-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e4c88-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e4c88-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e4c88-129">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e4c88-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

