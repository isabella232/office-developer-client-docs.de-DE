---
title: PidTagObjectType (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagObjectType
api_type:
- HeaderDef
ms.assetid: 37da4ff5-300d-479f-a8b4-6fc36df997d9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b433db7cb157afbf8c3b506f2ed95b04b7b88564
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392933"
---
# <a name="pidtagobjecttype-canonical-property"></a><span data-ttu-id="18e2e-103">PidTagObjectType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="18e2e-103">PidTagObjectType Canonical Property</span></span>

  
  
<span data-ttu-id="18e2e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18e2e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18e2e-105">Enthält den Typ eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="18e2e-105">Contains the type of an object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="18e2e-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="18e2e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="18e2e-107">PR_OBJECT_TYPE</span><span class="sxs-lookup"><span data-stu-id="18e2e-107">PR_OBJECT_TYPE</span></span>  <br/> |
|<span data-ttu-id="18e2e-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="18e2e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="18e2e-109">0x0FFE</span><span class="sxs-lookup"><span data-stu-id="18e2e-109">0x0FFE</span></span>  <br/> |
|<span data-ttu-id="18e2e-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="18e2e-110">Data type:</span></span>  <br/> |<span data-ttu-id="18e2e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="18e2e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="18e2e-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="18e2e-112">Area:</span></span>  <br/> |<span data-ttu-id="18e2e-113">Common</span><span class="sxs-lookup"><span data-stu-id="18e2e-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18e2e-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="18e2e-114">Remarks</span></span>

<span data-ttu-id="18e2e-115">Der in dieser Eigenschaft enthaltenen Objekttyp entspricht die primäre Schnittstelle für ein Objekt kann über die Schnittstelle **OpenEntry** zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="18e2e-115">The object type contained in this property corresponds to the primary interface available for an object accessible through the **OpenEntry** interface.</span></span> <span data-ttu-id="18e2e-116">Es wird in der Regel durch consulting des _LpulObjType_ -Parameters der entsprechenden **OpenEntry** -Methode zurückgegebene abgerufen.</span><span class="sxs-lookup"><span data-stu-id="18e2e-116">It is usually obtained by consulting the  _lpulObjType_ parameter returned by the appropriate **OpenEntry** method.</span></span> <span data-ttu-id="18e2e-117">Wenn die Schnittstelle auf andere Weise abgerufen wird, rufen Sie [IMAPIProp::GetProps](imapiprop-getprops.md) , um den Wert für diese Eigenschaft zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="18e2e-117">When the interface is obtained in other ways, call [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the value for this property.</span></span> 
  
<span data-ttu-id="18e2e-118">Diese Eigenschaft kann genau einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="18e2e-118">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="18e2e-119">MAPI_ABCONT</span><span class="sxs-lookup"><span data-stu-id="18e2e-119">MAPI_ABCONT</span></span> 
  
> <span data-ttu-id="18e2e-120">Address Book Container-Objekt</span><span class="sxs-lookup"><span data-stu-id="18e2e-120">Address book container object</span></span> 
    
<span data-ttu-id="18e2e-121">MAPI_ADDRBOOK</span><span class="sxs-lookup"><span data-stu-id="18e2e-121">MAPI_ADDRBOOK</span></span> 
  
> <span data-ttu-id="18e2e-122">Address Book-Objekt</span><span class="sxs-lookup"><span data-stu-id="18e2e-122">Address book object</span></span> 
    
<span data-ttu-id="18e2e-123">MAPI_ATTACH</span><span class="sxs-lookup"><span data-stu-id="18e2e-123">MAPI_ATTACH</span></span> 
  
> <span data-ttu-id="18e2e-124">Nachricht Attachment-Objekt</span><span class="sxs-lookup"><span data-stu-id="18e2e-124">Message attachment object</span></span> 
    
<span data-ttu-id="18e2e-125">MAPI_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="18e2e-125">MAPI_DISTLIST</span></span> 
  
> <span data-ttu-id="18e2e-126">Verteilung List-Objekt</span><span class="sxs-lookup"><span data-stu-id="18e2e-126">Distribution list object</span></span> 
    
<span data-ttu-id="18e2e-127">MAPI_FOLDER</span><span class="sxs-lookup"><span data-stu-id="18e2e-127">MAPI_FOLDER</span></span> 
  
> <span data-ttu-id="18e2e-128">Folder-Objekt</span><span class="sxs-lookup"><span data-stu-id="18e2e-128">Folder object</span></span> 
    
<span data-ttu-id="18e2e-129">MAPI_FORMINFO</span><span class="sxs-lookup"><span data-stu-id="18e2e-129">MAPI_FORMINFO</span></span> 
  
> <span data-ttu-id="18e2e-130">Form-Objekt</span><span class="sxs-lookup"><span data-stu-id="18e2e-130">Form object</span></span> 
    
<span data-ttu-id="18e2e-131">MAPI_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="18e2e-131">MAPI_MAILUSER</span></span> 
  
> <span data-ttu-id="18e2e-132">Messaging-Benutzerobjekt</span><span class="sxs-lookup"><span data-stu-id="18e2e-132">Messaging user object</span></span> 
    
<span data-ttu-id="18e2e-133">MAPI_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="18e2e-133">MAPI_MESSAGE</span></span> 
  
> <span data-ttu-id="18e2e-134">Objekt Message</span><span class="sxs-lookup"><span data-stu-id="18e2e-134">Message object</span></span> 
    
<span data-ttu-id="18e2e-135">MAPI_PROFSECT</span><span class="sxs-lookup"><span data-stu-id="18e2e-135">MAPI_PROFSECT</span></span> 
  
> <span data-ttu-id="18e2e-136">Profil Section-Objekt</span><span class="sxs-lookup"><span data-stu-id="18e2e-136">Profile section object</span></span> 
    
<span data-ttu-id="18e2e-137">MAPI_SESSION</span><span class="sxs-lookup"><span data-stu-id="18e2e-137">MAPI_SESSION</span></span> 
  
> <span data-ttu-id="18e2e-138">Session-Objekt</span><span class="sxs-lookup"><span data-stu-id="18e2e-138">Session object</span></span> 
    
<span data-ttu-id="18e2e-139">MAPI_STATUS</span><span class="sxs-lookup"><span data-stu-id="18e2e-139">MAPI_STATUS</span></span> 
  
> <span data-ttu-id="18e2e-140">Statusobjekt</span><span class="sxs-lookup"><span data-stu-id="18e2e-140">Status object</span></span> 
    
<span data-ttu-id="18e2e-141">MAPI_STORE</span><span class="sxs-lookup"><span data-stu-id="18e2e-141">MAPI_STORE</span></span> 
  
> <span data-ttu-id="18e2e-142">Objekt "Message" store</span><span class="sxs-lookup"><span data-stu-id="18e2e-142">Message store object</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="18e2e-143">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="18e2e-143">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="18e2e-144">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="18e2e-144">Protocol specifications</span></span>

<span data-ttu-id="18e2e-145">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18e2e-145">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18e2e-146">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="18e2e-146">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="18e2e-147">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18e2e-147">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18e2e-148">Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="18e2e-148">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="18e2e-149">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18e2e-149">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18e2e-150">Verarbeitet ein Client-Kommunikation mit einem Server (NSPI = Name Service Provider Interface).</span><span class="sxs-lookup"><span data-stu-id="18e2e-150">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
<span data-ttu-id="18e2e-151">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18e2e-151">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18e2e-152">Ordner Vorgänge behandelt.</span><span class="sxs-lookup"><span data-stu-id="18e2e-152">Handles folder operations.</span></span>
    
<span data-ttu-id="18e2e-153">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18e2e-153">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18e2e-154">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="18e2e-154">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="18e2e-155">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18e2e-155">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18e2e-156">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="18e2e-156">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="18e2e-157">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18e2e-157">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18e2e-158">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="18e2e-158">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="18e2e-159">[[MS-OXOAB]](https://msdn.microsoft.com/library/b4750386-66ec-4e69-abb6-208dd131c7de%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18e2e-159">[[MS-OXOAB]](https://msdn.microsoft.com/library/b4750386-66ec-4e69-abb6-208dd131c7de%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18e2e-160">Gibt die Offlineadressbuch Offlineadressbuch (OAB)-Dateiformate für den lokalen Adresse Adressbuch Objektcache an.</span><span class="sxs-lookup"><span data-stu-id="18e2e-160">Specifies the offline address book (OAB) file formats for the local address book objects cache.</span></span>
    
<span data-ttu-id="18e2e-161">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18e2e-161">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18e2e-162">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="18e2e-162">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="18e2e-163">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18e2e-163">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18e2e-164">Gibt die Eigenschaften und Operationen für das Bearbeiten der Liste einer Suchkonfiguration-Ordner.</span><span class="sxs-lookup"><span data-stu-id="18e2e-164">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="18e2e-165">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="18e2e-165">Header files</span></span>

<span data-ttu-id="18e2e-166">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="18e2e-166">Mapidefs.h</span></span>
  
> <span data-ttu-id="18e2e-167">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="18e2e-167">Provides data type definitions.</span></span>
    
<span data-ttu-id="18e2e-168">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="18e2e-168">Mapitags.h</span></span>
  
> <span data-ttu-id="18e2e-169">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="18e2e-169">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="18e2e-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18e2e-170">See also</span></span>



[<span data-ttu-id="18e2e-171">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="18e2e-171">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="18e2e-172">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="18e2e-172">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="18e2e-173">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="18e2e-173">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="18e2e-174">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="18e2e-174">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

