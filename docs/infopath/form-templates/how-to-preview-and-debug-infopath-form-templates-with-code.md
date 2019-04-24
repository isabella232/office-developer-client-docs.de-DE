---
title: Vorschau und Debuggen von InfoPath-Formularvorlagen mit Code
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Vorschau von Formularvorlagen [InfoPath 2007], Debuggen von Formularvorlagen [InfoPath 2007], Formularvorlagen [InfoPath 2007], Vorschau, Debuggen [InfoPath 2007], Formularvorlagen für verwalteten Code, Formularvorlagen [InfoPath 2007], Debuggen, InfoPath 2007, Debuggen Formularvorlagen, InfoPath 2007, Vorschau von Formularvorlagen
localization_priority: Normal
ms.assetid: c8387f1c-b34c-490e-8bf9-d824bf98d826
description: Microsoft InfoPath mit Visual Studio 2012 ermöglicht das Debuggen, indem der Formularcode im Vorschaumodus ausgeführt wird. Wenn Sie mit dem Debuggen von Formularcode beginnen, wird das Projekt kompiliert, und das Formular wird von InfoPath im InfoPath-Vorschaufenster angezeigt. Wenn eine Codezeile ermittelt wird, für die ein Haltepunkt festgelegt wurde, wird der Fokus auf den Code-Editor verschoben. Wenn Sie den Vorgang nach einem Haltepunkt fortsetzen, wird der Fokus wieder zum Vorschaufenster verschoben. Das Debuggen wird beendet, wenn Sie das Vorschaufenster schließen.
ms.openlocfilehash: 8f9ff97fdd5b4b016d96129304fa6f994d7b4561
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300434"
---
# <a name="preview-and-debug-infopath-form-templates-with-code"></a><span data-ttu-id="bc259-108">Vorschau und Debuggen von InfoPath-Formularvorlagen mit Code</span><span class="sxs-lookup"><span data-stu-id="bc259-108">Preview and Debug InfoPath Form Templates with Code</span></span>

<span data-ttu-id="bc259-109">Microsoft InfoPath mit Visual Studio 2012 ermöglicht das Debuggen, indem der Formularcode im Vorschaumodus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bc259-109">Microsoft InfoPath with Visual Studio 2012 enables debugging by running form code in preview mode.</span></span> <span data-ttu-id="bc259-110">Wenn Sie mit dem Debuggen von Formularcode beginnen, wird das Projekt kompiliert, und das Formular wird von InfoPath im InfoPath-Vorschaufenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bc259-110">When you start debugging form code, your project is compiled and InfoPath displays your form in the InfoPath preview window.</span></span> <span data-ttu-id="bc259-111">Wenn eine Codezeile ermittelt wird, für die ein Haltepunkt festgelegt wurde, wird der Fokus auf den Code-Editor verschoben.</span><span class="sxs-lookup"><span data-stu-id="bc259-111">When a line of code that has a breakpoint set for it is encountered, the focus moves to the code editor.</span></span> <span data-ttu-id="bc259-112">Wenn Sie den Vorgang nach einem Haltepunkt fortsetzen, wird der Fokus wieder zum Vorschaufenster verschoben.</span><span class="sxs-lookup"><span data-stu-id="bc259-112">When you continue past a breakpoint, the focus moves back to the preview window.</span></span> <span data-ttu-id="bc259-113">Das Debuggen wird beendet, wenn Sie das Vorschaufenster schließen.</span><span class="sxs-lookup"><span data-stu-id="bc259-113">Debugging stops when you close the preview window.</span></span>
  
<span data-ttu-id="bc259-114">Sie können die Formularoptionen für die Formularvorlage auch so ändern, dass Vorschau und Debuggen mithilfe einer bestimmten Benutzerrolle, einer Beispieldatendatei oder durch Angeben der Domäne ausgeführt werden, in der das Formular veröffentlicht wird. </span><span class="sxs-lookup"><span data-stu-id="bc259-114">You can also modify the form options of the form template to preview and debug using a specific user role, a sample data file, or by specifying the domain to which the form will be published.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="bc259-115">Es ist nicht möglich, Formularvorlagen zu debuggen, nachdem Sie zur Laufzeit von Visual Studio 2012 bereitgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="bc259-115">It is not possible to debug form templates after they are deployed at run time from Visual Studio 2012.</span></span> <span data-ttu-id="bc259-116">Dies umfasst Formularvorlagen, die nur mit InfoPath kompatibel sind, sowie mit InfoPath und dem Webbrowser, der InfoPath Forms Services verwendet.</span><span class="sxs-lookup"><span data-stu-id="bc259-116">This includes form templates that are compatible only with InfoPath, as well as those that are compatible with InfoPath and the Web browser using InfoPath Forms Services.</span></span> <span data-ttu-id="bc259-117">Sie können jedoch Werte im Code in einem Feld zur Laufzeit protokollieren, um das Debugging der Geschäftslogik einer Formularvorlage zu unterstützten.</span><span class="sxs-lookup"><span data-stu-id="bc259-117">However, it is possible to log values to a field from code at run time to help with debugging a form template's business logic.</span></span> <span data-ttu-id="bc259-118">Weitere Informationen dazu finden Sie unter [Log values to a field for Debugging](how-to-log-values-to-a-field-for-debugging.md).</span><span class="sxs-lookup"><span data-stu-id="bc259-118">For information about how to do that, see [Log Values to a Field for Debugging](how-to-log-values-to-a-field-for-debugging.md).</span></span> 
  
