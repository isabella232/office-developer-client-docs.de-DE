---
title: Grundlegendes zum InfoPath 2003-Objektmodell
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- InfoPath 2003-kompatible Formularvorlagen, -Objektmodell, InfoPath 2003-kompatible Objektmodell, Objektmodelle [InfoPath 2003]
localization_priority: Normal
ms.assetid: cd0a890b-5a8b-42c0-abdd-5ce28aff1ba1
description: In diesem Abschnitt wird das Objektmodell für InfoPath-Lösungen mit verwaltetem Code erläutert, und es werden allgemeine Programmieraufgaben beschrieben.
ms.openlocfilehash: 6fe649d068fd21b46e2a4d2824c1afbf8d9474ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790849"
---
# <a name="understanding-the-infopath-2003-object-model"></a><span data-ttu-id="aaf72-104">Grundlegendes zum InfoPath 2003-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="aaf72-104">Understanding the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="aaf72-105">In diesem Abschnitt wird das Objektmodell für InfoPath-Lösungen mit verwaltetem Code erläutert, und es werden allgemeine Programmieraufgaben beschrieben.</span><span class="sxs-lookup"><span data-stu-id="aaf72-105">This section discusses the object model for InfoPath managed-code solutions, and describes common programming tasks.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="aaf72-106">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="aaf72-106">In this section</span></span>

[<span data-ttu-id="aaf72-107">InfoPath 2003-kompatible Objektmodelle</span><span class="sxs-lookup"><span data-stu-id="aaf72-107">InfoPath 2003 Compatible Object Models</span></span>](infopath-2003-compatible-object-models.md)
  
> <span data-ttu-id="aaf72-108">Bietet eine Übersicht über die in InfoPath-Projekten mit verwaltetem Code verwendeten Objektmodelle.</span><span class="sxs-lookup"><span data-stu-id="aaf72-108">Provides an overview of the object models used in InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="aaf72-109">Access-Anwendungsdaten mithilfe des InfoPath 2003-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="aaf72-109">Access Application Data Using the InfoPath 2003 Object Model</span></span>](how-to-access-application-data-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="aaf72-110">Erläutert den Zugriff auf Informationen über die InfoPath-Anwendung, zum zugrunde liegenden XML-Dokument des Formulars und zur Formulardefinitionsdatei (XSF).</span><span class="sxs-lookup"><span data-stu-id="aaf72-110">Discusses how to access information about the InfoPath application, the form's underlying XML document, and the form definition (.xsf) file.</span></span>
    
[<span data-ttu-id="aaf72-111">Zugriff auf externe Datenquellen mithilfe des InfoPath 2003-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="aaf72-111">Access External Data Sources Using the InfoPath 2003 Object Model</span></span>](how-to-access-external-data-sources-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="aaf72-112">Erläutert den Zugriff auf Daten von externen Datenquellen aus.</span><span class="sxs-lookup"><span data-stu-id="aaf72-112">Discusses how to access data from external data sources.</span></span>
    
[<span data-ttu-id="aaf72-113">Access-Formulardaten mithilfe des InfoPath 2003-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="aaf72-113">Access Form Data Using the InfoPath 2003 Object Model</span></span>](how-to-access-form-data-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="aaf72-114">Erläutert den Zugriff auf Informationen über das zugrunde liegende XML-Dokument des Formulars, die enthaltenen Daten sowie Informationen zum Ausführen von Aktionen im XML-Dokument.</span><span class="sxs-lookup"><span data-stu-id="aaf72-114">Discusses how to access information about the form's underlying XML document, the data it contains, or to perform some action on the XML document.</span></span>
    
[<span data-ttu-id="aaf72-115">Anzeigen von Warnungen und Dialogfeldern mit dem InfoPath 2003-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="aaf72-115">Display Alerts and Dialog Boxes Using the InfoPath 2003 Object Model</span></span>](how-to-display-alerts-and-dialog-boxes-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="aaf72-116">Erläutert das Anzeigen von Warnungen und Dialogfeldern in InfoPath-Projekten mit verwaltetem Code.</span><span class="sxs-lookup"><span data-stu-id="aaf72-116">Discusses how to display alerts and dialog boxes in InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="aaf72-117">Behandeln von Fehlern mit dem InfoPath 2003-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="aaf72-117">Handle Errors Using the InfoPath 2003 Object Model</span></span>](how-to-handle-errors-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="aaf72-118">Erläutert das Behandeln von Fehlern in InfoPath-Projekten mit verwaltetem Code.</span><span class="sxs-lookup"><span data-stu-id="aaf72-118">Discusses how to handle errors in InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="aaf72-119">Reagieren auf Formularereignisse mithilfe des InfoPath 2003-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="aaf72-119">Respond to Form Events Using the InfoPath 2003 Object Model</span></span>](how-to-respond-to-form-events-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="aaf72-120">Erläutert das Erstellen von Ereignishandlern, die auf Ereignisse reagieren, die auftreten, wenn ein Benutzer ein Formular ausfüllt.</span><span class="sxs-lookup"><span data-stu-id="aaf72-120">Discusses how to create event handlers that respond to events that occur as a user fills out a form.</span></span>
    
[<span data-ttu-id="aaf72-121">Arbeiten Sie mit Formularfenstern mithilfe des InfoPath 2003-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="aaf72-121">Work with Form Windows Using the InfoPath 2003 Object Model</span></span>](how-to-work-with-form-windows-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="aaf72-122">Erläutert das Arbeiten mit Formularfenstern.</span><span class="sxs-lookup"><span data-stu-id="aaf72-122">Discusses how to work with form windows.</span></span>
    
[<span data-ttu-id="aaf72-123">Arbeiten Sie mit Ansichten mithilfe des InfoPath 2003-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="aaf72-123">Work with Views Using the InfoPath 2003 Object Model</span></span>](how-to-work-with-views-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="aaf72-124">Erläutert das Arbeiten mit Ansichten.</span><span class="sxs-lookup"><span data-stu-id="aaf72-124">Discusses how to work with views.</span></span>
    
[<span data-ttu-id="aaf72-125">Arbeiten Sie mit digitalen Signaturen mithilfe des InfoPath 2003-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="aaf72-125">Work with Digital Signatures Using the InfoPath 2003 Object Model</span></span>](how-to-work-with-digital-signatures-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="aaf72-126">Erläutert das Arbeiten mit digitalen Signaturen.</span><span class="sxs-lookup"><span data-stu-id="aaf72-126">Discusses how to work with digital signatures.</span></span>
    
[<span data-ttu-id="aaf72-127">Arbeiten Sie mit Offlinelösungen mithilfe des InfoPath 2003-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="aaf72-127">Work with Offline Solutions Using the InfoPath 2003 Object Model</span></span>](how-to-work-with-offline-solutions-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="aaf72-128">Erläutert das Arbeiten mit Offlinelösungen.</span><span class="sxs-lookup"><span data-stu-id="aaf72-128">Discusses how to work with offline solutions.</span></span>
    

