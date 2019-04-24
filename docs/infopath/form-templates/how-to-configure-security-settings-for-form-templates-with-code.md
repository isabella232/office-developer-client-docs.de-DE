---
title: Konfigurieren von Sicherheitseinstellungen für Formularvorlagen mit Code
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Sicherheitsrichtlinien-Bereitstellungspaket [InfoPath 2007], URLs [InfoPath 2007], Zuweisen von FullTrust, Codezugriffssicherheit [InfoPath 2007], UNCs [InfoPath 2007], Zuweisen von FullTrust, CAS [InfoPath 2007], Sicherheit [InfoPath 2007], konfigurieren, Codegruppen [ InfoPath 2007], FullTrust [InfoPath 2007], zuweisen zu UNCs, FullTrust [InfoPath 2007], zuweisen zu URLs
localization_priority: Normal
ms.assetid: 24d1a322-581f-497e-b97b-bd02c4516551
description: Sie können den Berechtigungssatz anpassen, der auf eine InfoPath-Formularvorlage mit verwaltetem Code angewendet wird, indem Sie das .NET-Konfigurations-Snap-in verwenden.
ms.openlocfilehash: 77f3546d976bb5ea353aa3fbe58ba7af6cd92a6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300160"
---
# <a name="configure-security-settings-for-form-templates-with-code"></a><span data-ttu-id="46a1b-104">Konfigurieren von Sicherheitseinstellungen für Formularvorlagen mit Code</span><span class="sxs-lookup"><span data-stu-id="46a1b-104">Configure Security Settings for Form Templates with Code</span></span>

<span data-ttu-id="46a1b-105">Sie können den Berechtigungssatz anpassen, der auf eine InfoPath-Formularvorlage mit verwaltetem Code angewendet wird, indem Sie das .NET-Konfigurations-Snap-in verwenden.</span><span class="sxs-lookup"><span data-stu-id="46a1b-105">You can customize the permission set that is applied to an InfoPath managed code form template by using the .NET Configuration snap-in.</span></span>
  
<span data-ttu-id="46a1b-106">Die Common Language Runtime (CLR), die von InfoPath gehostet wird, sucht nach einer vordefinierten Codegruppe mit dem Namen *InfoPath-Formularvorlagen* auf der Ebene der Computerrichtlinien unter der Gruppe All_Code.</span><span class="sxs-lookup"><span data-stu-id="46a1b-106">The common language runtime (CLR) hosted by InfoPath will look for a predefined code group named  *InfoPath Form Templates*  at the Machine policy level under the All_Code group.</span></span> <span data-ttu-id="46a1b-107">Die CLR wendet die Berechtigungssätze, die unter dieser Gruppe definiert sind, auf die Anwendungsdomäne (AppDomain) an, in der der Formularcode ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46a1b-107">The CLR will apply the permission sets that are defined under that group to the application domain (AppDomain) where the form code runs.</span></span> <span data-ttu-id="46a1b-108">Auf diese Weise können Sie die Berechtigungssätze anpassen, die InfoPath-Formularvorlagen mit verwaltetem Code erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="46a1b-108">This enables you to customize the permission sets that are granted to InfoPath managed code form templates.</span></span> <span data-ttu-id="46a1b-109">Sie können beispielsweise einer Formularvorlage, die von https://MySite der Berechtigung für den Zugriff auf Active Directory heruntergeladen wurde, erteilen.</span><span class="sxs-lookup"><span data-stu-id="46a1b-109">For example, you can grant a form template downloaded from https://MySite permission to access the Active Directory.</span></span> 
  
<span data-ttu-id="46a1b-110">Zur Anwendung benutzerdefinierter Sicherheitsrichtlinien, die mithilfe des Snap-Ins .NET-Konfiguration definiert wurden, müssen diese auf allen Clientcomputern bereitgestellt werden, auf denen die Formularvorlage ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="46a1b-110">For custom security policy defined by using the .NET Configuration snap-in to be applied, it must be deployed on all the client computers where the form template will run.</span></span>
  
<span data-ttu-id="46a1b-111">Weitere Informationen zum Sicherheitsmodell für InfoPath-Formularvorlagen mit verwaltetem Code finden Sie unter [Informationen zum Sicherheitsmodell für Formularvorlagen mit Code](about-the-security-model-for-form-templates-with-code.md)</span><span class="sxs-lookup"><span data-stu-id="46a1b-111">For more information about the security model for InfoPath managed code form templates, see [About the Security Model for Form Templates with Code](about-the-security-model-for-form-templates-with-code.md)</span></span>
  
