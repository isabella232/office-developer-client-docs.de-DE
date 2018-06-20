---
title: Entwickeln mit Visual Studio
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39d633d-d8fb-4e2f-a396-6cb50beb8c3e
description: Sie können die Funktionalität von InfoPath-Formularen erheblich verbessern, indem Sie sie mit verwaltetem Code in Visual Studio 2012 entwickelt erweitern. Sie können von Formularen mit Code klicken Sie dann auf SharePoint Server 2013 in Formularbibliotheken veröffentlichen.
ms.openlocfilehash: d6a2cfa1847b4b59b6978b8f4a0775aedf07a72d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790756"
---
# <a name="develop-with-visual-studio"></a><span data-ttu-id="8e781-104">Entwickeln mit Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8e781-104">Develop with Visual Studio</span></span>

<span data-ttu-id="8e781-105">Sie können die Funktionalität von InfoPath-Formularen erheblich verbessern, indem Sie sie mit verwaltetem Code in Visual Studio 2012 entwickelt erweitern.</span><span class="sxs-lookup"><span data-stu-id="8e781-105">You can greatly enhance the functionality of your InfoPath forms by extending them with managed code developed in Visual Studio 2012.</span></span> <span data-ttu-id="8e781-106">Sie können von Formularen mit Code klicken Sie dann auf SharePoint Server 2013 in Formularbibliotheken veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="8e781-106">You can then publish your forms with code to form libraries on SharePoint Server 2013.</span></span>
  
<span data-ttu-id="8e781-107">Wenn Sie InfoPath-Formulare mit verwaltetem Code programmieren und bereitstellen möchten, müssen Sie zunächst drei allgemeine Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="8e781-107">You can start programming and deploying your InfoPath forms with managed code in three high-level steps:</span></span>
  
