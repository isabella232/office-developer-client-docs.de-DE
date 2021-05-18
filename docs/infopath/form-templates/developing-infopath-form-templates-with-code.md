---
title: Entwickeln von InfoPath-Formularvorlagen mit Code
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Formularvorlagen [infopath 2007], developing,form templates [InfoPath 2007], managed code,InfoPath 2007,managed code form templates [InfoPath 2007]
localization_priority: Normal
ms.assetid: b43ada73-349d-498f-a8bb-e8fd5020d207
description: Die Themen in diesem Abschnitt enthalten Informationen zum Erstellen von Formularvorlagen, deren Geschäftslogik in verwalteten Code (Visual Basic oder C#) für Mitglieder von Microsoft geschrieben wurde. Office. InfoPath-Namespace.
ms.openlocfilehash: 386542b5c5f4e502f48d97c2a18194638e8e1536
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303731"
---
# <a name="developing-infopath-form-templates-with-code"></a><span data-ttu-id="e5940-104">Entwickeln von InfoPath-Formularvorlagen mit Code</span><span class="sxs-lookup"><span data-stu-id="e5940-104">Developing InfoPath Form Templates with Code</span></span>

<span data-ttu-id="e5940-105">Die Themen in diesem Abschnitt enthalten Informationen zum Erstellen von Formularvorlagen, deren Geschäftslogik in verwalteten Code (Visual Basic oder C#) für Mitglieder der [Microsoft.Office. InfoPath-Namespace.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx)</span><span class="sxs-lookup"><span data-stu-id="e5940-105">The topics in this section provide information about creating form templates that have business logic written in managed code (Visual Basic or C#) against members of the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="e5940-106">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="e5940-106">In this section</span></span>

[<span data-ttu-id="e5940-107">Erste Schritte beim Entwickeln von Formularvorlagen mit Code</span><span class="sxs-lookup"><span data-stu-id="e5940-107">Getting Started Developing Form Templates with Code</span></span>](getting-started-developing-form-templates-with-code.md)
  
> <span data-ttu-id="e5940-108">Enthält Informationen zum Erstellen von Formularvorlagen für verwalteten Code, die mit dem infoPath-Objektmodell von [Microsoft.Office. InfoPath-Namespace.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx)</span><span class="sxs-lookup"><span data-stu-id="e5940-108">Provides information about how to start creating managed code form templates that work with the InfoPath object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace.</span></span> 
    
[<span data-ttu-id="e5940-109">Grundlegendes zum InfoPath-Objektmodell und zu allgemeinen Entwickleraufgaben</span><span class="sxs-lookup"><span data-stu-id="e5940-109">Understanding the InfoPath Object Model and Common Developer Tasks</span></span>](understanding-the-infopath-object-model-and-common-developer-tasks.md)
  
> <span data-ttu-id="e5940-110">Erläutert das InfoPath-Objektmodell und allgemeine Programmieraufgaben für Formularvorlagen mit verwalteten Code, die mit dem von Microsoft.Office bereitgestellten [Objektmodell funktionieren. InfoPath-Namespace.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx)</span><span class="sxs-lookup"><span data-stu-id="e5940-110">Discusses the InfoPath object model, and common programming tasks for managed code form templates that work with the object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace.</span></span> 
    
[<span data-ttu-id="e5940-111">Sicherheit in InfoPath-Formularvorlagen mit Code</span><span class="sxs-lookup"><span data-stu-id="e5940-111">Security in InfoPath Form Templates with Code</span></span>](security-in-infopath-form-templates-with-code.md)
  
> <span data-ttu-id="e5940-112">Erläutert das Sicherheitsmodell für InfoPath-Formularvorlagen, die verwalteten Code verwenden, sowie verwandte Sicherheitsprozeduren.</span><span class="sxs-lookup"><span data-stu-id="e5940-112">Discusses the security model for InfoPath form templates that use managed code, and related security procedures.</span></span>
    
[<span data-ttu-id="e5940-113">Arbeiten mit SharePoint- und InfoPath-Formulardiensten</span><span class="sxs-lookup"><span data-stu-id="e5940-113">Working with SharePoint and InfoPath Forms Services</span></span>](working-with-sharepoint-and-infopath-forms-services.md)
  
> <span data-ttu-id="e5940-114">Erläutert die Objektmodellunterstützung und die Featurekompatibilität bei Formularvorlagen mit verwaltetem Code, die für InfoPath Forms Services erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="e5940-114">Discusses object model support and feature compatibility in managed code form templates created for InfoPath Forms Services.</span></span> 
    
[<span data-ttu-id="e5940-115">Zusätzliche InfoPath-Entwicklungskonzepte</span><span class="sxs-lookup"><span data-stu-id="e5940-115">Additional InfoPath Development Concepts</span></span>](additional-infopath-development-concepts.md)
  
> <span data-ttu-id="e5940-116">Erörtert weitere Konzepte, die sich auf die Entwicklung von InfoPath-Formularvorlagen beziehen.</span><span class="sxs-lookup"><span data-stu-id="e5940-116">Discusses additional concepts that relate to InfoPath form template development.</span></span>
    
## <a name="related-sections"></a><span data-ttu-id="e5940-117">Verwandte Abschnitte</span><span class="sxs-lookup"><span data-stu-id="e5940-117">Related sections</span></span>

[<span data-ttu-id="e5940-118">InfoPath Developer Portal</span><span class="sxs-lookup"><span data-stu-id="e5940-118">InfoPath Developer Portal</span></span>](https://go.microsoft.com/fwlink?LinkID=11689)
  
> <span data-ttu-id="e5940-119">Enthält Links zu technischen Artikeln, Codebeispielen, Downloads, Support sowie sonstige MSDN-Dokumentationen zum Erstellen benutzerdefinierter InfoPath-Lösungen.</span><span class="sxs-lookup"><span data-stu-id="e5940-119">Contains links to technical articles, code samples, downloads, support, and other MSDN documentation on building custom InfoPath solutions.</span></span>
    
[<span data-ttu-id="e5940-120">Office Developer Center</span><span class="sxs-lookup"><span data-stu-id="e5940-120">Microsoft Office Developer Center</span></span>](https://go.microsoft.com/fwlink?LinkID=27128)
  
> <span data-ttu-id="e5940-121">Enthält Links zu technischen Artikeln, Codebeispielen, Downloads, Support sowie sonstige MSDN-Dokumentationen zum Erstellen benutzerdefinierter Office-Lösungen.</span><span class="sxs-lookup"><span data-stu-id="e5940-121">Contains links to technical articles, code samples, downloads, support, and other MSDN documentation on building custom Office solutions.</span></span>
    

