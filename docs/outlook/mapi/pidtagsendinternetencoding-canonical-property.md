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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342672"
---
# <a name="pidtagsendinternetencoding-canonical-property"></a><span data-ttu-id="f5e53-103">PidTagSendInternetEncoding (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f5e53-103">PidTagSendInternetEncoding Canonical Property</span></span>

  
  
<span data-ttu-id="f5e53-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5e53-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5e53-105">Enthält eine Bitmaske mit Codierungseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="f5e53-105">Contains a bitmask of encoding preferences.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f5e53-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f5e53-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f5e53-107">PR_SEND_INTERNET_ENCODING</span><span class="sxs-lookup"><span data-stu-id="f5e53-107">PR_SEND_INTERNET_ENCODING</span></span>  <br/> |
|<span data-ttu-id="f5e53-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="f5e53-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f5e53-109">0x3A71</span><span class="sxs-lookup"><span data-stu-id="f5e53-109">0x3A71</span></span>  <br/> |
|<span data-ttu-id="f5e53-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f5e53-110">Data type:</span></span>  <br/> |<span data-ttu-id="f5e53-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f5e53-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f5e53-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f5e53-112">Area:</span></span>  <br/> |<span data-ttu-id="f5e53-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="f5e53-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5e53-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f5e53-114">Remarks</span></span>

<span data-ttu-id="f5e53-115">Legen Sie diese Eigenschaft so ein, dass die verwendeten Codierungsoptionen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f5e53-115">Set this property to indicate the encoding options used.</span></span> 
  
<span data-ttu-id="f5e53-116">Diese Eigenschaft enthält die folgenden Flags:</span><span class="sxs-lookup"><span data-stu-id="f5e53-116">This property contains the following flags:</span></span>
  
<span data-ttu-id="f5e53-117">BODY_ENCODING_HTML</span><span class="sxs-lookup"><span data-stu-id="f5e53-117">BODY_ENCODING_HTML</span></span> 
  
> <span data-ttu-id="f5e53-118">Codieren Sie den Nachrichtentext in HTML.</span><span class="sxs-lookup"><span data-stu-id="f5e53-118">Encode the message text in HTML.</span></span> <span data-ttu-id="f5e53-119">Dieses Flag wird ignoriert, es sei denn, ENCODING_MIME festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f5e53-119">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="f5e53-120">BODY_ENCODING_TEXT_AND_HTML</span><span class="sxs-lookup"><span data-stu-id="f5e53-120">BODY_ENCODING_TEXT_AND_HTML</span></span> 
  
> <span data-ttu-id="f5e53-121">Codieren Sie den Nachrichtentext mithilfe von Text und HTML als mehrteilige Multipartalternativen (Multipurpose Internet Mail Extensions, MIME).</span><span class="sxs-lookup"><span data-stu-id="f5e53-121">Encode the message text using text and HTML as Multipurpose Internet Mail Extensions (MIME) multipart alternatives.</span></span> <span data-ttu-id="f5e53-122">Dieses Flag wird ignoriert, es sei denn, ENCODING_MIME festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f5e53-122">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="f5e53-123">ENCODING_MIME</span><span class="sxs-lookup"><span data-stu-id="f5e53-123">ENCODING_MIME</span></span> 
  
> <span data-ttu-id="f5e53-124">Codieren Sie die Nachricht mithilfe von MIME.</span><span class="sxs-lookup"><span data-stu-id="f5e53-124">Encode the message using MIME.</span></span> <span data-ttu-id="f5e53-125">Wenn dieses Flag nicht festgelegt ist, codiert MAPI den Nachrichtentext in Nur-Text und die Anlagen in UUENCODE.</span><span class="sxs-lookup"><span data-stu-id="f5e53-125">If this flag is not set, MAPI encodes the message text in plain text and the attachments in UUENCODE.</span></span> 
    
<span data-ttu-id="f5e53-126">ENCODING_PREFERENCE</span><span class="sxs-lookup"><span data-stu-id="f5e53-126">ENCODING_PREFERENCE</span></span> 
  
