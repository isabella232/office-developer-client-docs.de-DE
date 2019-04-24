---
title: Referenz zur primären Interopassembly für Outlook
TOCTitle: '@NoTitle'
ms:assetid: 54bdde85-8dc9-4498-a1ac-f72eaf8f0cd3
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb652780(v=office.15)
ms:contentKeyID: 55119771
ms.date: 09/15/2015
mtps_version: v=office.15
f1_keywords:
- Outlook 2010, programming
- Outlook 2010, object model
- Outlook 2010, PIA
- Outlook code samples
- Outlook 2010, primary interop assembly
- primary interop assembly [Outlook 2010]
- PIA [Outlook 2010]
- reference [Outlook 2010], primary interop assembly
localization_priority: Normal
ms.openlocfilehash: 53c50c447c6f132c562a1a22934df646347a51bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335749"
---
# <a name="outlook-primary-interop-assembly-reference"></a><span data-ttu-id="9d0dd-102">Referenz zur primären Interopassembly für Outlook</span><span class="sxs-lookup"><span data-stu-id="9d0dd-102">Outlook Primary Interop Assembly reference</span></span>

<span data-ttu-id="9d0dd-103">Die Outlook 2013 PIA-Referenz (Primäre Interopassembly) bietet Hilfe bei der Entwicklung verwalteter Anwendungen für Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="9d0dd-103">The Outlook 2013 Primary Interop Assembly (PIA) reference provides help for developing managed applications for Outlook 2013.</span></span> <span data-ttu-id="9d0dd-104">Sie erweitert die [Outlook 2013-Entwicklerreferenz](https://docs.microsoft.com/office/vba/api/overview/outlook) von der COM-Umgebung zur verwalteten Umgebung und konzentriert sich auf die Verwendung der PIA.</span><span class="sxs-lookup"><span data-stu-id="9d0dd-104">It extends the [Outlook 2013 Developer Reference](https://docs.microsoft.com/office/vba/api/overview/outlook) from the COM environment to the managed environment and focuses on how to use the PIA.</span></span> <span data-ttu-id="9d0dd-105">Sie enthält alle Ergänzungen und Änderungen des Objektmodells in Outlook 2013 und stellt viele Codebeispiele in C\# und Visual Basic zur Verfügung, die die Durchführung gängiger Aufgaben in Outlook veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="9d0dd-105">It includes all the additions and changes to the object model in Outlook 2013, and provides many code samples in C\# and Visual Basic to show how to perform common tasks in Outlook.</span></span>

<span data-ttu-id="9d0dd-106">Wenn Sie gerade erst mit dem Entwickeln von Lösungen für Outlook begonnen haben, finden Sie im Artikel [Auswählen einer API oder Technologie zum Entwickeln von Lösungen für Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) weitere Informationen zu den APIs und Technologien, die am besten zu Ihren Anforderungen passen.</span><span class="sxs-lookup"><span data-stu-id="9d0dd-106">If you are new to developing solutions for Outlook, see [Selecting an API or technology for developing solutions for Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) to identify the APIs and technologies that are most appropriate for your needs.</span></span>

## <a name="purpose-of-the-outlook-pia-reference"></a><span data-ttu-id="9d0dd-107">Zweck der Outlook-PIA-Referenz</span><span class="sxs-lookup"><span data-stu-id="9d0dd-107">Purpose of the Outlook PIA reference</span></span>

<span data-ttu-id="9d0dd-p102">Wenn Sie noch keine Erfahrung mit dem Schreiben von Add-Ins für Outlook haben, sollten Sie sich zuerst mit den konzeptionellen Inhalten der Outlook 2013-Entwicklerreferenz beschäftigen. Obwohl die Programmierumgebung, der Zugriff auf bestimmte Methoden und das Herstellen von Verbindungen mit Ereignissen in COM und in der verwalteten Entwicklungsumgebung unterschiedlich sind, verhalten sich Features im Outlook-Objektmodell in COM und in der verwalteten Entwicklungsumgebung gleich. In den konzeptionellen Inhalten der Outlook 2013-Entwicklerreferenz finden Sie Informationen über die Verwendung der verschiedenen Features des Objektmodells.</span><span class="sxs-lookup"><span data-stu-id="9d0dd-p102">If you are just beginning to write add-ins for Outlook, you should first refer to the conceptual content in the Outlook 2013 Developer Reference. Even though the programming environment and accessing certain methods and connecting to events are different in COM and in managed development, features in the Outlook object model behave the same way in both COM and managed development. You can refer to the conceptual content in the Outlook 2013 Developer Reference to understand how to use the different features of the object model.</span></span>

<span data-ttu-id="9d0dd-111">Wenn Sie über Grundkenntnisse des Outlook-Objektmodells verfügen und jetzt die Entwicklung verwalteter Outlook-Add-Ins erlernen, finden Sie hilfreiche Informationen unter [Einrichten der Outlook-PIA](setting-up-to-use-the-outlook-pia.md).</span><span class="sxs-lookup"><span data-stu-id="9d0dd-111">If you have a basic understanding of the Outlook object model and are learning to develop managed Outlook add-ins, see [Setting up to use the Outlook PIA](setting-up-to-use-the-outlook-pia.md).</span></span> 

<span data-ttu-id="9d0dd-112">Informationen zum Entwickeln verwalteter Office-Lösungen mithilfe der Office Developer Tools für Visual Studio 2013 finden Sie unter [Office-Entwicklung in Visual Studio](https://docs.microsoft.com/visualstudio/vsto/office-and-sharepoint-development-in-visual-studio?view=vs-2017).</span><span class="sxs-lookup"><span data-stu-id="9d0dd-112">For information about developing managed Office solutions by using Office Developer Tools for Visual Studio 2013, see [Office Development in Visual Studio](https://docs.microsoft.com/visualstudio/vsto/office-and-sharepoint-development-in-visual-studio?view=vs-2017).</span></span> 

<span data-ttu-id="9d0dd-113">Informationen über die Programmierung einiger einfacher Outlook-Aufgaben in Visual Basic und C\# finden Sie unter [Outlook-Lösungen](https://docs.microsoft.com/visualstudio/vsto/outlook-solutions?view=vs-2017).</span><span class="sxs-lookup"><span data-stu-id="9d0dd-113">For information about how to program some basic Outlook tasks in both Visual Basic and C\#, see [Outlook solutions](https://docs.microsoft.com/visualstudio/vsto/outlook-solutions?view=vs-2017).</span></span> 

<span data-ttu-id="9d0dd-114">Komplexere Codebeispiele finden Sie unter [Gewusst wie... (Outlook 2013 PIA-Referenz)](how-do-i-outlook-2013-pia-reference.md) in dieser Referenz.</span><span class="sxs-lookup"><span data-stu-id="9d0dd-114">For more advanced code examples, see [How do I... (Outlook 2013 PIA Reference)](how-do-i-outlook-2013-pia-reference.md) in this reference.</span></span>

<span data-ttu-id="9d0dd-115">Wenn Sie bereits mit dem Outlook-Objektmodell vertraut sind, über einige Erfahrung im Schreiben von verwalteten Anwendungen verfügen und das erste Mal mit der Outlook PIA arbeiten, beginnen Sie mit den Themen [Installieren der Outlook-PIA und Verweisen auf diese](installing-and-referencing-the-outlook-pia.md) und [Architektur der Outlook-PIA](architecture-of-the-outlook-pia.md).</span><span class="sxs-lookup"><span data-stu-id="9d0dd-115">If you are already familiar with the Outlook object model, you have some experience writing managed applications, and you are using the Outlook PIA for the first time, start with [Installing and referencing the Outlook PIA](installing-and-referencing-the-outlook-pia.md) and [Architecture of the Outlook PIA](architecture-of-the-outlook-pia.md).</span></span>

## <a name="accessing-the-outlook-pia-reference-in-design-time"></a><span data-ttu-id="9d0dd-116">Zugreifen auf die Outlook-PIA-Referenz zur Entwurfszeit</span><span class="sxs-lookup"><span data-stu-id="9d0dd-116">Accessing the Outlook PIA reference in design time</span></span>

<span data-ttu-id="9d0dd-117">Wenn Sie Office Developer Tools für Visual Studio 2013 verwenden und mit dem Internet verbunden sind, können Sie auf kontextbezogene Hilfe zugreifen, indem Sie in der integrierten Entwicklungsumgebung (IDE) von Visual Studio die Taste F1 drücken.</span><span class="sxs-lookup"><span data-stu-id="9d0dd-117">If you use Office Developer Tools for Visual Studio 2013 and you are connected to the Internet, you can access context-sensitive Help when you press F1 in the Visual Studio integrated development environment (IDE).</span></span> <span data-ttu-id="9d0dd-118">Bei dem Inhalt dieser Hilfe handelt es sich um Outlook 2013-PIA-Referenz.</span><span class="sxs-lookup"><span data-stu-id="9d0dd-118">This Help content is the Outlook 2013 PIA reference.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9d0dd-119">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="9d0dd-119">In this section</span></span>

- [<span data-ttu-id="9d0dd-120">Neuerungen in der Outlook-PIA-Referenz</span><span class="sxs-lookup"><span data-stu-id="9d0dd-120">What's new in the Outlook PIA reference</span></span>](what-s-new-in-the-outlook-pia-reference.md)
- [<span data-ttu-id="9d0dd-121">Einrichten der Outlook-PIA</span><span class="sxs-lookup"><span data-stu-id="9d0dd-121">Setting up to use the Outlook PIA</span></span>](setting-up-to-use-the-outlook-pia.md)
- [<span data-ttu-id="9d0dd-122">Architektur der Outlook-PIA</span><span class="sxs-lookup"><span data-stu-id="9d0dd-122">Architecture of the Outlook PIA</span></span>](architecture-of-the-outlook-pia.md)
- [<span data-ttu-id="9d0dd-123">Entwickeln von verwalteten Outlook-Add-Ins mithilfe der Outlook-PIA</span><span class="sxs-lookup"><span data-stu-id="9d0dd-123">Developing managed Outlook add-ins using the Outlook PIA</span></span>](developing-managed-outlook-add-ins-using-the-outlook-pia.md)
- [<span data-ttu-id="9d0dd-124">Gewusst wie... (Outlook 2013 PIA-Referenz)</span><span class="sxs-lookup"><span data-stu-id="9d0dd-124">How do I... (Outlook 2013 PIA Reference)</span></span>](how-do-i-outlook-2013-pia-reference.md)
- [<span data-ttu-id="9d0dd-125">Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="9d0dd-125">Class library</span></span>](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook?view=outlook-pia)

## <a name="see-also"></a><span data-ttu-id="9d0dd-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d0dd-126">See also</span></span>

- [<span data-ttu-id="9d0dd-127">Outlook Developer Center</span><span class="sxs-lookup"><span data-stu-id="9d0dd-127">Outlook Developer Center</span></span>](../outlook-home.md)
- [<span data-ttu-id="9d0dd-128">COM- und .NET-Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="9d0dd-128">COM and .NET Interoperability</span></span>](https://www.apress.com/us/book/9781590590119)
- [<span data-ttu-id="9d0dd-129">Office-Entwicklung in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9d0dd-129">Office Development in Visual Studio</span></span>](https://docs.microsoft.com/visualstudio/vsto/office-and-sharepoint-development-in-visual-studio?view=vs-2017)
- [<span data-ttu-id="9d0dd-130">Barrierefreiheit in Microsoft-Produkten</span><span class="sxs-lookup"><span data-stu-id="9d0dd-130">Accessibility in Microsoft Products</span></span>](https://www.microsoft.com/en-us/accessibility/)

