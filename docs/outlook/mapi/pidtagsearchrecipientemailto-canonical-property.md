---
title: PidTagSearchRecipientEmailTo (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f5de77c3-5912-f7bc-8e8c-3a053545c359
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5d6c029ba91b6b3489d3f6544ead6788760363a7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795120"
---
# <a name="pidtagsearchrecipientemailto-canonical-property"></a><span data-ttu-id="211b7-103">PidTagSearchRecipientEmailTo (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="211b7-103">PidTagSearchRecipientEmailTo Canonical Property</span></span>

  
  
<span data-ttu-id="211b7-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="211b7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="211b7-105">Enthält eine Unicode-Zeichenfolge, die in der Liste der e-Mail-Adressen oder Anzeigenamen der Empfänger an, die in der Zeile **an** der Nachrichten im Store behandelt werden abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="211b7-105">Contains a Unicode string that is being queried in the list of email addresses or display names of recipients that are addressed in the **To** line of messages on the store.</span></span> 
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="211b7-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="211b7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="211b7-107">PR_SEARCH_RECIP_EMAIL_TO_W</span><span class="sxs-lookup"><span data-stu-id="211b7-107">PR_SEARCH_RECIP_EMAIL_TO_W</span></span>  <br/> |
|<span data-ttu-id="211b7-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="211b7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="211b7-109">0x0EA6</span><span class="sxs-lookup"><span data-stu-id="211b7-109">0x0EA6</span></span>  <br/> |
|<span data-ttu-id="211b7-110">Der Eigenschaftentyp:</span><span class="sxs-lookup"><span data-stu-id="211b7-110">Property type:</span></span>  <br/> |<span data-ttu-id="211b7-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="211b7-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="211b7-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="211b7-112">Area:</span></span>  <br/> |<span data-ttu-id="211b7-113">Suche</span><span class="sxs-lookup"><span data-stu-id="211b7-113">Search</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="211b7-114">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="211b7-114">Related resources</span></span>

> [!NOTE]
> <span data-ttu-id="211b7-115">Diese MAPI-Einschränkung Tag verwendet, wenn Sie nach e-Mail-Adressen suchen oder Anzeigen von Namen, die die Nachricht gesendet wird, möglicherweise nicht in der herunterladbaren Headerdatei definiert werden, die Sie besitzen.</span><span class="sxs-lookup"><span data-stu-id="211b7-115">This MAPI restriction tag, used when you search for email addresses or display names to which the message is sent, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="211b7-116">Mit dem folgenden Wert dem Code hinzufügen: >`#define PR_SEARCH_RECIP_EMAIL_TO_W PROP_TAG(PT_UNICODE, 0x0EA6)`</span><span class="sxs-lookup"><span data-stu-id="211b7-116">You can add it to your code by using the following value: >  `#define PR_SEARCH_RECIP_EMAIL_TO_W PROP_TAG(PT_UNICODE, 0x0EA6)`</span></span>
  
### <a name="protocol-specifications"></a><span data-ttu-id="211b7-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="211b7-117">Protocol specifications</span></span>

<span data-ttu-id="211b7-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="211b7-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="211b7-119">Bietet Verweise auf Verwandte Spezifikationen von Microsoft Exchange Server-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="211b7-119">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="211b7-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="211b7-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="211b7-121">Gibt die Eigenschaften und Operationen für das Bearbeiten der Liste einer Suchkonfiguration-Ordner.</span><span class="sxs-lookup"><span data-stu-id="211b7-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="211b7-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="211b7-122">Header files</span></span>

<span data-ttu-id="211b7-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="211b7-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="211b7-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="211b7-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="211b7-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="211b7-125">Mapitags.h</span></span>
  
> <span data-ttu-id="211b7-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="211b7-126">Contains definitions of properties that are listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="211b7-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="211b7-127">See also</span></span>



[<span data-ttu-id="211b7-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="211b7-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="211b7-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="211b7-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="211b7-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="211b7-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="211b7-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="211b7-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

