---
title: IMAPIViewContext IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext
api_type:
- COM
ms.assetid: d566ff39-92c1-4a14-85e5-1c406825f805
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: db0c375218755c3a28475e2ebce2d097fb789f75
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406031"
---
# <a name="imapiviewcontext--iunknown"></a><span data-ttu-id="b2736-103">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b2736-103">IMAPIViewContext : IUnknown</span></span>

  
  
<span data-ttu-id="b2736-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2736-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2736-105">Verwaltet ein Formular im Formular-Viewer einer Clientanwendung.</span><span class="sxs-lookup"><span data-stu-id="b2736-105">Manages a form in a client application's form viewer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b2736-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="b2736-106">Header file:</span></span>  <br/> |<span data-ttu-id="b2736-107">Mapiform. h</span><span class="sxs-lookup"><span data-stu-id="b2736-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="b2736-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="b2736-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="b2736-109">Anzeigen von Kontextobjekten</span><span class="sxs-lookup"><span data-stu-id="b2736-109">View context objects</span></span>  <br/> |
|<span data-ttu-id="b2736-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="b2736-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="b2736-111">Formular Betrachter</span><span class="sxs-lookup"><span data-stu-id="b2736-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="b2736-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="b2736-112">Called by:</span></span>  <br/> |<span data-ttu-id="b2736-113">Formularobjekte</span><span class="sxs-lookup"><span data-stu-id="b2736-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="b2736-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="b2736-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b2736-115">IID_IMAPIViewContext</span><span class="sxs-lookup"><span data-stu-id="b2736-115">IID_IMAPIViewContext</span></span>  <br/> |
|<span data-ttu-id="b2736-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="b2736-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="b2736-117">LPMAPIVIEWCONTEXT</span><span class="sxs-lookup"><span data-stu-id="b2736-117">LPMAPIVIEWCONTEXT</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b2736-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="b2736-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="b2736-119">SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="b2736-119">SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md) <br/> |<span data-ttu-id="b2736-120">Verwaltet die Registrierung eines Formulars, um Benachrichtigungen zu Änderungen im Viewer zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b2736-120">Manages a form's registration to receive notifications about changes in the viewer.</span></span>  <br/> |
|[<span data-ttu-id="b2736-121">ActivateNext</span><span class="sxs-lookup"><span data-stu-id="b2736-121">ActivateNext</span></span>](imapiviewcontext-activatenext.md) <br/> |<span data-ttu-id="b2736-122">Aktiviert die nächste oder vorherige Nachricht im Formular-Viewer.</span><span class="sxs-lookup"><span data-stu-id="b2736-122">Activates the next or previous message in the form viewer.</span></span>  <br/> |
|[<span data-ttu-id="b2736-123">GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="b2736-123">GetPrintSetup</span></span>](imapiviewcontext-getprintsetup.md) <br/> |<span data-ttu-id="b2736-124">Ruft aktuelle Druckinformationen ab.</span><span class="sxs-lookup"><span data-stu-id="b2736-124">Retrieves current printing information.</span></span>  <br/> |
|[<span data-ttu-id="b2736-125">GetSaveStream</span><span class="sxs-lookup"><span data-stu-id="b2736-125">GetSaveStream</span></span>](imapiviewcontext-getsavestream.md) <br/> |<span data-ttu-id="b2736-126">Ruft einen Stream ab, der zum Speichern der aktuellen Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2736-126">Retrieves a stream to be used for saving the current message.</span></span>  <br/> |
|[<span data-ttu-id="b2736-127">GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="b2736-127">GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md) <br/> |<span data-ttu-id="b2736-128">Ruft den aktuellen viewerstatus ab.</span><span class="sxs-lookup"><span data-stu-id="b2736-128">Retrieves the current viewer status.</span></span>  <br/> |
|[<span data-ttu-id="b2736-129">Getlasterroraufzurufen</span><span class="sxs-lookup"><span data-stu-id="b2736-129">GetLastError</span></span>](imapiviewcontext-getlasterror.md) <br/> |<span data-ttu-id="b2736-130">Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen über den vorherigen Fehler enthält, der im View-Kontextobjekt auftritt.</span><span class="sxs-lookup"><span data-stu-id="b2736-130">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring in the view context object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b2736-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2736-131">See also</span></span>



[<span data-ttu-id="b2736-132">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b2736-132">MAPI Interfaces</span></span>](mapi-interfaces.md)

