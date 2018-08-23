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
ms.openlocfilehash: c320b2c42b9a14c6dc428fc3df59991528cdbe36
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592570"
---
# <a name="ipropdata--imapiprop"></a><span data-ttu-id="33c25-103">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="33c25-103">IPropData : IMAPIProp</span></span>

  
  
<span data-ttu-id="33c25-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33c25-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33c25-105">Bietet die Möglichkeit zum Abrufen und ändern Sie den Zugriff für die Eigenschaften eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="33c25-105">Provides the ability to retrieve and change the access for an object's properties.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="33c25-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="33c25-106">Header file:</span></span>  <br/> |<span data-ttu-id="33c25-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="33c25-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="33c25-108">Verfügbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="33c25-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="33c25-109">Property-Daten-Objekt</span><span class="sxs-lookup"><span data-stu-id="33c25-109">Property data object</span></span>  <br/> |
|<span data-ttu-id="33c25-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="33c25-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="33c25-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="33c25-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="33c25-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="33c25-112">Called by:</span></span>  <br/> |<span data-ttu-id="33c25-113">Dienstanbieter und -Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="33c25-113">Service providers and client applications</span></span>  <br/> |
|<span data-ttu-id="33c25-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="33c25-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="33c25-115">IID_IMAPIPropData</span><span class="sxs-lookup"><span data-stu-id="33c25-115">IID_IMAPIPropData</span></span>  <br/> |
|<span data-ttu-id="33c25-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="33c25-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="33c25-117">LPPROPDATA</span><span class="sxs-lookup"><span data-stu-id="33c25-117">LPPROPDATA</span></span>  <br/> |
|<span data-ttu-id="33c25-118">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="33c25-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="33c25-119">Nontransacted</span><span class="sxs-lookup"><span data-stu-id="33c25-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="33c25-120">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="33c25-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="33c25-121">HrSetObjAccess</span><span class="sxs-lookup"><span data-stu-id="33c25-121">HrSetObjAccess</span></span>](ipropdata-hrsetobjaccess.md) <br/> |<span data-ttu-id="33c25-122">Legt die Zugriffsebene f�r das Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="33c25-122">Sets the access level for the object.</span></span>  <br/> |
|[<span data-ttu-id="33c25-123">HrSetPropAccess</span><span class="sxs-lookup"><span data-stu-id="33c25-123">HrSetPropAccess</span></span>](ipropdata-hrsetpropaccess.md) <br/> |<span data-ttu-id="33c25-124">Die Zugriffsebene und den Status für eine oder mehrere der Eigenschaften des Objekts festgelegt.</span><span class="sxs-lookup"><span data-stu-id="33c25-124">Sets the access level and status for one or more of the object's properties.</span></span>  <br/> |
|[<span data-ttu-id="33c25-125">HrGetPropAccess</span><span class="sxs-lookup"><span data-stu-id="33c25-125">HrGetPropAccess</span></span>](ipropdata-hrgetpropaccess.md) <br/> |<span data-ttu-id="33c25-126">Ruft die Zugriffsebene und den Status f�r eine oder mehrere der Eigenschaften des Objekts an.</span><span class="sxs-lookup"><span data-stu-id="33c25-126">Retrieves the access level and status for one or more of the object's properties.</span></span>  <br/> |
|[<span data-ttu-id="33c25-127">HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="33c25-127">HrAddObjProps</span></span>](ipropdata-hraddobjprops.md) <br/> |<span data-ttu-id="33c25-128">Fügt eine oder mehrere Eigenschaften vom Typ PT_OBJECT auf das Objekt.</span><span class="sxs-lookup"><span data-stu-id="33c25-128">Adds one or more properties of type PT_OBJECT to the object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33c25-129">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="33c25-129">Remarks</span></span>

<span data-ttu-id="33c25-130">Die **IPropData::IMAPIProp** -Schnittstelle wird von MAPI implementierte und in erster Linie vom Dienstanbieter, die dieser Implementierung zugreifen, indem die [CreateIProp](createiprop.md) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="33c25-130">The **IPropData::IMAPIProp** interface is implemented by MAPI and used primarily by service providers that access this implementation by calling the [CreateIProp](createiprop.md) function.</span></span> 
  
<span data-ttu-id="33c25-131">Weitere Informationen zu Zugriffsebenen-Objekten und Eigenschaften finden Sie unter [Berechtigungen für Objekte und Eigenschaften](permissions-for-mapi-objects-and-properties.md).</span><span class="sxs-lookup"><span data-stu-id="33c25-131">For more information about access levels on objects and properties, see [Permissions for Objects and Properties](permissions-for-mapi-objects-and-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="33c25-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33c25-132">See also</span></span>



[<span data-ttu-id="33c25-133">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="33c25-133">MAPI Interfaces</span></span>](mapi-interfaces.md)

