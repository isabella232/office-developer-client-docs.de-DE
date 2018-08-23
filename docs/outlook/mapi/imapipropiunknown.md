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
ms.openlocfilehash: a397ac9110429911755552298ffe244343d54a8a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583729"
---
# <a name="imapiprop--iunknown"></a><span data-ttu-id="25abe-103">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="25abe-103">IMAPIProp : IUnknown</span></span>

  
  
<span data-ttu-id="25abe-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25abe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25abe-105">Ermöglicht es Clients, Service Provider und MAPI-Eigenschaften entwickelt.</span><span class="sxs-lookup"><span data-stu-id="25abe-105">Enables clients, service providers, and MAPI to work with properties.</span></span> <span data-ttu-id="25abe-106">Alle Objekte, Eigenschaften unterstützen, implementieren Sie diese Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="25abe-106">All objects that support properties implement this interface.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="25abe-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="25abe-107">Header file:</span></span>  <br/> |<span data-ttu-id="25abe-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="25abe-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="25abe-109">Verfügbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="25abe-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="25abe-110">Kein Objekt macht diese Schnittstelle direkt verfügbar.</span><span class="sxs-lookup"><span data-stu-id="25abe-110">No object exposes this interface directly.</span></span>  <br/> |
|<span data-ttu-id="25abe-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="25abe-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="25abe-112">Dienstanbieter und MAPI</span><span class="sxs-lookup"><span data-stu-id="25abe-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="25abe-113">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="25abe-113">Called by:</span></span>  <br/> |<span data-ttu-id="25abe-114">Clientanwendungen, Service Provider und MAPI</span><span class="sxs-lookup"><span data-stu-id="25abe-114">Client applications, service providers, and MAPI</span></span>  <br/> |
|<span data-ttu-id="25abe-115">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="25abe-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="25abe-116">IID_IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="25abe-116">IID_IMAPIProp</span></span>  <br/> |
|<span data-ttu-id="25abe-117">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="25abe-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="25abe-118">LPMAPIPROP</span><span class="sxs-lookup"><span data-stu-id="25abe-118">LPMAPIPROP</span></span>  <br/> |
|<span data-ttu-id="25abe-119">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="25abe-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="25abe-120">Abstrakte Basisklasse, die nie implementiert</span><span class="sxs-lookup"><span data-stu-id="25abe-120">Abstract class, never implemented</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="25abe-121">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="25abe-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="25abe-122">GetLastError</span><span class="sxs-lookup"><span data-stu-id="25abe-122">GetLastError</span></span>](imapiprop-getlasterror.md) <br/> |<span data-ttu-id="25abe-123">Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den vorherigen Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="25abe-123">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error.</span></span>  <br/> |
|[<span data-ttu-id="25abe-124">SaveChanges</span><span class="sxs-lookup"><span data-stu-id="25abe-124">SaveChanges</span></span>](imapiprop-savechanges.md) <br/> |<span data-ttu-id="25abe-125">Macht dauerhaft entfernt alle Änderungen, die seit dem letzten Speichervorgang auf ein Objekt vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="25abe-125">Makes permanent any changes that were made to an object since the last save operation.</span></span>  <br/> |
|[<span data-ttu-id="25abe-126">GetProps</span><span class="sxs-lookup"><span data-stu-id="25abe-126">GetProps</span></span>](imapiprop-getprops.md) <br/> |<span data-ttu-id="25abe-127">Ruft den Wert der Eigenschaft um, der eine oder mehrere Eigenschaften eines Objekts an.</span><span class="sxs-lookup"><span data-stu-id="25abe-127">Retrieves the property value of one or more properties of an object.</span></span>  <br/> |
|[<span data-ttu-id="25abe-128">GetPropList</span><span class="sxs-lookup"><span data-stu-id="25abe-128">GetPropList</span></span>](imapiprop-getproplist.md) <br/> |<span data-ttu-id="25abe-129">Eigenschaftentags für alle Eigenschaften zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="25abe-129">Returns property tags for all properties.</span></span>  <br/> |
|[<span data-ttu-id="25abe-130">OpenProperty</span><span class="sxs-lookup"><span data-stu-id="25abe-130">OpenProperty</span></span>](imapiprop-openproperty.md) <br/> |<span data-ttu-id="25abe-131">Gibt einen Zeiger auf eine Schnittstelle, die Zugriff auf eine Eigenschaft verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="25abe-131">Returns a pointer to an interface that can be used to access a property.</span></span>  <br/> |
|[<span data-ttu-id="25abe-132">SetProps</span><span class="sxs-lookup"><span data-stu-id="25abe-132">SetProps</span></span>](imapiprop-setprops.md) <br/> |<span data-ttu-id="25abe-133">Aktualisiert eine oder mehrere Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="25abe-133">Updates one or more properties.</span></span>  <br/> |
|[<span data-ttu-id="25abe-134">"DeleteProps"</span><span class="sxs-lookup"><span data-stu-id="25abe-134">DeleteProps</span></span>](imapiprop-deleteprops.md) <br/> |<span data-ttu-id="25abe-135">Löscht eine oder mehrere Eigenschaften aus einem Objekt.</span><span class="sxs-lookup"><span data-stu-id="25abe-135">Deletes one or more properties from an object.</span></span>  <br/> |
|[<span data-ttu-id="25abe-136">CopyTo</span><span class="sxs-lookup"><span data-stu-id="25abe-136">CopyTo</span></span>](imapiprop-copyto.md) <br/> |<span data-ttu-id="25abe-137">Kopiert oder verschiebt alle Eigenschaften, mit Ausnahme von speziell Ausgeschlossene Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="25abe-137">Copies or moves all properties, except for specifically excluded properties.</span></span>  <br/> |
|[<span data-ttu-id="25abe-138">CopyProps</span><span class="sxs-lookup"><span data-stu-id="25abe-138">CopyProps</span></span>](imapiprop-copyprops.md) <br/> |<span data-ttu-id="25abe-139">Kopiert oder verschiebt ausgewählten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="25abe-139">Copies or moves selected properties.</span></span>  <br/> |
|[<span data-ttu-id="25abe-140">GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="25abe-140">GetNamesFromIDs</span></span>](imapiprop-getnamesfromids.md) <br/> |<span data-ttu-id="25abe-141">Enthält die Eigenschaftennamen, die einen oder mehrere Eigenschaftenbezeichner entsprechen.</span><span class="sxs-lookup"><span data-stu-id="25abe-141">Provides the property names that correspond to one or more property identifiers.</span></span>  <br/> |
|[<span data-ttu-id="25abe-142">GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="25abe-142">GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md) <br/> |<span data-ttu-id="25abe-143">Enthält die Eigenschaftenbezeichner, die mindestens einen Eigenschaftennamen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="25abe-143">Provides the property identifiers that correspond to one or more property names.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25abe-144">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="25abe-144">Remarks</span></span>

 <span data-ttu-id="25abe-145">**IMAPIProp** ist die Basis-Schnittstelle für die folgenden Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="25abe-145">**IMAPIProp** is the base interface for the following interfaces:</span></span> 
  
