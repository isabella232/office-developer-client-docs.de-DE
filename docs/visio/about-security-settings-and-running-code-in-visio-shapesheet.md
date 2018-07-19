---
title: Informationen zu Sicherheitseinstellungen und Ausführen von Code in Visio (ShapeSheet)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm1042370
localization_priority: Normal
ms.assetid: 506b3d81-9c93-aeff-f5b2-3354ffd3e075
description: Erstellen sichere Anwendungen ist eines der wichtigsten Probleme facing Lösungsentwickler. Benutzer, Administratoren und Entwickler sind immer bewusst das Potenzial der unwissentlich Ausführung von Code, die auf ihre Computer beschädigen kann. Es ist wichtiger denn je, Ihnen helfen, um die Integrität der Anwendung sicherzustellen.
ms.openlocfilehash: e114fef650f31a6e0adf368d339f71e3a32113f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796353"
---
# <a name="about-security-settings-and-running-code-in-visio-shapesheet"></a><span data-ttu-id="317b1-105">Informationen zu Sicherheitseinstellungen und Ausführen von Code in Visio (ShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="317b1-105">About Security Settings and Running Code in Visio (ShapeSheet)</span></span>

 <span data-ttu-id="317b1-106">Erstellen sichere Anwendungen ist eines der wichtigsten Probleme facing Lösungsentwickler.</span><span class="sxs-lookup"><span data-stu-id="317b1-106">Creating secure applications is one of the primary challenges facing solution developers.</span></span> <span data-ttu-id="317b1-107">Benutzer, Administratoren und Entwickler sind immer bewusst das Potenzial der unwissentlich Ausführung von Code, die auf ihre Computer beschädigen kann.</span><span class="sxs-lookup"><span data-stu-id="317b1-107">Users, administrators, and developers are increasingly aware of the potential of unknowingly running code that can be harmful to their computers.</span></span> <span data-ttu-id="317b1-108">Es ist wichtiger denn je, Ihnen helfen, um die Integrität der Anwendung sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="317b1-108">It is more important than ever that you help to ensure the integrity of your applications.</span></span> 
  
<span data-ttu-id="317b1-109">Alle Sicherheitseinstellungen für Office-Programme sind und im **Vertrauensstellungscenter** festgelegt sind (klicken Sie auf der Registerkarte **Datei** , klicken Sie auf **Optionen**, und klicken Sie dann auf **Trust Center**).</span><span class="sxs-lookup"><span data-stu-id="317b1-109">All security settings are Office-wide and are set in the **Trust Center** (click the **File** tab, click **Options**, and then click **Trust Center**).</span></span> <span data-ttu-id="317b1-110">Betroffene Einstellungen umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="317b1-110">Affected settings include the following:</span></span>
  
- <span data-ttu-id="317b1-111">Angeben vertrauenswürdiger Herausgeber</span><span class="sxs-lookup"><span data-stu-id="317b1-111">Specifying trusted publishers</span></span>
    
- <span data-ttu-id="317b1-112">Angeben vertrauenswürdiger Speicherorte</span><span class="sxs-lookup"><span data-stu-id="317b1-112">Specifying trusted locations</span></span>
    
- <span data-ttu-id="317b1-113">Laden von COM-Add-Ins</span><span class="sxs-lookup"><span data-stu-id="317b1-113">Loading COM add-ins</span></span> 
    
- <span data-ttu-id="317b1-114">Laden veröffentlichter und im Pfad gefundener Add-Ons</span><span class="sxs-lookup"><span data-stu-id="317b1-114">Loading published and path-discovered add-ons</span></span>
    
- <span data-ttu-id="317b1-115">Laden von VBA-Makros</span><span class="sxs-lookup"><span data-stu-id="317b1-115">Loading VBA macros</span></span>
    
<span data-ttu-id="317b1-116">In früheren Versionen von Visio wurden die Einstellungen in das Dialogfeld **Sicherheit** und die Registerkarte **Sicherheit** im Dialogfeld **Optionen** (Menü**Extras** ) vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="317b1-116">In previous versions of Visio, settings were made in the **Security** dialog box and the **Security** tab of the **Options** dialog box (**Tools** menu).</span></span> <span data-ttu-id="317b1-117">Ab Office Visio 2007 diese Dialogfelder werden entfernt, und ab Microsoft Visio 2010, Visio-Symbolleisten und Menüs ersetzt wurden durch die Multifunktionsleiste.</span><span class="sxs-lookup"><span data-stu-id="317b1-117">As of Office Visio 2007, these dialog boxes have been eliminated, and as of Microsoft Visio 2010, Visio toolbars and menus have been replaced by the ribbon.</span></span> 
  
<span data-ttu-id="317b1-118">Weitere Informationen zu den Einstellungen in der Office- **Sicherheitscenter**finden Sie unter [Sicherheitshinweise für Microsoft Office-Lösungsentwickler](http://msdn2.microsoft.com/de-de/library/aa433259.aspx).</span><span class="sxs-lookup"><span data-stu-id="317b1-118">For more information about settings in the Office **Trust Center**, see [Security Notes for Microsoft Office Solution Developers](http://msdn2.microsoft.com/de-de/library/aa433259.aspx).</span></span>
  
 <span data-ttu-id="317b1-119">Suchen Sie auf der MSDN-Website, der Website von Microsoft Developer Network, nach dem Suchbegriff "code signing" (Signieren von Code), um weitere Informationen über das digitale Signieren von Code und vertrauenswürdige Quellen und Herausgeber zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="317b1-119">For information about digitally signing code and trusted sources and publishers, search for "code signing" on MSDN, the Microsoft Developer Network Web site.</span></span> 
  
<span data-ttu-id="317b1-120">Weitere Informationen über Verfahren und Technologien für ein hohes Maß an Sicherheit erhalten Sie, wenn Sie MSDN nach dem Suchbegriff "security" durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="317b1-120">For more information about good security design practices and technologies, search for "security" on MSDN.</span></span> 
  
## <a name="additional-visio-resources"></a><span data-ttu-id="317b1-121">Weitere Ressourcen für Visio</span><span class="sxs-lookup"><span data-stu-id="317b1-121">Additional Visio resources</span></span>

- <span data-ttu-id="317b1-122">Weitere Informationen zu Visio-Add-Ons und COM-add-ins finden Sie unter [Übersicht über Add-ons und COM-Add-ins in Visio 2007](http://msdn.microsoft.com/de-de/library/bb851468.aspx)im MSDN-Artikel.</span><span class="sxs-lookup"><span data-stu-id="317b1-122">To learn more about Visio add-ons and COM add-ins, see the MSDN article, [Overview of Add-ons and COM Add-ins in Visio 2007](http://msdn.microsoft.com/de-de/library/bb851468.aspx).</span></span>
    
- <span data-ttu-id="317b1-123">Um weitere Informationen über die RUNADDON-Funktion und der **AddonName** -Eigenschaft finden Sie im MSDN-Artikel [Änderungen in die RUNADDON-Funktion und der AddOnName Property for Visio 2002](http://msdn.microsoft.com/de-de/library/aa140368%28office.10%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="317b1-123">To learn more about the RUNADDON function and the **AddonName** property, see the MSDN article [Changes in the RUNADDON Function and the AddOnName Property for Visio 2002](http://msdn.microsoft.com/de-de/library/aa140368%28office.10%29.aspx).</span></span>
    

