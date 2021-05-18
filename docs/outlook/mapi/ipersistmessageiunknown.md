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
ms.openlocfilehash: 7eb65bbae2fca6648c3a701dfa5c83c5bf297ec5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309604"
---
# <a name="ipersistmessage--iunknown"></a><span data-ttu-id="3c19b-103">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3c19b-103">IPersistMessage : IUnknown</span></span>

  
  
<span data-ttu-id="3c19b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c19b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c19b-105">Ermöglicht Formularanzeigen die Verarbeitung des Speichers eines Formulars und den Übergang zwischen den verschiedenen Zuständen.</span><span class="sxs-lookup"><span data-stu-id="3c19b-105">Enables form viewers to handle the storage of a form and to transition between the various states.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3c19b-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="3c19b-106">Header file:</span></span>  <br/> |<span data-ttu-id="3c19b-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="3c19b-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="3c19b-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="3c19b-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="3c19b-109">Beibehalten von Nachrichtenobjekten</span><span class="sxs-lookup"><span data-stu-id="3c19b-109">Persist message objects</span></span>  <br/> |
|<span data-ttu-id="3c19b-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="3c19b-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="3c19b-111">Formularobjekte</span><span class="sxs-lookup"><span data-stu-id="3c19b-111">Form objects</span></span>  <br/> |
|<span data-ttu-id="3c19b-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="3c19b-112">Called by:</span></span>  <br/> |<span data-ttu-id="3c19b-113">Formularanzeigen</span><span class="sxs-lookup"><span data-stu-id="3c19b-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="3c19b-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="3c19b-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="3c19b-115">IID_IPersistMessage</span><span class="sxs-lookup"><span data-stu-id="3c19b-115">IID_IPersistMessage</span></span>  <br/> |
|<span data-ttu-id="3c19b-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="3c19b-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="3c19b-117">LPPERSISTMESSAGE</span><span class="sxs-lookup"><span data-stu-id="3c19b-117">LPPERSISTMESSAGE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="3c19b-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="3c19b-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="3c19b-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="3c19b-119">GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="3c19b-120">Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Fehler im Formularobjekt enthält.</span><span class="sxs-lookup"><span data-stu-id="3c19b-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error in the form object.</span></span>  <br/> |
|[<span data-ttu-id="3c19b-121">GetClassID</span><span class="sxs-lookup"><span data-stu-id="3c19b-121">GetClassID</span></span>](ipersistmessage-getclassid.md) <br/> |<span data-ttu-id="3c19b-122">Gibt einen Bezeichner zurück, der den Formularserver darstellt, der das Formular verwalten kann.</span><span class="sxs-lookup"><span data-stu-id="3c19b-122">Returns an identifier that represents the form server that can manage the form.</span></span>  <br/> |
|[<span data-ttu-id="3c19b-123">IsDirty</span><span class="sxs-lookup"><span data-stu-id="3c19b-123">IsDirty</span></span>](ipersistmessage-isdirty.md) <br/> |<span data-ttu-id="3c19b-124">Überprüft das Formular auf Änderungen, die seit dem letzten Speichern vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="3c19b-124">Checks the form for changes that were made since the last save.</span></span>  <br/> |
|[<span data-ttu-id="3c19b-125">InitNew</span><span class="sxs-lookup"><span data-stu-id="3c19b-125">InitNew</span></span>](ipersistmessage-initnew.md) <br/> |<span data-ttu-id="3c19b-126">Initialisiert eine neue Nachricht.</span><span class="sxs-lookup"><span data-stu-id="3c19b-126">Initializes a new message.</span></span>  <br/> |
|[<span data-ttu-id="3c19b-127">Load</span><span class="sxs-lookup"><span data-stu-id="3c19b-127">Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="3c19b-128">Lädt das Formular für eine angegebene Nachricht.</span><span class="sxs-lookup"><span data-stu-id="3c19b-128">Loads the form for a specified message.</span></span>  <br/> |
|[<span data-ttu-id="3c19b-129">Save</span><span class="sxs-lookup"><span data-stu-id="3c19b-129">Save</span></span>](ipersistmessage-save.md) <br/> |<span data-ttu-id="3c19b-130">Speichert ein überarbeitetes Formular in der Nachricht zurück, aus der es geladen oder erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="3c19b-130">Saves a revised form back to the message from which it was loaded or created.</span></span>  <br/> |
|[<span data-ttu-id="3c19b-131">SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="3c19b-131">SaveCompleted</span></span>](ipersistmessage-savecompleted.md) <br/> |<span data-ttu-id="3c19b-132">Benachrichtigt das Formular, dass ein Speichervorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="3c19b-132">Notifies the form that a save operation has been completed.</span></span>  <br/> |
|[<span data-ttu-id="3c19b-133">HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="3c19b-133">HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md) <br/> |<span data-ttu-id="3c19b-134">Bewirkt, dass das Formular seine aktuelle Nachricht veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="3c19b-134">Causes the form to release its current message.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3c19b-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3c19b-135">Remarks</span></span>

<span data-ttu-id="3c19b-136">Alle Formulare sind erforderlich, um die **IPersistMessage-Schnittstelle zu** implementieren.</span><span class="sxs-lookup"><span data-stu-id="3c19b-136">All forms are required to implement the **IPersistMessage** interface.</span></span> 
  
 <span data-ttu-id="3c19b-137">**IPersistMessage** funktioniert ähnlich wie die OLE [IPersistStorage-Schnittstelle.](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3c19b-137">**IPersistMessage** works similarly to the OLE [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) interface.</span></span> <span data-ttu-id="3c19b-138">Weitere Informationen finden Sie unter **IPersistStorage-Methoden.**</span><span class="sxs-lookup"><span data-stu-id="3c19b-138">For more information, see the **IPersistStorage** methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3c19b-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c19b-139">See also</span></span>



[<span data-ttu-id="3c19b-140">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="3c19b-140">MAPI Interfaces</span></span>](mapi-interfaces.md)

