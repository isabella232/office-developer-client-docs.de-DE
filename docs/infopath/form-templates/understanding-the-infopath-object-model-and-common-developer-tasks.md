---
title: Grundlegendes zum InfoPath-Objektmodell und zu allgemeinen Entwickleraufgaben
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Beispiele [InfoPath 2007], InfoPath 2007, Entwickleraufgaben, Entwickleraufgaben [InfoPath 2007], InfoPath 2007, Objektmodelle, Objektmodelle [InfoPath 2007]
localization_priority: Normal
ms.assetid: a2c18b72-426b-4f63-8454-187e96d26199
description: Dieser Abschnitt enthält Informationen zu allgemeinen Entwickleraufgaben beim Entwickeln von InfoPath-Formularvorlagen mit verwaltetem Code.
ms.openlocfilehash: a84bf1a70407ca87e1a83f74856d363d8860d4a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418855"
---
# <a name="understanding-the-infopath-object-model-and-common-developer-tasks"></a><span data-ttu-id="3e8b0-104">Grundlegendes zum InfoPath-Objektmodell und zu allgemeinen Entwickleraufgaben</span><span class="sxs-lookup"><span data-stu-id="3e8b0-104">Understanding the InfoPath Object Model and Common Developer Tasks</span></span>

<span data-ttu-id="3e8b0-105">Dieser Abschnitt enthält Informationen zu allgemeinen Entwickleraufgaben beim Entwickeln von InfoPath-Formularvorlagen mit verwaltetem Code.</span><span class="sxs-lookup"><span data-stu-id="3e8b0-105">This section provides information on common developer tasks when developing InfoPath managed code form templates.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="3e8b0-106">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="3e8b0-106">In this section</span></span>

[<span data-ttu-id="3e8b0-107">Zugreifen auf Anwendungsdaten</span><span class="sxs-lookup"><span data-stu-id="3e8b0-107">Access Application Data</span></span>](how-to-access-application-data.md)
  
> <span data-ttu-id="3e8b0-108">Erläutert das Zugreifen auf Informationen zur InfoPath-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="3e8b0-108">Discusses how to access information about the InfoPath application.</span></span>
    
[<span data-ttu-id="3e8b0-109">Reagieren auf Formularereignisse</span><span class="sxs-lookup"><span data-stu-id="3e8b0-109">Respond to Form Events</span></span>](how-to-respond-to-form-events.md)
  
> <span data-ttu-id="3e8b0-110">Erläutert das Erstellen von Ereignishandlern, die auf Ereignisse reagieren, die auftreten, wenn ein Benutzer ein Formular ausfüllt.</span><span class="sxs-lookup"><span data-stu-id="3e8b0-110">Discusses how to create event handlers that respond to events that occur as a user fills out a form.</span></span>
    
[<span data-ttu-id="3e8b0-111">Access-Formulardaten</span><span class="sxs-lookup"><span data-stu-id="3e8b0-111">Access Form Data</span></span>](how-to-access-form-data.md)
  
> <span data-ttu-id="3e8b0-112">Erläutert, wie auf Informationen zum dem Formular zugrunde liegenden XML-Dokument und auf die enthaltenen Daten zugegriffen wird oder Aktionen im XML-Dokument ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3e8b0-112">Discusses how to access information about the form's underlying XML document, the data it contains, or to perform some action on the XML document.</span></span>
    
[<span data-ttu-id="3e8b0-113">Zugriff auf externe Datenquellen</span><span class="sxs-lookup"><span data-stu-id="3e8b0-113">Access External Data Sources</span></span>](how-to-access-external-data-sources.md)
  
> <span data-ttu-id="3e8b0-114">Erläutert das Zugreifen auf Daten aus externen Datenquellen.</span><span class="sxs-lookup"><span data-stu-id="3e8b0-114">Discusses how to access data from external data sources.</span></span>
    
[<span data-ttu-id="3e8b0-115">Schreiben von bedingter Logik zur Bestimmung der Laufzeitumgebung</span><span class="sxs-lookup"><span data-stu-id="3e8b0-115">Write Conditional Logic That Determines the Run-time Environment</span></span>](how-to-write-conditional-logic-that-determines-the-run-time-environment.md)
  
