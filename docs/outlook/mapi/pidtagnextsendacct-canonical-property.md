---
title: Kanonische Pidtagnextsendacct (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNextSendAcct
api_type:
- HeaderDef
ms.assetid: b7429c2e-0d9d-4921-9f56-9ecad817f8cb
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: eff053fda58266afd5500e322559059f051d5ac3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329393"
---
# <a name="pidtagnextsendacct-canonical-property"></a><span data-ttu-id="2e531-103">Kanonische Pidtagnextsendacct (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2e531-103">PidTagNextSendAcct Canonical Property</span></span>

  
  
<span data-ttu-id="2e531-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e531-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e531-105">Gibt den Server an, den ein Client derzeit zum Senden von e-Mails verwendet.</span><span class="sxs-lookup"><span data-stu-id="2e531-105">Specifies the server that a client is currently attempting to use to send email.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2e531-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="2e531-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2e531-107">PR_NEXT_SEND_ACCT</span><span class="sxs-lookup"><span data-stu-id="2e531-107">PR_NEXT_SEND_ACCT</span></span>  <br/> |
|<span data-ttu-id="2e531-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="2e531-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2e531-109">0x0E29</span><span class="sxs-lookup"><span data-stu-id="2e531-109">0x0E29</span></span>  <br/> |
|<span data-ttu-id="2e531-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="2e531-110">Data type:</span></span>  <br/> |<span data-ttu-id="2e531-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2e531-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2e531-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="2e531-112">Area:</span></span>  <br/> |<span data-ttu-id="2e531-113">Outlook-Anwendung</span><span class="sxs-lookup"><span data-stu-id="2e531-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e531-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e531-114">Remarks</span></span>

<span data-ttu-id="2e531-115">Das Format dieser Eigenschaft ist abhängig von der Implementierung.</span><span class="sxs-lookup"><span data-stu-id="2e531-115">The format of this property is implementation dependent.</span></span> <span data-ttu-id="2e531-116">Diese Eigenschaft kann vom Client verwendet werden, um zu bestimmen, auf welchem Server die e-Mail umgeleitet werden soll, aber optional ist und der Wert keine Bedeutung für den Server hat.</span><span class="sxs-lookup"><span data-stu-id="2e531-116">This property can be used by the client to determine which server to direct the email to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2e531-117">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2e531-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2e531-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="2e531-118">Protocol specifications</span></span>

<span data-ttu-id="2e531-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2e531-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2e531-120">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="2e531-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2e531-121">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2e531-121">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2e531-122">Konvertiert zwischen IETF-RFC2445, RFC2446 und RFC2447 sowie Termin-und Besprechungs Objekten.</span><span class="sxs-lookup"><span data-stu-id="2e531-122">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="2e531-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2e531-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2e531-124">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="2e531-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2e531-125">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="2e531-125">Header files</span></span>

<span data-ttu-id="2e531-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="2e531-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="2e531-127">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="2e531-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="2e531-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="2e531-128">Mapitags.h</span></span>
  
> <span data-ttu-id="2e531-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="2e531-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2e531-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e531-130">See also</span></span>



[<span data-ttu-id="2e531-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2e531-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2e531-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2e531-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2e531-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="2e531-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2e531-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="2e531-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

