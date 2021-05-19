---
title: Grundlegendes zum InfoPath 2003-Objektmodell
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-kompatible Formularvorlagen, Objektmodell,InfoPath 2003-kompatibles Objektmodell,Objektmodelle [InfoPath 2003]
localization_priority: Normal
ms.assetid: cd0a890b-5a8b-42c0-abdd-5ce28aff1ba1
description: In diesem Abschnitt wird das Objektmodell für InfoPath-Lösungen mit verwaltetem Code erläutert, und es werden allgemeine Programmieraufgaben beschrieben.
ms.openlocfilehash: 0c07201475bb7bfe24182faf61cc1bf6df733709
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416657"
---
# <a name="understanding-the-infopath-2003-object-model"></a><span data-ttu-id="63103-104">Grundlegendes zum InfoPath 2003-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="63103-104">Understanding the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="63103-105">In diesem Abschnitt wird das Objektmodell für InfoPath-Lösungen mit verwaltetem Code erläutert, und es werden allgemeine Programmieraufgaben beschrieben.</span><span class="sxs-lookup"><span data-stu-id="63103-105">This section discusses the object model for InfoPath managed-code solutions, and describes common programming tasks.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="63103-106">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="63103-106">In this section</span></span>

[<span data-ttu-id="63103-107">InfoPath 2003-kompatible Objektmodelle</span><span class="sxs-lookup"><span data-stu-id="63103-107">InfoPath 2003 Compatible Object Models</span></span>](infopath-2003-compatible-object-models.md)
  
> <span data-ttu-id="63103-108">Bietet eine Übersicht über die in InfoPath-Projekten mit verwaltetem Code verwendeten Objektmodelle.</span><span class="sxs-lookup"><span data-stu-id="63103-108">Provides an overview of the object models used in InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="63103-109">Zugreifen auf Anwendungsdaten mithilfe des InfoPath 2003-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="63103-109">Access Application Data Using the InfoPath 2003 Object Model</span></span>](how-to-access-application-data-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="63103-110">Erläutert den Zugriff auf Informationen über die InfoPath-Anwendung, zum zugrunde liegenden XML-Dokument des Formulars und zur Formulardefinitionsdatei (XSF).</span><span class="sxs-lookup"><span data-stu-id="63103-110">Discusses how to access information about the InfoPath application, the form's underlying XML document, and the form definition (.xsf) file.</span></span>
    
[<span data-ttu-id="63103-111">Zugreifen auf externe Datenquellen mithilfe des InfoPath 2003-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="63103-111">Access External Data Sources Using the InfoPath 2003 Object Model</span></span>](how-to-access-external-data-sources-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="63103-112">Erläutert das Zugreifen auf Daten aus externen Datenquellen.</span><span class="sxs-lookup"><span data-stu-id="63103-112">Discusses how to access data from external data sources.</span></span>
    
[<span data-ttu-id="63103-113">Zugreifen auf Formulardaten mithilfe des InfoPath 2003-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="63103-113">Access Form Data Using the InfoPath 2003 Object Model</span></span>](how-to-access-form-data-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="63103-114">Erläutert, wie auf Informationen zum dem Formular zugrunde liegenden XML-Dokument und auf die enthaltenen Daten zugegriffen wird oder Aktionen im XML-Dokument ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="63103-114">Discusses how to access information about the form's underlying XML document, the data it contains, or to perform some action on the XML document.</span></span>
    
[<span data-ttu-id="63103-115">Anzeigen von Warnungen und Dialogfelder mithilfe des InfoPath 2003-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="63103-115">Display Alerts and Dialog Boxes Using the InfoPath 2003 Object Model</span></span>](how-to-display-alerts-and-dialog-boxes-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="63103-116">Erläutert das Anzeigen von Warnungen und Dialogfeldern in InfoPath-Projekten mit verwaltetem Code.</span><span class="sxs-lookup"><span data-stu-id="63103-116">Discusses how to display alerts and dialog boxes in InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="63103-117">Behandeln von Fehlern mithilfe des InfoPath 2003-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="63103-117">Handle Errors Using the InfoPath 2003 Object Model</span></span>](how-to-handle-errors-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="63103-118">Erläutert die Fehlerbehandlung in InfoPath-Projekten mit verwaltetem Code.</span><span class="sxs-lookup"><span data-stu-id="63103-118">Discusses how to handle errors in InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="63103-119">Antworten auf Formularereignisse mithilfe des InfoPath 2003-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="63103-119">Respond to Form Events Using the InfoPath 2003 Object Model</span></span>](how-to-respond-to-form-events-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="63103-120">Erläutert das Erstellen von Ereignishandlern, die auf Ereignisse reagieren, die auftreten, wenn ein Benutzer ein Formular ausfüllt.</span><span class="sxs-lookup"><span data-stu-id="63103-120">Discusses how to create event handlers that respond to events that occur as a user fills out a form.</span></span>
    
[<span data-ttu-id="63103-121">Arbeiten mit formular Windows Verwenden des InfoPath 2003-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="63103-121">Work with Form Windows Using the InfoPath 2003 Object Model</span></span>](how-to-work-with-form-windows-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="63103-122">Erläutert das Arbeiten mit Formularfenstern.</span><span class="sxs-lookup"><span data-stu-id="63103-122">Discusses how to work with form windows.</span></span>
    
[<span data-ttu-id="63103-123">Arbeiten mit Ansichten mithilfe des InfoPath 2003-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="63103-123">Work with Views Using the InfoPath 2003 Object Model</span></span>](how-to-work-with-views-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="63103-124">Erläutert das Arbeiten mit Ansichten.</span><span class="sxs-lookup"><span data-stu-id="63103-124">Discusses how to work with views.</span></span>
    
[<span data-ttu-id="63103-125">Arbeiten mit digitalen Signaturen mithilfe des InfoPath 2003-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="63103-125">Work with Digital Signatures Using the InfoPath 2003 Object Model</span></span>](how-to-work-with-digital-signatures-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="63103-126">Erläutert das Arbeiten mit digitalen Signaturen.</span><span class="sxs-lookup"><span data-stu-id="63103-126">Discusses how to work with digital signatures.</span></span>
    
[<span data-ttu-id="63103-127">Arbeiten mit Offlinelösungen mithilfe des InfoPath 2003-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="63103-127">Work with Offline Solutions Using the InfoPath 2003 Object Model</span></span>](how-to-work-with-offline-solutions-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="63103-128">Erläutert das Arbeiten mit Offlinelösungen.</span><span class="sxs-lookup"><span data-stu-id="63103-128">Discusses how to work with offline solutions.</span></span>
    

