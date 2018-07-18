---
title: PidTagSearchRecipientEmailBcc (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d9561d13-8d52-500c-5369-15a2cf5c92c3
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 498a740a6523434cc6c70793cf98fd1e2ccfbdb3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795111"
---
# <a name="pidtagsearchrecipientemailbcc-canonical-property"></a><span data-ttu-id="5da95-103">PidTagSearchRecipientEmailBcc (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5da95-103">PidTagSearchRecipientEmailBcc Canonical Property</span></span>

  
  
<span data-ttu-id="5da95-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5da95-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5da95-105">Enthält eine Unicodezeichenfolge, die in der Liste der e-Mail-Adressen oder Anzeigenamen der Empfänger in der **BCC** -Zeile von nicht gesendeten Nachrichten im Store abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="5da95-105">Contains a Unicode string that is being queried in the list of email addresses or display names of recipients addressed in the **BCC** line of unsent messages on the store.</span></span> 
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="5da95-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5da95-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5da95-107">PR_SEARCH_RECIP_EMAIL_BCC_W</span><span class="sxs-lookup"><span data-stu-id="5da95-107">PR_SEARCH_RECIP_EMAIL_BCC_W</span></span>  <br/> |
|<span data-ttu-id="5da95-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="5da95-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5da95-109">0x0EA8</span><span class="sxs-lookup"><span data-stu-id="5da95-109">0x0EA8</span></span>  <br/> |
|<span data-ttu-id="5da95-110">Der Eigenschaftentyp:</span><span class="sxs-lookup"><span data-stu-id="5da95-110">Property type:</span></span>  <br/> |<span data-ttu-id="5da95-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5da95-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5da95-112">Access:</span><span class="sxs-lookup"><span data-stu-id="5da95-112">Access:</span></span>  <br/> |<span data-ttu-id="5da95-113">Suche</span><span class="sxs-lookup"><span data-stu-id="5da95-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5da95-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5da95-114">Remarks</span></span>

<span data-ttu-id="5da95-115">Diese Eigenschaft ist nur relevant, die Nachrichten auf den Speicher, die nicht gesendet wurden, da Nachrichten, die gesendet oder empfangen wurde keine BCC-Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="5da95-115">This property is only relevant to messages on the store that have not been sent, because messages that have been sent or received do not contain BCC information.</span></span>
  
> [!NOTE]
> <span data-ttu-id="5da95-116">Diese MAPI-Einschränkung Tag verwendet, wenn die Suche nach e-Mail-Adressen oder Anzeigenamen, die die Nachricht als eine Blindkopie gesendet wird, möglicherweise nicht in der herunterladbaren Headerdatei definiert werden, die Sie besitzen.</span><span class="sxs-lookup"><span data-stu-id="5da95-116">This MAPI restriction tag, used when searching for email addresses or display names to which the message will be sent as a blind carbon copy, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="5da95-117">Mit dem folgenden Wert dem Code hinzufügen: >`#define PR_SEARCH_RECIP_EMAIL_BCC_W PROP_TAG(PT_UNICODE, 0x0EA8)`</span><span class="sxs-lookup"><span data-stu-id="5da95-117">You can add it to your code by using the following value: >  `#define PR_SEARCH_RECIP_EMAIL_BCC_W PROP_TAG(PT_UNICODE, 0x0EA8)`</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5da95-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5da95-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5da95-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5da95-119">Protocol specifications</span></span>

<span data-ttu-id="5da95-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5da95-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5da95-121">Bietet Verweise auf Verwandte Spezifikationen von Microsoft Exchange Server-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="5da95-121">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5da95-122">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5da95-122">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5da95-123">Gibt die Eigenschaften und Operationen für das Bearbeiten der Liste einer Suchkonfiguration-Ordner.</span><span class="sxs-lookup"><span data-stu-id="5da95-123">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5da95-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="5da95-124">Header files</span></span>

<span data-ttu-id="5da95-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5da95-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="5da95-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5da95-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="5da95-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5da95-127">Mapitags.h</span></span>
  
> <span data-ttu-id="5da95-128">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5da95-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5da95-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5da95-129">See also</span></span>



[<span data-ttu-id="5da95-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5da95-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5da95-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5da95-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5da95-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5da95-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5da95-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5da95-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

