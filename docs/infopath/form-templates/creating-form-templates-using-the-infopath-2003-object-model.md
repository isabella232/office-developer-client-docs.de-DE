---
title: Erstellen von Formularvorlagen mit dem InfoPath-Objektmodell 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- InfoPath 2003-kompatible Formularvorlagen, erstellen, Objektmodelle [InfoPath 2003], Erstellen von Formularvorlagen mit verwaltetem Code für InfoPath 2007, Formularvorlagen [InfoPath 2007], Erstellen von InfoPath 2003-kompatibel
localization_priority: Normal
ms.assetid: e0513178-ddcb-4086-ab19-1bc80cf114cc
description: In diesem Abschnitt wird Initialisierungs- und Bereinigungscode sowie das Hinzufügen von Ereignishandlern, Debuggen und das Bereitstellen von InfoPath-Formularvorlagen erläutert, die das InfoPath 2003-kompatible Objektmodell verwenden, die Unterstützung von Threads und das Arbeiten mit Microsoft XML Core Services (MSXML) aus InfoPath-Lösungen mit verwaltetem Code.
ms.openlocfilehash: 5069636dde87eb473a2b8bef4b58a6006d557085
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410532"
---
# <a name="creating-form-templates-using-the-infopath-2003-object-model"></a><span data-ttu-id="eb6c9-104">Erstellen von Formularvorlagen mit dem InfoPath-Objektmodell 2003</span><span class="sxs-lookup"><span data-stu-id="eb6c9-104">Creating Form Templates Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="eb6c9-105">In diesem Abschnitt wird Initialisierungs- und Bereinigungscode sowie das Hinzufügen von Ereignishandlern, Debuggen und das Bereitstellen von InfoPath-Formularvorlagen erläutert, die das InfoPath 2003-kompatible Objektmodell verwenden, die Unterstützung von Threads und das Arbeiten mit Microsoft XML Core Services (MSXML) aus InfoPath-Lösungen mit verwaltetem Code.</span><span class="sxs-lookup"><span data-stu-id="eb6c9-105">This section discusses initialization and clean-up code, how to add event handlers, how to debug and deploy InfoPath form templates that use the InfoPath 2003-compatible object model, threading support, and working with Microsoft XML Core Services (MSXML) from InfoPath managed-code solutions.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="eb6c9-106">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="eb6c9-106">In this section</span></span>

[<span data-ttu-id="eb6c9-107">Initialisierungs- und Bereinigungscode mit dem InfoPath 2003-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="eb6c9-107">Initialization and Clean-up Code Using InfoPath 2003 Object Model</span></span>](initialization-and-clean-up-code-using-infopath-2003-object-model.md)
  
> <span data-ttu-id="eb6c9-108">Enthält Erklärungen zum Schreiben von Initialisierungs- und Bereinigungscode in den Methoden "_Startup" und "_Shutdown" Ihres Projekts.</span><span class="sxs-lookup"><span data-stu-id="eb6c9-108">Discusses how to write initialization and clean-up code in the _Startup and _Shutdown methods of your project.</span></span>
    
[<span data-ttu-id="eb6c9-109">Hinzufügen eines Ereignishandlers mit dem InfoPath-Objektmodell 2003</span><span class="sxs-lookup"><span data-stu-id="eb6c9-109">Add an Event Handler Using the InfoPath 2003 Object Model</span></span>](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="eb6c9-110">Erläutert, wie Ereignishandler und die Attribute zur Identifizierung von Ereignishandlern angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb6c9-110">Discusses how to add event handlers and the attributes that are applied to identify event handlers.</span></span>
    
[<span data-ttu-id="eb6c9-111">Debuggen von InfoPath-Projekten mit dem InfoPath-2003-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="eb6c9-111">Debug InfoPath Projects Using the InfoPath 2003 Object Model</span></span>](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="eb6c9-112">Erläutert das Debuggen von InfoPath-Projekten mit verwaltetem Code.</span><span class="sxs-lookup"><span data-stu-id="eb6c9-112">Discusses how to debug InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="eb6c9-113">Bereitstellen von InfoPath-Formularvorlagen mit Code</span><span class="sxs-lookup"><span data-stu-id="eb6c9-113">Deploy InfoPath Form Templates with Code</span></span>](how-to-deploy-infopath-form-templates-with-code.md)
  
> <span data-ttu-id="eb6c9-114">Erläutert die Bereitstellung von InfoPath-Projekten mit verwaltetem Code.</span><span class="sxs-lookup"><span data-stu-id="eb6c9-114">Discusses how to deploy InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="eb6c9-115">Threadunterstützung in InfoPath-Projekten mit dem InfoPath 2003-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="eb6c9-115">Threading Support in InfoPath Projects Using the InfoPath 2003 Object Model</span></span>](threading-support-in-infopath-projects-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="eb6c9-116">Erläutert die Unterstützung von Threads in InfoPath-Projekten mit verwaltetem Code.</span><span class="sxs-lookup"><span data-stu-id="eb6c9-116">Discusses threading support in InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="eb6c9-117">Arbeiten mit MSXML und System.Xml mit dem InfoPath 2003-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="eb6c9-117">Working with MSXML and System.Xml Using the InfoPath 2003 Object Model</span></span>](working-with-msxml-and-system-xml-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="eb6c9-118">Erläutert den Umgang mit MSXML- und System.Xml-Code in InfoPath-Projekten mit verwaltetem Code.</span><span class="sxs-lookup"><span data-stu-id="eb6c9-118">Discusses how to work with MSXML and System.Xml code in InfoPath managed-code projects.</span></span>
    

