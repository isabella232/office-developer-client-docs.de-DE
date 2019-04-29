---
title: IMAPIProp IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp
api_type:
- COM
ms.assetid: 3c9e4e05-cd3a-4b56-9dff-879e33ff6fd5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6b0a8923ee5efe22584170ce9853698885527ee8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407662"
---
# <a name="imapiprop--iunknown"></a><span data-ttu-id="b7102-103">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b7102-103">IMAPIProp : IUnknown</span></span>

  
  
<span data-ttu-id="b7102-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7102-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7102-105">Ermöglicht es Clients, Dienstanbietern und MAPI, mit Eigenschaften zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="b7102-105">Enables clients, service providers, and MAPI to work with properties.</span></span> <span data-ttu-id="b7102-106">Alle Objekte, die Eigenschaften unterstützen, implementieren diese Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b7102-106">All objects that support properties implement this interface.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b7102-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="b7102-107">Header file:</span></span>  <br/> |<span data-ttu-id="b7102-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b7102-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b7102-109">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="b7102-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="b7102-110">Diese Schnittstelle wird von keinem Objekt direkt verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="b7102-110">No object exposes this interface directly.</span></span>  <br/> |
|<span data-ttu-id="b7102-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="b7102-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="b7102-112">Dienstanbieter und MAPI</span><span class="sxs-lookup"><span data-stu-id="b7102-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="b7102-113">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="b7102-113">Called by:</span></span>  <br/> |<span data-ttu-id="b7102-114">Client Anwendungen, Dienstanbieter und MAPI</span><span class="sxs-lookup"><span data-stu-id="b7102-114">Client applications, service providers, and MAPI</span></span>  <br/> |
|<span data-ttu-id="b7102-115">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="b7102-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b7102-116">IID_IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b7102-116">IID_IMAPIProp</span></span>  <br/> |
|<span data-ttu-id="b7102-117">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="b7102-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="b7102-118">LPMAPIPROP</span><span class="sxs-lookup"><span data-stu-id="b7102-118">LPMAPIPROP</span></span>  <br/> |
|<span data-ttu-id="b7102-119">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="b7102-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="b7102-120">Abstrakte Klasse, nie implementiert</span><span class="sxs-lookup"><span data-stu-id="b7102-120">Abstract class, never implemented</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b7102-121">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="b7102-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="b7102-122">Getlasterroraufzurufen</span><span class="sxs-lookup"><span data-stu-id="b7102-122">GetLastError</span></span>](imapiprop-getlasterror.md) <br/> |<span data-ttu-id="b7102-123">Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen zum vorherigen Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="b7102-123">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error.</span></span>  <br/> |
|[<span data-ttu-id="b7102-124">SaveChanges</span><span class="sxs-lookup"><span data-stu-id="b7102-124">SaveChanges</span></span>](imapiprop-savechanges.md) <br/> |<span data-ttu-id="b7102-125">Macht alle Änderungen, die an einem Objekt seit dem letzten Speichervorgang vorgenommen wurden, dauerhaft.</span><span class="sxs-lookup"><span data-stu-id="b7102-125">Makes permanent any changes that were made to an object since the last save operation.</span></span>  <br/> |
|[<span data-ttu-id="b7102-126">GetProps</span><span class="sxs-lookup"><span data-stu-id="b7102-126">GetProps</span></span>](imapiprop-getprops.md) <br/> |<span data-ttu-id="b7102-127">Ruft den Eigenschaftswert einer oder mehrerer Eigenschaften eines Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="b7102-127">Retrieves the property value of one or more properties of an object.</span></span>  <br/> |
|[<span data-ttu-id="b7102-128">GetProplist</span><span class="sxs-lookup"><span data-stu-id="b7102-128">GetPropList</span></span>](imapiprop-getproplist.md) <br/> |<span data-ttu-id="b7102-129">Gibt Eigenschaftentags für alle Eigenschaften zurück.</span><span class="sxs-lookup"><span data-stu-id="b7102-129">Returns property tags for all properties.</span></span>  <br/> |
|[<span data-ttu-id="b7102-130">OpenProperty</span><span class="sxs-lookup"><span data-stu-id="b7102-130">OpenProperty</span></span>](imapiprop-openproperty.md) <br/> |<span data-ttu-id="b7102-131">Gibt einen Zeiger auf eine Schnittstelle zurück, die für den Zugriff auf eine Eigenschaft verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b7102-131">Returns a pointer to an interface that can be used to access a property.</span></span>  <br/> |
|[<span data-ttu-id="b7102-132">SetProps</span><span class="sxs-lookup"><span data-stu-id="b7102-132">SetProps</span></span>](imapiprop-setprops.md) <br/> |<span data-ttu-id="b7102-133">Aktualisiert eine oder mehrere Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b7102-133">Updates one or more properties.</span></span>  <br/> |
|[<span data-ttu-id="b7102-134">DeleteProps</span><span class="sxs-lookup"><span data-stu-id="b7102-134">DeleteProps</span></span>](imapiprop-deleteprops.md) <br/> |<span data-ttu-id="b7102-135">Löscht eine oder mehrere Eigenschaften aus einem Objekt.</span><span class="sxs-lookup"><span data-stu-id="b7102-135">Deletes one or more properties from an object.</span></span>  <br/> |
|[<span data-ttu-id="b7102-136">CopyTo</span><span class="sxs-lookup"><span data-stu-id="b7102-136">CopyTo</span></span>](imapiprop-copyto.md) <br/> |<span data-ttu-id="b7102-137">Kopiert oder verschiebt alle Eigenschaften, mit Ausnahme der explizit ausgeschlossenen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b7102-137">Copies or moves all properties, except for specifically excluded properties.</span></span>  <br/> |
|[<span data-ttu-id="b7102-138">CopyProps</span><span class="sxs-lookup"><span data-stu-id="b7102-138">CopyProps</span></span>](imapiprop-copyprops.md) <br/> |<span data-ttu-id="b7102-139">Kopiert oder verschiebt ausgewählte Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b7102-139">Copies or moves selected properties.</span></span>  <br/> |
|[<span data-ttu-id="b7102-140">GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="b7102-140">GetNamesFromIDs</span></span>](imapiprop-getnamesfromids.md) <br/> |<span data-ttu-id="b7102-141">Stellt die Eigenschaftennamen bereit, die einem oder mehreren Eigenschafts Bezeichnern entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b7102-141">Provides the property names that correspond to one or more property identifiers.</span></span>  <br/> |
|[<span data-ttu-id="b7102-142">GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="b7102-142">GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md) <br/> |<span data-ttu-id="b7102-143">Stellt die Eigenschaftenbezeichner bereit, die einem oder mehreren Eigenschaftsnamen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b7102-143">Provides the property identifiers that correspond to one or more property names.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7102-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7102-144">Remarks</span></span>

 <span data-ttu-id="b7102-145">**IMAPIProp** ist die Basisschnittstelle für die folgenden Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="b7102-145">**IMAPIProp** is the base interface for the following interfaces:</span></span> 
  