> <span data-ttu-id="3e8b0-116">Erläutert das Scheiben von Code, der unterschiedliche Aktionen ausführt, abhängig davon, ob das Formular in InfoPath, einem Webbrowser oder einem mobilen Browser geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="3e8b0-116">Discusses how to write code that performs a different action depending on whether the form is open in InfoPath, a Web browser, or a mobile browser.</span></span>
    
[<span data-ttu-id="3e8b0-117">Arbeiten mit Formularfenstern</span><span class="sxs-lookup"><span data-stu-id="3e8b0-117">Work with Form Windows</span></span>](how-to-work-with-form-windows.md)
  
> <span data-ttu-id="3e8b0-118">Erläutert das Arbeiten mit Formularfenstern.</span><span class="sxs-lookup"><span data-stu-id="3e8b0-118">Discusses how to work with form windows.</span></span>
    
[<span data-ttu-id="3e8b0-119">Arbeiten mit Ansichten</span><span class="sxs-lookup"><span data-stu-id="3e8b0-119">Work with Views</span></span>](how-to-work-with-views.md)
  
> <span data-ttu-id="3e8b0-120">Erläutert das Arbeiten mit Ansichten.</span><span class="sxs-lookup"><span data-stu-id="3e8b0-120">Discusses how to work with views.</span></span>
    
[<span data-ttu-id="3e8b0-121">Arbeiten mit Offline Lösungen</span><span class="sxs-lookup"><span data-stu-id="3e8b0-121">Work with Offline Solutions</span></span>](how-to-work-with-offline-solutions.md)
  
> <span data-ttu-id="3e8b0-122">Erläutert das Arbeiten mit Offlinelösungen.</span><span class="sxs-lookup"><span data-stu-id="3e8b0-122">Discusses how to work with offline solutions.</span></span>
    
[<span data-ttu-id="3e8b0-123">Arbeiten mit digitalen Signaturen</span><span class="sxs-lookup"><span data-stu-id="3e8b0-123">Work with Digital Signatures</span></span>](how-to-work-with-digital-signatures.md)
  
> <span data-ttu-id="3e8b0-124">Erläutert das Arbeiten mit digitalen Signaturen.</span><span class="sxs-lookup"><span data-stu-id="3e8b0-124">Discusses how to work with digital signatures.</span></span>
    
[<span data-ttu-id="3e8b0-125">Behandeln von Fehlern</span><span class="sxs-lookup"><span data-stu-id="3e8b0-125">Handle Errors</span></span>](how-to-handle-errors.md)
  
> <span data-ttu-id="3e8b0-126">Erläutert die Fehlerbehandlung in InfoPath-Projekten mit verwaltetem Code.</span><span class="sxs-lookup"><span data-stu-id="3e8b0-126">Discusses how to handle errors in InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="3e8b0-127">Arbeiten mit Einstellungen für die Verwaltung von Informationsrechten</span><span class="sxs-lookup"><span data-stu-id="3e8b0-127">Work with Information Rights Management Settings</span></span>](how-to-work-with-information-rights-management-settings.md)
  
> <span data-ttu-id="3e8b0-128">Erläutert das Arbeiten mit IRM-Einstellungen (Information Rights Management, Verwaltung von Informationsrechten ).</span><span class="sxs-lookup"><span data-stu-id="3e8b0-128">Discusses how to work with Information Rights Management (IRM) settings.</span></span>
    
[<span data-ttu-id="3e8b0-129">Hinzufügen und verweisen auf benutzerdefinierte Assemblys</span><span class="sxs-lookup"><span data-stu-id="3e8b0-129">Add and Reference Custom Assemblies</span></span>](how-to-add-and-reference-custom-assemblies.md)
  
> <span data-ttu-id="3e8b0-130">Erläutert das Hinzufügen benutzerdefinierter Assemblys zu einem Formularvorlagenprojekt.</span><span class="sxs-lookup"><span data-stu-id="3e8b0-130">Discusses how to add custom assemblies to a form template project.</span></span>
    

