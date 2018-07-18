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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 222ca10e58b50fa06876718658d1a6f3843da2f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794804"
---
# <a name="pidtagprimarysendaccount-canonical-property"></a><span data-ttu-id="a894f-103">PidTagPrimarySendAccount (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a894f-103">PidTagPrimarySendAccount Canonical Property</span></span>

  
  
<span data-ttu-id="a894f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a894f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a894f-105">Enthält eine Zeichenfolge, die den Namen des ersten Servers, der zum Senden der Nachricht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a894f-105">Contains a string that names the first server that is used to send the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a894f-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a894f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a894f-107">PR_PRIMARY_SEND_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="a894f-107">PR_PRIMARY_SEND_ACCOUNT</span></span>  <br/> |
|<span data-ttu-id="a894f-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="a894f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a894f-109">0x0E28</span><span class="sxs-lookup"><span data-stu-id="a894f-109">0x0E28</span></span>  <br/> |
|<span data-ttu-id="a894f-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a894f-110">Data type:</span></span>  <br/> |<span data-ttu-id="a894f-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a894f-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a894f-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a894f-112">Area:</span></span>  <br/> |<span data-ttu-id="a894f-113">Konto</span><span class="sxs-lookup"><span data-stu-id="a894f-113">Account</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a894f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a894f-114">Remarks</span></span>

<span data-ttu-id="a894f-115">Gibt den ersten Server, den ein Client verwenden sollten, um die e-Mail-Nachrichten senden.</span><span class="sxs-lookup"><span data-stu-id="a894f-115">Specifies the first server that a client should use to send the mail.</span></span> <span data-ttu-id="a894f-116">Das Format dieser Eigenschaften ist die Implementierung ab.</span><span class="sxs-lookup"><span data-stu-id="a894f-116">The format of these properties is implementation dependent.</span></span> <span data-ttu-id="a894f-117">Diese Eigenschaften zum Ermitteln des Servers, der e-Mail-Nachrichten über direkte vom Client verwendet werden können, jedoch ist optional, und der Wert hat keine Bedeutung für den Server.</span><span class="sxs-lookup"><span data-stu-id="a894f-117">These properties can be used by the client to determine which server to direct the mail through, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a894f-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a894f-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a894f-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a894f-119">Protocol specifications</span></span>

<span data-ttu-id="a894f-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a894f-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a894f-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="a894f-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a894f-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a894f-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a894f-123">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="a894f-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a894f-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="a894f-124">Header files</span></span>

<span data-ttu-id="a894f-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a894f-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="a894f-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a894f-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="a894f-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a894f-127">Mapitags.h</span></span>
  
> <span data-ttu-id="a894f-128">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a894f-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a894f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a894f-129">See also</span></span>



[<span data-ttu-id="a894f-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a894f-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a894f-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a894f-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a894f-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a894f-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a894f-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a894f-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

