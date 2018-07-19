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
ms.openlocfilehash: d6a53d112e4c12cd9092ac627e99cf3c13d901f3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792770"
---
# <a name="ipropdata--imapiprop"></a><span data-ttu-id="014e2-103">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="014e2-103">IPropData : IMAPIProp</span></span>

  
  
<span data-ttu-id="014e2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="014e2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="014e2-105">Bietet die Möglichkeit zum Abrufen und ändern Sie den Zugriff für die Eigenschaften eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="014e2-105">Provides the ability to retrieve and change the access for an object's properties.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="014e2-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="014e2-106">Header file:</span></span>  <br/> |<span data-ttu-id="014e2-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="014e2-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="014e2-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="014e2-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="014e2-109">Property-Daten-Objekt</span><span class="sxs-lookup"><span data-stu-id="014e2-109">Property data object</span></span>  <br/> |
|<span data-ttu-id="014e2-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="014e2-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="014e2-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="014e2-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="014e2-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="014e2-112">Called by:</span></span>  <br/> |<span data-ttu-id="014e2-113">Dienstanbieter und -Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="014e2-113">Service providers and client applications</span></span>  <br/> |
|<span data-ttu-id="014e2-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="014e2-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="014e2-115">IID_IMAPIPropData</span><span class="sxs-lookup"><span data-stu-id="014e2-115">IID_IMAPIPropData</span></span>  <br/> |
|<span data-ttu-id="014e2-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="014e2-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="014e2-117">LPPROPDATA</span><span class="sxs-lookup"><span data-stu-id="014e2-117">LPPROPDATA</span></span>  <br/> |
|<span data-ttu-id="014e2-118">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="014e2-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="014e2-119">Nontransacted</span><span class="sxs-lookup"><span data-stu-id="014e2-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="014e2-120">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="014e2-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="014e2-121">HrSetObjAccess</span><span class="sxs-lookup"><span data-stu-id="014e2-121">HrSetObjAccess</span></span>](ipropdata-hrsetobjaccess.md) <br/> |<span data-ttu-id="014e2-122">Legt die Zugriffsebene f�r das Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="014e2-122">Sets the access level for the object.</span></span>  <br/> |
|[<span data-ttu-id="014e2-123">HrSetPropAccess</span><span class="sxs-lookup"><span data-stu-id="014e2-123">HrSetPropAccess</span></span>](ipropdata-hrsetpropaccess.md) <br/> |<span data-ttu-id="014e2-124">Die Zugriffsebene und den Status für eine oder mehrere der Eigenschaften des Objekts festgelegt.</span><span class="sxs-lookup"><span data-stu-id="014e2-124">Sets the access level and status for one or more of the object's properties.</span></span>  <br/> |
|[<span data-ttu-id="014e2-125">HrGetPropAccess</span><span class="sxs-lookup"><span data-stu-id="014e2-125">HrGetPropAccess</span></span>](ipropdata-hrgetpropaccess.md) <br/> |<span data-ttu-id="014e2-126">Ruft die Zugriffsebene und den Status f�r eine oder mehrere der Eigenschaften des Objekts an.</span><span class="sxs-lookup"><span data-stu-id="014e2-126">Retrieves the access level and status for one or more of the object's properties.</span></span>  <br/> |
|[<span data-ttu-id="014e2-127">HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="014e2-127">HrAddObjProps</span></span>](ipropdata-hraddobjprops.md) <br/> |<span data-ttu-id="014e2-128">Fügt eine oder mehrere Eigenschaften vom Typ PT_OBJECT auf das Objekt.</span><span class="sxs-lookup"><span data-stu-id="014e2-128">Adds one or more properties of type PT_OBJECT to the object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="014e2-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="014e2-129">Remarks</span></span>

<span data-ttu-id="014e2-130">Die **IPropData::IMAPIProp** -Schnittstelle wird von MAPI implementierte und in erster Linie vom Dienstanbieter, die dieser Implementierung zugreifen, indem die [CreateIProp](createiprop.md) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="014e2-130">The **IPropData::IMAPIProp** interface is implemented by MAPI and used primarily by service providers that access this implementation by calling the [CreateIProp](createiprop.md) function.</span></span> 
  
<span data-ttu-id="014e2-131">Weitere Informationen zu Zugriffsebenen-Objekten und Eigenschaften finden Sie unter [Berechtigungen für Objekte und Eigenschaften](permissions-for-mapi-objects-and-properties.md).</span><span class="sxs-lookup"><span data-stu-id="014e2-131">For more information about access levels on objects and properties, see [Permissions for Objects and Properties](permissions-for-mapi-objects-and-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="014e2-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="014e2-132">See also</span></span>



[<span data-ttu-id="014e2-133">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="014e2-133">MAPI Interfaces</span></span>](mapi-interfaces.md)

