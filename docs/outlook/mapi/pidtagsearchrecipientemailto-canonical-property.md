---
title: Kanonische Pidtagsearchrecipientemailto (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f5de77c3-5912-f7bc-8e8c-3a053545c359
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d254df132db5542ce5235c1c3ab42ea768399f0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358919"
---
# <a name="pidtagsearchrecipientemailto-canonical-property"></a><span data-ttu-id="ee78f-103">Kanonische Pidtagsearchrecipientemailto (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ee78f-103">PidTagSearchRecipientEmailTo Canonical Property</span></span>

  
  
<span data-ttu-id="ee78f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee78f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee78f-105">Enthält eine Unicode-Zeichenfolge, die in der Liste der e-Mail-Adressen oder Anzeigenamen von Empfängern abgefragt wird, die in der **an** -Nachrichten Reihe im Speicher adressiert sind.</span><span class="sxs-lookup"><span data-stu-id="ee78f-105">Contains a Unicode string that is being queried in the list of email addresses or display names of recipients that are addressed in the **To** line of messages on the store.</span></span> 
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="ee78f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ee78f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ee78f-107">PR_SEARCH_RECIP_EMAIL_TO_W</span><span class="sxs-lookup"><span data-stu-id="ee78f-107">PR_SEARCH_RECIP_EMAIL_TO_W</span></span>  <br/> |
|<span data-ttu-id="ee78f-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="ee78f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ee78f-109">0x0EA6</span><span class="sxs-lookup"><span data-stu-id="ee78f-109">0x0EA6</span></span>  <br/> |
|<span data-ttu-id="ee78f-110">Eigenschafts:</span><span class="sxs-lookup"><span data-stu-id="ee78f-110">Property type:</span></span>  <br/> |<span data-ttu-id="ee78f-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ee78f-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ee78f-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ee78f-112">Area:</span></span>  <br/> |<span data-ttu-id="ee78f-113">Suche</span><span class="sxs-lookup"><span data-stu-id="ee78f-113">Search</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ee78f-114">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ee78f-114">Related resources</span></span>

> [!NOTE]
> <span data-ttu-id="ee78f-115">Dieses MAPI-Einschränkungs, das verwendet wird, wenn Sie nach e-Mail-Adressen oder Anzeigenamen suchen, an die die Nachricht gesendet wird, wird möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben.</span><span class="sxs-lookup"><span data-stu-id="ee78f-115">This MAPI restriction tag, used when you search for email addresses or display names to which the message is sent, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="ee78f-116">Sie können Sie dem Code hinzufügen, indem Sie den folgenden Wert verwenden: >`#define PR_SEARCH_RECIP_EMAIL_TO_W PROP_TAG(PT_UNICODE, 0x0EA6)`</span><span class="sxs-lookup"><span data-stu-id="ee78f-116">You can add it to your code by using the following value: >  `#define PR_SEARCH_RECIP_EMAIL_TO_W PROP_TAG(PT_UNICODE, 0x0EA6)`</span></span>
  
### <a name="protocol-specifications"></a><span data-ttu-id="ee78f-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="ee78f-117">Protocol specifications</span></span>

<span data-ttu-id="ee78f-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ee78f-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ee78f-119">Enthält Verweise auf zugehörige Microsoft Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="ee78f-119">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ee78f-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ee78f-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ee78f-121">Gibt die Eigenschaften und Vorgänge zum Bearbeiten einer Suchordner Listen Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="ee78f-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ee78f-122">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="ee78f-122">Header files</span></span>

<span data-ttu-id="ee78f-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ee78f-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="ee78f-124">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="ee78f-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="ee78f-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="ee78f-125">Mapitags.h</span></span>
  
> <span data-ttu-id="ee78f-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="ee78f-126">Contains definitions of properties that are listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ee78f-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee78f-127">See also</span></span>



[<span data-ttu-id="ee78f-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ee78f-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ee78f-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ee78f-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ee78f-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ee78f-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ee78f-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ee78f-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