## <a name="creating-a-code-group-for-infopath-form-templates"></a><span data-ttu-id="46a1b-112">Erstellen einer Codegruppe für InfoPath-Formularvorlagen</span><span class="sxs-lookup"><span data-stu-id="46a1b-112">Creating a Code Group for InfoPath Form Templates</span></span>

<span data-ttu-id="46a1b-113">Mit dem folgenden Verfahren wird eine Codegruppe erstellt, die keine Berechtigungen für InfoPath-Formularvorlagen mit verwaltetem Code gewährt (mit Ausnahme derjenigen, die auf dem lokalen Computer installiert oder registriert sind), unter der Sie Berechtigungssätze zu InfoPath-Formularvorlagen zuweisen können. bei bestimmten URLs oder UNCs.</span><span class="sxs-lookup"><span data-stu-id="46a1b-113">The following procedure will create a code group that grants no permissions to InfoPath managed code form templates (except those that are installed or registered on your local computer) under which you can assign permission sets to InfoPath form templates located at specific URLs or UNCs.</span></span> <span data-ttu-id="46a1b-114">Weitere Informationen zum Erstellen und Zuweisen von Berechtigungssätzen zu Codegruppen innerhalb der `InfoPath Form Templates` Codegruppe finden Sie im folgenden Verfahren.</span><span class="sxs-lookup"><span data-stu-id="46a1b-114">For information about how to create and assign permission sets to code groups within the  `InfoPath Form Templates` code group, see the following procedure.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="46a1b-115">Im Gegensatz zum **Microsoft .NET framework 1,1-Konfigurations** Tool, das mit dem Redistributable-Paket von Microsoft .net Framework 1,1 installiert wird, wird die **microsoft .NET Framework 2,0-Konfiguration** nur mit Microsoft .NET Framework installiert. 2,0 Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="46a1b-115">Unlike the **Microsoft .NET Framework 1.1 Configuration** tool that is installed with the Microsoft .NET Framework 1.1 Redistributable Package, the **Microsoft .NET Framework 2.0 Configuration** is installed only with the Microsoft .NET Framework 2.0 Software Development Kit (SDK).</span></span> 
  
### <a name="to-create-a-custom-security-code-group-for-infopath-managed-code-forms"></a><span data-ttu-id="46a1b-116">So erstellen Sie eine benutzerdefinierte Sicherheitscodegruppe für InfoPath-Formulare mit verwaltetem Code</span><span class="sxs-lookup"><span data-stu-id="46a1b-116">To create a custom security code group for InfoPath managed code forms</span></span>

1. <span data-ttu-id="46a1b-117">Zeigen Sie im Menü **Start** auf **Verwaltung**, und klicken Sie dann auf **Microsoft .NET Framework 2.0-Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="46a1b-117">From the **Start** menu, point to **Administrative Tools**, and then click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
    <span data-ttu-id="46a1b-118">Wenn Sie im **Startmenü** nicht über **Verwaltungstools** verfügen, öffnen Sie in der **System** Steuerung die Option **Verwaltung**, und doppelklicken Sie dann auf **Microsoft .NET Framework 2,0-Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="46a1b-118">If you do not have **Administrative Tools** on the **Start** menu, from the **Control Panel** open **Administrative Tools**, and then double-click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
2. <span data-ttu-id="46a1b-119">Erweitern Sie unter **Arbeitsplatz**den Knoten **Laufzeitsicherheitsrichtlinie** , den Knoten **Computer** , **Code Gruppen** , den Knoten **All_Code** , klicken Sie dann mit der rechten Maustaste auf den Knoten **All_Code** , und klicken Sie dann auf **neu** , um das **Create Dialogfeld Code Gruppe** .</span><span class="sxs-lookup"><span data-stu-id="46a1b-119">Under **My Computer**, expand the **Runtime Security Policy** node, the **Machine** node, **Code Groups** node, the **All_Code** node, and then right-click the **All_Code** node and click **New** to open the **Create Code Group** dialog box.</span></span> 
    
3. <span data-ttu-id="46a1b-120">Benennen Sie die neue Code `InfoPath Form Templates` Gruppe (dieser Text muss genau sein), und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="46a1b-120">Name the new code group  `InfoPath Form Templates` (this text must be exact), and then click **Next**.</span></span>
    
