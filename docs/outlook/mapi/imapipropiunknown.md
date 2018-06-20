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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 02d2b136ed1437ba53ce1e54a202d70a48b2abe9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792296"
---
# <a name="imapiprop--iunknown"></a><span data-ttu-id="76094-103">IMAPIProp: IUnknown</span><span class="sxs-lookup"><span data-stu-id="76094-103">IMAPIProp : IUnknown</span></span>

  
  
<span data-ttu-id="76094-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="76094-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="76094-105">Ermöglicht es Clients, Service Provider und MAPI-Eigenschaften entwickelt.</span><span class="sxs-lookup"><span data-stu-id="76094-105">Enables clients, service providers, and MAPI to work with properties.</span></span> <span data-ttu-id="76094-106">Alle Objekte, Eigenschaften unterstützen, implementieren Sie diese Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="76094-106">All objects that support properties implement this interface.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="76094-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="76094-107">Header file:</span></span>  <br/> |<span data-ttu-id="76094-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="76094-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="76094-109">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="76094-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="76094-110">Kein Objekt macht diese Schnittstelle direkt verfügbar.</span><span class="sxs-lookup"><span data-stu-id="76094-110">No object exposes this interface directly.</span></span>  <br/> |
|<span data-ttu-id="76094-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="76094-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="76094-112">Dienstanbieter und MAPI</span><span class="sxs-lookup"><span data-stu-id="76094-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="76094-113">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="76094-113">Called by:</span></span>  <br/> |<span data-ttu-id="76094-114">Clientanwendungen, Service Provider und MAPI</span><span class="sxs-lookup"><span data-stu-id="76094-114">Client applications, service providers, and MAPI</span></span>  <br/> |
|<span data-ttu-id="76094-115">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="76094-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="76094-116">IID_IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="76094-116">IID_IMAPIProp</span></span>  <br/> |
|<span data-ttu-id="76094-117">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="76094-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="76094-118">LPMAPIPROP</span><span class="sxs-lookup"><span data-stu-id="76094-118">LPMAPIPROP</span></span>  <br/> |
|<span data-ttu-id="76094-119">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="76094-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="76094-120">Abstrakte Basisklasse, die nie implementiert</span><span class="sxs-lookup"><span data-stu-id="76094-120">Abstract class, never implemented</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="76094-121">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="76094-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="76094-122">GetLastError</span><span class="sxs-lookup"><span data-stu-id="76094-122">GetLastError</span></span>](imapiprop-getlasterror.md) <br/> |<span data-ttu-id="76094-123">Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den vorherigen Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="76094-123">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error.</span></span>  <br/> |
|[<span data-ttu-id="76094-124">SaveChanges</span><span class="sxs-lookup"><span data-stu-id="76094-124">SaveChanges</span></span>](imapiprop-savechanges.md) <br/> |<span data-ttu-id="76094-125">Macht dauerhaft entfernt alle Änderungen, die seit dem letzten Speichervorgang auf ein Objekt vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="76094-125">Makes permanent any changes that were made to an object since the last save operation.</span></span>  <br/> |
|[<span data-ttu-id="76094-126">GetProps</span><span class="sxs-lookup"><span data-stu-id="76094-126">GetProps</span></span>](imapiprop-getprops.md) <br/> |<span data-ttu-id="76094-127">Ruft den Wert der Eigenschaft um, der eine oder mehrere Eigenschaften eines Objekts an.</span><span class="sxs-lookup"><span data-stu-id="76094-127">Retrieves the property value of one or more properties of an object.</span></span>  <br/> |
|[<span data-ttu-id="76094-128">GetPropList</span><span class="sxs-lookup"><span data-stu-id="76094-128">GetPropList</span></span>](imapiprop-getproplist.md) <br/> |<span data-ttu-id="76094-129">Eigenschaftentags für alle Eigenschaften zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="76094-129">Returns property tags for all properties.</span></span>  <br/> |
|[<span data-ttu-id="76094-130">OpenProperty</span><span class="sxs-lookup"><span data-stu-id="76094-130">OpenProperty</span></span>](imapiprop-openproperty.md) <br/> |<span data-ttu-id="76094-131">Gibt einen Zeiger auf eine Schnittstelle, die Zugriff auf eine Eigenschaft verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="76094-131">Returns a pointer to an interface that can be used to access a property.</span></span>  <br/> |
|[<span data-ttu-id="76094-132">SetProps</span><span class="sxs-lookup"><span data-stu-id="76094-132">SetProps</span></span>](imapiprop-setprops.md) <br/> |<span data-ttu-id="76094-133">Aktualisiert eine oder mehrere Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="76094-133">Updates one or more properties.</span></span>  <br/> |
|[<span data-ttu-id="76094-134">"DeleteProps"</span><span class="sxs-lookup"><span data-stu-id="76094-134">DeleteProps</span></span>](imapiprop-deleteprops.md) <br/> |<span data-ttu-id="76094-135">Löscht eine oder mehrere Eigenschaften aus einem Objekt.</span><span class="sxs-lookup"><span data-stu-id="76094-135">Deletes one or more properties from an object.</span></span>  <br/> |
|[<span data-ttu-id="76094-136">CopyTo</span><span class="sxs-lookup"><span data-stu-id="76094-136">CopyTo</span></span>](imapiprop-copyto.md) <br/> |<span data-ttu-id="76094-137">Kopiert oder verschiebt alle Eigenschaften, mit Ausnahme von speziell Ausgeschlossene Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="76094-137">Copies or moves all properties, except for specifically excluded properties.</span></span>  <br/> |
|[<span data-ttu-id="76094-138">CopyProps</span><span class="sxs-lookup"><span data-stu-id="76094-138">CopyProps</span></span>](imapiprop-copyprops.md) <br/> |<span data-ttu-id="76094-139">Kopiert oder verschiebt ausgewählten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="76094-139">Copies or moves selected properties.</span></span>  <br/> |
|[<span data-ttu-id="76094-140">GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="76094-140">GetNamesFromIDs</span></span>](imapiprop-getnamesfromids.md) <br/> |<span data-ttu-id="76094-141">Enthält die Eigenschaftennamen, die einen oder mehrere Eigenschaftenbezeichner entsprechen.</span><span class="sxs-lookup"><span data-stu-id="76094-141">Provides the property names that correspond to one or more property identifiers.</span></span>  <br/> |
|[<span data-ttu-id="76094-142">GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="76094-142">GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md) <br/> |<span data-ttu-id="76094-143">Enthält die Eigenschaftenbezeichner, die mindestens einen Eigenschaftennamen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="76094-143">Provides the property identifiers that correspond to one or more property names.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76094-144">Hinweise</span><span class="sxs-lookup"><span data-stu-id="76094-144">Remarks</span></span>

 <span data-ttu-id="76094-145">**IMAPIProp** ist die Basis-Schnittstelle für die folgenden Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="76094-145">**IMAPIProp** is the base interface for the following interfaces:</span></span> 
  