## <a name="debugging-in-preview-mode"></a><span data-ttu-id="bc259-119">Debuggen im Vorschaumodus</span><span class="sxs-lookup"><span data-stu-id="bc259-119">Debugging in Preview Mode</span></span>

### <a name="to-debug-an-infopath-project-in-preview-mode"></a><span data-ttu-id="bc259-120">So debuggen Sie ein InfoPath-Projekt im Vorschaumodus</span><span class="sxs-lookup"><span data-stu-id="bc259-120">To debug an InfoPath project in Preview Mode</span></span>

1. <span data-ttu-id="bc259-121">Erstellen oder öffnen Sie eine InfoPath-Formularvorlage mit verwaltetem Code in Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="bc259-121">Create or open an InfoPath managed code form template in Visual Studio 2012.</span></span>
    
2. <span data-ttu-id="bc259-122">Legen Sie im Code-Editor im Formularcode mindestens einen Haltepunkt fest, indem Sie links neben der Codezeile, in der ein Haltepunkt eingefügt werden soll, auf die graue Leiste klicken.</span><span class="sxs-lookup"><span data-stu-id="bc259-122">Set one or more breakpoints in your form code in the code editor by clicking the grey bar to the left of the line of code where you want to insert a breakpoint.</span></span>
    
    <span data-ttu-id="bc259-123">Ein roter Kreis wird angezeigt, und die Codezeile wird hervorgehoben, um darauf hinzuweisen, dass die Laufzeit an diesem Haltepunkt im Formularcode angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="bc259-123">A red circle is displayed and the line of code is highlighted to indicate that the runtime will pause at this breakpoint in your form code.</span></span>
    
3. <span data-ttu-id="bc259-124">Klicken Sie im Menü **Debuggen** auf **Debuggen starten**, oder drücken Sie F5.</span><span class="sxs-lookup"><span data-stu-id="bc259-124">On the **Debug** menu, click **Start Debugging**; or press F5.</span></span>
    
    <span data-ttu-id="bc259-125">Das Projekt wird kompiliert und das Formular im Vorschaufenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bc259-125">The project will be compiled and the form is displayed in the preview window.</span></span>
    
4. <span data-ttu-id="bc259-126">Führen Sie eine Interaktion mit dem Formular aus, bis eine Codezeile mit einem Haltepunkt ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="bc259-126">Interact with the form until a line of code containing a breakpoint is encountered.</span></span>
    
    <span data-ttu-id="bc259-127">Der Fokus wechselt zurück zum Code-Editor.</span><span class="sxs-lookup"><span data-stu-id="bc259-127">The focus returns to the code editor.</span></span>
    
5. <span data-ttu-id="bc259-128">Klicken Sie im Menü **Debuggen** auf **Weiter**, oder drücken Sie F5.</span><span class="sxs-lookup"><span data-stu-id="bc259-128">On the **Debug** menu, click **Continue**; or press F5.</span></span>
    
