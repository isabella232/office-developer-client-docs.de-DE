---
title: Anwenden einer Beispielanbieter Vorlage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: da487569-f2f0-404c-b944-38ed1c1b82bb
description: 'Die Beispielvorlagen für Outlook Social Connector (OSC) bieten Ihnen ein Framework für die Implementierung eines OSC-Anbieters. '
ms.openlocfilehash: 10fb21ab640e298bc655b8cad554fae789e2ad47
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281127"
---
# <a name="applying-a-sample-provider-template"></a><span data-ttu-id="fa203-103">Anwenden einer Beispielanbieter Vorlage</span><span class="sxs-lookup"><span data-stu-id="fa203-103">Applying a Sample Provider Template</span></span>

<span data-ttu-id="fa203-104">Die Beispielvorlagen für Outlook Social Connector (OSC) bieten Ihnen ein Framework für die Implementierung eines OSC-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="fa203-104">The sample Outlook Social Connector (OSC) provider templates give you a framework for implementing an OSC provider.</span></span> <span data-ttu-id="fa203-105">Die Anbietervorlagen sind in C++, C# und Visual Basic verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fa203-105">The provider templates are available in C++, C#, and Visual Basic.</span></span> <span data-ttu-id="fa203-106">Diese Vorlagen sind nur ein Ausgangspunkt für die Entwicklung Ihres Anbieters. die Vorlagen richten sich nicht auf das Schreiben des Implementierungscodes für den Anbieter und das Erstellen eines Setuppakets für den Anbieter.</span><span class="sxs-lookup"><span data-stu-id="fa203-106">These templates are just a starting point for your provider development; the templates do not address writing the implementation code for the provider and creating a setup package for the provider.</span></span> <span data-ttu-id="fa203-107">Im folgenden Verfahren wird gezeigt, wie Sie eine OSC-Anbietervorlage anwenden, wenn Sie mit der Entwicklung eines Anbieters beginnen.</span><span class="sxs-lookup"><span data-stu-id="fa203-107">The following procedure shows how to apply an OSC provider template when you begin to develop a provider.</span></span>
  
### <a name="to-apply-an-osc-provider-template"></a><span data-ttu-id="fa203-108">So wenden Sie eine OSC-Anbietervorlage an</span><span class="sxs-lookup"><span data-stu-id="fa203-108">To apply an OSC provider template</span></span>

1. <span data-ttu-id="fa203-109">Klicken Sie im **Startmenü** mit der rechten Maustaste auf **Microsoft Visual Studio 2010** , und klicken Sie auf den Befehl **als Administrator ausführen** .</span><span class="sxs-lookup"><span data-stu-id="fa203-109">On the **Start** menu, right-click **Microsoft Visual Studio 2010** and click the **Run as administrator** command.</span></span> <span data-ttu-id="fa203-110">Wenn Sie dazu aufgefordert werden, klicken Sie auf **Ja** , um Visual Studio als Administrator auszuführen.</span><span class="sxs-lookup"><span data-stu-id="fa203-110">When prompted, click **Yes** to run Visual Studio as an administrator.</span></span> 
    
2. <span data-ttu-id="fa203-111">Ändern Sie den Projektnamen und den Namespace in der Vorlage in den Projektnamen und die Namespace-IDs.</span><span class="sxs-lookup"><span data-stu-id="fa203-111">Change the project name and namespace in the template to your project name and namespace identifiers.</span></span>
    
3. <span data-ttu-id="fa203-112">Ändern Sie die **AssemblyInfo** -Klasse, um die entsprechenden Assemblyinformationen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="fa203-112">Modify the **AssemblyInfo** class to specify the appropriate assembly information.</span></span> 
    
4. <span data-ttu-id="fa203-113">Implementieren Sie die Schnittstellenmember, die als **Aufgabe** markiert sind, und fügen Sie je nach Bedarf weitere Abhängigkeiten und Verweise hinzu.</span><span class="sxs-lookup"><span data-stu-id="fa203-113">Implement the interface members marked as **To-Do** and add more dependencies and references, as required.</span></span> 
    
5. <span data-ttu-id="fa203-114">Erstellen Sie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="fa203-114">Build the project.</span></span>
    
6. <span data-ttu-id="fa203-115">Stellen Sie sicher, dass die ProgID der Anbieter-Assembly als `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`Schlüssel unter aufgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fa203-115">Ensure that the provider assembly ProgID is listed as a key under  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span></span>
    
7. <span data-ttu-id="fa203-116">Um das Setup-Projekt zu verteilen, erstellen Sie ein Setup-Projekt in Visual Studio oder ein Setup-Tool Ihrer Wahl.</span><span class="sxs-lookup"><span data-stu-id="fa203-116">To distribute the setup project, create a setup project in Visual Studio or a setup tool of your choice.</span></span>
    
8. <span data-ttu-id="fa203-117">Das Setupprojekt sollte die COM-Registrierung für Ihre Assembly abschließen und auch den ProgID-Schlüssel erstellen, wie in Schritt 5 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="fa203-117">Your setup project should complete COM registration for your assembly and also create the ProgID key as listed in step 5.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fa203-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa203-118">See also</span></span>

- [<span data-ttu-id="fa203-119">Herunterladen der Beispiele</span><span class="sxs-lookup"><span data-stu-id="fa203-119">Downloading the Samples</span></span>](downloading-the-samples.md)
- [<span data-ttu-id="fa203-120">Über den OSC-Beispielvorlagen</span><span class="sxs-lookup"><span data-stu-id="fa203-120">OSC Sample Templates</span></span>](osc-sample-templates.md)

