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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 62fb2b069a50408713eea741cf837c421a749fcd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792764"
---
# <a name="ipersistmessage--iunknown"></a><span data-ttu-id="bfa55-103">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bfa55-103">IPersistMessage : IUnknown</span></span>

  
  
<span data-ttu-id="bfa55-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bfa55-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bfa55-105">Ermöglicht das Formular Leser von Berichten, die Speicherung eines Formulars und zum Wechseln zwischen den verschiedenen Zuständen zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="bfa55-105">Enables form viewers to handle the storage of a form and to transition between the various states.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bfa55-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="bfa55-106">Header file:</span></span>  <br/> |<span data-ttu-id="bfa55-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="bfa55-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="bfa55-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="bfa55-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="bfa55-109">Beibehalten von Message-Objekten</span><span class="sxs-lookup"><span data-stu-id="bfa55-109">Persist message objects</span></span>  <br/> |
|<span data-ttu-id="bfa55-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="bfa55-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="bfa55-111">Formular-Objekte</span><span class="sxs-lookup"><span data-stu-id="bfa55-111">Form objects</span></span>  <br/> |
|<span data-ttu-id="bfa55-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="bfa55-112">Called by:</span></span>  <br/> |<span data-ttu-id="bfa55-113">Formular-Viewer</span><span class="sxs-lookup"><span data-stu-id="bfa55-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="bfa55-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="bfa55-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="bfa55-115">IID_IPersistMessage</span><span class="sxs-lookup"><span data-stu-id="bfa55-115">IID_IPersistMessage</span></span>  <br/> |
|<span data-ttu-id="bfa55-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="bfa55-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="bfa55-117">LPPERSISTMESSAGE</span><span class="sxs-lookup"><span data-stu-id="bfa55-117">LPPERSISTMESSAGE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="bfa55-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="bfa55-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="bfa55-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="bfa55-119">GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="bfa55-120">Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen zu den vorherigen Fehler in das Form-Objekt enthält, zurück.</span><span class="sxs-lookup"><span data-stu-id="bfa55-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error in the form object.</span></span>  <br/> |
|[<span data-ttu-id="bfa55-121">GetClassID</span><span class="sxs-lookup"><span data-stu-id="bfa55-121">GetClassID</span></span>](ipersistmessage-getclassid.md) <br/> |<span data-ttu-id="bfa55-122">Gibt einen Bezeichner, der den Formular Server darstellt, der das Formular verwaltet werden können.</span><span class="sxs-lookup"><span data-stu-id="bfa55-122">Returns an identifier that represents the form server that can manage the form.</span></span>  <br/> |
|[<span data-ttu-id="bfa55-123">IsDirty</span><span class="sxs-lookup"><span data-stu-id="bfa55-123">IsDirty</span></span>](ipersistmessage-isdirty.md) <br/> |<span data-ttu-id="bfa55-124">Überprüft das Formular, damit die Änderungen, die seit dem letzten Speichervorgang vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="bfa55-124">Checks the form for changes that were made since the last save.</span></span>  <br/> |
|[<span data-ttu-id="bfa55-125">InitNew</span><span class="sxs-lookup"><span data-stu-id="bfa55-125">InitNew</span></span>](ipersistmessage-initnew.md) <br/> |<span data-ttu-id="bfa55-126">Initialisiert eine neue Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="bfa55-126">Initializes a new message.</span></span>  <br/> |
|[<span data-ttu-id="bfa55-127">Load</span><span class="sxs-lookup"><span data-stu-id="bfa55-127">Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="bfa55-128">Lädt das Formular für eine angegebene Nachricht.</span><span class="sxs-lookup"><span data-stu-id="bfa55-128">Loads the form for a specified message.</span></span>  <br/> |
|[<span data-ttu-id="bfa55-129">Save</span><span class="sxs-lookup"><span data-stu-id="bfa55-129">Save</span></span>](ipersistmessage-save.md) <br/> |<span data-ttu-id="bfa55-130">Speichert eine überarbeitete Formular an die Nachricht aus der es geladen oder erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="bfa55-130">Saves a revised form back to the message from which it was loaded or created.</span></span>  <br/> |
|[<span data-ttu-id="bfa55-131">SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="bfa55-131">SaveCompleted</span></span>](ipersistmessage-savecompleted.md) <br/> |<span data-ttu-id="bfa55-132">Das Formular benachrichtigt, einen Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="bfa55-132">Notifies the form that a save operation has been completed.</span></span>  <br/> |
|[<span data-ttu-id="bfa55-133">HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="bfa55-133">HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md) <br/> |<span data-ttu-id="bfa55-134">Bewirkt, dass das Formular, um die aktuelle Nachricht freigeben.</span><span class="sxs-lookup"><span data-stu-id="bfa55-134">Causes the form to release its current message.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bfa55-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bfa55-135">Remarks</span></span>

<span data-ttu-id="bfa55-136">Alle Formulare sind erforderlich, um die **IPersistMessage** -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="bfa55-136">All forms are required to implement the **IPersistMessage** interface.</span></span> 
  
 <span data-ttu-id="bfa55-137">**IPersistMessage** funktioniert ähnlich wie die OLE [IPersistStorage](http://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="bfa55-137">**IPersistMessage** works similarly to the OLE [IPersistStorage](http://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) interface.</span></span> <span data-ttu-id="bfa55-138">Weitere Informationen finden Sie unter die **IPersistStorage** -Methoden.</span><span class="sxs-lookup"><span data-stu-id="bfa55-138">For more information, see the **IPersistStorage** methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bfa55-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bfa55-139">See also</span></span>



[<span data-ttu-id="bfa55-140">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="bfa55-140">MAPI Interfaces</span></span>](mapi-interfaces.md)

