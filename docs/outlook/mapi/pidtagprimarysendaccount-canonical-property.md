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
ms.openlocfilehash: 2c32cc61fea63cd38215c30e04e8a467d4901cc9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339375"
---
# <a name="pidtagprimarysendaccount-canonical-property"></a><span data-ttu-id="13b70-103">PidTagPrimarySendAccount (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="13b70-103">PidTagPrimarySendAccount Canonical Property</span></span>

  
  
<span data-ttu-id="13b70-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13b70-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13b70-105">Enthält eine Zeichenfolge, die den ersten Server benennt, der zum Senden der Nachricht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="13b70-105">Contains a string that names the first server that is used to send the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="13b70-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="13b70-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="13b70-107">PR_PRIMARY_SEND_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="13b70-107">PR_PRIMARY_SEND_ACCOUNT</span></span>  <br/> |
|<span data-ttu-id="13b70-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="13b70-108">Identifier:</span></span>  <br/> |<span data-ttu-id="13b70-109">0x0E28</span><span class="sxs-lookup"><span data-stu-id="13b70-109">0x0E28</span></span>  <br/> |
|<span data-ttu-id="13b70-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="13b70-110">Data type:</span></span>  <br/> |<span data-ttu-id="13b70-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="13b70-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="13b70-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="13b70-112">Area:</span></span>  <br/> |<span data-ttu-id="13b70-113">Konto</span><span class="sxs-lookup"><span data-stu-id="13b70-113">Account</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13b70-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="13b70-114">Remarks</span></span>

<span data-ttu-id="13b70-115">Gibt den ersten Server an, den ein Client zum Senden der E-Mails verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="13b70-115">Specifies the first server that a client should use to send the mail.</span></span> <span data-ttu-id="13b70-116">Das Format dieser Eigenschaften ist implementierungsabhängig.</span><span class="sxs-lookup"><span data-stu-id="13b70-116">The format of these properties is implementation dependent.</span></span> <span data-ttu-id="13b70-117">Diese Eigenschaften können vom Client verwendet werden, um zu bestimmen, durch welchen Server die E-Mails gesendet werden sollen, ist jedoch optional, und der Wert hat keine Bedeutung für den Server.</span><span class="sxs-lookup"><span data-stu-id="13b70-117">These properties can be used by the client to determine which server to direct the mail through, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="13b70-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="13b70-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="13b70-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="13b70-119">Protocol specifications</span></span>

<span data-ttu-id="13b70-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13b70-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13b70-121">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="13b70-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="13b70-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13b70-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13b70-123">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="13b70-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="13b70-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="13b70-124">Header files</span></span>

<span data-ttu-id="13b70-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="13b70-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="13b70-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="13b70-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="13b70-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="13b70-127">Mapitags.h</span></span>
  
> <span data-ttu-id="13b70-128">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="13b70-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="13b70-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13b70-129">See also</span></span>



[<span data-ttu-id="13b70-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="13b70-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="13b70-131">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="13b70-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="13b70-132">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="13b70-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="13b70-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="13b70-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

