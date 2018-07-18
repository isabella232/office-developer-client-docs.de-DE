---
title: Anwenden einer Beispielvorlage Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: da487569-f2f0-404c-b944-38ed1c1b82bb
description: 'Die Outlook Social Connector (OSC)-Anbieter Beispielvorlagen können Sie einen Rahmen für die Implementierung eines OSC-Anbieters. '
ms.openlocfilehash: 2388da58690e1870434c576bfa68649937156c54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795946"
---
# <a name="applying-a-sample-provider-template"></a><span data-ttu-id="181e8-103">Anwenden einer Beispielvorlage Anbieter</span><span class="sxs-lookup"><span data-stu-id="181e8-103">Applying a Sample Provider Template</span></span>

<span data-ttu-id="181e8-104">Die Outlook Social Connector (OSC)-Anbieter Beispielvorlagen können Sie einen Rahmen für die Implementierung eines OSC-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="181e8-104">The sample Outlook Social Connector (OSC) provider templates give you a framework for implementing an OSC provider.</span></span> <span data-ttu-id="181e8-105">Die Anbietervorlagen vom sind in C++, c# und Visual Basic verfügbar.</span><span class="sxs-lookup"><span data-stu-id="181e8-105">The provider templates are available in C++, C#, and Visual Basic.</span></span> <span data-ttu-id="181e8-106">Diese Vorlagen sind nur als Ausgangspunkt für die Entwicklung Anbieter. die Vorlagen berücksichtigen nicht schreiben den Code zur Implementierung für den Anbieter und erstellen ein Setup-Paket für den Anbieter.</span><span class="sxs-lookup"><span data-stu-id="181e8-106">These templates are just a starting point for your provider development; the templates do not address writing the implementation code for the provider and creating a setup package for the provider.</span></span> <span data-ttu-id="181e8-107">Das folgende Verfahren zeigt, wie eine OSC-Anbietervorlage anwenden, wenn Sie beginnen, um einen Anbieter zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="181e8-107">The following procedure shows how to apply an OSC provider template when you begin to develop a provider.</span></span>
  
### <a name="to-apply-an-osc-provider-template"></a><span data-ttu-id="181e8-108">Anwenden eine OSC-Anbieter-Vorlage</span><span class="sxs-lookup"><span data-stu-id="181e8-108">To apply an OSC provider template</span></span>

1. <span data-ttu-id="181e8-109">Klicken Sie im **Startmenü** mit der rechten Maustaste in **Microsoft Visual Studio 2010** , und klicken Sie auf den Befehl **als Administrator ausführen** .</span><span class="sxs-lookup"><span data-stu-id="181e8-109">On the **Start** menu, right-click **Microsoft Visual Studio 2010** and click the **Run as administrator** command.</span></span> <span data-ttu-id="181e8-110">Wenn Sie aufgefordert werden, klicken Sie auf **Ja** , um Visual Studio als Administrator ausführen.</span><span class="sxs-lookup"><span data-stu-id="181e8-110">When prompted, click **Yes** to run Visual Studio as an administrator.</span></span> 
    
2. <span data-ttu-id="181e8-111">Ändern Sie den Namen des Projekts und den Namespace in der Vorlage in Ihrem Projekt Name und Namespacebezeichnern.</span><span class="sxs-lookup"><span data-stu-id="181e8-111">Change the project name and namespace in the template to your project name and namespace identifiers.</span></span>
    
3. <span data-ttu-id="181e8-112">Ändern Sie die **AssemblyInfo** -Klasse, um die entsprechenden Assemblyinformationen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="181e8-112">Modify the **AssemblyInfo** class to specify the appropriate assembly information.</span></span> 
    
4. <span data-ttu-id="181e8-113">Implementieren Sie die Schnittstellenmember als **Aufgabe** gekennzeichnet, und fügen Sie weitere Abhängigkeiten und Referenzen, nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="181e8-113">Implement the interface members marked as **To-Do** and add more dependencies and references, as required.</span></span> 
    
5. <span data-ttu-id="181e8-114">Erstellen Sie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="181e8-114">Build the project.</span></span>
    
6. <span data-ttu-id="181e8-115">Stellen Sie sicher, dass die Anbieterassembly ProgID, als Schlüssel unter aufgeführt ist `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span><span class="sxs-lookup"><span data-stu-id="181e8-115">Ensure that the provider assembly ProgID is listed as a key under  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span></span>
    
7. <span data-ttu-id="181e8-116">Erstellen Sie ein Setup-Projekt in Visual Studio oder ein Setup-Tool Ihrer Wahl, um das Setup-Projekt zu verteilen.</span><span class="sxs-lookup"><span data-stu-id="181e8-116">To distribute the setup project, create a setup project in Visual Studio or a setup tool of your choice.</span></span>
    
8. <span data-ttu-id="181e8-117">Das Setup-Projekt auszufüllen COM-Registrierung für die Assembly und auch den Schlüssel ProgID erstellen, wie in Schritt 5 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="181e8-117">Your setup project should complete COM registration for your assembly and also create the ProgID key as listed in step 5.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="181e8-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="181e8-118">See also</span></span>

- [<span data-ttu-id="181e8-119">Herunterladen der Beispiele</span><span class="sxs-lookup"><span data-stu-id="181e8-119">Downloading the Samples</span></span>](downloading-the-samples.md)
- [<span data-ttu-id="181e8-120">Über den OSC-Beispielvorlagen</span><span class="sxs-lookup"><span data-stu-id="181e8-120">OSC Sample Templates</span></span>](osc-sample-templates.md)

