---
title: Erste Schritte beim Entwickeln von Formularvorlagen mithilfe des InfoPath-Objektmodells
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Formularvorlagen [infopath 2007], erste Schritte,InfoPath 2003-kompatible Formularvorlagen, erste Schritte
localization_priority: Normal
ms.assetid: 45867711-3231-43ce-bae9-caf588120550
description: Dieser Abschnitt enthält Informationen zum Ersten Erstellen von Formularvorlagen mit verwalteten Code, die mit dem InfoPath 2003-kompatiblen Objektmodell arbeiten, das von Mitgliedern des Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace bereitgestellt wird.
ms.openlocfilehash: 54d60e6d73ee224845c87c08f4de1e554e6182da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408054"
---
# <a name="get-started-developing-form-templates-using-the-infopath-object-model"></a><span data-ttu-id="bf7f9-104">Erste Schritte beim Entwickeln von Formularvorlagen mithilfe des InfoPath-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="bf7f9-104">Get started developing form templates using the InfoPath object model</span></span>

<span data-ttu-id="bf7f9-105">Dieser Abschnitt enthält Informationen zum Ersten Erstellen von Formularvorlagen mit verwalteten Code, die mit dem InfoPath 2003-kompatiblen Objektmodell arbeiten, das von Mitgliedern des [Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="bf7f9-105">This section provides information on how to get started creating managed-code form templates that work with the InfoPath 2003-compatible object model provided by members of the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="bf7f9-106">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="bf7f9-106">In this section</span></span>

- <span data-ttu-id="bf7f9-107">Erstellen einer Formularvorlage mithilfe des [InfoPath 2003-Objektmodells](how-to-create-a-form-template-using-the-infopath-2003-object-model.md): Enthält Informationen und Schritte zum Erstellen von Formularvorlagen, die Geschäftslogik enthalten, die mit dem InfoPath 2003-kompatiblen Objektmodell funktioniert.</span><span class="sxs-lookup"><span data-stu-id="bf7f9-107">[Create a Form Template Using the InfoPath 2003 Object Model](how-to-create-a-form-template-using-the-infopath-2003-object-model.md): Provides information and steps for creating form templates that contain business logic that works with the InfoPath 2003-compatible object model.</span></span>
    
- <span data-ttu-id="bf7f9-108">Exemplarische Vorgehensweise: Erstellen und Debuggen einer einfachen Formularvorlage mithilfe des [InfoPath 2003-Objektmodells:](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md)Eine schrittweise Anleitung, die eine Einführung in das Erstellen und Bereitstellen einer einfachen InfoPath-Formularvorlage bietet, die mit dem InfoPath 2003-kompatiblen Objektmodell funktioniert.</span><span class="sxs-lookup"><span data-stu-id="bf7f9-108">[Walkthrough: Creating and Debugging a Basic Form Template Using the InfoPath 2003 Object Model](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md): A step-by-step guide that provides an introduction to creating and deploying a basic InfoPath form template that works with the InfoPath 2003-compatible object model.</span></span>
    
- <span data-ttu-id="bf7f9-109">Allgemeine Aufgaben zum Entwickeln von Formularvorlagen mithilfe des [InfoPath 2003-Objektmodells:](common-tasks-for-developing-form-templates-using-infopath-object-model.md)Hilft Ihnen, schnell antworten auf häufig gestellte Fragen zum Entwickeln von Formularvorlagen mit Geschäftslogik, die für das InfoPath 2003-kompatible Objektmodell geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="bf7f9-109">[Common Tasks for Developing Form Templates Using the InfoPath 2003 Object Model](common-tasks-for-developing-form-templates-using-infopath-object-model.md): Helps you quickly find the answers to common questions about developing form templates with business logic that works against the InfoPath 2003-compatible object model.</span></span>
    
- <span data-ttu-id="bf7f9-110">Verwenden von [Microsoft.Office.Interop.InfoPath.SemiTrust-Mitgliedern,](how-to-use-microsoft-office-interop-infopath-semitrust-members.md)die nicht mit InfoPath 2003 kompatibel sind: Erläutert die Arbeit mit neuen Objektmodellmmitgliedern, die dem [Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) in Office InfoPath 2007 und InfoPath 2010 hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="bf7f9-110">[Use Microsoft.Office.Interop.InfoPath.SemiTrust Members That Are Not Compatible with InfoPath 2003](how-to-use-microsoft-office-interop-infopath-semitrust-members.md): Discusses how to work with new object model members that were added to the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace in Office InfoPath 2007 and InfoPath 2010.</span></span> 
    
## <a name="related-sections"></a><span data-ttu-id="bf7f9-111">Verwandte Abschnitte</span><span class="sxs-lookup"><span data-stu-id="bf7f9-111">Related sections</span></span>

- <span data-ttu-id="bf7f9-112">Erstellen von Formularvorlagen mithilfe des [InfoPath 2003-Objektmodells:](creating-form-templates-using-the-infopath-2003-object-model.md)Erläutert die Initialisierung und Bereinigung von Code, das Hinzufügen von Ereignishandlern, das Debuggen und Bereitstellen von InfoPath-Formularvorlagen, die das InfoPath 2003-kompatible Objektmodell, die Threadunterstützung und das Arbeiten mit Microsoft XML Core Services (MSXML) verwenden.</span><span class="sxs-lookup"><span data-stu-id="bf7f9-112">[Creating Form Templates Using the InfoPath 2003 Object Model](creating-form-templates-using-the-infopath-2003-object-model.md): Discusses initialization and clean-up code, how to add event handlers, how to debug and deploy InfoPath form templates that use the InfoPath 2003-compatible object model, threading support, and working with Microsoft XML Core Services (MSXML).</span></span>
    
- <span data-ttu-id="bf7f9-113">[Grundlegendes zum InfoPath 2003-Objektmodell:](understanding-the-infopath-2003-object-model.md)Erläutert das InfoPath 2003-kompatible Objektmodell und beschreibt allgemeine Programmieraufgaben.</span><span class="sxs-lookup"><span data-stu-id="bf7f9-113">[Understanding the InfoPath 2003 Object Model](understanding-the-infopath-2003-object-model.md): Discusses the InfoPath 2003-compatible object model, and describes common programming tasks.</span></span>
    
- <span data-ttu-id="bf7f9-114">Problembehandlung bei Formularvorlagen, die das [InfoPath 2003-Objektmodell](troubleshoot-form-templates-that-use-infopath-object-model.md)verwenden: Enthält Tipps zur Lösung gängiger Probleme, die beim Entwickeln von Formularvorlagen auftreten können, die mit dem InfoPath 2003-kompatiblen Objektmodell funktionieren.</span><span class="sxs-lookup"><span data-stu-id="bf7f9-114">[Troubleshooting Form Templates That Use the InfoPath 2003 Object Model](troubleshoot-form-templates-that-use-infopath-object-model.md): Contains tips for solving common problems that you might encounter when developing form templates that work with the InfoPath 2003-compatible object model.</span></span>
    

