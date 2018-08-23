---
title: PidTagSearchAttachments (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534c3881-e12f-f228-7760-788fe2b72ae8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 80d1fc3f711369471eb2c1473700f13a6b995594
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578507"
---
# <a name="pidtagsearchattachments-canonical-property"></a><span data-ttu-id="2685d-103">PidTagSearchAttachments (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2685d-103">PidTagSearchAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="2685d-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2685d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2685d-105">Enthält eine Unicodezeichenfolge, die im Anlageninhalt für den Speicher abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="2685d-105">Contains a Unicode string that is being queried in attachment contents on the store.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="2685d-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="2685d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2685d-107">PR_SEARCH_ATTACHMENTS_W</span><span class="sxs-lookup"><span data-stu-id="2685d-107">PR_SEARCH_ATTACHMENTS_W</span></span>  <br/> |
|<span data-ttu-id="2685d-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="2685d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2685d-109">0x0EA5</span><span class="sxs-lookup"><span data-stu-id="2685d-109">0x0EA5</span></span>  <br/> |
|<span data-ttu-id="2685d-110">Der Eigenschaftentyp:</span><span class="sxs-lookup"><span data-stu-id="2685d-110">Property type:</span></span>  <br/> |<span data-ttu-id="2685d-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2685d-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2685d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="2685d-112">Area:</span></span>  <br/> |<span data-ttu-id="2685d-113">Suche</span><span class="sxs-lookup"><span data-stu-id="2685d-113">Search</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="2685d-114">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2685d-114">Related resources</span></span>

> [!NOTE]
> <span data-ttu-id="2685d-115">Diese MAPI-Einschränkung Tag verwendet bei der Suche für Anlageninhalt, möglicherweise nicht in der Headerdatei zum Herunterladen definiert werden, die Sie besitzen.</span><span class="sxs-lookup"><span data-stu-id="2685d-115">This MAPI restriction tag, used when you are searching for attachment contents, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="2685d-116">Mit dem folgenden Wert dem Code hinzufügen: >`#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`</span><span class="sxs-lookup"><span data-stu-id="2685d-116">You can add it to your code by using the following value: >  `#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`</span></span>
  
### <a name="protocol-specifications"></a><span data-ttu-id="2685d-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="2685d-117">Protocol specifications</span></span>

<span data-ttu-id="2685d-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2685d-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2685d-119">Bietet Verweise auf Verwandte Spezifikationen von Microsoft Exchange Server-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="2685d-119">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2685d-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2685d-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2685d-121">Gibt die Eigenschaften und Operationen für das Bearbeiten der Liste einer Suchkonfiguration-Ordner.</span><span class="sxs-lookup"><span data-stu-id="2685d-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2685d-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="2685d-122">Header files</span></span>

<span data-ttu-id="2685d-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2685d-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="2685d-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="2685d-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="2685d-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2685d-125">Mapitags.h</span></span>
  
> <span data-ttu-id="2685d-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="2685d-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2685d-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2685d-127">See also</span></span>



[<span data-ttu-id="2685d-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2685d-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2685d-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2685d-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2685d-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="2685d-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2685d-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="2685d-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