4. <span data-ttu-id="46a1b-121">Legen Sie den Bedingungstyp für die Codegruppe **Gesamter Code** fest, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="46a1b-121">Set the condition type for the code group to **All Code**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="46a1b-122">Klicken Sie auf **Vorhandenen Berechtigungssatz verwenden**, weisen Sie den Berechtigungssatz **Nothing** der Codegruppe zu, klicken Sie auf **Weiter** und anschließend auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="46a1b-122">Click **Use existing permission set**, assign the **Nothing** permission set to the code group, click **Next**, and then click **Finish**.</span></span>
    
6. <span data-ttu-id="46a1b-123">Zum Anwenden der neuen Einstellungen müssen Sie InfoPath beenden und neu starten.</span><span class="sxs-lookup"><span data-stu-id="46a1b-123">To apply the new settings, close and restart InfoPath.</span></span>
    
<span data-ttu-id="46a1b-124">Wenn Sie es vorziehen, können Sie den Berechtigungssatz für alle InfoPath-Formularvorlagen mit verwaltetem Code verwalten, indem Sie der Codegruppe InfoPath- **Formularvorlagen** einen anderen Berechtigungssatz als **Nothing** zuweisen.</span><span class="sxs-lookup"><span data-stu-id="46a1b-124">If you prefer, you can manage the permission set for all InfoPath managed code form templates by assigning a permission set other than the **Nothing** permission set to the **InfoPath Form Templates** code group.</span></span> 
> [!NOTE]
> <span data-ttu-id="46a1b-125">Sie können den Berechtigungssatz für eine Sicherheitscodegruppe jederzeit ändern, indem Sie mit der rechten Maustaste auf die Gruppe in der klicken.</span><span class="sxs-lookup"><span data-stu-id="46a1b-125">You can change the permission set for a security code group at any time by right-clicking the group in the .</span></span> <span data-ttu-id="46a1b-126">**Net-konfiguration 2,0** -Snap-in, klicken Sie auf **Eigenschaften**, und klicken Sie dann auf die Registerkarte **Berechtigungssatz** .</span><span class="sxs-lookup"><span data-stu-id="46a1b-126">**NET Configuration 2.0** snap-in, clicking **Properties**, and then clicking the **Permission Set** tab.</span></span> 
  
## <a name="assigning-fulltrust-to-forms-at-a-specific-url-or-unc"></a><span data-ttu-id="46a1b-127">Zuweisen von "Voll vertrauenswürdig" an Formulare unter einem bestimmten URL oder UNC</span><span class="sxs-lookup"><span data-stu-id="46a1b-127">Assigning FullTrust to Forms at a Specific URL or UNC</span></span>

<span data-ttu-id="46a1b-128">Sie können Codegruppen unter der Gruppe **InfoPath-Formularvorlagen** erstellen, um den Berechtigungssatz voll vertrauenswürdig auf Formularvorlagen von einer bestimmten URL oder UNC-Speicherort zu gewähren.</span><span class="sxs-lookup"><span data-stu-id="46a1b-128">You can create code groups under the **InfoPath Form Templates** group to grant the full trust permission set to form templates from a particular URL or UNC location.</span></span> <span data-ttu-id="46a1b-129">Danach wird jede Formularvorlage, die am angegebenen Speicherort veröffentlicht wurde, voll vertrauenswürdig ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46a1b-129">After doing this, every form template published to the specified location will run fully trusted.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="46a1b-130">Eine Formularvorlage, die auf dem lokalen Computer (Computer Zonen Codegruppe) geladen wird, wird von InfoPath mithilfe einer zufälligen URL geladen.</span><span class="sxs-lookup"><span data-stu-id="46a1b-130">A form template that is loaded from the local computer (My Computer Zone code group) is loaded by InfoPath using a random URL.</span></span> <span data-ttu-id="46a1b-131">Aus diesem Grund können Sie das folgende Verfahren nicht verwenden, um dem Berechtigungssatz FullTrust eine solche Formularvorlage zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="46a1b-131">For this reason, you cannot use the following procedure to grant the FullTrust permission set to such a form template.</span></span> <span data-ttu-id="46a1b-132">Wenn Sie eine lokal installierte Formularvorlage mit dem Berechtigungssatz FullTrust erteilen möchten, verwenden Sie eines der Verfahren, die im Thema bereitStellen von Formularvorlagen, die die vollständige Vertrauenswürdigkeit erfordern, des Abschnitts [InfoPath-Formularvorlagen mit Code](how-to-deploy-infopath-form-templates-with-code.md) ausführen beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="46a1b-132">To grant a locally installed form template the FullTrust permission set, use one of the procedures that are described in the "Deploying Form Templates That Require Full Trust" section of the [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md) topic.</span></span> 
  
