---
title: PidTagPrimarySendAccount (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a0f4ae75117dff3610175b785ab3f982cc7e7552
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590407"
---
# <a name="pidtagprimarysendaccount-canonical-property"></a><span data-ttu-id="8b0a6-103">PidTagPrimarySendAccount (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8b0a6-103">PidTagPrimarySendAccount Canonical Property</span></span>

  
  
<span data-ttu-id="8b0a6-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b0a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b0a6-105">Enthält eine Zeichenfolge, die den Namen des ersten Servers, der zum Senden der Nachricht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8b0a6-105">Contains a string that names the first server that is used to send the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8b0a6-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8b0a6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8b0a6-107">PR_PRIMARY_SEND_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="8b0a6-107">PR_PRIMARY_SEND_ACCOUNT</span></span>  <br/> |
|<span data-ttu-id="8b0a6-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="8b0a6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8b0a6-109">0x0E28</span><span class="sxs-lookup"><span data-stu-id="8b0a6-109">0x0E28</span></span>  <br/> |
|<span data-ttu-id="8b0a6-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="8b0a6-110">Data type:</span></span>  <br/> |<span data-ttu-id="8b0a6-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8b0a6-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8b0a6-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="8b0a6-112">Area:</span></span>  <br/> |<span data-ttu-id="8b0a6-113">Konto</span><span class="sxs-lookup"><span data-stu-id="8b0a6-113">Account</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b0a6-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="8b0a6-114">Remarks</span></span>

<span data-ttu-id="8b0a6-115">Gibt den ersten Server, den ein Client verwenden sollten, um die e-Mail-Nachrichten senden.</span><span class="sxs-lookup"><span data-stu-id="8b0a6-115">Specifies the first server that a client should use to send the mail.</span></span> <span data-ttu-id="8b0a6-116">Das Format dieser Eigenschaften ist die Implementierung ab.</span><span class="sxs-lookup"><span data-stu-id="8b0a6-116">The format of these properties is implementation dependent.</span></span> <span data-ttu-id="8b0a6-117">Diese Eigenschaften zum Ermitteln des Servers, der e-Mail-Nachrichten über direkte vom Client verwendet werden können, jedoch ist optional, und der Wert hat keine Bedeutung für den Server.</span><span class="sxs-lookup"><span data-stu-id="8b0a6-117">These properties can be used by the client to determine which server to direct the mail through, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8b0a6-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8b0a6-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8b0a6-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="8b0a6-119">Protocol specifications</span></span>

<span data-ttu-id="8b0a6-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b0a6-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8b0a6-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="8b0a6-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8b0a6-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b0a6-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8b0a6-123">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="8b0a6-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8b0a6-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="8b0a6-124">Header files</span></span>

<span data-ttu-id="8b0a6-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8b0a6-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="8b0a6-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="8b0a6-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="8b0a6-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8b0a6-127">Mapitags.h</span></span>
  
> <span data-ttu-id="8b0a6-128">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="8b0a6-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8b0a6-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b0a6-129">See also</span></span>



[<span data-ttu-id="8b0a6-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8b0a6-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8b0a6-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8b0a6-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8b0a6-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="8b0a6-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8b0a6-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="8b0a6-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

