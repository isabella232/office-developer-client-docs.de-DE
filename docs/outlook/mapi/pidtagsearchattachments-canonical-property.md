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
ms.openlocfilehash: 95729474db29fe21f808ec5c8f571bec4600db70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336323"
---
# <a name="pidtagsearchattachments-canonical-property"></a><span data-ttu-id="e8cb0-103">PidTagSearchAttachments (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e8cb0-103">PidTagSearchAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="e8cb0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8cb0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8cb0-105">Enthält eine Unicode-Zeichenfolge, die in Anlageninhalten im Speicher abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="e8cb0-105">Contains a Unicode string that is being queried in attachment contents on the store.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="e8cb0-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e8cb0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e8cb0-107">PR_SEARCH_ATTACHMENTS_W</span><span class="sxs-lookup"><span data-stu-id="e8cb0-107">PR_SEARCH_ATTACHMENTS_W</span></span>  <br/> |
|<span data-ttu-id="e8cb0-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e8cb0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e8cb0-109">0x0EA5</span><span class="sxs-lookup"><span data-stu-id="e8cb0-109">0x0EA5</span></span>  <br/> |
|<span data-ttu-id="e8cb0-110">Eigenschaftstyp:</span><span class="sxs-lookup"><span data-stu-id="e8cb0-110">Property type:</span></span>  <br/> |<span data-ttu-id="e8cb0-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e8cb0-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e8cb0-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e8cb0-112">Area:</span></span>  <br/> |<span data-ttu-id="e8cb0-113">Suche</span><span class="sxs-lookup"><span data-stu-id="e8cb0-113">Search</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="e8cb0-114">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e8cb0-114">Related resources</span></span>

> [!NOTE]
> <span data-ttu-id="e8cb0-115">Dieses MAPI-Einschränkungstag, das bei der Suche nach Anlageninhalten verwendet wird, ist möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben.</span><span class="sxs-lookup"><span data-stu-id="e8cb0-115">This MAPI restriction tag, used when you are searching for attachment contents, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="e8cb0-116">Sie können sie ihrem Code mithilfe des folgenden Werts hinzufügen: >  `#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`</span><span class="sxs-lookup"><span data-stu-id="e8cb0-116">You can add it to your code by using the following value: >  `#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`</span></span>
  
### <a name="protocol-specifications"></a><span data-ttu-id="e8cb0-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e8cb0-117">Protocol specifications</span></span>

<span data-ttu-id="e8cb0-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e8cb0-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e8cb0-119">Enthält Verweise auf Microsoft Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="e8cb0-119">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e8cb0-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e8cb0-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e8cb0-121">Gibt die Eigenschaften und Vorgänge zum Bearbeiten einer Suchordnerlistenkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="e8cb0-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e8cb0-122">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="e8cb0-122">Header files</span></span>

<span data-ttu-id="e8cb0-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e8cb0-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="e8cb0-124">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e8cb0-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="e8cb0-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e8cb0-125">Mapitags.h</span></span>
  
> <span data-ttu-id="e8cb0-126">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e8cb0-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e8cb0-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8cb0-127">See also</span></span>



[<span data-ttu-id="e8cb0-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e8cb0-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e8cb0-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="e8cb0-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e8cb0-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e8cb0-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e8cb0-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e8cb0-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

