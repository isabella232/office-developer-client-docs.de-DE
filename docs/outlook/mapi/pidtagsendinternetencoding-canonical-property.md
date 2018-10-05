---
title: PidTagSendInternetEncoding (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSendInternetEncoding
api_type:
- COM
ms.assetid: ae408b4f-dee3-484b-a19c-f472cfa95996
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e157fa640026d13362084b30ad73cdb66a0b35b5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392568"
---
# <a name="pidtagsendinternetencoding-canonical-property"></a><span data-ttu-id="11881-103">PidTagSendInternetEncoding (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="11881-103">PidTagSendInternetEncoding Canonical Property</span></span>

  
  
<span data-ttu-id="11881-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11881-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11881-105">Enthält eine Bitmaske der Voreinstellungen-Codierung.</span><span class="sxs-lookup"><span data-stu-id="11881-105">Contains a bitmask of encoding preferences.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="11881-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="11881-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="11881-107">PR_SEND_INTERNET_ENCODING</span><span class="sxs-lookup"><span data-stu-id="11881-107">PR_SEND_INTERNET_ENCODING</span></span>  <br/> |
|<span data-ttu-id="11881-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="11881-108">Identifier:</span></span>  <br/> |<span data-ttu-id="11881-109">0x3A71</span><span class="sxs-lookup"><span data-stu-id="11881-109">0x3A71</span></span>  <br/> |
|<span data-ttu-id="11881-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="11881-110">Data type:</span></span>  <br/> |<span data-ttu-id="11881-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="11881-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="11881-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="11881-112">Area:</span></span>  <br/> |<span data-ttu-id="11881-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="11881-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="11881-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="11881-114">Remarks</span></span>

<span data-ttu-id="11881-115">Legen Sie diese Eigenschaft an, dass die Codierungsoptionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="11881-115">Set this property to indicate the encoding options used.</span></span> 
  
<span data-ttu-id="11881-116">Diese Eigenschaft enthält die folgenden Kennzeichen:</span><span class="sxs-lookup"><span data-stu-id="11881-116">This property contains the following flags:</span></span>
  
<span data-ttu-id="11881-117">BODY_ENCODING_HTML</span><span class="sxs-lookup"><span data-stu-id="11881-117">BODY_ENCODING_HTML</span></span> 
  
> <span data-ttu-id="11881-118">Codieren Sie den Nachrichtentext im HTML-Format.</span><span class="sxs-lookup"><span data-stu-id="11881-118">Encode the message text in HTML.</span></span> <span data-ttu-id="11881-119">Dieses Kennzeichen werden ignoriert, es sei denn, das Flag ENCODING_MIME festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="11881-119">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="11881-120">BODY_ENCODING_TEXT_AND_HTML</span><span class="sxs-lookup"><span data-stu-id="11881-120">BODY_ENCODING_TEXT_AND_HTML</span></span> 
  
> <span data-ttu-id="11881-121">Codieren Sie den Nachrichtentext mit Text und HTML als mehrteiligen alternativen Multipurpose Internet Mail Extensions (MIME).</span><span class="sxs-lookup"><span data-stu-id="11881-121">Encode the message text using text and HTML as Multipurpose Internet Mail Extensions (MIME) multipart alternatives.</span></span> <span data-ttu-id="11881-122">Dieses Kennzeichen werden ignoriert, es sei denn, das Flag ENCODING_MIME festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="11881-122">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="11881-123">ENCODING_MIME</span><span class="sxs-lookup"><span data-stu-id="11881-123">ENCODING_MIME</span></span> 
  
> <span data-ttu-id="11881-124">Codieren Sie die Nachricht mithilfe von MIME.</span><span class="sxs-lookup"><span data-stu-id="11881-124">Encode the message using MIME.</span></span> <span data-ttu-id="11881-125">Wenn dieses Flag nicht festgelegt ist, werden MAPI den Nachrichtentext in nur-Text und die Anlagen in UUENCODE codiert.</span><span class="sxs-lookup"><span data-stu-id="11881-125">If this flag is not set, MAPI encodes the message text in plain text and the attachments in UUENCODE.</span></span> 
    
<span data-ttu-id="11881-126">ENCODING_PREFERENCE</span><span class="sxs-lookup"><span data-stu-id="11881-126">ENCODING_PREFERENCE</span></span> 
  
> <span data-ttu-id="11881-127">Verwenden Sie die anderen Flags in dieser Bitmaske, um die Codierung zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="11881-127">Use the other flags in this bitmask to determine the encoding.</span></span> <span data-ttu-id="11881-128">Wenn dieses Flag nicht festgelegt ist, bleibt MAPI an die messaging-System Codierung Entscheidungen treffen.</span><span class="sxs-lookup"><span data-stu-id="11881-128">If this flag is not set, MAPI leaves it to the messaging system to make encoding decisions.</span></span> 
    
<span data-ttu-id="11881-129">MAC_ATTACH_ENCODING_APPLEDOUBLE</span><span class="sxs-lookup"><span data-stu-id="11881-129">MAC_ATTACH_ENCODING_APPLEDOUBLE</span></span> 
  
> <span data-ttu-id="11881-130">Codieren von Anlagen in doppelte Modus Apple Macintosh.</span><span class="sxs-lookup"><span data-stu-id="11881-130">Encode Macintosh attachments in Apple double mode.</span></span> <span data-ttu-id="11881-131">Dieses Kennzeichen werden ignoriert, es sei denn, das Flag ENCODING_MIME festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="11881-131">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="11881-132">MAC_ATTACH_ENCODING_APPLESINGLE</span><span class="sxs-lookup"><span data-stu-id="11881-132">MAC_ATTACH_ENCODING_APPLESINGLE</span></span> 
  
> <span data-ttu-id="11881-133">Codieren von Anlagen in einzelnen Modus Apple Macintosh.</span><span class="sxs-lookup"><span data-stu-id="11881-133">Encode Macintosh attachments in Apple single mode.</span></span> <span data-ttu-id="11881-134">Dieses Kennzeichen werden ignoriert, es sei denn, das Flag ENCODING_MIME festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="11881-134">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="11881-135">MAC_ATTACH_ENCODING_UUENCODE</span><span class="sxs-lookup"><span data-stu-id="11881-135">MAC_ATTACH_ENCODING_UUENCODE</span></span> 
  
> <span data-ttu-id="11881-136">Codieren Sie Macintosh-Anlagen in UUENCODE.</span><span class="sxs-lookup"><span data-stu-id="11881-136">Encode Macintosh attachments in UUENCODE.</span></span> <span data-ttu-id="11881-137">Wenn das Flag ENCODING_MIME festgelegt ist, dieses Flag wird ignoriert, und wird stattdessen BinHex-Codierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="11881-137">If the ENCODING_MIME flag is set, this flag is ignored and BinHex encoding is used instead.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="11881-138">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="11881-138">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="11881-139">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="11881-139">Protocol specifications</span></span>

<span data-ttu-id="11881-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11881-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11881-141">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="11881-141">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="11881-142">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11881-142">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11881-143">Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="11881-143">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="11881-144">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11881-144">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11881-145">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="11881-145">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="11881-146">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11881-146">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11881-147">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="11881-147">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="11881-148">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11881-148">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11881-149">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="11881-149">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="11881-150">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="11881-150">Header files</span></span>

<span data-ttu-id="11881-151">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="11881-151">Mapidefs.h</span></span>
  
> <span data-ttu-id="11881-152">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="11881-152">Provides data type definitions.</span></span>
    
<span data-ttu-id="11881-153">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="11881-153">Mapitags.h</span></span>
  
> <span data-ttu-id="11881-154">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="11881-154">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="11881-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11881-155">See also</span></span>



[<span data-ttu-id="11881-156">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="11881-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="11881-157">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="11881-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="11881-158">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="11881-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="11881-159">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="11881-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

