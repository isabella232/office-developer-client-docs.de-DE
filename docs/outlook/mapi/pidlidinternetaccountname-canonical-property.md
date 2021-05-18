---
title: PidLidInternetAccountName (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidInternetAccountName
api_type:
- COM
ms.assetid: 29bedadf-903d-419d-804d-dc8bd92b745d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2da826fe7ab9e4d7ca3eaaf0f9806193c47100d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315491"
---
# <a name="pidlidinternetaccountname-canonical-property"></a><span data-ttu-id="857e7-103">PidLidInternetAccountName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="857e7-103">PidLidInternetAccountName Canonical Property</span></span>

  
  
<span data-ttu-id="857e7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="857e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="857e7-105">Gibt den benutzer sichtbaren E-Mail-Kontonamen an, über den die E-Mail-Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="857e7-105">Specifies the user-visible email account name through which the email message is sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="857e7-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="857e7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="857e7-107">dispidInetAcctName</span><span class="sxs-lookup"><span data-stu-id="857e7-107">dispidInetAcctName</span></span>  <br/> |
|<span data-ttu-id="857e7-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="857e7-108">Property set:</span></span>  <br/> |<span data-ttu-id="857e7-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="857e7-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="857e7-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="857e7-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="857e7-111">0x00008580</span><span class="sxs-lookup"><span data-stu-id="857e7-111">0x00008580</span></span>  <br/> |
|<span data-ttu-id="857e7-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="857e7-112">Data type:</span></span>  <br/> |<span data-ttu-id="857e7-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="857e7-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="857e7-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="857e7-114">Area:</span></span>  <br/> |<span data-ttu-id="857e7-115">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="857e7-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="857e7-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="857e7-116">Remarks</span></span>

<span data-ttu-id="857e7-117">Das Format dieser Zeichenfolge ist implementierungsabhängig.</span><span class="sxs-lookup"><span data-stu-id="857e7-117">The format of this string is implementation dependent.</span></span> <span data-ttu-id="857e7-118">Diese Eigenschaft kann vom Client verwendet werden, um zu bestimmen, an welchen Server die E-Mails gesendet werden sollen, ist jedoch optional, und der Wert hat keine Bedeutung für den Server.</span><span class="sxs-lookup"><span data-stu-id="857e7-118">This property can be used by the client to determine which server to direct the mail to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="857e7-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="857e7-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="857e7-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="857e7-120">Protocol specifications</span></span>

<span data-ttu-id="857e7-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="857e7-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="857e7-122">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="857e7-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="857e7-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="857e7-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="857e7-124">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="857e7-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="857e7-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="857e7-125">Header files</span></span>

<span data-ttu-id="857e7-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="857e7-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="857e7-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="857e7-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="857e7-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="857e7-128">See also</span></span>



[<span data-ttu-id="857e7-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="857e7-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="857e7-130">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="857e7-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="857e7-131">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="857e7-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="857e7-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="857e7-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

