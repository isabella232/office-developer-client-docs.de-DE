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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329225"
---
# <a name="pidtagobjecttype-canonical-property"></a><span data-ttu-id="47873-103">PidTagObjectType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="47873-103">PidTagObjectType Canonical Property</span></span>

  
  
<span data-ttu-id="47873-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47873-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47873-105">Enthält den Typ eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="47873-105">Contains the type of an object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="47873-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="47873-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="47873-107">PR_OBJECT_TYPE</span><span class="sxs-lookup"><span data-stu-id="47873-107">PR_OBJECT_TYPE</span></span>  <br/> |
|<span data-ttu-id="47873-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="47873-108">Identifier:</span></span>  <br/> |<span data-ttu-id="47873-109">0x0FFE</span><span class="sxs-lookup"><span data-stu-id="47873-109">0x0FFE</span></span>  <br/> |
|<span data-ttu-id="47873-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="47873-110">Data type:</span></span>  <br/> |<span data-ttu-id="47873-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="47873-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="47873-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="47873-112">Area:</span></span>  <br/> |<span data-ttu-id="47873-113">Standard</span><span class="sxs-lookup"><span data-stu-id="47873-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="47873-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="47873-114">Remarks</span></span>

<span data-ttu-id="47873-115">Der in dieser Eigenschaft enthaltene Objekttyp entspricht der primären Schnittstelle, die für ein Objekt verfügbar ist, auf das über die **OpenEntry-Schnittstelle zugegriffen werden** kann.</span><span class="sxs-lookup"><span data-stu-id="47873-115">The object type contained in this property corresponds to the primary interface available for an object accessible through the **OpenEntry** interface.</span></span> <span data-ttu-id="47873-116">Sie wird in der Regel durch Rücksprache mit dem  _lpulObjType-Parameter_ ermittelt, der von der entsprechenden **OpenEntry-Methode zurückgegeben** wird.</span><span class="sxs-lookup"><span data-stu-id="47873-116">It is usually obtained by consulting the  _lpulObjType_ parameter returned by the appropriate **OpenEntry** method.</span></span> <span data-ttu-id="47873-117">Wenn die Schnittstelle auf andere Weise erhalten wird, rufen [Sie IMAPIProp::GetProps](imapiprop-getprops.md) auf, um den Wert für diese Eigenschaft zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="47873-117">When the interface is obtained in other ways, call [IMAPIProp::GetProps](imapiprop-getprops.md) to obtain the value for this property.</span></span> 
  
<span data-ttu-id="47873-118">Diese Eigenschaft kann genau einen der folgenden Werte haben:</span><span class="sxs-lookup"><span data-stu-id="47873-118">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="47873-119">MAPI_ABCONT</span><span class="sxs-lookup"><span data-stu-id="47873-119">MAPI_ABCONT</span></span> 
  
> <span data-ttu-id="47873-120">Adressbuchcontainerobjekt</span><span class="sxs-lookup"><span data-stu-id="47873-120">Address book container object</span></span> 
    
<span data-ttu-id="47873-121">MAPI_ADDRBOOK</span><span class="sxs-lookup"><span data-stu-id="47873-121">MAPI_ADDRBOOK</span></span> 
  
> <span data-ttu-id="47873-122">Adressbuchobjekt</span><span class="sxs-lookup"><span data-stu-id="47873-122">Address book object</span></span> 
    
<span data-ttu-id="47873-123">MAPI_ATTACH</span><span class="sxs-lookup"><span data-stu-id="47873-123">MAPI_ATTACH</span></span> 
  
> <span data-ttu-id="47873-124">Message attachment-Objekt</span><span class="sxs-lookup"><span data-stu-id="47873-124">Message attachment object</span></span> 
    
<span data-ttu-id="47873-125">MAPI_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="47873-125">MAPI_DISTLIST</span></span> 
  
> <span data-ttu-id="47873-126">Verteilerlistenobjekt</span><span class="sxs-lookup"><span data-stu-id="47873-126">Distribution list object</span></span> 
    
<span data-ttu-id="47873-127">MAPI_FOLDER</span><span class="sxs-lookup"><span data-stu-id="47873-127">MAPI_FOLDER</span></span> 
  
> <span data-ttu-id="47873-128">Ordnerobjekt</span><span class="sxs-lookup"><span data-stu-id="47873-128">Folder object</span></span> 
    
<span data-ttu-id="47873-129">MAPI_FORMINFO</span><span class="sxs-lookup"><span data-stu-id="47873-129">MAPI_FORMINFO</span></span> 
  
