---
title: Kanonische PidTagContactAddressBookMultipleAddressFlag-Eigenschaft
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
ms.openlocfilehash: 42f164f09dbffcc05986771aa05f7ce14eee789c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794196"
---
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a><span data-ttu-id="336a5-103">Kanonische PidTagContactAddressBookMultipleAddressFlag-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="336a5-103">PidTagContactAddressBookMultipleAddressFlag Canonical Property</span></span>

  
  
<span data-ttu-id="336a5-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="336a5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="336a5-105">Enthält ein Flag, das auf true festgelegt ist, wenn der Anbieter pro Kontaktelement mehrere e-Mail-Adressen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="336a5-105">Contains a flag that is TRUE when the provider supports multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="336a5-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="336a5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="336a5-107">PR_CONTAB_MULTI_ADDR_FLAG</span><span class="sxs-lookup"><span data-stu-id="336a5-107">PR_CONTAB_MULTI_ADDR_FLAG</span></span>  <br/> |
|<span data-ttu-id="336a5-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="336a5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="336a5-109">0x6614</span><span class="sxs-lookup"><span data-stu-id="336a5-109">0x6614</span></span>  <br/> |
|<span data-ttu-id="336a5-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="336a5-110">Data type:</span></span>  <br/> |<span data-ttu-id="336a5-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="336a5-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="336a5-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="336a5-112">Area:</span></span>  <br/> |<span data-ttu-id="336a5-113">Kontakt-Adressbuch</span><span class="sxs-lookup"><span data-stu-id="336a5-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="336a5-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="336a5-114">Remarks</span></span>

<span data-ttu-id="336a5-115">Wenn diese Eigenschaft auf true festgelegt ist, ist der Anbieter Kontakte ohne e-Mail-Adressen nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="336a5-115">If this property is TRUE, the provider does not allow contacts without email addresses.</span></span> <span data-ttu-id="336a5-116">Ist der Wert FALSE ist, zeigt der Anbieter alle Kontakte unabhängig davon, ob sie eine primäre e-Mail-Adresse besitzen.</span><span class="sxs-lookup"><span data-stu-id="336a5-116">If FALSE, the provider shows all contacts whether or not they have a primary email address.</span></span> <span data-ttu-id="336a5-117">Nur die primäre e-Mail-Adresse wird berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="336a5-117">Only the primary email address will be honored.</span></span> <span data-ttu-id="336a5-118">Dies ist eine Eigenschaft für einen Kontakt Adressbuch-Container und eine Spalte in der Tabelle der Kontakt-Adressbuch-Container.</span><span class="sxs-lookup"><span data-stu-id="336a5-118">This is a property on a Contact Address Book container, and a column in the table of Contact Address Book containers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="336a5-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="336a5-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="336a5-120">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="336a5-120">Header files</span></span>

<span data-ttu-id="336a5-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="336a5-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="336a5-122">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="336a5-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="336a5-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="336a5-123">Mapitags.h</span></span>
  
> <span data-ttu-id="336a5-124">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="336a5-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="336a5-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="336a5-125">See also</span></span>



[<span data-ttu-id="336a5-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="336a5-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="336a5-127">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="336a5-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="336a5-128">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="336a5-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="336a5-129">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="336a5-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

