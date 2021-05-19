---
title: Anwenden einer Beispielanbietervorlage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: da487569-f2f0-404c-b944-38ed1c1b82bb
description: 'Das Beispiel für Outlook (Social Connector, OSC)-Anbietervorlagen bieten Ihnen ein Framework für die Implementierung eines OSC-Anbieters. '
ms.openlocfilehash: 10fb21ab640e298bc655b8cad554fae789e2ad47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425911"
---
# <a name="applying-a-sample-provider-template"></a><span data-ttu-id="75313-103">Anwenden einer Beispielanbietervorlage</span><span class="sxs-lookup"><span data-stu-id="75313-103">Applying a Sample Provider Template</span></span>

<span data-ttu-id="75313-104">Das Beispiel für Outlook (Social Connector, OSC)-Anbietervorlagen bieten Ihnen ein Framework für die Implementierung eines OSC-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="75313-104">The sample Outlook Social Connector (OSC) provider templates give you a framework for implementing an OSC provider.</span></span> <span data-ttu-id="75313-105">Die Anbietervorlagen sind in C++, C# und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="75313-105">The provider templates are available in C++, C#, and Visual Basic.</span></span> <span data-ttu-id="75313-106">Diese Vorlagen sind nur ein Ausgangspunkt für ihre Anbieterentwicklung. Die Vorlagen enthalten keine Informationen zum Schreiben des Implementierungscodes für den Anbieter und zum Erstellen eines Setuppakets für den Anbieter.</span><span class="sxs-lookup"><span data-stu-id="75313-106">These templates are just a starting point for your provider development; the templates do not address writing the implementation code for the provider and creating a setup package for the provider.</span></span> <span data-ttu-id="75313-107">Im folgenden Verfahren wird gezeigt, wie Sie eine OsC-Anbietervorlage anwenden, wenn Sie mit der Entwicklung eines Anbieters beginnen.</span><span class="sxs-lookup"><span data-stu-id="75313-107">The following procedure shows how to apply an OSC provider template when you begin to develop a provider.</span></span>
  
### <a name="to-apply-an-osc-provider-template"></a><span data-ttu-id="75313-108">So wenden Sie eine OSC-Anbietervorlage an</span><span class="sxs-lookup"><span data-stu-id="75313-108">To apply an OSC provider template</span></span>

1. <span data-ttu-id="75313-109">Klicken Sie **im Menü** Start mit der rechten Maustaste auf **Microsoft Visual Studio 2010,** und klicken Sie auf den Befehl **Als Administrator ausführen.**</span><span class="sxs-lookup"><span data-stu-id="75313-109">On the **Start** menu, right-click **Microsoft Visual Studio 2010** and click the **Run as administrator** command.</span></span> <span data-ttu-id="75313-110">Wenn Sie dazu  aufgefordert werden, klicken Sie auf Ja, um Visual Studio Administrator ausführen.</span><span class="sxs-lookup"><span data-stu-id="75313-110">When prompted, click **Yes** to run Visual Studio as an administrator.</span></span> 
    
2. <span data-ttu-id="75313-111">Ändern Sie den Projektnamen und Namespace in der Vorlage in Den Projektnamen und Namespacebezeichner.</span><span class="sxs-lookup"><span data-stu-id="75313-111">Change the project name and namespace in the template to your project name and namespace identifiers.</span></span>
    
3. <span data-ttu-id="75313-112">Ändern Sie die **AssemblyInfo-Klasse,** um die entsprechenden Assemblyinformationen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="75313-112">Modify the **AssemblyInfo** class to specify the appropriate assembly information.</span></span> 
    
4. <span data-ttu-id="75313-113">Implementieren Sie die als To-Do **gekennzeichneten** Schnittstellenmmitglieder, und fügen Sie bei Bedarf weitere Abhängigkeiten und Verweise hinzu.</span><span class="sxs-lookup"><span data-stu-id="75313-113">Implement the interface members marked as **To-Do** and add more dependencies and references, as required.</span></span> 
    
5. <span data-ttu-id="75313-114">Erstellen Sie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="75313-114">Build the project.</span></span>
    
6. <span data-ttu-id="75313-115">Stellen Sie sicher, dass die ProgID der Anbieter assembly als Schlüssel unter aufgeführt  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` ist.</span><span class="sxs-lookup"><span data-stu-id="75313-115">Ensure that the provider assembly ProgID is listed as a key under  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span></span>
    
7. <span data-ttu-id="75313-116">Um das Setupprojekt zu verteilen, erstellen Sie ein Setupprojekt in Visual Studio oder ein Setuptool Ihrer Wahl.</span><span class="sxs-lookup"><span data-stu-id="75313-116">To distribute the setup project, create a setup project in Visual Studio or a setup tool of your choice.</span></span>
    
8. <span data-ttu-id="75313-117">Ihr Setupprojekt sollte die COM-Registrierung für Ihre Assembly abschließen und den ProgID-Schlüssel erstellen, wie in Schritt 5 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="75313-117">Your setup project should complete COM registration for your assembly and also create the ProgID key as listed in step 5.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="75313-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75313-118">See also</span></span>

- [<span data-ttu-id="75313-119">Herunterladen der Beispiele</span><span class="sxs-lookup"><span data-stu-id="75313-119">Downloading the Samples</span></span>](downloading-the-samples.md)
- [<span data-ttu-id="75313-120">Über den OSC-Beispielvorlagen</span><span class="sxs-lookup"><span data-stu-id="75313-120">OSC Sample Templates</span></span>](osc-sample-templates.md)

