---
title: Kanonische PidTagAddressType-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAddressType
api_type:
- HeaderDef
ms.assetid: 986719d2-8837-46b4-8d04-c24508f5e19a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5398519dc841aa72f2c2655aac6c9f7acba7f335
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794069"
---
# <a name="pidtagaddresstype-canonical-property"></a><span data-ttu-id="30375-103">Kanonische PidTagAddressType-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="30375-103">PidTagAddressType Canonical Property</span></span>

<span data-ttu-id="30375-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="30375-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="30375-105">Enthält die messaging-Benutzer e-Mail-Adresstyp wie SMTP.</span><span class="sxs-lookup"><span data-stu-id="30375-105">Contains the messaging user's email address type, such as SMTP.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="30375-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="30375-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="30375-107">PR_ADDRTYPE, PR_ADDRTYPE_A, PR_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="30375-107">PR_ADDRTYPE, PR_ADDRTYPE_A, PR_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="30375-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="30375-108">Identifier:</span></span>  <br/> |<span data-ttu-id="30375-109">0x3002</span><span class="sxs-lookup"><span data-stu-id="30375-109">0x3002</span></span>  <br/> |
|<span data-ttu-id="30375-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="30375-110">Data type:</span></span>  <br/> |<span data-ttu-id="30375-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="30375-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="30375-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="30375-112">Area:</span></span>  <br/> |<span data-ttu-id="30375-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="30375-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30375-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="30375-114">Remarks</span></span>

<span data-ttu-id="30375-115">Diese Eigenschaften sind Beispiele für allgemeine Eigenschaften Basisadresse an alle messaging-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="30375-115">These properties are examples of the base address properties common to all messaging users.</span></span> <span data-ttu-id="30375-116">Es gibt an, welche messaging MAPI verwendet, um eine bestimmte Nachricht zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="30375-116">It specifies which messaging system MAPI uses to handle a given message.</span></span>
  
<span data-ttu-id="30375-117">Diese Eigenschaft bestimmt auch das Format der Adresszeichenfolge in der **PR_EMAIL_ADRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="30375-117">This property also determines the format of the address string in the **PR_EMAIL_ADRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)).</span></span> <span data-ttu-id="30375-118">Die kann Zeichenfolge Softwareentwicklern nur die Großbuchstaben a bis Z und Zahlen von 0 bis 9 enthalten.</span><span class="sxs-lookup"><span data-stu-id="30375-118">The string it provides can contain only the uppercase alphabetic characters from A through Z and the numbers from 0 through 9.</span></span>
  
<span data-ttu-id="30375-119">Gültige Beispiele für die Zeichenfolge können:</span><span class="sxs-lookup"><span data-stu-id="30375-119">Valid examples for the string include:</span></span> 
  
```cpp
FAX
MHS
PROFS
SMTP
X400

```

## <a name="related-resources"></a><span data-ttu-id="30375-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="30375-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="30375-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="30375-121">Protocol specifications</span></span>

<span data-ttu-id="30375-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30375-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30375-123">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="30375-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="30375-124">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30375-124">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30375-125">Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="30375-125">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="30375-126">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30375-126">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30375-127">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="30375-127">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="30375-128">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30375-128">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30375-129">Verarbeitet ein Client-Kommunikation mit einem Server (NSPI = Name Service Provider Interface).</span><span class="sxs-lookup"><span data-stu-id="30375-129">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
<span data-ttu-id="30375-130">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30375-130">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30375-131">Definiert die grundlegende Datenstrukturen, die verwendet werden remote-Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="30375-131">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="30375-132">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30375-132">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30375-133">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="30375-133">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="30375-134">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30375-134">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30375-135">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="30375-135">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="30375-136">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30375-136">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30375-137">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="30375-137">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="30375-138">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30375-138">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30375-139">Gibt die zulässige Vorgänge für die Hauptobjekte der Nachricht Store.</span><span class="sxs-lookup"><span data-stu-id="30375-139">Specifies permissible operations for the core message store objects.</span></span>
    
<span data-ttu-id="30375-140">[[MS-OXOABKT]](http://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30375-140">[[MS-OXOABKT]](http://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30375-141">Gibt die Eigenschaften und Operationen, die für Address Book Vorlagen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="30375-141">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
<span data-ttu-id="30375-142">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30375-142">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30375-143">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="30375-143">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="30375-144">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30375-144">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30375-145">Eingehende e-Mail-Nachrichten auf einem Server bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="30375-145">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="30375-146">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30375-146">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30375-147">Gibt die Eigenschaften und Operationen für das Bearbeiten der Liste einer Suchkonfiguration-Ordner.</span><span class="sxs-lookup"><span data-stu-id="30375-147">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="30375-148">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="30375-148">Header files</span></span>

<span data-ttu-id="30375-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="30375-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="30375-150">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="30375-150">Provides data type definitions.</span></span>
    
<span data-ttu-id="30375-151">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="30375-151">Mapitags.h</span></span>
  
> <span data-ttu-id="30375-152">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="30375-152">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="30375-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30375-153">See also</span></span>



[<span data-ttu-id="30375-154">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="30375-154">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="30375-155">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="30375-155">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="30375-156">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="30375-156">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="30375-157">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="30375-157">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
  
[<span data-ttu-id="30375-158">MAPI-Adresstypen</span><span class="sxs-lookup"><span data-stu-id="30375-158">MAPI Address Types</span></span>](mapi-address-types.md)

