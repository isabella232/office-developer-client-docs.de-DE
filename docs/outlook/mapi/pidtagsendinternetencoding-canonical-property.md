---
title: Kanonische Pidtagsendinternetencoding (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e157fa640026d13362084b30ad73cdb66a0b35b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342672"
---
# <a name="pidtagsendinternetencoding-canonical-property"></a><span data-ttu-id="f07ba-103">Kanonische Pidtagsendinternetencoding (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f07ba-103">PidTagSendInternetEncoding Canonical Property</span></span>

  
  
<span data-ttu-id="f07ba-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f07ba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f07ba-105">Enthält eine Bitmaske der Codierungseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="f07ba-105">Contains a bitmask of encoding preferences.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f07ba-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f07ba-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f07ba-107">PR_SEND_INTERNET_ENCODING</span><span class="sxs-lookup"><span data-stu-id="f07ba-107">PR_SEND_INTERNET_ENCODING</span></span>  <br/> |
|<span data-ttu-id="f07ba-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="f07ba-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f07ba-109">0x3A71</span><span class="sxs-lookup"><span data-stu-id="f07ba-109">0x3A71</span></span>  <br/> |
|<span data-ttu-id="f07ba-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f07ba-110">Data type:</span></span>  <br/> |<span data-ttu-id="f07ba-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f07ba-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f07ba-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f07ba-112">Area:</span></span>  <br/> |<span data-ttu-id="f07ba-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="f07ba-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f07ba-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f07ba-114">Remarks</span></span>

<span data-ttu-id="f07ba-115">Legen Sie diese Eigenschaft fest, um die verwendeten Codierungsoptionen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f07ba-115">Set this property to indicate the encoding options used.</span></span> 
  
<span data-ttu-id="f07ba-116">Diese Eigenschaft enthält die folgenden Flags:</span><span class="sxs-lookup"><span data-stu-id="f07ba-116">This property contains the following flags:</span></span>
  
<span data-ttu-id="f07ba-117">BODY_ENCODING_HTML</span><span class="sxs-lookup"><span data-stu-id="f07ba-117">BODY_ENCODING_HTML</span></span> 
  
> <span data-ttu-id="f07ba-118">Codieren Sie den Nachrichtentext in HTML.</span><span class="sxs-lookup"><span data-stu-id="f07ba-118">Encode the message text in HTML.</span></span> <span data-ttu-id="f07ba-119">Dieses Flag wird ignoriert, es sei denn, das ENCODING_MIME-Flag festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f07ba-119">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="f07ba-120">BODY_ENCODING_TEXT_AND_HTML</span><span class="sxs-lookup"><span data-stu-id="f07ba-120">BODY_ENCODING_TEXT_AND_HTML</span></span> 
  
> <span data-ttu-id="f07ba-121">Codieren Sie den Nachrichtentext mit Text und HTML als MIME-Multipart-Alternativen (Multipurpose Internet Mail Extensions).</span><span class="sxs-lookup"><span data-stu-id="f07ba-121">Encode the message text using text and HTML as Multipurpose Internet Mail Extensions (MIME) multipart alternatives.</span></span> <span data-ttu-id="f07ba-122">Dieses Flag wird ignoriert, es sei denn, das ENCODING_MIME-Flag festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f07ba-122">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="f07ba-123">ENCODING_MIME</span><span class="sxs-lookup"><span data-stu-id="f07ba-123">ENCODING_MIME</span></span> 
  
> <span data-ttu-id="f07ba-124">Codieren Sie die Nachricht mit MIME.</span><span class="sxs-lookup"><span data-stu-id="f07ba-124">Encode the message using MIME.</span></span> <span data-ttu-id="f07ba-125">Wenn dieses Flag nicht festgelegt ist, codiert MAPI den Nachrichtentext in nur-Text und die Anlagen in UUENCODE.</span><span class="sxs-lookup"><span data-stu-id="f07ba-125">If this flag is not set, MAPI encodes the message text in plain text and the attachments in UUENCODE.</span></span> 
    
<span data-ttu-id="f07ba-126">ENCODING_PREFERENCE</span><span class="sxs-lookup"><span data-stu-id="f07ba-126">ENCODING_PREFERENCE</span></span> 
  
> <span data-ttu-id="f07ba-127">Verwenden Sie die anderen Flags in dieser Bitmaske, um die Codierung zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="f07ba-127">Use the other flags in this bitmask to determine the encoding.</span></span> <span data-ttu-id="f07ba-128">Wenn dieses Flag nicht festgelegt ist, überlässt MAPI es dem Messagingsystem, um Codierungs Entscheidungen zu treffen.</span><span class="sxs-lookup"><span data-stu-id="f07ba-128">If this flag is not set, MAPI leaves it to the messaging system to make encoding decisions.</span></span> 
    
<span data-ttu-id="f07ba-129">MAC_ATTACH_ENCODING_APPLEDOUBLE</span><span class="sxs-lookup"><span data-stu-id="f07ba-129">MAC_ATTACH_ENCODING_APPLEDOUBLE</span></span> 
  
> <span data-ttu-id="f07ba-130">Codieren von Macintosh-Anlagen im Apple Double-Modus.</span><span class="sxs-lookup"><span data-stu-id="f07ba-130">Encode Macintosh attachments in Apple double mode.</span></span> <span data-ttu-id="f07ba-131">Dieses Flag wird ignoriert, es sei denn, das ENCODING_MIME-Flag festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f07ba-131">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="f07ba-132">MAC_ATTACH_ENCODING_APPLESINGLE</span><span class="sxs-lookup"><span data-stu-id="f07ba-132">MAC_ATTACH_ENCODING_APPLESINGLE</span></span> 
  
> <span data-ttu-id="f07ba-133">Codieren von Macintosh-Anlagen im Apple Singlemode.</span><span class="sxs-lookup"><span data-stu-id="f07ba-133">Encode Macintosh attachments in Apple single mode.</span></span> <span data-ttu-id="f07ba-134">Dieses Flag wird ignoriert, es sei denn, das ENCODING_MIME-Flag festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f07ba-134">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="f07ba-135">MAC_ATTACH_ENCODING_UUENCODE</span><span class="sxs-lookup"><span data-stu-id="f07ba-135">MAC_ATTACH_ENCODING_UUENCODE</span></span> 
  
> <span data-ttu-id="f07ba-136">Codieren von Macintosh-Anlagen in UUENCODE.</span><span class="sxs-lookup"><span data-stu-id="f07ba-136">Encode Macintosh attachments in UUENCODE.</span></span> <span data-ttu-id="f07ba-137">Wenn das ENCODING_MIME-Flag festgelegt ist, wird dieses Flag ignoriert, und stattdessen wird die BinHex-Codierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="f07ba-137">If the ENCODING_MIME flag is set, this flag is ignored and BinHex encoding is used instead.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="f07ba-138">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f07ba-138">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f07ba-139">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="f07ba-139">Protocol specifications</span></span>

<span data-ttu-id="f07ba-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f07ba-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f07ba-141">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="f07ba-141">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f07ba-142">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f07ba-142">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f07ba-143">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="f07ba-143">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="f07ba-144">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f07ba-144">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f07ba-145">Konvertiert von Internet Standard-e-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="f07ba-145">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="f07ba-146">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f07ba-146">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f07ba-147">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="f07ba-147">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="f07ba-148">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f07ba-148">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f07ba-149">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="f07ba-149">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f07ba-150">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="f07ba-150">Header files</span></span>

<span data-ttu-id="f07ba-151">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f07ba-151">Mapidefs.h</span></span>
  
> <span data-ttu-id="f07ba-152">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="f07ba-152">Provides data type definitions.</span></span>
    
<span data-ttu-id="f07ba-153">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="f07ba-153">Mapitags.h</span></span>
  
> <span data-ttu-id="f07ba-154">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="f07ba-154">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f07ba-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f07ba-155">See also</span></span>



[<span data-ttu-id="f07ba-156">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f07ba-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f07ba-157">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f07ba-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f07ba-158">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f07ba-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f07ba-159">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f07ba-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

