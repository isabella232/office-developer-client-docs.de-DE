---
title: Entwicklung mit Visual Studio
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39d633d-d8fb-4e2f-a396-6cb50beb8c3e
description: Sie können die Funktionalität Ihrer InfoPath-Formulare erheblich verbessern, indem Sie Sie mit verwaltetem Code erweitern, der in Visual Studio 2012 entwickelt wurde. Sie können Ihre Formulare dann mit Code veröffentlichen, um Bibliotheken auf SharePoint Server 2013 zu bilden.
ms.openlocfilehash: 1c67b85823fe567b494366a505be5dad51d20b32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300287"
---
# <a name="develop-with-visual-studio"></a><span data-ttu-id="758a5-104">Entwicklung mit Visual Studio</span><span class="sxs-lookup"><span data-stu-id="758a5-104">Develop with Visual Studio</span></span>

<span data-ttu-id="758a5-105">Sie können die Funktionalität Ihrer InfoPath-Formulare erheblich verbessern, indem Sie Sie mit verwaltetem Code erweitern, der in Visual Studio 2012 entwickelt wurde.</span><span class="sxs-lookup"><span data-stu-id="758a5-105">You can greatly enhance the functionality of your InfoPath forms by extending them with managed code developed in Visual Studio 2012.</span></span> <span data-ttu-id="758a5-106">Sie können Ihre Formulare dann mit Code veröffentlichen, um Bibliotheken auf SharePoint Server 2013 zu bilden.</span><span class="sxs-lookup"><span data-stu-id="758a5-106">You can then publish your forms with code to form libraries on SharePoint Server 2013.</span></span>
  
<span data-ttu-id="758a5-107">Wenn Sie InfoPath-Formulare mit verwaltetem Code programmieren und bereitstellen möchten, müssen Sie zunächst drei allgemeine Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="758a5-107">You can start programming and deploying your InfoPath forms with managed code in three high-level steps:</span></span>
  
