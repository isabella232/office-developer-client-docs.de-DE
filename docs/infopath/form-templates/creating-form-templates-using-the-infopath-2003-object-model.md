---
title: Erstellen von Formularvorlagen mithilfe des InfoPath 2003-Objektmodells
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- InfoPath 2003-kompatible Formularvorlagen erstellen, Objektmodelle [InfoPath 2003], Erstellen von verwaltetem Code Formularvorlagen für InfoPath 2007-Formularvorlagen [InfoPath 2007], Erstellen von InfoPath 2003-kompatible
localization_priority: Normal
ms.assetid: e0513178-ddcb-4086-ab19-1bc80cf114cc
description: In diesem Abschnitt wird Initialisierungs- und Bereinigungscode sowie das Hinzufügen von Ereignishandlern, Debuggen und das Bereitstellen von InfoPath-Formularvorlagen erläutert, die das InfoPath 2003-kompatible Objektmodell verwenden, die Unterstützung von Threads und das Arbeiten mit Microsoft XML Core Services (MSXML) aus InfoPath-Lösungen mit verwaltetem Code.
ms.openlocfilehash: 16d49b24b2eed3b7fe15621d47663a94f1958cfa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790724"
---
# <a name="creating-form-templates-using-the-infopath-2003-object-model"></a><span data-ttu-id="e94a7-104">Erstellen von Formularvorlagen mithilfe des InfoPath 2003-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="e94a7-104">Creating Form Templates Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="e94a7-105">In diesem Abschnitt wird Initialisierungs- und Bereinigungscode sowie das Hinzufügen von Ereignishandlern, Debuggen und das Bereitstellen von InfoPath-Formularvorlagen erläutert, die das InfoPath 2003-kompatible Objektmodell verwenden, die Unterstützung von Threads und das Arbeiten mit Microsoft XML Core Services (MSXML) aus InfoPath-Lösungen mit verwaltetem Code.</span><span class="sxs-lookup"><span data-stu-id="e94a7-105">This section discusses initialization and clean-up code, how to add event handlers, how to debug and deploy InfoPath form templates that use the InfoPath 2003-compatible object model, threading support, and working with Microsoft XML Core Services (MSXML) from InfoPath managed-code solutions.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="e94a7-106">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="e94a7-106">In this section</span></span>

[<span data-ttu-id="e94a7-107">Initialisierungs- und Bereinigungscode Code mit InfoPath 2003-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="e94a7-107">Initialization and Clean-up Code Using InfoPath 2003 Object Model</span></span>](initialization-and-clean-up-code-using-infopath-2003-object-model.md)
  
> <span data-ttu-id="e94a7-108">Enthält Erklärungen zum Schreiben von Initialisierungs- und Bereinigungscode in den Methoden "_Startup" und "_Shutdown" Ihres Projekts.</span><span class="sxs-lookup"><span data-stu-id="e94a7-108">Discusses how to write initialization and clean-up code in the _Startup and _Shutdown methods of your project.</span></span>
    
[<span data-ttu-id="e94a7-109">Hinzufügen eines Ereignishandlers mit dem InfoPath 2003-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="e94a7-109">Add an Event Handler Using the InfoPath 2003 Object Model</span></span>](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="e94a7-110">Erläutert, wie Ereignishandler und die Attribute zur Identifizierung von Ereignishandlern angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="e94a7-110">Discusses how to add event handlers and the attributes that are applied to identify event handlers.</span></span>
    
[<span data-ttu-id="e94a7-111">Debuggen von InfoPath-Projekten mit dem InfoPath 2003-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="e94a7-111">Debug InfoPath Projects Using the InfoPath 2003 Object Model</span></span>](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="e94a7-112">Erläutert das Debuggen von InfoPath-Projekten mit verwaltetem Code.</span><span class="sxs-lookup"><span data-stu-id="e94a7-112">Discusses how to debug InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="e94a7-113">Bereitstellen von InfoPath-Formularvorlagen mit Code</span><span class="sxs-lookup"><span data-stu-id="e94a7-113">Deploy InfoPath Form Templates with Code</span></span>](how-to-deploy-infopath-form-templates-with-code.md)
  
> <span data-ttu-id="e94a7-114">Erläutert die Bereitstellung von InfoPath-Projekten mit verwaltetem Code.</span><span class="sxs-lookup"><span data-stu-id="e94a7-114">Discusses how to deploy InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="e94a7-115">Threadunterstützung in InfoPath-Projekten mit dem InfoPath 2003-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="e94a7-115">Threading Support in InfoPath Projects Using the InfoPath 2003 Object Model</span></span>](threading-support-in-infopath-projects-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="e94a7-116">Erläutert die Unterstützung von Threads in InfoPath-Projekten mit verwaltetem Code.</span><span class="sxs-lookup"><span data-stu-id="e94a7-116">Discusses threading support in InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="e94a7-117">Arbeiten mit MSXML und System.Xml mit dem InfoPath 2003-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="e94a7-117">Working with MSXML and System.Xml Using the InfoPath 2003 Object Model</span></span>](working-with-msxml-and-system-xml-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="e94a7-118">Erläutert den Umgang mit MSXML- und System.Xml-Code in InfoPath-Projekten mit verwaltetem Code.</span><span class="sxs-lookup"><span data-stu-id="e94a7-118">Discusses how to work with MSXML and System.Xml code in InfoPath managed-code projects.</span></span>
    

