---
title: PidTagTemplateid (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTemplateid
api_type:
- COM
ms.assetid: 1a418c76-ebc7-47f2-ac91-797162e6e099
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 96bcd15606771bd112568ad94133507ab14b2bcd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396393"
---
# <a name="pidtagtemplateid-canonical-property"></a><span data-ttu-id="71640-103">PidTagTemplateid (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="71640-103">PidTagTemplateid Canonical Property</span></span>

  
  
<span data-ttu-id="71640-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71640-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71640-105">Enthält die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), ausgedrückt als Format permanente Eintrags-ID an.</span><span class="sxs-lookup"><span data-stu-id="71640-105">Contains the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), expressed as a permanent entry ID format.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="71640-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="71640-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="71640-107">PR_TEMPLATEID</span><span class="sxs-lookup"><span data-stu-id="71640-107">PR_TEMPLATEID</span></span>  <br/> |
|<span data-ttu-id="71640-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="71640-108">Identifier:</span></span>  <br/> |<span data-ttu-id="71640-109">0x3902</span><span class="sxs-lookup"><span data-stu-id="71640-109">0x3902</span></span>  <br/> |
|<span data-ttu-id="71640-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="71640-110">Data type:</span></span>  <br/> |<span data-ttu-id="71640-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="71640-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="71640-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="71640-112">Area:</span></span>  <br/> |<span data-ttu-id="71640-113">MAPI-Adressbuch</span><span class="sxs-lookup"><span data-stu-id="71640-113">MAPI Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="71640-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="71640-114">Remarks</span></span>

<span data-ttu-id="71640-115">Dieser Wert muss für alle Address Book-Objekte auf einem Server (NSPI = Name Service Provider Interface) vorhanden sein, den distinguished Name (DN) gleich dem Wert für **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) und der DN muss das DN-Format folgen die Spezifikation für den Typ des Objekts.</span><span class="sxs-lookup"><span data-stu-id="71640-115">This value must be present for all address book objects on an Name Service Provider Interface (NSPI) server, its distinguished name (DN) must match the value for **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), and its DN must follow the DN format specification particular to the type of object.</span></span> 
  
<span data-ttu-id="71640-116">Diese Eigenschaft ist nicht für Objekte, die in einem offline-Adressbuch vorhanden.</span><span class="sxs-lookup"><span data-stu-id="71640-116">This property is not present on objects in an offline address book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="71640-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="71640-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="71640-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="71640-118">Protocol specifications</span></span>

<span data-ttu-id="71640-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="71640-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="71640-120">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="71640-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="71640-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="71640-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="71640-122">Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="71640-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="71640-123">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="71640-123">Header files</span></span>

<span data-ttu-id="71640-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="71640-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="71640-125">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="71640-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="71640-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="71640-126">Mapitags.h</span></span>
  
> <span data-ttu-id="71640-127">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="71640-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="71640-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71640-128">See also</span></span>



[<span data-ttu-id="71640-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="71640-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="71640-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="71640-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="71640-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="71640-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="71640-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="71640-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