1. <span data-ttu-id="8e781-108">Installieren Sie Visual Studio 2012, mit dem [Microsoft Visual Studio Tools for Applications 2012](http://www.microsoft.com/en-us/download/details.aspx?id=38807) Add-on.</span><span class="sxs-lookup"><span data-stu-id="8e781-108">Install Visual Studio 2012 with the [Microsoft Visual Studio Tools for Applications 2012](http://www.microsoft.com/en-us/download/details.aspx?id=38807) add-on.</span></span> 
    
2. <span data-ttu-id="8e781-109">Die Programmiersprache festlegen und Schreiben und Debuggen von Code im Code-Editor von Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="8e781-109">Set your programming language, and then write and debug code in the Visual Studio 2012 code editor.</span></span>
    
3. <span data-ttu-id="8e781-110">Wenn Sie das Formular entwerfen und Entwickeln von Ihrem Code abgeschlossen haben, kann die Formularvorlage in SharePoint Server 2013 veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="8e781-110">When you have finished designing the form and developing your code, the form template can be published to SharePoint Server 2013.</span></span>
    
<span data-ttu-id="8e781-111">Es folgen einige Gründe Formulare erstellen, die mit SharePoint Server 2013 kompatibel sind:</span><span class="sxs-lookup"><span data-stu-id="8e781-111">Here are some reasons to consider creating forms that are compatible with SharePoint Server 2013:</span></span>
  
- <span data-ttu-id="8e781-112">Formulare, die in SharePoint Server 2013 mit InfoPath Forms Services bereitgestellt können in einem Browser ausgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="8e781-112">Forms deployed to SharePoint Server 2013 with InfoPath Forms Services can be filled out in a browser.</span></span> <span data-ttu-id="8e781-113">Dies ermöglicht Benutzern, die nicht über InfoPath installiert sind, öffnen und Verwenden von Formularen verfügen.</span><span class="sxs-lookup"><span data-stu-id="8e781-113">This enables users who do not have InfoPath installed to open and use your forms.</span></span>
    
- <span data-ttu-id="8e781-114">Entwerfen Sie nur eine Version des Formulars.</span><span class="sxs-lookup"><span data-stu-id="8e781-114">You design only one version of the form.</span></span> <span data-ttu-id="8e781-115">Formulare, die mit Microsoft SharePoint Server kompatibel sind, sind auch kompatibel mit InfoPath Filler, aber die Formulare, die nur mit InfoPath Filler kompatibel sind, können nicht im Browser geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="8e781-115">Forms that are compatible with Microsoft SharePoint Server are also compatible with the InfoPath Filler, but forms that are compatible only with the InfoPath Filler cannot be opened in the browser.</span></span>
    
<span data-ttu-id="8e781-116">Es gibt zwei Methoden, um das Formular in SharePoint veröffentlichen: SharePoint sandboxed Solutions und vom Administrator bereitgestellte Lösungen.</span><span class="sxs-lookup"><span data-stu-id="8e781-116">There are two ways to publish your form to SharePoint: SharePoint sandboxed solutions, and administrator-deployed solutions.</span></span> <span data-ttu-id="8e781-117">Weitere Informationen zu den einzelnen Publikation-Methode und Vorschläge, welche Methode am besten für Ihr Szenario ist, finden Sie unter [Publishing Forms with Code](publishing-forms-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="8e781-117">For more information about each publication method and suggestions about which method is best for your scenario, see [Publishing Forms with Code](publishing-forms-with-code.md).</span></span> <span data-ttu-id="8e781-118">Beispiel: Lösungen für sandkastenlösungen, [Beispiele für Sandkastenlösungen](sample-sandboxed-solutions.md)angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8e781-118">For example solutions for sandboxed solutions, see [Sample Sandboxed Solutions](sample-sandboxed-solutions.md).</span></span>
  
## <a name="developing-with-visual-studio"></a><span data-ttu-id="8e781-119">Bei der Entwicklung mit Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8e781-119">Developing with Visual Studio</span></span>

<span data-ttu-id="8e781-120">Mit Visual Studio 2012 und Microsoft Visual Studio Tools for Applications 2012 Add-on installiert können Sie zum Entwickeln von Lösungen für InfoPath managed Code beginnen.</span><span class="sxs-lookup"><span data-stu-id="8e781-120">With Visual Studio 2012 and the Microsoft Visual Studio Tools for Applications 2012 add-on installed, you are ready to start to develop InfoPath managed code solutions.</span></span>
  
### <a name="choosing-a-programming-language"></a><span data-ttu-id="8e781-121">Auswählen einer Programmiersprache</span><span class="sxs-lookup"><span data-stu-id="8e781-121">Choosing a Programming Language</span></span>

<span data-ttu-id="8e781-122">InfoPath finden Sie die Optionen zum Programmieren mit vier Versionen von InfoPath-Objektmodells in zwei Sprachen: Visual Basic und c#.</span><span class="sxs-lookup"><span data-stu-id="8e781-122">InfoPath provides the options to program by using four versions of the InfoPath object model in two languages: Visual Basic and C#.</span></span> <span data-ttu-id="8e781-123">Die vier Versionen des Objektmodells bieten die Kompatibilität mit InfoPath 2013, InfoPath, Office InfoPath 2007 und Microsoft InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="8e781-123">The four versions of the object model provide compatibility with InfoPath 2013, InfoPath, Office InfoPath 2007, and Microsoft InfoPath 2003.</span></span>
  
### <a name="to-specify-the-programming-language-and-object-model"></a><span data-ttu-id="8e781-124">So geben Sie die Programmiersprache und das Objektmodell an</span><span class="sxs-lookup"><span data-stu-id="8e781-124">To specify the programming language and object model</span></span>

1. <span data-ttu-id="8e781-125">Ein Formularvorlagenprojekt in InfoPath-Designer geöffnet klicken Sie auf der Registerkarte **Entwickler** auf **Sprache** .</span><span class="sxs-lookup"><span data-stu-id="8e781-125">With a form template project open in the InfoPath designer, click **Language** on the **Developer** tab.</span></span> 
    
2. <span data-ttu-id="8e781-126">Wählen Sie in der Kategorie **Programmierung** im Dialogfeld **Formularoptionen** die Sprache, die Sie aus der Dropdownliste **Codesprache der Formularvorlage** mit arbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="8e781-126">In the **Programming** category of the **Form Options** dialog box, select the language that you want to work with from the **Form template code language** drop-down list.</span></span> <span data-ttu-id="8e781-127">Wählen Sie dann die Version des Objektmodells aus der Dropdownliste **Zielversion** .</span><span class="sxs-lookup"><span data-stu-id="8e781-127">Then, select the version of the object model from the **Target version** drop-down list.</span></span> <span data-ttu-id="8e781-128">Eine Version Jahr nach dem Namen der **InfoPath** keinen die **Zielversion** -Option, die nur mit InfoPath 2013 kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="8e781-128">The **Target version** option that is compatible only with InfoPath 2013 does not have a version year following the **InfoPath** name.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="8e781-129">Nicht alle Formulartypen Vorlage unterstützen Code.</span><span class="sxs-lookup"><span data-stu-id="8e781-129">Not all form template types support code.</span></span> <span data-ttu-id="8e781-130">Beispielsweise führen Sie die **SharePoint-Liste** Vorlage Formulartyp und **Vorlagenparts** Formularcode nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8e781-130">For example, the **SharePoint List** form template type and **Template Parts** do not support form code.</span></span> <span data-ttu-id="8e781-131">Wenn Sie einen Vorlagentyp Formular entwerfen, der Code nicht unterstützt, wird die Registerkarte **Entwicklertools** nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8e781-131">When designing a form template type that does not support code, the **Developer** tab will not be available.</span></span> <span data-ttu-id="8e781-132">Darüber hinaus unterstützen nur einige Formulartypen Vorlage alle vier Versionen des Objektmodells.</span><span class="sxs-lookup"><span data-stu-id="8e781-132">Also, only some form template types support all four versions of the object model.</span></span> <span data-ttu-id="8e781-133">Beispielsweise der Vorlagentyp **Leeres Formular (InfoPath Filler)** unterstützt alle vier Versionen des Objektmodells (und erstellt die Formularvorlage, die nur mit InfoPath Filler in diesen Versionen kompatibel sind), aber die Vorlage **Leeres Formular** unterstützt nur InfoPath 2013 und InfoPath (und -Formularvorlagen, die mit InfoPath Filler und im Browser kompatibel sind erstellt).</span><span class="sxs-lookup"><span data-stu-id="8e781-133">For example, the **Blank Form (InfoPath Filler)** template type supports all four versions of the object model (and creates form template that are compatible only with the InfoPath Filler in those versions), but the **Blank Form** template supports only InfoPath 2013 and InfoPath (and creates form templates that are compatible with both the InfoPath Filler and the browser).</span></span> 
  
    <span data-ttu-id="8e781-134">Sie können festlegen, dass eine Standardprogrammiersprache, sodass immer im InfoPath-Formular-Designer mit der Sprache und Objektmodellversion Ihrer Wahl gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="8e781-134">You can set a default programming language so that the InfoPath form designer will always start with the language and object model version of your choice.</span></span>
    
### <a name="to-set-the-default-programming-language"></a><span data-ttu-id="8e781-135">So legen Sie die Standardprogrammiersprache fest</span><span class="sxs-lookup"><span data-stu-id="8e781-135">To set the default programming language</span></span>

1. <span data-ttu-id="8e781-136">Klicken Sie auf die Registerkarte **Datei** und dann auf **Optionen**.</span><span class="sxs-lookup"><span data-stu-id="8e781-136">Click the **File** tab, and then click **Options**.</span></span>
    
2. <span data-ttu-id="8e781-137">Klicken Sie im Abschnitt **Allgemein** des Dialogfelds **InfoPath-Optionen** auf **Weitere Optionen**.</span><span class="sxs-lookup"><span data-stu-id="8e781-137">In the **General** section of the **InfoPath Options** dialog box, click **More Options**.</span></span>
    
3. <span data-ttu-id="8e781-138">Wählen Sie auf der Registerkarte **Entwurf** des Dialogfelds **Optionen** im Abschnitt **Standardeinstellungen für Programmierung** die Standardprogrammiersprache aus.</span><span class="sxs-lookup"><span data-stu-id="8e781-138">On the **Design** tab of the **Options** dialog box, select the default programming language in the **Programming Defaults** section.</span></span> 
    
### <a name="writing-code"></a><span data-ttu-id="8e781-139">Schreiben von Code</span><span class="sxs-lookup"><span data-stu-id="8e781-139">Writing Code</span></span>

<span data-ttu-id="8e781-140">Nun können Sie mit InfoPath 2013 und Visual Studio 2012 entwickeln.</span><span class="sxs-lookup"><span data-stu-id="8e781-140">You can now start to develop with InfoPath 2013 and Visual Studio 2012.</span></span> 
  
### <a name="to-start-the-visual-studio-code-editor"></a><span data-ttu-id="8e781-141">Starten Sie im Code-Editor von Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8e781-141">To start the Visual Studio Code Editor</span></span>

1. <span data-ttu-id="8e781-142">Öffnen Sie eine Formularvorlage im InfoPath-Designer.</span><span class="sxs-lookup"><span data-stu-id="8e781-142">Open a form template in the InfoPath designer.</span></span>
    
2. <span data-ttu-id="8e781-143">Klicken Sie auf der Registerkarte **Entwicklertools** auf **Code-Editor** .</span><span class="sxs-lookup"><span data-stu-id="8e781-143">Click **Code Editor** on the **Developer** tab.</span></span> 
    
> [!TIP]
> <span data-ttu-id="8e781-144">Sie können auch im Code-Editor zu starten und automatisch hinzufügen Ereignishandler für Formular- und Ereignisse, die mithilfe der Befehle auf der Registerkarte **Entwicklertools** , Kontextmenüs und andere User Interface-Methoden.</span><span class="sxs-lookup"><span data-stu-id="8e781-144">You can also start the code editor and automatically add event handlers for form and control events using commands on the **Developer** tab, context menus, and other user interface methods.</span></span> <span data-ttu-id="8e781-145">Weitere Informationen finden Sie unter [Hinzufügen eines Ereignishandlers](how-to-add-an-event-handler.md)</span><span class="sxs-lookup"><span data-stu-id="8e781-145">For more information, see [Add an Event Handler](how-to-add-an-event-handler.md)</span></span>
  

