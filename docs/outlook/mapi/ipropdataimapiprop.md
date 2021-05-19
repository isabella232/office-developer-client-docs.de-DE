---
title: IPropData IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData
api_type:
- COM
ms.assetid: 30b8ae9e-0c0c-4468-b286-29e083696fed
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: aed9120ac264a6c47c9d02502093e56d3268d08a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435145"
---
# <a name="ipropdata--imapiprop"></a><span data-ttu-id="60296-103">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="60296-103">IPropData : IMAPIProp</span></span>

  
  
<span data-ttu-id="60296-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60296-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60296-105">Ermöglicht das Abrufen und Ändern des Zugriffs für die Eigenschaften eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="60296-105">Provides the ability to retrieve and change the access for an object's properties.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="60296-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="60296-106">Header file:</span></span>  <br/> |<span data-ttu-id="60296-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="60296-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="60296-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="60296-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="60296-109">Eigenschaftsdatenobjekt</span><span class="sxs-lookup"><span data-stu-id="60296-109">Property data object</span></span>  <br/> |
|<span data-ttu-id="60296-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="60296-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="60296-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="60296-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="60296-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="60296-112">Called by:</span></span>  <br/> |<span data-ttu-id="60296-113">Dienstanbieter und Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="60296-113">Service providers and client applications</span></span>  <br/> |
|<span data-ttu-id="60296-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="60296-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="60296-115">IID_IMAPIPropData</span><span class="sxs-lookup"><span data-stu-id="60296-115">IID_IMAPIPropData</span></span>  <br/> |
|<span data-ttu-id="60296-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="60296-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="60296-117">LPPROPDATA</span><span class="sxs-lookup"><span data-stu-id="60296-117">LPPROPDATA</span></span>  <br/> |
|<span data-ttu-id="60296-118">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="60296-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="60296-119">Nichttransaktioniert</span><span class="sxs-lookup"><span data-stu-id="60296-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="60296-120">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="60296-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="60296-121">HrSetObjAccess</span><span class="sxs-lookup"><span data-stu-id="60296-121">HrSetObjAccess</span></span>](ipropdata-hrsetobjaccess.md) <br/> |<span data-ttu-id="60296-122">Legt die Zugriffsebene f�r das Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="60296-122">Sets the access level for the object.</span></span>  <br/> |
|[<span data-ttu-id="60296-123">HrSetPropAccess</span><span class="sxs-lookup"><span data-stu-id="60296-123">HrSetPropAccess</span></span>](ipropdata-hrsetpropaccess.md) <br/> |<span data-ttu-id="60296-124">Legt die Zugriffsebene und den Status für eine oder mehrere Eigenschaften des Objekts fest.</span><span class="sxs-lookup"><span data-stu-id="60296-124">Sets the access level and status for one or more of the object's properties.</span></span>  <br/> |
|[<span data-ttu-id="60296-125">HrGetPropAccess</span><span class="sxs-lookup"><span data-stu-id="60296-125">HrGetPropAccess</span></span>](ipropdata-hrgetpropaccess.md) <br/> |<span data-ttu-id="60296-126">Ruft die Zugriffsebene und den Status f�r eine oder mehrere der Eigenschaften des Objekts an.</span><span class="sxs-lookup"><span data-stu-id="60296-126">Retrieves the access level and status for one or more of the object's properties.</span></span>  <br/> |
|[<span data-ttu-id="60296-127">HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="60296-127">HrAddObjProps</span></span>](ipropdata-hraddobjprops.md) <br/> |<span data-ttu-id="60296-128">Fügt eine oder mehrere Eigenschaften vom Typ PT_OBJECT objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="60296-128">Adds one or more properties of type PT_OBJECT to the object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="60296-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="60296-129">Remarks</span></span>

<span data-ttu-id="60296-130">Die **IPropData::IMAPIProp-Schnittstelle** wird von MAPI implementiert und hauptsächlich von Dienstanbietern verwendet, die auf diese Implementierung zugreifen, indem sie die [CreateIProp-Funktion](createiprop.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="60296-130">The **IPropData::IMAPIProp** interface is implemented by MAPI and used primarily by service providers that access this implementation by calling the [CreateIProp](createiprop.md) function.</span></span> 
  
<span data-ttu-id="60296-131">Weitere Informationen zu Zugriffsebenen für Objekte und Eigenschaften finden Sie unter [Permissions for Objects and Properties](permissions-for-mapi-objects-and-properties.md).</span><span class="sxs-lookup"><span data-stu-id="60296-131">For more information about access levels on objects and properties, see [Permissions for Objects and Properties](permissions-for-mapi-objects-and-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="60296-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60296-132">See also</span></span>



[<span data-ttu-id="60296-133">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="60296-133">MAPI Interfaces</span></span>](mapi-interfaces.md)