- [<span data-ttu-id="b7102-146">IAttach</span><span class="sxs-lookup"><span data-stu-id="b7102-146">IAttach</span></span>](iattachimapiprop.md)
    
- [<span data-ttu-id="b7102-147">IMailUser</span><span class="sxs-lookup"><span data-stu-id="b7102-147">IMailUser</span></span>](imailuserimapiprop.md)
    
- [<span data-ttu-id="b7102-148">IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="b7102-148">IMAPIContainer</span></span>](imapicontainerimapiprop.md)
    
- [<span data-ttu-id="b7102-149">IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="b7102-149">IMAPIFormInfo</span></span>](imapiforminfoimapiprop.md)
    
- [<span data-ttu-id="b7102-150">IMAPIStatus</span><span class="sxs-lookup"><span data-stu-id="b7102-150">IMAPIStatus</span></span>](imapistatusimapiprop.md)
    
- [<span data-ttu-id="b7102-151">IMessage</span><span class="sxs-lookup"><span data-stu-id="b7102-151">IMessage</span></span>](imessageimapiprop.md)
    
- [<span data-ttu-id="b7102-152">IMsgStore</span><span class="sxs-lookup"><span data-stu-id="b7102-152">IMsgStore</span></span>](imsgstoreimapiprop.md)
    
- [<span data-ttu-id="b7102-153">IProfSect</span><span class="sxs-lookup"><span data-stu-id="b7102-153">IProfSect</span></span>](iprofsectimapiprop.md)
    
- [<span data-ttu-id="b7102-154">IPropData</span><span class="sxs-lookup"><span data-stu-id="b7102-154">IPropData</span></span>](ipropdataimapiprop.md)
    
## <a name="see-also"></a><span data-ttu-id="b7102-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7102-155">See also</span></span>



[<span data-ttu-id="b7102-156">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b7102-156">MAPI Interfaces</span></span>](mapi-interfaces.md)

