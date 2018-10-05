---
title: PidTagMessageCodepage (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageCodepage
api_type:
- HeaderDef
ms.assetid: eef73e34-470c-4c37-94ce-ea95fe83bc10
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 49f2c1c0b8af21f837582698763c17b9c41e1923
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387230"
---
# <a name="pidtagmessagecodepage-canonical-property"></a><span data-ttu-id="62073-103">PidTagMessageCodepage (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="62073-103">PidTagMessageCodepage Canonical Property</span></span>

  
  
<span data-ttu-id="62073-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62073-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62073-105">Enthält die Codepage, die für die Nachricht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="62073-105">Contains the code page that is used for the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="62073-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="62073-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="62073-107">PR_MESSAGE_CODEPAGE</span><span class="sxs-lookup"><span data-stu-id="62073-107">PR_MESSAGE_CODEPAGE</span></span>  <br/> |
|<span data-ttu-id="62073-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="62073-108">Identifier:</span></span>  <br/> |<span data-ttu-id="62073-109">0x3FFD</span><span class="sxs-lookup"><span data-stu-id="62073-109">0x3FFD</span></span>  <br/> |
|<span data-ttu-id="62073-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="62073-110">Data type:</span></span>  <br/> |<span data-ttu-id="62073-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="62073-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="62073-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="62073-112">Area:</span></span>  <br/> |<span data-ttu-id="62073-113">Common</span><span class="sxs-lookup"><span data-stu-id="62073-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="62073-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="62073-114">Remarks</span></span>

<span data-ttu-id="62073-115">Die Ordner-Objekt auf der Seite Code wird verwendet, wenn diese Eigenschaft auf 0 (null) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="62073-115">The folder object code page is used if this property is set to zero (0).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="62073-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="62073-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="62073-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="62073-117">Protocol specifications</span></span>

<span data-ttu-id="62073-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="62073-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="62073-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="62073-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="62073-120">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="62073-120">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="62073-121">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="62073-121">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="62073-122">[[MS-OXPFOAB]](https://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="62073-122">[[MS-OXPFOAB]](https://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="62073-123">Gibt die Methode spielt Offlineadressbuch (OAB) Adressbuchdaten vom Server an den Client.</span><span class="sxs-lookup"><span data-stu-id="62073-123">Specifies the method of delivering offline address book (OAB) data from server to client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="62073-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="62073-124">Header files</span></span>

<span data-ttu-id="62073-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="62073-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="62073-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="62073-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="62073-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="62073-127">Mapitags.h</span></span>
  
> <span data-ttu-id="62073-128">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="62073-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="62073-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62073-129">See also</span></span>



[<span data-ttu-id="62073-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="62073-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="62073-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="62073-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="62073-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="62073-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="62073-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="62073-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

