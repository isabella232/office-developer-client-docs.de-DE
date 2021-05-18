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
ms.openlocfilehash: c2d8eaf627f789c3e862a83d71e4ca2e3e55e1e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327958"
---
# <a name="pidtaginternetreturnpath-canonical-property"></a><span data-ttu-id="b150a-103">PidTagInternetReturnPath (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b150a-103">PidTagInternetReturnPath Canonical Property</span></span>

  
  
<span data-ttu-id="b150a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b150a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b150a-105">Enthält den Wert einer MIME-Nachricht (Multipurpose Internet Mail Extensions) Return-Path Kopfzeilenfeld.</span><span class="sxs-lookup"><span data-stu-id="b150a-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's Return-Path header field.</span></span> <span data-ttu-id="b150a-106">Die E-Mail-Adresse des Absenders der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="b150a-106">The email address of the message's sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b150a-107">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b150a-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="b150a-108">PR_INTERNET_RETURN_PATH, PR_INTERNET_RETURN_PATH_A, PR_INTERNET_RETURN_PATH_W</span><span class="sxs-lookup"><span data-stu-id="b150a-108">PR_INTERNET_RETURN_PATH, PR_INTERNET_RETURN_PATH_A, PR_INTERNET_RETURN_PATH_W</span></span>  <br/> |
|<span data-ttu-id="b150a-109">Kennung:</span><span class="sxs-lookup"><span data-stu-id="b150a-109">Identifier:</span></span>  <br/> |<span data-ttu-id="b150a-110">0x1046</span><span class="sxs-lookup"><span data-stu-id="b150a-110">0x1046</span></span>  <br/> |
|<span data-ttu-id="b150a-111">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b150a-111">Data type:</span></span>  <br/> |<span data-ttu-id="b150a-112">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b150a-112">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b150a-113">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b150a-113">Area:</span></span>  <br/> |<span data-ttu-id="b150a-114">MIME</span><span class="sxs-lookup"><span data-stu-id="b150a-114">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b150a-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b150a-115">Remarks</span></span>

<span data-ttu-id="b150a-116">Um den Wert dieser Eigenschaft abzurufen, verwenden Sie zunächst [IMAPIProp::GetIDsFromNames,](imapiprop-getidsfromnames.md) um das Eigenschaftstag abzurufen, und geben Sie dann dieses Eigenschaftstag in [IMAPIProp::GetProps](imapiprop-getprops.md) an, um den Wert abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b150a-116">To retrieve the value of this property, first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="b150a-117">Geben Sie beim Aufrufen von [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)die folgenden Werte für die [MAPINAMEID-Struktur](mapinameid.md) an, auf die der Eingabeparameter _lppPropNames verweist:_</span><span class="sxs-lookup"><span data-stu-id="b150a-117">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b150a-118">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="b150a-118">lpGuid:</span></span>  <br/> |<span data-ttu-id="b150a-119">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="b150a-119">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="b150a-120">ulKind:</span><span class="sxs-lookup"><span data-stu-id="b150a-120">ulKind:</span></span>  <br/> |<span data-ttu-id="b150a-121">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="b150a-121">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="b150a-122">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="b150a-122">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="b150a-123">L"return-path"</span><span class="sxs-lookup"><span data-stu-id="b150a-123">L"return-path"</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b150a-124">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b150a-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b150a-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b150a-125">Protocol specifications</span></span>

<span data-ttu-id="b150a-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b150a-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b150a-127">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="b150a-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b150a-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b150a-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b150a-129">Konvertiert zwischen IETF RFC2445, RFC2446 und RFC2447 sowie Termin- und Besprechungsobjekten.</span><span class="sxs-lookup"><span data-stu-id="b150a-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b150a-130">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="b150a-130">Header files</span></span>

<span data-ttu-id="b150a-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b150a-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="b150a-132">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="b150a-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="b150a-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b150a-133">Mapitags.h</span></span>
  
> <span data-ttu-id="b150a-134">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b150a-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b150a-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b150a-135">See also</span></span>



[<span data-ttu-id="b150a-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b150a-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b150a-137">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="b150a-137">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="b150a-138">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="b150a-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b150a-139">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b150a-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b150a-140">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b150a-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