> <span data-ttu-id="f5e53-127">Verwenden Sie die anderen Flags in dieser Bitmaske, um die Codierung zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="f5e53-127">Use the other flags in this bitmask to determine the encoding.</span></span> <span data-ttu-id="f5e53-128">Wenn dieses Flag nicht festgelegt ist, überlässt MAPI es dem Messagingsystem, Codierungsentscheidungen zu treffen.</span><span class="sxs-lookup"><span data-stu-id="f5e53-128">If this flag is not set, MAPI leaves it to the messaging system to make encoding decisions.</span></span> 
    
<span data-ttu-id="f5e53-129">MAC_ATTACH_ENCODING_APPLEDOUBLE</span><span class="sxs-lookup"><span data-stu-id="f5e53-129">MAC_ATTACH_ENCODING_APPLEDOUBLE</span></span> 
  
> <span data-ttu-id="f5e53-130">Codieren Sie Macintosh-Anlagen im Apple-Doppelmodus.</span><span class="sxs-lookup"><span data-stu-id="f5e53-130">Encode Macintosh attachments in Apple double mode.</span></span> <span data-ttu-id="f5e53-131">Dieses Flag wird ignoriert, es sei denn, ENCODING_MIME festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f5e53-131">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="f5e53-132">MAC_ATTACH_ENCODING_APPLESINGLE</span><span class="sxs-lookup"><span data-stu-id="f5e53-132">MAC_ATTACH_ENCODING_APPLESINGLE</span></span> 
  
> <span data-ttu-id="f5e53-133">Codieren Sie Macintosh-Anlagen im Apple-Einzelmodus.</span><span class="sxs-lookup"><span data-stu-id="f5e53-133">Encode Macintosh attachments in Apple single mode.</span></span> <span data-ttu-id="f5e53-134">Dieses Flag wird ignoriert, es sei denn, ENCODING_MIME festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f5e53-134">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="f5e53-135">MAC_ATTACH_ENCODING_UUENCODE</span><span class="sxs-lookup"><span data-stu-id="f5e53-135">MAC_ATTACH_ENCODING_UUENCODE</span></span> 
  
> <span data-ttu-id="f5e53-136">Codieren Sie Macintosh-Anlagen in UUENCODE.</span><span class="sxs-lookup"><span data-stu-id="f5e53-136">Encode Macintosh attachments in UUENCODE.</span></span> <span data-ttu-id="f5e53-137">Wenn das ENCODING_MIME festgelegt ist, wird dieses Flag ignoriert, und stattdessen wird die BinHex-Codierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="f5e53-137">If the ENCODING_MIME flag is set, this flag is ignored and BinHex encoding is used instead.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="f5e53-138">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f5e53-138">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f5e53-139">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="f5e53-139">Protocol specifications</span></span>

<span data-ttu-id="f5e53-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5e53-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5e53-141">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="f5e53-141">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f5e53-142">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5e53-142">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5e53-143">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="f5e53-143">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="f5e53-144">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5e53-144">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5e53-145">Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="f5e53-145">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="f5e53-146">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5e53-146">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5e53-147">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="f5e53-147">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="f5e53-148">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5e53-148">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5e53-149">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="f5e53-149">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f5e53-150">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="f5e53-150">Header files</span></span>

<span data-ttu-id="f5e53-151">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f5e53-151">Mapidefs.h</span></span>
  
> <span data-ttu-id="f5e53-152">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f5e53-152">Provides data type definitions.</span></span>
    
<span data-ttu-id="f5e53-153">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f5e53-153">Mapitags.h</span></span>
  
> <span data-ttu-id="f5e53-154">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="f5e53-154">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f5e53-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5e53-155">See also</span></span>



[<span data-ttu-id="f5e53-156">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f5e53-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f5e53-157">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="f5e53-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f5e53-158">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f5e53-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f5e53-159">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f5e53-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

