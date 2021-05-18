---
title: Entwicklung mit Visual Studio
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39d633d-d8fb-4e2f-a396-6cb50beb8c3e
description: Sie können die Funktionalität Ihrer InfoPath-Formulare erheblich verbessern, indem Sie sie mit verwalteten Code erweitern, der in Visual Studio 2012 entwickelt wurde. Anschließend können Sie Ihre Formulare mit Code in Formularbibliotheken auf SharePoint Server 2013 veröffentlichen.
ms.openlocfilehash: 1c67b85823fe567b494366a505be5dad51d20b32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300287"
---
# <a name="develop-with-visual-studio"></a><span data-ttu-id="85f5f-104">Entwicklung mit Visual Studio</span><span class="sxs-lookup"><span data-stu-id="85f5f-104">Develop with Visual Studio</span></span>

<span data-ttu-id="85f5f-105">Sie können die Funktionalität Ihrer InfoPath-Formulare erheblich verbessern, indem Sie sie mit verwalteten Code erweitern, der in Visual Studio 2012 entwickelt wurde.</span><span class="sxs-lookup"><span data-stu-id="85f5f-105">You can greatly enhance the functionality of your InfoPath forms by extending them with managed code developed in Visual Studio 2012.</span></span> <span data-ttu-id="85f5f-106">Anschließend können Sie Ihre Formulare mit Code in Formularbibliotheken auf SharePoint Server 2013 veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="85f5f-106">You can then publish your forms with code to form libraries on SharePoint Server 2013.</span></span>
  
<span data-ttu-id="85f5f-107">Wenn Sie InfoPath-Formulare mit verwaltetem Code programmieren und bereitstellen möchten, müssen Sie zunächst drei allgemeine Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="85f5f-107">You can start programming and deploying your InfoPath forms with managed code in three high-level steps:</span></span>
  
