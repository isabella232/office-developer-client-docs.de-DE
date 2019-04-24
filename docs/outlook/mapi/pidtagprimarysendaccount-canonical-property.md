---
title: Kanonische Pidtagprimarysendaccount (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagPrimarySendAccount
api_type:
- COM
ms.assetid: 2f268b3b-2e4c-4aea-8879-bdd0ac1df35c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2c32cc61fea63cd38215c30e04e8a467d4901cc9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339375"
---
# <a name="pidtagprimarysendaccount-canonical-property"></a><span data-ttu-id="b2731-103">Kanonische Pidtagprimarysendaccount (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b2731-103">PidTagPrimarySendAccount Canonical Property</span></span>

  
  
<span data-ttu-id="b2731-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2731-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2731-105">Enthält eine Zeichenfolge, die den ersten Server benennt, der zum Senden der Nachricht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b2731-105">Contains a string that names the first server that is used to send the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b2731-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b2731-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b2731-107">PR_PRIMARY_SEND_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="b2731-107">PR_PRIMARY_SEND_ACCOUNT</span></span>  <br/> |
|<span data-ttu-id="b2731-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="b2731-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b2731-109">0x0E28</span><span class="sxs-lookup"><span data-stu-id="b2731-109">0x0E28</span></span>  <br/> |
|<span data-ttu-id="b2731-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b2731-110">Data type:</span></span>  <br/> |<span data-ttu-id="b2731-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b2731-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b2731-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b2731-112">Area:</span></span>  <br/> |<span data-ttu-id="b2731-113">Konto</span><span class="sxs-lookup"><span data-stu-id="b2731-113">Account</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b2731-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2731-114">Remarks</span></span>

<span data-ttu-id="b2731-115">Gibt den ersten Server an, der vom Client zum Senden der e-Mail verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2731-115">Specifies the first server that a client should use to send the mail.</span></span> <span data-ttu-id="b2731-116">Das Format dieser Eigenschaften ist abhängig von der Implementierung.</span><span class="sxs-lookup"><span data-stu-id="b2731-116">The format of these properties is implementation dependent.</span></span> <span data-ttu-id="b2731-117">Diese Eigenschaften können vom Client verwendet werden, um zu bestimmen, auf welchem Server die e-Mail weitergeleitet werden soll, aber optional ist und der Wert keine Bedeutung für den Server hat.</span><span class="sxs-lookup"><span data-stu-id="b2731-117">These properties can be used by the client to determine which server to direct the mail through, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b2731-118">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b2731-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b2731-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b2731-119">Protocol specifications</span></span>

<span data-ttu-id="b2731-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b2731-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b2731-121">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="b2731-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b2731-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b2731-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b2731-123">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="b2731-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b2731-124">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="b2731-124">Header files</span></span>

<span data-ttu-id="b2731-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b2731-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="b2731-126">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="b2731-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="b2731-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="b2731-127">Mapitags.h</span></span>
  
> <span data-ttu-id="b2731-128">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="b2731-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b2731-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2731-129">See also</span></span>



[<span data-ttu-id="b2731-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b2731-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b2731-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b2731-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b2731-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b2731-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b2731-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b2731-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

