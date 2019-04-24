---
title: IPersistMessage IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage
api_type:
- COM
ms.assetid: 40ec6dd4-2206-4e59-aafe-53aaf693f973
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7eb65bbae2fca6648c3a701dfa5c83c5bf297ec5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309604"
---
# <a name="ipersistmessage--iunknown"></a><span data-ttu-id="781d7-103">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="781d7-103">IPersistMessage : IUnknown</span></span>

  
  
<span data-ttu-id="781d7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="781d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="781d7-105">Ermöglicht es den Formular Viewern, die Speicherung eines Formulars und den Übergang zwischen den verschiedenen Status zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="781d7-105">Enables form viewers to handle the storage of a form and to transition between the various states.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="781d7-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="781d7-106">Header file:</span></span>  <br/> |<span data-ttu-id="781d7-107">Mapiform. h</span><span class="sxs-lookup"><span data-stu-id="781d7-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="781d7-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="781d7-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="781d7-109">Nachrichtenobjekte beibehalten</span><span class="sxs-lookup"><span data-stu-id="781d7-109">Persist message objects</span></span>  <br/> |
|<span data-ttu-id="781d7-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="781d7-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="781d7-111">Formularobjekte</span><span class="sxs-lookup"><span data-stu-id="781d7-111">Form objects</span></span>  <br/> |
|<span data-ttu-id="781d7-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="781d7-112">Called by:</span></span>  <br/> |<span data-ttu-id="781d7-113">Formular Betrachter</span><span class="sxs-lookup"><span data-stu-id="781d7-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="781d7-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="781d7-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="781d7-115">IID_IPersistMessage</span><span class="sxs-lookup"><span data-stu-id="781d7-115">IID_IPersistMessage</span></span>  <br/> |
|<span data-ttu-id="781d7-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="781d7-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="781d7-117">LPPERSISTMESSAGE</span><span class="sxs-lookup"><span data-stu-id="781d7-117">LPPERSISTMESSAGE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="781d7-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="781d7-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="781d7-119">Getlasterroraufzurufen</span><span class="sxs-lookup"><span data-stu-id="781d7-119">GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="781d7-120">Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen zum vorherigen Fehler im Form-Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="781d7-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error in the form object.</span></span>  <br/> |
|[<span data-ttu-id="781d7-121">GetClassID</span><span class="sxs-lookup"><span data-stu-id="781d7-121">GetClassID</span></span>](ipersistmessage-getclassid.md) <br/> |<span data-ttu-id="781d7-122">Gibt einen Bezeichner zurück, der den Formularserver darstellt, der das Formular verwalten kann.</span><span class="sxs-lookup"><span data-stu-id="781d7-122">Returns an identifier that represents the form server that can manage the form.</span></span>  <br/> |
|[<span data-ttu-id="781d7-123">IsDirty</span><span class="sxs-lookup"><span data-stu-id="781d7-123">IsDirty</span></span>](ipersistmessage-isdirty.md) <br/> |<span data-ttu-id="781d7-124">Überprüft das Formular auf Änderungen, die seit dem letzten Speichern vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="781d7-124">Checks the form for changes that were made since the last save.</span></span>  <br/> |
|[<span data-ttu-id="781d7-125">InitNew</span><span class="sxs-lookup"><span data-stu-id="781d7-125">InitNew</span></span>](ipersistmessage-initnew.md) <br/> |<span data-ttu-id="781d7-126">Initialisiert eine neue Nachricht.</span><span class="sxs-lookup"><span data-stu-id="781d7-126">Initializes a new message.</span></span>  <br/> |
|[<span data-ttu-id="781d7-127">Load</span><span class="sxs-lookup"><span data-stu-id="781d7-127">Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="781d7-128">Lädt das Formular für eine angegebene Nachricht.</span><span class="sxs-lookup"><span data-stu-id="781d7-128">Loads the form for a specified message.</span></span>  <br/> |
|[<span data-ttu-id="781d7-129">Save</span><span class="sxs-lookup"><span data-stu-id="781d7-129">Save</span></span>](ipersistmessage-save.md) <br/> |<span data-ttu-id="781d7-130">Speichert ein überarbeitete Formular zurück in der Nachricht, von der es geladen oder erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="781d7-130">Saves a revised form back to the message from which it was loaded or created.</span></span>  <br/> |
|[<span data-ttu-id="781d7-131">SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="781d7-131">SaveCompleted</span></span>](ipersistmessage-savecompleted.md) <br/> |<span data-ttu-id="781d7-132">Benachrichtigt das Formular, dass ein Speichervorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="781d7-132">Notifies the form that a save operation has been completed.</span></span>  <br/> |
|[<span data-ttu-id="781d7-133">HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="781d7-133">HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md) <br/> |<span data-ttu-id="781d7-134">Bewirkt, dass das Formular die aktuelle Nachricht freigibt.</span><span class="sxs-lookup"><span data-stu-id="781d7-134">Causes the form to release its current message.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="781d7-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="781d7-135">Remarks</span></span>

<span data-ttu-id="781d7-136">Alle Formulare sind erforderlich, um die **IPersistMessage** -Schnittstelle zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="781d7-136">All forms are required to implement the **IPersistMessage** interface.</span></span> 
  
 <span data-ttu-id="781d7-137">**IPersistMessage** funktioniert ähnlich wie die OLE [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="781d7-137">**IPersistMessage** works similarly to the OLE [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) interface.</span></span> <span data-ttu-id="781d7-138">Weitere Informationen finden Sie unter den **IPersistStorage** -Methoden.</span><span class="sxs-lookup"><span data-stu-id="781d7-138">For more information, see the **IPersistStorage** methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="781d7-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="781d7-139">See also</span></span>



[<span data-ttu-id="781d7-140">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="781d7-140">MAPI Interfaces</span></span>](mapi-interfaces.md)