6. <span data-ttu-id="bc259-129">Wenn Sie das Debuggen abgeschlossen haben, schließen Sie das Vorschaufenster, oder klicken Sie im Menü **Debuggen** auf **Debuggen beenden**.</span><span class="sxs-lookup"><span data-stu-id="bc259-129">When you are finished debugging, close the preview window; or on the **Debug** menu, click **Stop Debugging**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="bc259-130">Um eine InfoPath-Formularvorlage mit verwaltetem Code zu debuggen, wenn Sie ein Objektmodellelement verwenden, das volle Vertrauenswürdigkeit erfordert, müssen Sie die Formularvorlage konfigurieren, wie in [Vorschau-und Debug-Formularvorlagen beschrieben, die volle VertrauenswürdigKeit erfordern](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span><span class="sxs-lookup"><span data-stu-id="bc259-130">To debug an InfoPath managed code form template when using an object model member that requires full trust, you must configure your form template as described in [Preview and Debug Form Templates that Require Full Trust](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span></span> 
  
## <a name="using-a-sample-data-file"></a><span data-ttu-id="bc259-131">Verwenden einer Beispieldatendatei</span><span class="sxs-lookup"><span data-stu-id="bc259-131">Using a Sample Data File</span></span>

<span data-ttu-id="bc259-p104">Standardmäßig wird für das Debuggen und die Vorschau die Datei "template.xml" verwendet, die beim Erstellen einer Formularvorlage erstellt wird. Sie können eine eigene Datendatei erstellen und angeben, dass diese Datei zum Anzeigen der Vorschau oder zum Debuggen verwendet wird, indem Sie eine der folgenden Verfahren verwenden. </span><span class="sxs-lookup"><span data-stu-id="bc259-p104">By default, debugging and previewing uses the template.xml file that is created when a form template is created. You can create your own data file and specify to use it when previewing or debugging by using one of the following procedures.</span></span> 
  
### <a name="to-specify-a-sample-data-file-to-use-while-debugging-or-previewing-in-visual-studio-tools-for-applications"></a><span data-ttu-id="bc259-134">So geben Sie eine Beispieldatendatei an, die beim Debuggen oder Anzeigen der Vorschau in Visual Studio Tools for Applications verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="bc259-134">To specify a sample data file to use while debugging or previewing in Visual Studio Tools for Applications</span></span>

1. <span data-ttu-id="bc259-135">Öffnen Sie die Formularvorlage im InfoPath-Entwurfsmodus, um die Datei "template.xml" anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="bc259-135">To view template.xml, open the form template in InfoPath design mode.</span></span>
    
2. <span data-ttu-id="bc259-136">Klicken Sie auf die Registerkarte **Datei**, klicken Sie auf **Speichern**, dann auf **Formularvorlage speichern als** und dann auf **Quelldateien**.</span><span class="sxs-lookup"><span data-stu-id="bc259-136">Click the **File** tab, click **Saving**, click **Save Form Template As**, and the click **Source Files**.</span></span>
    
3. <span data-ttu-id="bc259-137">Speichern Sie die Formularvorlagendateien in einem Ordner, und öffnen Sie dann die Datei template.xml in einem Text-Editor.</span><span class="sxs-lookup"><span data-stu-id="bc259-137">Save the form template files to a folder, and then open the template.xml file in a text editor.</span></span>
    
4. <span data-ttu-id="bc259-138">Erstellen Sie mit den gewünschten Beispieldaten eine Datei mit derselben Struktur wie die Datei "template.xml", und speichern Sie sie.</span><span class="sxs-lookup"><span data-stu-id="bc259-138">Create and save a file with the same structure as template.xml with the sample data you want to use.</span></span>
    
5. <span data-ttu-id="bc259-139">Klicken Sie auf die Registerkarte **Datei**, und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen**.</span><span class="sxs-lookup"><span data-stu-id="bc259-139">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
6. <span data-ttu-id="bc259-140">Klicken Sie im Dialogfeld **Formularoptionen** auf die Kategorie **Vorschau**, und geben Sie dann unter **Beispieldaten** im Feld **Pfad** die Beispieldaten an, die Sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="bc259-140">Click the **Preview** category of the **Form Options** dialog box, and then under **Sample data** specify the sample data file you created in the **File location** box.</span></span> 
    
## <a name="specifying-a-user-role-to-use-while-debugging-or-previewing"></a><span data-ttu-id="bc259-141">Angeben einer Benutzerrolle zur Verwendung während des Debuggens oder des Anzeigens der Vorschau</span><span class="sxs-lookup"><span data-stu-id="bc259-141">Specifying a User Role to Use While Debugging or Previewing</span></span>

<span data-ttu-id="bc259-p105">Wenn für das Formular, mit dem Sie arbeiten, Benutzerrollen definiert wurden, können Sie eine Benutzerrolle angeben, die während des Debuggens oder des Anzeigens der Formularvorschau verwendet werden soll. Weitere Informationen zum Definieren von Benutzerrollen finden Sie in der InfoPath-Hilfe, wenn Sie nach "Benutzerrolle" suchen.</span><span class="sxs-lookup"><span data-stu-id="bc259-p105">If the form you are working with has user roles defined for it, you can specify a user role to use while debugging or previewing your form. For information on how to define user roles, search InfoPath help for "user role".</span></span>
  
> [!NOTE]
> <span data-ttu-id="bc259-p106">Die Option zum Angeben einer Benutzerrolle ist nicht verfügbar, wenn die Kompatibilitätseinstellung für die Formularvorlage auf **Webbrowserformulare** festgelegt ist. Benutzerrollen werden in Formularvorlagen, die über InfoPath Forms Services im Browser geöffnet werden, nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bc259-p106">The option to specify a user role is not available if the compatibility setting for your form template is set to **Web Browser Form**. User roles are not supported in form templates opened in the browser from InfoPath Forms Services.</span></span> 
  
### <a name="to-specify-a-role-to-use-while-debugging-or-previewing"></a><span data-ttu-id="bc259-146">So geben Sie eine Rolle an, die während des Debuggens oder des Anzeigens der Vorschau verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="bc259-146">To specify a role to use while debugging or previewing</span></span>

1. <span data-ttu-id="bc259-147">Wenn Sie in Visual Studio 2012 arbeiten, wechseln Sie zum InfoPath-Designer.</span><span class="sxs-lookup"><span data-stu-id="bc259-147">If you are working in Visual Studio 2012, switch to the InfoPath designer.</span></span>
    
2. <span data-ttu-id="bc259-148">Klicken Sie auf die Registerkarte **Datei**, und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen**.</span><span class="sxs-lookup"><span data-stu-id="bc259-148">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
3. <span data-ttu-id="bc259-149">Klicken Sie im Dialogfeld **Formularoptionen** auf die Kategorie **Vorschau**, und geben Sie dann im Dropdownfeld **Vorschau anzeigen als** die zu verwendende Benutzerrolle an.</span><span class="sxs-lookup"><span data-stu-id="bc259-149">Click the **Preview** category of the **Form Options** dialog box, and then specify the user role to use in the **Preview as** drop-down box.</span></span> 
    
## <a name="specifying-a-domain-to-use-while-debugging-or-previewing"></a><span data-ttu-id="bc259-150">Angeben einer Domäne zur Verwendung während des Debuggens oder des Anzeigens der Vorschau</span><span class="sxs-lookup"><span data-stu-id="bc259-150">Specifying a Domain to Use While Debugging or Previewing</span></span>

<span data-ttu-id="bc259-p107">Sie können eine Vorschau eines Formulars so anzeigen, als ob das Formular in einer bestimmten Domäne veröffentlicht würde. Diese Einstellung wird nur angewendet, wenn die Sicherheitsebene der Formularvorlage explizit auf **Domäne** festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="bc259-p107">You can preview a form as if it was published to a specific domain. This setting will only apply if the security level of the form template is explicitly set to **Domain**.</span></span>
  
### <a name="to-specify-a-domain-to-use-while-debugging-or-previewing"></a><span data-ttu-id="bc259-153">So geben Sie eine Domäne an, die beim Debuggen oder beim Anzeigen der Vorschau verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="bc259-153">To specify a domain to use while debugging or previewing</span></span>

1. <span data-ttu-id="bc259-154">Wenn Sie in Visual Studio 2012 arbeiten, wechseln Sie zum InfoPath-Designer.</span><span class="sxs-lookup"><span data-stu-id="bc259-154">If you are working in Visual Studio 2012, switch to the InfoPath designer.</span></span>
    
2. <span data-ttu-id="bc259-155">Klicken Sie auf die Registerkarte **Datei**, und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen**.</span><span class="sxs-lookup"><span data-stu-id="bc259-155">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
3. <span data-ttu-id="bc259-156">Klicken Sie im Dialogfeld **Formularoptionen** auf die Kategorie **Vorschau**, und geben Sie dann im Feld **Domäne** die beim Anzeigen der Vorschau und beim Debuggen zu verwendende Domäne an.</span><span class="sxs-lookup"><span data-stu-id="bc259-156">Click the **Preview** category of the **Form Options** dialog box, and then specify the domain to use while previewing and debugging in the **Domain** box.</span></span> 
    
4. <span data-ttu-id="bc259-157">Klicken Sie im Dialogfeld **Formularoptionen** auf die Kategorie **Sicherheit und Vertrauensstellung**, deaktivieren Sie das Kontrollkästchen **Sicherheitsstufe automatisch ermitteln**, und klicken Sie dann auf **Domäne**.</span><span class="sxs-lookup"><span data-stu-id="bc259-157">Click the **Security and Trust** category of the **Forms Options** dialog box, clear the **Automatically determine security level** check box, and then click **Domain**.</span></span>
    

