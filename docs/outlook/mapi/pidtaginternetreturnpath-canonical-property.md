---
title: PidTagInternetReturnPath (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInternetReturnPath
api_type:
- HeaderDef
ms.assetid: 4530dbcf-9436-4f29-b79e-1bb0f791f60b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: aa8a683c0033682aa46944c5cc78503dc1a7d729
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794502"
---
# <a name="pidtaginternetreturnpath-canonical-property"></a><span data-ttu-id="983f5-103">PidTagInternetReturnPath (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="983f5-103">PidTagInternetReturnPath Canonical Property</span></span>

  
  
<span data-ttu-id="983f5-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="983f5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="983f5-105">Enthält den Wert der Rückgabe-Path-Header ein Feld einer Nachricht Multipurpose Internet Mail Extensions (MIME).</span><span class="sxs-lookup"><span data-stu-id="983f5-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's Return-Path header field.</span></span> <span data-ttu-id="983f5-106">Die e-Mail-Adresse des Absenders der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="983f5-106">The email address of the message's sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="983f5-107">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="983f5-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="983f5-108">PR_INTERNET_RETURN_PATH, PR_INTERNET_RETURN_PATH_A, PR_INTERNET_RETURN_PATH_W</span><span class="sxs-lookup"><span data-stu-id="983f5-108">PR_INTERNET_RETURN_PATH, PR_INTERNET_RETURN_PATH_A, PR_INTERNET_RETURN_PATH_W</span></span>  <br/> |
|<span data-ttu-id="983f5-109">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="983f5-109">Identifier:</span></span>  <br/> |<span data-ttu-id="983f5-110">0x1046</span><span class="sxs-lookup"><span data-stu-id="983f5-110">0x1046</span></span>  <br/> |
|<span data-ttu-id="983f5-111">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="983f5-111">Data type:</span></span>  <br/> |<span data-ttu-id="983f5-112">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="983f5-112">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="983f5-113">Bereich:</span><span class="sxs-lookup"><span data-stu-id="983f5-113">Area:</span></span>  <br/> |<span data-ttu-id="983f5-114">MIME</span><span class="sxs-lookup"><span data-stu-id="983f5-114">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="983f5-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="983f5-115">Remarks</span></span>

<span data-ttu-id="983f5-116">Um den Wert dieser Eigenschaft abzurufen, zunächst mit dem [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) um das Eigenschafts-Tag zu erhalten, und geben Sie in [IMAPIProp::GetProps](imapiprop-getprops.md) zum Abrufen des Werts dieser Eigenschaftentag.</span><span class="sxs-lookup"><span data-stu-id="983f5-116">To retrieve the value of this property, first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="983f5-117">Beim Aufruf von [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), geben Sie die folgenden Werte für die [MAPINAMEID](mapinameid.md) -Struktur an, das Eingabeparameter _LppPropNames_auf zeigt:</span><span class="sxs-lookup"><span data-stu-id="983f5-117">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="983f5-118">x LpGuid:</span><span class="sxs-lookup"><span data-stu-id="983f5-118">lpGuid:</span></span>  <br/> |<span data-ttu-id="983f5-119">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="983f5-119">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="983f5-120">UlKind:</span><span class="sxs-lookup"><span data-stu-id="983f5-120">ulKind:</span></span>  <br/> |<span data-ttu-id="983f5-121">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="983f5-121">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="983f5-122">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="983f5-122">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="983f5-123">L "Return-Pfad"</span><span class="sxs-lookup"><span data-stu-id="983f5-123">L"return-path"</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="983f5-124">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="983f5-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="983f5-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="983f5-125">Protocol specifications</span></span>

<span data-ttu-id="983f5-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="983f5-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="983f5-127">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="983f5-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="983f5-128">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="983f5-128">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="983f5-129">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="983f5-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="983f5-130">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="983f5-130">Header files</span></span>

<span data-ttu-id="983f5-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="983f5-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="983f5-132">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="983f5-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="983f5-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="983f5-133">Mapitags.h</span></span>
  
> <span data-ttu-id="983f5-134">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="983f5-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="983f5-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="983f5-135">See also</span></span>



[<span data-ttu-id="983f5-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="983f5-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="983f5-137">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="983f5-137">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="983f5-138">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="983f5-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="983f5-139">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="983f5-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="983f5-140">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="983f5-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