### <a name="to-assign-fulltrust-to-infopath-forms-at-a-specific-url-or-unc-location"></a><span data-ttu-id="46a1b-133">So weisen Sie InfoPath-Formularen unter einer bestimmten URL oder UNC die Berechtigung "Voll vertrauenswürdig" zu</span><span class="sxs-lookup"><span data-stu-id="46a1b-133">To assign FullTrust to InfoPath forms at a specific URL or UNC location</span></span>

1. <span data-ttu-id="46a1b-134">Zeigen Sie im Menü **Start** auf **Verwaltung**, und klicken Sie dann auf **Microsoft .NET Framework 2.0-Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="46a1b-134">From the **Start** menu, point to **Administrative Tools**, and then click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
    <span data-ttu-id="46a1b-135">Wenn Sie im **Startmenü** nicht über **Verwaltungstools** verfügen, öffnen Sie in der **System** Steuerung die Option **Verwaltung**, und doppelklicken Sie dann auf **Microsoft .NET Framework 2,0-Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="46a1b-135">If you do not have **Administrative Tools** on the **Start** menu, from the **Control Panel** open **Administrative Tools**, and then double-click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
2. <span data-ttu-id="46a1b-136">Erweitern Sie unter **Arbeitsplatz**den Knoten **Laufzeitsicherheitsrichtlinie** , den Knoten **Computer** , **Code Gruppen** und den Knoten **All_Code** , und klicken Sie dann auf den Knoten **InfoPath-Formularvorlagen** .</span><span class="sxs-lookup"><span data-stu-id="46a1b-136">Under **My Computer**, expand the **Runtime Security Policy** node, the **Machine** node, **Code Groups** node, the **All_Code** node, and then click the **InfoPath Form Templates** node.</span></span> 
    
3. <span data-ttu-id="46a1b-137">Klicken Sie in der Liste **Aufgaben** im rechten Bereich auf **Untergeordnete Codegruppe hinzufügen**, benennen Sie die Codegruppe, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="46a1b-137">In **Tasks** list in the right pane, click **Add a Child Code Group**, name the code group, and then click **Next**.</span></span>
    
4. <span data-ttu-id="46a1b-138">Wählen Sie in der Liste **Wählen Sie die Konditionsart für diese Codegruppe** aus die Option **URL**aus, und geben Sie dann die URL oder UNC für den Speicherort der InfoPath-Formularvorlagen mit verwaltetem Code ein, denen Sie den **FullTrust** -Berechtigungssatz erteilen möchten.</span><span class="sxs-lookup"><span data-stu-id="46a1b-138">In the **Choose the condition type for this code group** list, select **URL**, and then enter the URL or UNC for the location of the InfoPath managed code form templates that you want to grant the **FullTrust** permission set.</span></span> 
    
    <span data-ttu-id="46a1b-139">Zum Einschränken des Berechtigungssatzes auf eine einzelne Formularvorlage geben Sie den vollständigen Pfad für die jeweilige Formularvorlage ein.</span><span class="sxs-lookup"><span data-stu-id="46a1b-139">To restrict the permission set to a single form template, specify the full path of that particular form template.</span></span> <span data-ttu-id="46a1b-140">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="46a1b-140">For example:</span></span>
    
     `\\MyServer\MyShare\MyFormTemplate.xsn`
    
     `https://MySite/MySubsite/MyFormTempate.xsn`
    
    <span data-ttu-id="46a1b-p107">Wenn der Berechtigungssatz allen Formularvorlagen unter dieser URL oder UNC erteilt werden soll, lassen Sie den Namen der Vorlage weg, und fügen Sie ein Sternchen am Ende der URL oder UNC hinzu. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="46a1b-p107">To grant the permission set to all form templates in a URL or UNC, omit the name of the template and add an asterisk at the end of the URL or UNC. For example:</span></span>
    
     `\\MyServer\MyShare\*`
    
     `https://MySite/MySubsite/*`
    
5. <span data-ttu-id="46a1b-143">Klicken Sie auf **Weiter**, dann auf **Vorhandenen Berechtigungssatz verwenden**, und weisen Sie der Codegruppe den Berechtigungssatz **Voll vertrauenswürdig** zu.</span><span class="sxs-lookup"><span data-stu-id="46a1b-143">Click **Next**, and then click **Use existing permission set** and assign the **FullTrust** permission set to the code group.</span></span> 
    
6. <span data-ttu-id="46a1b-144">Klicken Sie auf **Weiter** und dann auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="46a1b-144">Click **Next**, and then click **Finish**.</span></span>
    