- [<span data-ttu-id="76094-146">IAttach</span><span class="sxs-lookup"><span data-stu-id="76094-146">IAttach</span></span>](iattachimapiprop.md)
    
- [<span data-ttu-id="76094-147">IMailUser</span><span class="sxs-lookup"><span data-stu-id="76094-147">IMailUser</span></span>](imailuserimapiprop.md)
    
- [<span data-ttu-id="76094-148">IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="76094-148">IMAPIContainer</span></span>](imapicontainerimapiprop.md)
    
- [<span data-ttu-id="76094-149">IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="76094-149">IMAPIFormInfo</span></span>](imapiforminfoimapiprop.md)
    
- [<span data-ttu-id="76094-150">IMAPIStatus</span><span class="sxs-lookup"><span data-stu-id="76094-150">IMAPIStatus</span></span>](imapistatusimapiprop.md)
    
- [<span data-ttu-id="76094-151">IMessage</span><span class="sxs-lookup"><span data-stu-id="76094-151">IMessage</span></span>](imessageimapiprop.md)
    
- [<span data-ttu-id="76094-152">IMsgStore</span><span class="sxs-lookup"><span data-stu-id="76094-152">IMsgStore</span></span>](imsgstoreimapiprop.md)
    
- [<span data-ttu-id="76094-153">IProfSect</span><span class="sxs-lookup"><span data-stu-id="76094-153">IProfSect</span></span>](iprofsectimapiprop.md)
    
- [<span data-ttu-id="76094-154">IPropData</span><span class="sxs-lookup"><span data-stu-id="76094-154">IPropData</span></span>](ipropdataimapiprop.md)
    
## <a name="see-also"></a><span data-ttu-id="76094-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76094-155">See also</span></span>



[<span data-ttu-id="76094-156">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="76094-156">MAPI Interfaces</span></span>](mapi-interfaces.md)

