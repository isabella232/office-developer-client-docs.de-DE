---
title: PidLidInternetAccountStamp (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidInternetAccountStamp
api_type:
- COM
ms.assetid: 819179fe-e58e-415c-abc7-1949036745ee
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ebd64392d24cd170a7babf77865aa00c7be24802
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315456"
---
# <a name="pidlidinternetaccountstamp-canonical-property"></a><span data-ttu-id="75b41-103">PidLidInternetAccountStamp (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="75b41-103">PidLidInternetAccountStamp Canonical Property</span></span>

  
  
<span data-ttu-id="75b41-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75b41-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75b41-105">Gibt die E-Mail-Konto-ID an, über die die E-Mail-Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="75b41-105">Specifies the email account ID through which the email message is sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="75b41-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="75b41-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="75b41-107">dispidInetAcctStamp</span><span class="sxs-lookup"><span data-stu-id="75b41-107">dispidInetAcctStamp</span></span>  <br/> |
|<span data-ttu-id="75b41-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="75b41-108">Property set:</span></span>  <br/> |<span data-ttu-id="75b41-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="75b41-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="75b41-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="75b41-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="75b41-111">0x00008581</span><span class="sxs-lookup"><span data-stu-id="75b41-111">0x00008581</span></span>  <br/> |
|<span data-ttu-id="75b41-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="75b41-112">Data type:</span></span>  <br/> |<span data-ttu-id="75b41-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="75b41-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="75b41-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="75b41-114">Area:</span></span>  <br/> |<span data-ttu-id="75b41-115">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="75b41-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75b41-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="75b41-116">Remarks</span></span>

<span data-ttu-id="75b41-117">Das Format dieser Zeichenfolge ist implementierungsabhängig.</span><span class="sxs-lookup"><span data-stu-id="75b41-117">The format of this string is implementation dependent.</span></span> <span data-ttu-id="75b41-118">Diese Eigenschaft kann vom Client verwendet werden, um zu bestimmen, an welchen Server die E-Mails gesendet werden sollen, ist jedoch optional, und der Wert hat keine Bedeutung für den Server.</span><span class="sxs-lookup"><span data-stu-id="75b41-118">This property can be used by the client to determine which server to direct the mail to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="75b41-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="75b41-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="75b41-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="75b41-120">Protocol specifications</span></span>

<span data-ttu-id="75b41-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75b41-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75b41-122">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="75b41-122">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="75b41-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75b41-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75b41-124">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="75b41-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="75b41-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="75b41-125">Header files</span></span>

<span data-ttu-id="75b41-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="75b41-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="75b41-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="75b41-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="75b41-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75b41-128">See also</span></span>



[<span data-ttu-id="75b41-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="75b41-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="75b41-130">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="75b41-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="75b41-131">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="75b41-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="75b41-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="75b41-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