> <span data-ttu-id="47873-130">Form-Objekt</span><span class="sxs-lookup"><span data-stu-id="47873-130">Form object</span></span> 
    
<span data-ttu-id="47873-131">MAPI_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="47873-131">MAPI_MAILUSER</span></span> 
  
> <span data-ttu-id="47873-132">Messagingbenutzerobjekt</span><span class="sxs-lookup"><span data-stu-id="47873-132">Messaging user object</span></span> 
    
<span data-ttu-id="47873-133">MAPI_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="47873-133">MAPI_MESSAGE</span></span> 
  
> <span data-ttu-id="47873-134">Objekt Message</span><span class="sxs-lookup"><span data-stu-id="47873-134">Message object</span></span> 
    
<span data-ttu-id="47873-135">MAPI_PROFSECT</span><span class="sxs-lookup"><span data-stu-id="47873-135">MAPI_PROFSECT</span></span> 
  
> <span data-ttu-id="47873-136">Profilabschnittsobjekt</span><span class="sxs-lookup"><span data-stu-id="47873-136">Profile section object</span></span> 
    
<span data-ttu-id="47873-137">MAPI_SESSION</span><span class="sxs-lookup"><span data-stu-id="47873-137">MAPI_SESSION</span></span> 
  
> <span data-ttu-id="47873-138">Session-Objekt</span><span class="sxs-lookup"><span data-stu-id="47873-138">Session object</span></span> 
    
<span data-ttu-id="47873-139">MAPI_STATUS</span><span class="sxs-lookup"><span data-stu-id="47873-139">MAPI_STATUS</span></span> 
  
> <span data-ttu-id="47873-140">Status-Objekt</span><span class="sxs-lookup"><span data-stu-id="47873-140">Status object</span></span> 
    
<span data-ttu-id="47873-141">MAPI_STORE</span><span class="sxs-lookup"><span data-stu-id="47873-141">MAPI_STORE</span></span> 
  
> <span data-ttu-id="47873-142">Message store-Objekt</span><span class="sxs-lookup"><span data-stu-id="47873-142">Message store object</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="47873-143">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="47873-143">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="47873-144">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="47873-144">Protocol specifications</span></span>

<span data-ttu-id="47873-145">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47873-145">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47873-146">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="47873-146">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="47873-147">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47873-147">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47873-148">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="47873-148">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="47873-149">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47873-149">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47873-150">Verarbeitet die Kommunikation eines Clients mit einem NSPI-Server (Name Service Provider Interface).</span><span class="sxs-lookup"><span data-stu-id="47873-150">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
<span data-ttu-id="47873-151">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47873-151">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47873-152">Verarbeitet Ordnervorgänge.</span><span class="sxs-lookup"><span data-stu-id="47873-152">Handles folder operations.</span></span>
    
<span data-ttu-id="47873-153">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47873-153">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47873-154">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="47873-154">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="47873-155">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47873-155">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47873-156">Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="47873-156">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="47873-157">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47873-157">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47873-158">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="47873-158">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="47873-159">[[MS-OXOAB]](https://msdn.microsoft.com/library/b4750386-66ec-4e69-abb6-208dd131c7de%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47873-159">[[MS-OXOAB]](https://msdn.microsoft.com/library/b4750386-66ec-4e69-abb6-208dd131c7de%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47873-160">Gibt die Offlineadressbuchdateiformate (OAB) für den Cache für lokale Adressbuchobjekte an.</span><span class="sxs-lookup"><span data-stu-id="47873-160">Specifies the offline address book (OAB) file formats for the local address book objects cache.</span></span>
    
<span data-ttu-id="47873-161">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47873-161">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47873-162">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="47873-162">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="47873-163">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47873-163">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47873-164">Gibt die Eigenschaften und Vorgänge zum Bearbeiten einer Suchordnerlistenkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="47873-164">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="47873-165">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="47873-165">Header files</span></span>

<span data-ttu-id="47873-166">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="47873-166">Mapidefs.h</span></span>
  
> <span data-ttu-id="47873-167">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="47873-167">Provides data type definitions.</span></span>
    
<span data-ttu-id="47873-168">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="47873-168">Mapitags.h</span></span>
  
> <span data-ttu-id="47873-169">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="47873-169">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="47873-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47873-170">See also</span></span>



[<span data-ttu-id="47873-171">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="47873-171">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="47873-172">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="47873-172">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="47873-173">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="47873-173">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="47873-174">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="47873-174">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

