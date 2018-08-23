---
title: PidTagSearchRecipientEmailTo (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f5de77c3-5912-f7bc-8e8c-3a053545c359
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ad96b448018ec43cda85aab1245afb1ca22552f8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583211"
---
# <a name="pidtagsearchrecipientemailto-canonical-property"></a><span data-ttu-id="3bceb-103">PidTagSearchRecipientEmailTo (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3bceb-103">PidTagSearchRecipientEmailTo Canonical Property</span></span>

  
  
<span data-ttu-id="3bceb-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3bceb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3bceb-105">Enthält eine Unicode-Zeichenfolge, die in der Liste der e-Mail-Adressen oder Anzeigenamen der Empfänger an, die in der Zeile **an** der Nachrichten im Store behandelt werden abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="3bceb-105">Contains a Unicode string that is being queried in the list of email addresses or display names of recipients that are addressed in the **To** line of messages on the store.</span></span> 
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="3bceb-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="3bceb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3bceb-107">PR_SEARCH_RECIP_EMAIL_TO_W</span><span class="sxs-lookup"><span data-stu-id="3bceb-107">PR_SEARCH_RECIP_EMAIL_TO_W</span></span>  <br/> |
|<span data-ttu-id="3bceb-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="3bceb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3bceb-109">0x0EA6</span><span class="sxs-lookup"><span data-stu-id="3bceb-109">0x0EA6</span></span>  <br/> |
|<span data-ttu-id="3bceb-110">Der Eigenschaftentyp:</span><span class="sxs-lookup"><span data-stu-id="3bceb-110">Property type:</span></span>  <br/> |<span data-ttu-id="3bceb-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3bceb-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3bceb-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="3bceb-112">Area:</span></span>  <br/> |<span data-ttu-id="3bceb-113">Suche</span><span class="sxs-lookup"><span data-stu-id="3bceb-113">Search</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="3bceb-114">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3bceb-114">Related resources</span></span>

> [!NOTE]
> <span data-ttu-id="3bceb-115">Diese MAPI-Einschränkung Tag verwendet, wenn Sie nach e-Mail-Adressen suchen oder Anzeigen von Namen, die die Nachricht gesendet wird, möglicherweise nicht in der herunterladbaren Headerdatei definiert werden, die Sie besitzen.</span><span class="sxs-lookup"><span data-stu-id="3bceb-115">This MAPI restriction tag, used when you search for email addresses or display names to which the message is sent, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="3bceb-116">Mit dem folgenden Wert dem Code hinzufügen: >`#define PR_SEARCH_RECIP_EMAIL_TO_W PROP_TAG(PT_UNICODE, 0x0EA6)`</span><span class="sxs-lookup"><span data-stu-id="3bceb-116">You can add it to your code by using the following value: >  `#define PR_SEARCH_RECIP_EMAIL_TO_W PROP_TAG(PT_UNICODE, 0x0EA6)`</span></span>
  
### <a name="protocol-specifications"></a><span data-ttu-id="3bceb-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="3bceb-117">Protocol specifications</span></span>

<span data-ttu-id="3bceb-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3bceb-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3bceb-119">Bietet Verweise auf Verwandte Spezifikationen von Microsoft Exchange Server-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="3bceb-119">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3bceb-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3bceb-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3bceb-121">Gibt die Eigenschaften und Operationen für das Bearbeiten der Liste einer Suchkonfiguration-Ordner.</span><span class="sxs-lookup"><span data-stu-id="3bceb-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3bceb-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="3bceb-122">Header files</span></span>

<span data-ttu-id="3bceb-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3bceb-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="3bceb-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="3bceb-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="3bceb-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3bceb-125">Mapitags.h</span></span>
  
> <span data-ttu-id="3bceb-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3bceb-126">Contains definitions of properties that are listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3bceb-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3bceb-127">See also</span></span>



[<span data-ttu-id="3bceb-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3bceb-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3bceb-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3bceb-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3bceb-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="3bceb-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3bceb-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="3bceb-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