1. <span data-ttu-id="85f5f-108">Installieren Visual Studio 2012 mit [dem Microsoft Visual Studio-Tools für Anwendungen 2012-Add-On.](https://www.microsoft.com/en-us/download/details.aspx?id=38807)</span><span class="sxs-lookup"><span data-stu-id="85f5f-108">Install Visual Studio 2012 with the [Microsoft Visual Studio Tools for Applications 2012](https://www.microsoft.com/en-us/download/details.aspx?id=38807) add-on.</span></span> 
    
2. <span data-ttu-id="85f5f-109">Legen Sie Ihre Programmiersprache, und schreiben und debuggen Sie code dann im Visual Studio 2012-Code-Editor.</span><span class="sxs-lookup"><span data-stu-id="85f5f-109">Set your programming language, and then write and debug code in the Visual Studio 2012 code editor.</span></span>
    
3. <span data-ttu-id="85f5f-110">Wenn Sie mit dem Entwerfen des Formulars und der Entwicklung des Codes fertig sind, kann die Formularvorlage auf server 2013 SharePoint veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="85f5f-110">When you have finished designing the form and developing your code, the form template can be published to SharePoint Server 2013.</span></span>
    
<span data-ttu-id="85f5f-111">Hier finden Sie einige Gründe, warum Sie das Erstellen von Formularen in Betracht ziehen sollten, die mit SharePoint Server 2013 kompatibel sind:</span><span class="sxs-lookup"><span data-stu-id="85f5f-111">Here are some reasons to consider creating forms that are compatible with SharePoint Server 2013:</span></span>
  
- <span data-ttu-id="85f5f-112">Formulare, die auf SharePoint Server 2013 mit InfoPath Forms Services bereitgestellt werden, können in einem Browser ausgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="85f5f-112">Forms deployed to SharePoint Server 2013 with InfoPath Forms Services can be filled out in a browser.</span></span> <span data-ttu-id="85f5f-113">Auf diese Weise können Benutzer, für die InfoPath nicht installiert ist, Ihre Formulare öffnen und verwenden.</span><span class="sxs-lookup"><span data-stu-id="85f5f-113">This enables users who do not have InfoPath installed to open and use your forms.</span></span>
    
- <span data-ttu-id="85f5f-114">Sie entwerfen nur eine Version des Formulars.</span><span class="sxs-lookup"><span data-stu-id="85f5f-114">You design only one version of the form.</span></span> <span data-ttu-id="85f5f-115">Formulare, die mit Microsoft SharePoint Server kompatibel sind, sind auch mit dem InfoPath Filler kompatibel, aber Formulare, die nur mit dem InfoPath Filler kompatibel sind, können nicht im Browser geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="85f5f-115">Forms that are compatible with Microsoft SharePoint Server are also compatible with the InfoPath Filler, but forms that are compatible only with the InfoPath Filler cannot be opened in the browser.</span></span>
    
<span data-ttu-id="85f5f-116">Es gibt zwei Möglichkeiten zum Veröffentlichen des Formulars SharePoint: SharePoint Sandkastenlösungen und vom Administrator bereitgestellte Lösungen.</span><span class="sxs-lookup"><span data-stu-id="85f5f-116">There are two ways to publish your form to SharePoint: SharePoint sandboxed solutions, and administrator-deployed solutions.</span></span> <span data-ttu-id="85f5f-117">Weitere Informationen zu jeder Publikationsmethode und Vorschläge dazu, welche Methode für Ihr Szenario am besten ist, finden Sie unter [Publishing Forms with Code](publishing-forms-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="85f5f-117">For more information about each publication method and suggestions about which method is best for your scenario, see [Publishing Forms with Code](publishing-forms-with-code.md).</span></span> <span data-ttu-id="85f5f-118">Beispiellösungen für Sandkastenlösungen finden Sie unter [Beispiel sandkastenlösungen](sample-sandboxed-solutions.md).</span><span class="sxs-lookup"><span data-stu-id="85f5f-118">For example solutions for sandboxed solutions, see [Sample Sandboxed Solutions](sample-sandboxed-solutions.md).</span></span>
  
## <a name="developing-with-visual-studio"></a><span data-ttu-id="85f5f-119">Entwickeln mit Visual Studio</span><span class="sxs-lookup"><span data-stu-id="85f5f-119">Developing with Visual Studio</span></span>

<span data-ttu-id="85f5f-120">Mit Visual Studio 2012 und dem Microsoft Visual Studio-Tools für Anwendungen 2012-Add-On können Sie mit der Entwicklung von Lösungen für verwalteten Code von InfoPath beginnen.</span><span class="sxs-lookup"><span data-stu-id="85f5f-120">With Visual Studio 2012 and the Microsoft Visual Studio Tools for Applications 2012 add-on installed, you are ready to start to develop InfoPath managed code solutions.</span></span>
  
### <a name="choosing-a-programming-language"></a><span data-ttu-id="85f5f-121">Auswählen einer Programmiersprache</span><span class="sxs-lookup"><span data-stu-id="85f5f-121">Choosing a Programming Language</span></span>

<span data-ttu-id="85f5f-122">InfoPath bietet die Optionen zum Programmieren mithilfe von vier Versionen des InfoPath-Objektmodells in zwei Sprachen: Visual Basic und C#.</span><span class="sxs-lookup"><span data-stu-id="85f5f-122">InfoPath provides the options to program by using four versions of the InfoPath object model in two languages: Visual Basic and C#.</span></span> <span data-ttu-id="85f5f-123">Die vier Versionen des Objektmodells bieten Kompatibilität mit InfoPath 2013, InfoPath, Office InfoPath 2007 und Microsoft InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="85f5f-123">The four versions of the object model provide compatibility with InfoPath 2013, InfoPath, Office InfoPath 2007, and Microsoft InfoPath 2003.</span></span>
  
### <a name="to-specify-the-programming-language-and-object-model"></a><span data-ttu-id="85f5f-124">So geben Sie die Programmiersprache und das Objektmodell an</span><span class="sxs-lookup"><span data-stu-id="85f5f-124">To specify the programming language and object model</span></span>

1. <span data-ttu-id="85f5f-125">Wenn ein Formularvorlagenprojekt im InfoPath-Designer geöffnet ist, klicken Sie auf **der** Registerkarte Entwickler auf **Sprache.**</span><span class="sxs-lookup"><span data-stu-id="85f5f-125">With a form template project open in the InfoPath designer, click **Language** on the **Developer** tab.</span></span> 
    
2. <span data-ttu-id="85f5f-126">Wählen Sie in der Kategorie **Programmierung** des Dialogfelds **Formularoptionen** in der Dropdownliste **Codesprache der Formularvorlage** die Sprache aus, mit der Sie arbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="85f5f-126">In the **Programming** category of the **Form Options** dialog box, select the language that you want to work with from the **Form template code language** drop-down list.</span></span> <span data-ttu-id="85f5f-127">Wählen Sie dann in der Dropdownliste  Zielversion die Version des Objektmodells aus.</span><span class="sxs-lookup"><span data-stu-id="85f5f-127">Then, select the version of the object model from the **Target version** drop-down list.</span></span> <span data-ttu-id="85f5f-128">Die **Option Zielversion,** die nur mit InfoPath 2013 kompatibel ist, verfügt nicht über ein Versionsjahr nach dem **Namen InfoPath.**</span><span class="sxs-lookup"><span data-stu-id="85f5f-128">The **Target version** option that is compatible only with InfoPath 2013 does not have a version year following the **InfoPath** name.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="85f5f-129">Nicht alle Formularvorlagentypen unterstützen Code.</span><span class="sxs-lookup"><span data-stu-id="85f5f-129">Not all form template types support code.</span></span> <span data-ttu-id="85f5f-130">Der Formularvorlagentyp SharePoint **und** Vorlagenteile  unterstützen z. B. keinen Formularcode.</span><span class="sxs-lookup"><span data-stu-id="85f5f-130">For example, the **SharePoint List** form template type and **Template Parts** do not support form code.</span></span> <span data-ttu-id="85f5f-131">Beim Entwerfen eines Formularvorlagentyps, der keinen Code unterstützt, ist **die** Registerkarte Entwickler nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="85f5f-131">When designing a form template type that does not support code, the **Developer** tab will not be available.</span></span> <span data-ttu-id="85f5f-132">Außerdem unterstützen nur einige Formularvorlagentypen alle vier Versionen des Objektmodells.</span><span class="sxs-lookup"><span data-stu-id="85f5f-132">Also, only some form template types support all four versions of the object model.</span></span> <span data-ttu-id="85f5f-133">Beispielsweise unterstützt der Vorlagentyp Leeres **Formular (InfoPath Filler)** alle vier Versionen des Objektmodells (und erstellt Formularvorlagen,  die nur mit dem InfoPath Filler in diesen Versionen kompatibel sind), aber die Vorlage Leeres Formular unterstützt nur InfoPath 2013 und InfoPath (und erstellt Formularvorlagen, die sowohl mit dem InfoPath Filler als auch mit dem Browser kompatibel sind).</span><span class="sxs-lookup"><span data-stu-id="85f5f-133">For example, the **Blank Form (InfoPath Filler)** template type supports all four versions of the object model (and creates form template that are compatible only with the InfoPath Filler in those versions), but the **Blank Form** template supports only InfoPath 2013 and InfoPath (and creates form templates that are compatible with both the InfoPath Filler and the browser).</span></span> 
  
    <span data-ttu-id="85f5f-134">Sie können eine Standardprogrammiersprache festlegen, damit der InfoPath-Formulardesigner immer mit der Sprach- und Objektmodellversion Ihrer Wahl beginnt.</span><span class="sxs-lookup"><span data-stu-id="85f5f-134">You can set a default programming language so that the InfoPath form designer will always start with the language and object model version of your choice.</span></span>
    
### <a name="to-set-the-default-programming-language"></a><span data-ttu-id="85f5f-135">So legen Sie die Standardprogrammiersprache fest</span><span class="sxs-lookup"><span data-stu-id="85f5f-135">To set the default programming language</span></span>

1. <span data-ttu-id="85f5f-136">Klicken Sie auf die Registerkarte **Datei** und dann auf **Optionen**.</span><span class="sxs-lookup"><span data-stu-id="85f5f-136">Click the **File** tab, and then click **Options**.</span></span>
    
2. <span data-ttu-id="85f5f-137">Klicken Sie im Abschnitt **Allgemein** des Dialogfelds **InfoPath-Optionen** auf **Weitere Optionen**.</span><span class="sxs-lookup"><span data-stu-id="85f5f-137">In the **General** section of the **InfoPath Options** dialog box, click **More Options**.</span></span>
    
3. <span data-ttu-id="85f5f-138">Wählen Sie auf der Registerkarte **Entwurf** des Dialogfelds **Optionen** im Abschnitt **Standardeinstellungen für Programmierung** die Standardprogrammiersprache aus. </span><span class="sxs-lookup"><span data-stu-id="85f5f-138">On the **Design** tab of the **Options** dialog box, select the default programming language in the **Programming Defaults** section.</span></span> 
    
### <a name="writing-code"></a><span data-ttu-id="85f5f-139">Schreiben von Code</span><span class="sxs-lookup"><span data-stu-id="85f5f-139">Writing Code</span></span>

<span data-ttu-id="85f5f-140">Sie können nun mit der Entwicklung mit InfoPath 2013 und Visual Studio 2012 beginnen.</span><span class="sxs-lookup"><span data-stu-id="85f5f-140">You can now start to develop with InfoPath 2013 and Visual Studio 2012.</span></span> 
  
### <a name="to-start-the-visual-studio-code-editor"></a><span data-ttu-id="85f5f-141">So starten Sie den Visual Studio Code Editor</span><span class="sxs-lookup"><span data-stu-id="85f5f-141">To start the Visual Studio Code Editor</span></span>

1. <span data-ttu-id="85f5f-142">Öffnen Sie eine Formularvorlage im InfoPath-Designer.</span><span class="sxs-lookup"><span data-stu-id="85f5f-142">Open a form template in the InfoPath designer.</span></span>
    
2. <span data-ttu-id="85f5f-143">Klicken Sie auf der Registerkarte **Entwickler** auf **Code-Editor**.</span><span class="sxs-lookup"><span data-stu-id="85f5f-143">Click **Code Editor** on the **Developer** tab.</span></span> 
    
> [!TIP]
> <span data-ttu-id="85f5f-144">Sie können auch den Code-Editor starten und mithilfe von Befehlen  auf der Registerkarte Entwickler, Kontextmenüs und anderen Benutzeroberflächenmethoden automatisch Ereignishandler für Formular- und Steuerelementereignisse hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="85f5f-144">You can also start the code editor and automatically add event handlers for form and control events using commands on the **Developer** tab, context menus, and other user interface methods.</span></span> <span data-ttu-id="85f5f-145">Weitere Informationen finden Sie unter [Add an Event Handler](how-to-add-an-event-handler.md)</span><span class="sxs-lookup"><span data-stu-id="85f5f-145">For more information, see [Add an Event Handler](how-to-add-an-event-handler.md)</span></span>
  