7. <span data-ttu-id="46a1b-145">Zum Anwenden der neuen Einstellungen müssen Sie InfoPath beenden und neu starten.</span><span class="sxs-lookup"><span data-stu-id="46a1b-145">To apply the new settings, close and restart InfoPath.</span></span>
    
> [!NOTE]
> <span data-ttu-id="46a1b-146">Wenn Sie einen restriktiveren oder benutzerdefinierten Berechtigungssatz anwenden möchten, wählen Sie anstelle von **Voll vertrauenswürdig** in Schritt 4 die geeignete Option aus.</span><span class="sxs-lookup"><span data-stu-id="46a1b-146">To apply a more restrictive or custom permission set, select the appropriate option instead of **FullTrust** in step 4.</span></span> 
  
## <a name="creating-a-deployment-package-for-infopath-security-policy"></a><span data-ttu-id="46a1b-147">Erstellen eines Bereitstellungspakets für InfoPath-Sicherheitsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="46a1b-147">Creating a Deployment Package for InfoPath Security Policy</span></span>

<span data-ttu-id="46a1b-148">Nachdem Sie benutzerdefinierte Sicherheitsrichtlinien für InfoPath-Formularvorlagen definiert haben, können Sie ein Windows Installer-Paket (MSI) erstellen, um diese Sicherheitsrichtlinie auf Benutzercomputern mithilfe von Gruppenrichtlinien oder Microsoft Systems Management Server bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="46a1b-148">After defining custom security policy for InfoPath managed-form templates, you can create a Windows Installer Package (.msi) to deploy this security policy on users' computers by using Group Policy or Microsoft Systems Management Server.</span></span>
  
### <a name="to-create-a-deployment-package-for-custom-infopath-security-policy"></a><span data-ttu-id="46a1b-149">So erstellen Sie ein Bereitstellungspaket für benutzerdefinierte InfoPath-Sicherheitsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="46a1b-149">To create a deployment package for custom InfoPath security policy</span></span>

1. <span data-ttu-id="46a1b-150">Zeigen Sie im Menü **Start** auf **Verwaltung**, und klicken Sie dann auf **Microsoft .NET Framework 2.0-Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="46a1b-150">From the **Start** menu, point to **Administrative Tools**, and then click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
    <span data-ttu-id="46a1b-151">Wenn Sie im **Startmenü** nicht über **Verwaltungstools** verfügen, öffnen Sie in der **System** Steuerung die Option **Verwaltung**, und doppelklicken Sie dann auf **Microsoft .NET Framework 2,0-Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="46a1b-151">If you do not have **Administrative Tools** on the **Start** menu, from the **Control Panel** open **Administrative Tools**, and then double-click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
2. <span data-ttu-id="46a1b-152">Klicken Sie mit der rechten Maustaste auf **Laufzeitsicherheitsrichtlinie**, und klicken Sie dann auf **Bereitstellungspaket erstellen**.</span><span class="sxs-lookup"><span data-stu-id="46a1b-152">Right-click **Runtime Security Policy**, and then click **Create Deployment Package**.</span></span>
    
3. <span data-ttu-id="46a1b-153">Klicken Sie unter **Wählen Sie die weiterzugebende Sicherheitsrichtlinienebene aus** auf **Computer**, geben Sie den Ordner und den Dateinamen für das Windows Installer-Paket an, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="46a1b-153">Under **Select the security policy to deploy**, click **Machine**, specify the folder and file name for the Windows Installer Package, and then click **Next**.</span></span>
    
4. <span data-ttu-id="46a1b-154">Klicken Sie auf **Fertig stellen**, um das Bereitstellungspaket zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="46a1b-154">Click **Finish** to create the deployment package.</span></span> 
    
5. <span data-ttu-id="46a1b-155">Informationen zur Verwendung des .NET Framework-Konfigurationstools finden Sie in der Visual Studio-Hilfe oder auf der MSDN-Website für ".NET Framework Configuration Tool (Mscorcfg. msc)".</span><span class="sxs-lookup"><span data-stu-id="46a1b-155">For information about how to use the .NET Framework Configuration tool, search Visual Studio Help or the MSDN website for ".NET Framework Configuration Tool (Mscorcfg.msc)".</span></span>
    
## <a name="see-also"></a><span data-ttu-id="46a1b-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46a1b-156">See also</span></span>



[<span data-ttu-id="46a1b-157">Informationen zum Sicherheitsmodell für Formularvorlagen mit Code</span><span class="sxs-lookup"><span data-stu-id="46a1b-157">About the Security Model for Form Templates with Code</span></span>](about-the-security-model-for-form-templates-with-code.md)