1. <span data-ttu-id="758a5-108">Installieren Sie Visual Studio 2012 mit dem Add-on [für Microsoft Visual Studio Tools for Applications 2012](https://www.microsoft.com/en-us/download/details.aspx?id=38807) .</span><span class="sxs-lookup"><span data-stu-id="758a5-108">Install Visual Studio 2012 with the [Microsoft Visual Studio Tools for Applications 2012](https://www.microsoft.com/en-us/download/details.aspx?id=38807) add-on.</span></span> 
    
2. <span data-ttu-id="758a5-109">Legen Sie Ihre Programmiersprache fest, und schreiben und Debuggen Sie dann Code im Code-Editor von Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="758a5-109">Set your programming language, and then write and debug code in the Visual Studio 2012 code editor.</span></span>
    
3. <span data-ttu-id="758a5-110">Nachdem Sie das Formular entworfen und den Code entwickelt haben, kann die Formularvorlage in SharePoint Server 2013 veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="758a5-110">When you have finished designing the form and developing your code, the form template can be published to SharePoint Server 2013.</span></span>
    
<span data-ttu-id="758a5-111">Im folgenden finden Sie einige Gründe für die Erstellung von Formularen, die mit SharePoint Server 2013 kompatibel sind:</span><span class="sxs-lookup"><span data-stu-id="758a5-111">Here are some reasons to consider creating forms that are compatible with SharePoint Server 2013:</span></span>
  
- <span data-ttu-id="758a5-112">Formulare, die in SharePoint Server 2013 mit InfoPath Forms Services bereitgestellt werden, können in einem Browser ausgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="758a5-112">Forms deployed to SharePoint Server 2013 with InfoPath Forms Services can be filled out in a browser.</span></span> <span data-ttu-id="758a5-113">Dadurch können Benutzer, die InfoPath nicht installiert haben, ihre Formulare öffnen und verwenden.</span><span class="sxs-lookup"><span data-stu-id="758a5-113">This enables users who do not have InfoPath installed to open and use your forms.</span></span>
    
- <span data-ttu-id="758a5-114">Sie entwerfen nur eine Version des Formulars.</span><span class="sxs-lookup"><span data-stu-id="758a5-114">You design only one version of the form.</span></span> <span data-ttu-id="758a5-115">Formulare, die mit Microsoft SharePoint Server kompatibel sind, sind auch mit dem InfoPath-Filler kompatibel, aber Formulare, die nur mit dem InfoPath-Füllbereich kompatibel sind, können im Browser nicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="758a5-115">Forms that are compatible with Microsoft SharePoint Server are also compatible with the InfoPath Filler, but forms that are compatible only with the InfoPath Filler cannot be opened in the browser.</span></span>
    
<span data-ttu-id="758a5-116">Es gibt zwei Möglichkeiten, Ihr Formular in SharePoint zu veröffentlichen: SharePoint-sandkastenlösungen und vom Administrator bereitgestellte Lösungen.</span><span class="sxs-lookup"><span data-stu-id="758a5-116">There are two ways to publish your form to SharePoint: SharePoint sandboxed solutions, and administrator-deployed solutions.</span></span> <span data-ttu-id="758a5-117">Weitere Informationen zu den einzelnen Veröffentlichungsmethoden und Vorschlägen dazu, welche Methode für Ihr Szenario am besten geeignet ist, finden Sie unter [Veröffentlichen von Formularen mit Code](publishing-forms-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="758a5-117">For more information about each publication method and suggestions about which method is best for your scenario, see [Publishing Forms with Code](publishing-forms-with-code.md).</span></span> <span data-ttu-id="758a5-118">Beispiele für Lösungen für sandkastenlösungen finden Sie unter [Beispiel für Sandkasten](sample-sandboxed-solutions.md)Lösungen.</span><span class="sxs-lookup"><span data-stu-id="758a5-118">For example solutions for sandboxed solutions, see [Sample Sandboxed Solutions](sample-sandboxed-solutions.md).</span></span>
  
## <a name="developing-with-visual-studio"></a><span data-ttu-id="758a5-119">Entwickeln mit Visual Studio</span><span class="sxs-lookup"><span data-stu-id="758a5-119">Developing with Visual Studio</span></span>

<span data-ttu-id="758a5-120">Mit Visual Studio 2012 und Microsoft Visual Studio Tools for Applications 2012 Add-on installiert sind, können Sie mit der Entwicklung von InfoPath-Lösungen mit verwaltetem Code beginnen.</span><span class="sxs-lookup"><span data-stu-id="758a5-120">With Visual Studio 2012 and the Microsoft Visual Studio Tools for Applications 2012 add-on installed, you are ready to start to develop InfoPath managed code solutions.</span></span>
  
### <a name="choosing-a-programming-language"></a><span data-ttu-id="758a5-121">Auswählen einer Programmiersprache</span><span class="sxs-lookup"><span data-stu-id="758a5-121">Choosing a Programming Language</span></span>

<span data-ttu-id="758a5-122">InfoPath bietet die Optionen zum Programmieren mit vier Versionen des InfoPath-Objektmodells in zwei Sprachen: Visual Basic und C#.</span><span class="sxs-lookup"><span data-stu-id="758a5-122">InfoPath provides the options to program by using four versions of the InfoPath object model in two languages: Visual Basic and C#.</span></span> <span data-ttu-id="758a5-123">Die vier Versionen des Objektmodells bieten Kompatibilität mit InfoPath 2013, InfoPath, Office InfoPath 2007 und Microsoft InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="758a5-123">The four versions of the object model provide compatibility with InfoPath 2013, InfoPath, Office InfoPath 2007, and Microsoft InfoPath 2003.</span></span>
  
### <a name="to-specify-the-programming-language-and-object-model"></a><span data-ttu-id="758a5-124">So geben Sie die Programmiersprache und das Objektmodell an</span><span class="sxs-lookup"><span data-stu-id="758a5-124">To specify the programming language and object model</span></span>

1. <span data-ttu-id="758a5-125">Wenn ein Formularvorlagenprojekt im InfoPath-Designer geöffnet ist, klicken Sie auf der Registerkarte **Entwickler** auf **Sprache** .</span><span class="sxs-lookup"><span data-stu-id="758a5-125">With a form template project open in the InfoPath designer, click **Language** on the **Developer** tab.</span></span> 
    
2. <span data-ttu-id="758a5-126">Wählen Sie in der Kategorie **Programmierung** des Dialogfelds **Formularoptionen** in der Dropdownliste **Codesprache der Formularvorlage** die Sprache aus, mit der Sie arbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="758a5-126">In the **Programming** category of the **Form Options** dialog box, select the language that you want to work with from the **Form template code language** drop-down list.</span></span> <span data-ttu-id="758a5-127">Wählen Sie dann in der Dropdownliste **Zielversion** die Version des Objektmodells aus.</span><span class="sxs-lookup"><span data-stu-id="758a5-127">Then, select the version of the object model from the **Target version** drop-down list.</span></span> <span data-ttu-id="758a5-128">Die Option **Zielversion** , die nur mit InfoPath 2013 kompatibel ist, verfügt nicht über ein Versions Jahr, das dem **InfoPath** -Namen folgt.</span><span class="sxs-lookup"><span data-stu-id="758a5-128">The **Target version** option that is compatible only with InfoPath 2013 does not have a version year following the **InfoPath** name.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="758a5-129">Nicht alle Formularvorlagen Typen unterstützen Code.</span><span class="sxs-lookup"><span data-stu-id="758a5-129">Not all form template types support code.</span></span> <span data-ttu-id="758a5-130">Beispielsweise unterstützen der Typ der **SharePoint-Listen** Formularvorlagen und **Vorlagen Parts** den Formularcode nicht.</span><span class="sxs-lookup"><span data-stu-id="758a5-130">For example, the **SharePoint List** form template type and **Template Parts** do not support form code.</span></span> <span data-ttu-id="758a5-131">Beim Entwerfen eines Formularvorlagen Typs, der keinen Code unterstützt, ist die Registerkarte **Entwicklertools** nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="758a5-131">When designing a form template type that does not support code, the **Developer** tab will not be available.</span></span> <span data-ttu-id="758a5-132">Außerdem unterstützen nur einige Formularvorlagen Typen alle vier Versionen des Objektmodells.</span><span class="sxs-lookup"><span data-stu-id="758a5-132">Also, only some form template types support all four versions of the object model.</span></span> <span data-ttu-id="758a5-133">Der Vorlagentyp **leeres Formular (InfoPath Filler)** unterstützt beispielsweise alle vier Versionen des Objektmodells (und erstellt Formularvorlagen, die nur mit dem InfoPath-Füller in diesen Versionen kompatibel sind), aber die **leere Formular** Vorlage unterstützt nur InfoPath 2013 und InfoPath (und erstellt Formularvorlagen, die sowohl mit dem InfoPath-Füller als auch mit dem Browser kompatibel sind).</span><span class="sxs-lookup"><span data-stu-id="758a5-133">For example, the **Blank Form (InfoPath Filler)** template type supports all four versions of the object model (and creates form template that are compatible only with the InfoPath Filler in those versions), but the **Blank Form** template supports only InfoPath 2013 and InfoPath (and creates form templates that are compatible with both the InfoPath Filler and the browser).</span></span> 
  
    <span data-ttu-id="758a5-134">Sie können eine Standard Programmiersprache festlegen, sodass der InfoPath-Formular-Designer immer mit der Sprach-und Objektmodellversion Ihrer Wahl beginnt.</span><span class="sxs-lookup"><span data-stu-id="758a5-134">You can set a default programming language so that the InfoPath form designer will always start with the language and object model version of your choice.</span></span>
    
### <a name="to-set-the-default-programming-language"></a><span data-ttu-id="758a5-135">So legen Sie die Standardprogrammiersprache fest</span><span class="sxs-lookup"><span data-stu-id="758a5-135">To set the default programming language</span></span>

1. <span data-ttu-id="758a5-136">Klicken Sie auf die Registerkarte **Datei** und dann auf **Optionen**.</span><span class="sxs-lookup"><span data-stu-id="758a5-136">Click the **File** tab, and then click **Options**.</span></span>
    
2. <span data-ttu-id="758a5-137">Klicken Sie im Abschnitt **Allgemein** des Dialogfelds **InfoPath-Optionen** auf **Weitere Optionen**.</span><span class="sxs-lookup"><span data-stu-id="758a5-137">In the **General** section of the **InfoPath Options** dialog box, click **More Options**.</span></span>
    
3. <span data-ttu-id="758a5-138">Wählen Sie auf der Registerkarte **Entwurf** des Dialogfelds **Optionen** im Abschnitt **Standardeinstellungen für Programmierung** die Standardprogrammiersprache aus. </span><span class="sxs-lookup"><span data-stu-id="758a5-138">On the **Design** tab of the **Options** dialog box, select the default programming language in the **Programming Defaults** section.</span></span> 
    
### <a name="writing-code"></a><span data-ttu-id="758a5-139">Schreiben von Code</span><span class="sxs-lookup"><span data-stu-id="758a5-139">Writing Code</span></span>

<span data-ttu-id="758a5-140">Sie können nun mit InfoPath 2013 und Visual Studio 2012 entwickeln.</span><span class="sxs-lookup"><span data-stu-id="758a5-140">You can now start to develop with InfoPath 2013 and Visual Studio 2012.</span></span> 
  
### <a name="to-start-the-visual-studio-code-editor"></a><span data-ttu-id="758a5-141">So starten Sie den Visual Studio-Code-Editor</span><span class="sxs-lookup"><span data-stu-id="758a5-141">To start the Visual Studio Code Editor</span></span>

1. <span data-ttu-id="758a5-142">Öffnen Sie eine Formularvorlage im InfoPath-Designer.</span><span class="sxs-lookup"><span data-stu-id="758a5-142">Open a form template in the InfoPath designer.</span></span>
    
2. <span data-ttu-id="758a5-143">Klicken Sie auf der Registerkarte **Entwickler** auf **Code-Editor**.</span><span class="sxs-lookup"><span data-stu-id="758a5-143">Click **Code Editor** on the **Developer** tab.</span></span> 
    
> [!TIP]
> <span data-ttu-id="758a5-144">Sie können den Code-Editor auch starten und automatisch Ereignishandler für Formular-und Steuerelementereignisse mithilfe von Befehlen auf der Registerkarte **Entwickler** , Kontextmenüs und andere Benutzeroberflächenmethoden hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="758a5-144">You can also start the code editor and automatically add event handlers for form and control events using commands on the **Developer** tab, context menus, and other user interface methods.</span></span> <span data-ttu-id="758a5-145">Weitere Informationen finden Sie unter [Hinzufügen eines Ereignishandlers](how-to-add-an-event-handler.md) .</span><span class="sxs-lookup"><span data-stu-id="758a5-145">For more information, see [Add an Event Handler](how-to-add-an-event-handler.md)</span></span>
  

