---
title: Kanonische Pidtagsearchrecipientemailbcc (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d9561d13-8d52-500c-5369-15a2cf5c92c3
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5b0db4b3bc7903aae74fa7275d3e27e22d628514
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359157"
---
# <a name="pidtagsearchrecipientemailbcc-canonical-property"></a><span data-ttu-id="2b9d1-103">Kanonische Pidtagsearchrecipientemailbcc (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2b9d1-103">PidTagSearchRecipientEmailBcc Canonical Property</span></span>

  
  
<span data-ttu-id="2b9d1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b9d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b9d1-105">Enthält eine Unicode-Zeichenfolge, die in der Liste der e-Mail-Adressen oder Anzeige Namen von Empfängern abgefragt wird, die in der **Bcc** -Zeile nicht gesendeter Nachrichten im Speicher adressiert sind.</span><span class="sxs-lookup"><span data-stu-id="2b9d1-105">Contains a Unicode string that is being queried in the list of email addresses or display names of recipients addressed in the **BCC** line of unsent messages on the store.</span></span> 
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="2b9d1-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="2b9d1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2b9d1-107">PR_SEARCH_RECIP_EMAIL_BCC_W</span><span class="sxs-lookup"><span data-stu-id="2b9d1-107">PR_SEARCH_RECIP_EMAIL_BCC_W</span></span>  <br/> |
|<span data-ttu-id="2b9d1-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="2b9d1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2b9d1-109">0x0EA8</span><span class="sxs-lookup"><span data-stu-id="2b9d1-109">0x0EA8</span></span>  <br/> |
|<span data-ttu-id="2b9d1-110">Eigenschafts:</span><span class="sxs-lookup"><span data-stu-id="2b9d1-110">Property type:</span></span>  <br/> |<span data-ttu-id="2b9d1-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2b9d1-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2b9d1-112">Access</span><span class="sxs-lookup"><span data-stu-id="2b9d1-112">Access:</span></span>  <br/> |<span data-ttu-id="2b9d1-113">Suche</span><span class="sxs-lookup"><span data-stu-id="2b9d1-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2b9d1-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b9d1-114">Remarks</span></span>

<span data-ttu-id="2b9d1-115">Diese Eigenschaft ist nur für Nachrichten im Speicher relevant, die nicht gesendet wurden, da Nachrichten, die gesendet oder empfangen wurden, keine BCC-Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="2b9d1-115">This property is only relevant to messages on the store that have not been sent, because messages that have been sent or received do not contain BCC information.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2b9d1-116">Dieses MAPI-Einschränkungs, das bei der Suche nach e-Mail-Adressen oder Anzeigenamen verwendet wird, an die die Nachricht als Blind Carbon Copy gesendet wird, wird möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben.</span><span class="sxs-lookup"><span data-stu-id="2b9d1-116">This MAPI restriction tag, used when searching for email addresses or display names to which the message will be sent as a blind carbon copy, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="2b9d1-117">Sie können Sie dem Code hinzufügen, indem Sie den folgenden Wert verwenden: >`#define PR_SEARCH_RECIP_EMAIL_BCC_W PROP_TAG(PT_UNICODE, 0x0EA8)`</span><span class="sxs-lookup"><span data-stu-id="2b9d1-117">You can add it to your code by using the following value: >  `#define PR_SEARCH_RECIP_EMAIL_BCC_W PROP_TAG(PT_UNICODE, 0x0EA8)`</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2b9d1-118">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2b9d1-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2b9d1-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="2b9d1-119">Protocol specifications</span></span>

<span data-ttu-id="2b9d1-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2b9d1-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2b9d1-121">Enthält Verweise auf zugehörige Microsoft Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="2b9d1-121">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2b9d1-122">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2b9d1-122">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2b9d1-123">Gibt die Eigenschaften und Vorgänge zum Bearbeiten einer Suchordner Listen Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="2b9d1-123">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2b9d1-124">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="2b9d1-124">Header files</span></span>

<span data-ttu-id="2b9d1-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="2b9d1-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="2b9d1-126">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="2b9d1-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="2b9d1-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="2b9d1-127">Mapitags.h</span></span>
  
> <span data-ttu-id="2b9d1-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="2b9d1-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2b9d1-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b9d1-129">See also</span></span>



[<span data-ttu-id="2b9d1-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2b9d1-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2b9d1-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2b9d1-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2b9d1-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="2b9d1-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2b9d1-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="2b9d1-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

