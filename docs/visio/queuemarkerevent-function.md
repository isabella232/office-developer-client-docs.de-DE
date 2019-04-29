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
description: Bewirkt, dass die Anwendung ein Marker-Ereignis für Ihr Add-on, Microsoft Visual Basic für Applikationen (VBA)-Code oder ein COM-Add-in auslöst.
ms.openlocfilehash: 841f6acc63497a6f0b8930c89534b5f8b04c0393
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418806"
---
# <a name="queuemarkerevent-function"></a><span data-ttu-id="76bce-103">QUEUEMARKEREVENT Function</span><span class="sxs-lookup"><span data-stu-id="76bce-103">QUEUEMARKEREVENT Function</span></span>

<span data-ttu-id="76bce-104">Bewirkt, dass die Anwendung ein Marker-Ereignis für Ihr Add-on, Microsoft Visual Basic für Applikationen (VBA)-Code oder ein COM-Add-in auslöst.</span><span class="sxs-lookup"><span data-stu-id="76bce-104">Causes the application to fire a marker event to your add-on, Microsoft Visual Basic for Applications (VBA) code, or COM add-in.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="76bce-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="76bce-105">Syntax</span></span>

<span data-ttu-id="76bce-106">QUEUEMARKEREVENT (\* \* *event_string* \* \*)</span><span class="sxs-lookup"><span data-stu-id="76bce-106">QUEUEMARKEREVENT (\*\* *event_string* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="76bce-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="76bce-107">Parameters</span></span>

|<span data-ttu-id="76bce-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="76bce-108">**Name**</span></span>|<span data-ttu-id="76bce-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="76bce-109">**Required/Optional**</span></span>|<span data-ttu-id="76bce-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="76bce-110">**Data Type**</span></span>|<span data-ttu-id="76bce-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="76bce-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="76bce-112">_event_string_</span><span class="sxs-lookup"><span data-stu-id="76bce-112">_event_string_</span></span> <br/> |<span data-ttu-id="76bce-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="76bce-113">Required</span></span>  <br/> |<span data-ttu-id="76bce-114">**String**</span><span class="sxs-lookup"><span data-stu-id="76bce-114">**String**</span></span> <br/> | <span data-ttu-id="76bce-115">Die an den Ereignishandler zu übergebende Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="76bce-115">The string to pass to your event handler.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76bce-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76bce-116">Remarks</span></span>

<span data-ttu-id="76bce-117">Die QUEUEMARKEREVENT-Funktion bietet Entwicklern die Möglichkeit, ihren Code über eine ShapeSheet-Zelle zu benachrichtigen und lösungsspezifische Informationen zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="76bce-117">The QUEUEMARKEREVENT function provides developers with a way to notify their code from a ShapeSheet cell, and pass solution-specific information.</span></span> <span data-ttu-id="76bce-118">Wenn die Zelle mit der Formel mit der QUEUEMARKEREVENT-Funktion ausgewertet wird, löst die Anwendung ein Marker-Ereignis und übergibt _event_string_ an alle Ereignishandler, die das **MarkerEvent** -Ereignis überwachen.</span><span class="sxs-lookup"><span data-stu-id="76bce-118">When the cell containing the formula with the QUEUEMARKEREVENT function is evaluated, the application fires a marker event and passes  _event_string_ to all event handlers that are listening to the **MarkerEvent** event.</span></span> 
  
<span data-ttu-id="76bce-119">Weitere Informationen zu Marker-Ereignissen finden Sie unter den Themen **QueueMarkerEvent** -Methode und **MarkerEvent** -Ereignis in der Microsoft Visio-Automatisierungsreferenz.</span><span class="sxs-lookup"><span data-stu-id="76bce-119">For more information about marker events, see the **QueueMarkerEvent** method and **MarkerEvent** event topics in the Microsoft Visio Automation Reference.</span></span> 
  
## <a name="example"></a><span data-ttu-id="76bce-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="76bce-120">Example</span></span>

<span data-ttu-id="76bce-121">QUEUEMARKEREVENT ("MyCustomNotification")</span><span class="sxs-lookup"><span data-stu-id="76bce-121">QUEUEMARKEREVENT ("MyCustomNotification")</span></span> 
  
<span data-ttu-id="76bce-122">Bewirkt, dass die Anwendung ein Markerereignis auslöst und die Zeichenfolge "MyCustomNotification" an die Ereignishandler übergibt, die auf das **MarkerEvent**-Ereignis warten.</span><span class="sxs-lookup"><span data-stu-id="76bce-122">Causes the application to fire a marker event, and passes the string "MyCustomNotification" to event handlers that are listening to the **MarkerEvent** event.</span></span> 
  

