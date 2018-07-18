---
title: QUEUEMARKEREVENT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60107
localization_priority: Normal
ms.assetid: b4671715-4209-7774-c174-c19dc9721a02
description: Bewirkt, dass die Anwendung ein Markerereignis für das Add-on, Microsoft Visual Basic für Applikationen (VBA)-Code oder COM-add-in auslöst.
ms.openlocfilehash: b9175caf0845530c93f6db15e286f3eae21ea415
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797757"
---
# <a name="queuemarkerevent-function"></a><span data-ttu-id="ad536-103">QUEUEMARKEREVENT Function</span><span class="sxs-lookup"><span data-stu-id="ad536-103">QUEUEMARKEREVENT Function</span></span>

<span data-ttu-id="ad536-104">Bewirkt, dass die Anwendung ein Markerereignis für das Add-on, Microsoft Visual Basic für Applikationen (VBA)-Code oder COM-add-in auslöst.</span><span class="sxs-lookup"><span data-stu-id="ad536-104">Causes the application to fire a marker event to your add-on, Microsoft Visual Basic for Applications (VBA) code, or COM add-in.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ad536-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad536-105">Syntax</span></span>

<span data-ttu-id="ad536-106">QUEUEMARKEREVENT (** *Zeichenfolge Event_string* **)</span><span class="sxs-lookup"><span data-stu-id="ad536-106">QUEUEMARKEREVENT (** *event_string* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ad536-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad536-107">Parameters</span></span>

|<span data-ttu-id="ad536-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="ad536-108">**Name**</span></span>|<span data-ttu-id="ad536-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="ad536-109">**Required/Optional**</span></span>|<span data-ttu-id="ad536-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="ad536-110">**Data Type**</span></span>|<span data-ttu-id="ad536-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ad536-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ad536-112">_Zeichenfolge event_string_</span><span class="sxs-lookup"><span data-stu-id="ad536-112">_event_string_</span></span> <br/> |<span data-ttu-id="ad536-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ad536-113">Required</span></span>  <br/> |<span data-ttu-id="ad536-114">**String**</span><span class="sxs-lookup"><span data-stu-id="ad536-114">**String**</span></span> <br/> | <span data-ttu-id="ad536-115">Die Zeichenfolge, die an den Ereignishandler übergeben.</span><span class="sxs-lookup"><span data-stu-id="ad536-115">The string to pass to your event handler.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad536-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad536-116">Remarks</span></span>

<span data-ttu-id="ad536-117">Die QUEUEMARKEREVENT-Funktion bietet Entwicklern eine Möglichkeit Codeprobleme aus einer ShapeSheet-Zelle zu benachrichtigen und lösungsspezifische Informationen übergeben.</span><span class="sxs-lookup"><span data-stu-id="ad536-117">The QUEUEMARKEREVENT function provides developers with a way to notify their code from a ShapeSheet cell, and pass solution-specific information.</span></span> <span data-ttu-id="ad536-118">Wenn die Zelle mit der Formel mit der QUEUEMARKEREVENT-Funktion ausgewertet wird, wird die Anwendung ein Markerereignis löst und übergibt die _Zeichenfolge Event_string_ an alle Ereignishandler, die auf das **MarkerEvent** -Ereignis warten.</span><span class="sxs-lookup"><span data-stu-id="ad536-118">When the cell containing the formula with the QUEUEMARKEREVENT function is evaluated, the application fires a marker event and passes  _event_string_ to all event handlers that are listening to the **MarkerEvent** event.</span></span> 
  
<span data-ttu-id="ad536-119">Weitere Informationen zu Markerereignissen finden Sie unter **QueueMarkerEvent** -Methode und **MarkerEvent** -Ereignis Themen in der Microsoft Visio Automation Reference.</span><span class="sxs-lookup"><span data-stu-id="ad536-119">For more information about marker events, see the **QueueMarkerEvent** method and **MarkerEvent** event topics in the Microsoft Visio Automation Reference.</span></span> 
  
## <a name="example"></a><span data-ttu-id="ad536-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ad536-120">Example</span></span>

<span data-ttu-id="ad536-121">QUEUEMARKEREVENT ("MyCustomNotification")</span><span class="sxs-lookup"><span data-stu-id="ad536-121">QUEUEMARKEREVENT ("MyCustomNotification")</span></span> 
  
<span data-ttu-id="ad536-122">Bewirkt, dass die Anwendung ein Markerereignis auslöst und die Zeichenfolge "MyCustomNotification" an die Ereignishandler übergibt, die auf das **MarkerEvent**-Ereignis warten.</span><span class="sxs-lookup"><span data-stu-id="ad536-122">Causes the application to fire a marker event, and passes the string "MyCustomNotification" to event handlers that are listening to the **MarkerEvent** event.</span></span> 
  