- [<span data-ttu-id="25abe-146">IAttach</span><span class="sxs-lookup"><span data-stu-id="25abe-146">IAttach</span></span>](iattachimapiprop.md)
    
- [<span data-ttu-id="25abe-147">IMailUser</span><span class="sxs-lookup"><span data-stu-id="25abe-147">IMailUser</span></span>](imailuserimapiprop.md)
    
- [<span data-ttu-id="25abe-148">IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="25abe-148">IMAPIContainer</span></span>](imapicontainerimapiprop.md)
    
- [<span data-ttu-id="25abe-149">IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="25abe-149">IMAPIFormInfo</span></span>](imapiforminfoimapiprop.md)
    
- [<span data-ttu-id="25abe-150">IMAPIStatus</span><span class="sxs-lookup"><span data-stu-id="25abe-150">IMAPIStatus</span></span>](imapistatusimapiprop.md)
    
- [<span data-ttu-id="25abe-151">IMessage</span><span class="sxs-lookup"><span data-stu-id="25abe-151">IMessage</span></span>](imessageimapiprop.md)
    
- [<span data-ttu-id="25abe-152">IMsgStore</span><span class="sxs-lookup"><span data-stu-id="25abe-152">IMsgStore</span></span>](imsgstoreimapiprop.md)
    
- [<span data-ttu-id="25abe-153">IProfSect</span><span class="sxs-lookup"><span data-stu-id="25abe-153">IProfSect</span></span>](iprofsectimapiprop.md)
    
- [<span data-ttu-id="25abe-154">IPropData</span><span class="sxs-lookup"><span data-stu-id="25abe-154">IPropData</span></span>](ipropdataimapiprop.md)
    
## <a name="see-also"></a><span data-ttu-id="25abe-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25abe-155">See also</span></span>



[<span data-ttu-id="25abe-156">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="25abe-156">MAPI Interfaces</span></span>](mapi-interfaces.md)

