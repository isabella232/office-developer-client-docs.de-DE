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
ms.openlocfilehash: d254df132db5542ce5235c1c3ab42ea768399f0a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382617"
---
# <a name="pidtagsearchrecipientemailto-canonical-property"></a><span data-ttu-id="24080-103">PidTagSearchRecipientEmailTo (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="24080-103">PidTagSearchRecipientEmailTo Canonical Property</span></span>

  
  
<span data-ttu-id="24080-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24080-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24080-105">Enthält eine Unicode-Zeichenfolge, die in der Liste der e-Mail-Adressen oder Anzeigenamen der Empfänger an, die in der Zeile **an** der Nachrichten im Store behandelt werden abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="24080-105">Contains a Unicode string that is being queried in the list of email addresses or display names of recipients that are addressed in the **To** line of messages on the store.</span></span> 
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="24080-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="24080-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="24080-107">PR_SEARCH_RECIP_EMAIL_TO_W</span><span class="sxs-lookup"><span data-stu-id="24080-107">PR_SEARCH_RECIP_EMAIL_TO_W</span></span>  <br/> |
|<span data-ttu-id="24080-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="24080-108">Identifier:</span></span>  <br/> |<span data-ttu-id="24080-109">0x0EA6</span><span class="sxs-lookup"><span data-stu-id="24080-109">0x0EA6</span></span>  <br/> |
|<span data-ttu-id="24080-110">Der Eigenschaftentyp:</span><span class="sxs-lookup"><span data-stu-id="24080-110">Property type:</span></span>  <br/> |<span data-ttu-id="24080-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="24080-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="24080-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="24080-112">Area:</span></span>  <br/> |<span data-ttu-id="24080-113">Suche</span><span class="sxs-lookup"><span data-stu-id="24080-113">Search</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="24080-114">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="24080-114">Related resources</span></span>

> [!NOTE]
> <span data-ttu-id="24080-115">Diese MAPI-Einschränkung Tag verwendet, wenn Sie nach e-Mail-Adressen suchen oder Anzeigen von Namen, die die Nachricht gesendet wird, möglicherweise nicht in der herunterladbaren Headerdatei definiert werden, die Sie besitzen.</span><span class="sxs-lookup"><span data-stu-id="24080-115">This MAPI restriction tag, used when you search for email addresses or display names to which the message is sent, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="24080-116">Mit dem folgenden Wert dem Code hinzufügen: >`#define PR_SEARCH_RECIP_EMAIL_TO_W PROP_TAG(PT_UNICODE, 0x0EA6)`</span><span class="sxs-lookup"><span data-stu-id="24080-116">You can add it to your code by using the following value: >  `#define PR_SEARCH_RECIP_EMAIL_TO_W PROP_TAG(PT_UNICODE, 0x0EA6)`</span></span>
  
### <a name="protocol-specifications"></a><span data-ttu-id="24080-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="24080-117">Protocol specifications</span></span>

<span data-ttu-id="24080-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="24080-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="24080-119">Bietet Verweise auf Verwandte Spezifikationen von Microsoft Exchange Server-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="24080-119">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="24080-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="24080-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="24080-121">Gibt die Eigenschaften und Operationen für das Bearbeiten der Liste einer Suchkonfiguration-Ordner.</span><span class="sxs-lookup"><span data-stu-id="24080-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="24080-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="24080-122">Header files</span></span>

<span data-ttu-id="24080-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="24080-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="24080-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="24080-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="24080-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="24080-125">Mapitags.h</span></span>
  
> <span data-ttu-id="24080-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="24080-126">Contains definitions of properties that are listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="24080-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24080-127">See also</span></span>



[<span data-ttu-id="24080-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="24080-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="24080-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="24080-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="24080-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="24080-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="24080-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="24080-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

