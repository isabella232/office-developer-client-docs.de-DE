---
title: Konfigurieren von Sicherheitseinstellungen für Formularvorlagen mit Code
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- die Bereitstellung von Gruppenrichtlinien [Infopath 2007] URLs [InfoPath 2007], Zuweisen von FullTrust zu packen, Codezugriffssicherheit [InfoPath 2007], UNCs [InfoPath 2007], "voll vertrauenswürdig", CAS [InfoPath 2007], [InfoPath 2007] Sicherheit, konfigurieren, Code Gruppen [zuweisen InfoPath 2007] FullTrust [InfoPath 2007], zuweisen zu UNCs FullTrust [InfoPath 2007], zuweisen zu URLs
localization_priority: Normal
ms.assetid: 24d1a322-581f-497e-b97b-bd02c4516551
description: Sie können den Berechtigungssatz anpassen, der mit dem .NET Configuration-Snap-in auf einer InfoPath-Formularvorlage verwaltetem Code angewendet wird.
ms.openlocfilehash: f04ce71875eac7695d2900131ca7c9cd333fa90f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790751"
---
# <a name="configure-security-settings-for-form-templates-with-code"></a><span data-ttu-id="8fbca-104">Konfigurieren von Sicherheitseinstellungen für Formularvorlagen mit Code</span><span class="sxs-lookup"><span data-stu-id="8fbca-104">Configure Security Settings for Form Templates with Code</span></span>

<span data-ttu-id="8fbca-105">Sie können den Berechtigungssatz anpassen, der mit dem .NET Configuration-Snap-in auf einer InfoPath-Formularvorlage verwaltetem Code angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="8fbca-105">You can customize the permission set that is applied to an InfoPath managed code form template by using the .NET Configuration snap-in.</span></span>
  
<span data-ttu-id="8fbca-106">Die von InfoPath gehosteten common Language Runtime (CLR) sucht nach einer vordefinierten Codegruppe mit dem Namen *InfoPath-Formularvorlagen* auf Computerebene Richtlinie unter der Gruppe All_Code.</span><span class="sxs-lookup"><span data-stu-id="8fbca-106">The common language runtime (CLR) hosted by InfoPath will look for a predefined code group named  *InfoPath Form Templates*  at the Machine policy level under the All_Code group.</span></span> <span data-ttu-id="8fbca-107">Die CLR gelten die Berechtigungssätze, die unter dieser Gruppe sein, um die Anwendungsdomäne (AppDomain) definiert sind, wo die Formularcode ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8fbca-107">The CLR will apply the permission sets that are defined under that group to the application domain (AppDomain) where the form code runs.</span></span> <span data-ttu-id="8fbca-108">So können Sie die Berechtigungssätze anpassen, die verwalteten InfoPath-Formularvorlagen Code erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="8fbca-108">This enables you to customize the permission sets that are granted to InfoPath managed code form templates.</span></span> <span data-ttu-id="8fbca-109">Sie können beispielsweise eine Formularvorlage heruntergeladen erteilen http://MySite Berechtigung, um das Active Directory zugreifen.</span><span class="sxs-lookup"><span data-stu-id="8fbca-109">For example, you can grant a form template downloaded from http://MySite permission to access the Active Directory.</span></span> 
  
<span data-ttu-id="8fbca-110">Zur Anwendung benutzerdefinierter Sicherheitsrichtlinien, die mithilfe des Snap-Ins .NET-Konfiguration definiert wurden, müssen diese auf allen Clientcomputern bereitgestellt werden, auf denen die Formularvorlage ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8fbca-110">For custom security policy defined by using the .NET Configuration snap-in to be applied, it must be deployed on all the client computers where the form template will run.</span></span>
  
<span data-ttu-id="8fbca-111">Weitere Informationen zum Sicherheitsmodell für InfoPath verwaltete code Formularvorlagen finden Sie [Informationen zum Sicherheitsmodell für Formularvorlagen mit Code](about-the-security-model-for-form-templates-with-code.md)</span><span class="sxs-lookup"><span data-stu-id="8fbca-111">For more information about the security model for InfoPath managed code form templates, see [About the Security Model for Form Templates with Code](about-the-security-model-for-form-templates-with-code.md)</span></span>
  
## <a name="creating-a-code-group-for-infopath-form-templates"></a><span data-ttu-id="8fbca-112">Erstellen einer Codegruppe für InfoPath-Formularvorlagen</span><span class="sxs-lookup"><span data-stu-id="8fbca-112">Creating a Code Group for InfoPath Form Templates</span></span>

<span data-ttu-id="8fbca-113">Das folgende Verfahren wird eine Codegruppe, dass gewährt keine Berechtigungen in InfoPath managed code Formularvorlagen (ausgenommen solche, die installiert oder auf dem lokalen Computer registriert sind) erstellen, unter dem Sie zuweisen können Berechtigungssätze InfoPath-Formularvorlagen gefunden auf bestimmte URLs oder UNCs.</span><span class="sxs-lookup"><span data-stu-id="8fbca-113">The following procedure will create a code group that grants no permissions to InfoPath managed code form templates (except those that are installed or registered on your local computer) under which you can assign permission sets to InfoPath form templates located at specific URLs or UNCs.</span></span> <span data-ttu-id="8fbca-114">Für Informationen zum Erstellen und Zuweisen von Berechtigungen auf Codegruppen innerhalb setzt die `InfoPath Form Templates` Codegruppe, finden Sie unter die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="8fbca-114">For information about how to create and assign permission sets to code groups within the  `InfoPath Form Templates` code group, see the following procedure.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8fbca-115">Im Gegensatz zu den **Microsoft .NET Framework 1.1-Konfiguration** -Tool, das mit dem Microsoft .NET Framework 1.1 Redistributable Package installiert wird, wird die **Microsoft .NET Framework 2.0-Konfiguration** nur mit Microsoft .NET Framework installiert. 2.0-Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="8fbca-115">Unlike the **Microsoft .NET Framework 1.1 Configuration** tool that is installed with the Microsoft .NET Framework 1.1 Redistributable Package, the **Microsoft .NET Framework 2.0 Configuration** is installed only with the Microsoft .NET Framework 2.0 Software Development Kit (SDK).</span></span> 
  
### <a name="to-create-a-custom-security-code-group-for-infopath-managed-code-forms"></a><span data-ttu-id="8fbca-116">So erstellen Sie eine benutzerdefinierte Sicherheitscodegruppe für InfoPath-Formulare mit verwaltetem Code</span><span class="sxs-lookup"><span data-stu-id="8fbca-116">To create a custom security code group for InfoPath managed code forms</span></span>

1. <span data-ttu-id="8fbca-117">Klicken Sie im Menü **Start** auf **Verwaltung**zeigen Sie, und klicken Sie dann auf **Microsoft .NET Framework 2.0-Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="8fbca-117">From the **Start** menu, point to **Administrative Tools**, and then click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
    <span data-ttu-id="8fbca-118">Wenn Sie im **Startmenü** auf **Verwaltung** nicht verfügen, aus der **Control Panel** öffnen Sie **Verwaltung**, und doppelklicken Sie dann auf **Microsoft .NET Framework 2.0-Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="8fbca-118">If you do not have **Administrative Tools** on the **Start** menu, from the **Control Panel** open **Administrative Tools**, and then double-click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
2. <span data-ttu-id="8fbca-119">Unter **Arbeitsplatz**erweitern Sie den Knoten **Laufzeitsicherheitsrichtlinie** , den Knoten **Computer** , Knoten **Codegruppen** , den Knoten **All_Code** , und klicken Sie dann mit der rechten Maustaste in des Knotens **All_Code** und klicken Sie auf **neu** , um die **erstellen zu öffnen Codegruppe** im Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="8fbca-119">Under **My Computer**, expand the **Runtime Security Policy** node, the **Machine** node, **Code Groups** node, the **All_Code** node, and then right-click the **All_Code** node and click **New** to open the **Create Code Group** dialog box.</span></span> 
    
3. <span data-ttu-id="8fbca-120">Nennen Sie die neue Codegruppe `InfoPath Form Templates` (dieser Text muss genauen), und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="8fbca-120">Name the new code group  `InfoPath Form Templates` (this text must be exact), and then click **Next**.</span></span>
    
4. <span data-ttu-id="8fbca-121">Legen Sie den Bedingungstyp für die Codegruppe **Gesamter**Code, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="8fbca-121">Set the condition type for the code group to **All Code**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="8fbca-122">Klicken Sie auf **vorhandenen Berechtigungssatz verwenden**, weisen Sie den Berechtigungssatz **Nothing** der Codegruppe, klicken Sie auf **Weiter**, und klicken Sie dann auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="8fbca-122">Click **Use existing permission set**, assign the **Nothing** permission set to the code group, click **Next**, and then click **Finish**.</span></span>
    
6. <span data-ttu-id="8fbca-123">Um die neuen Einstellungen anzuwenden, schließen Sie, und starten Sie InfoPath.</span><span class="sxs-lookup"><span data-stu-id="8fbca-123">To apply the new settings, close and restart InfoPath.</span></span>
    
<span data-ttu-id="8fbca-124">Wenn Sie es vorziehen, können Sie den Berechtigungssatz für alle Formularvorlagen für InfoPath managed Code durch Zuweisen von einem Berechtigungssatz als den Berechtigungssatz **Nothing** der Codegruppe **InfoPath-Formularvorlagen** verwalten.</span><span class="sxs-lookup"><span data-stu-id="8fbca-124">If you prefer, you can manage the permission set for all InfoPath managed code form templates by assigning a permission set other than the **Nothing** permission set to the **InfoPath Form Templates** code group.</span></span> 
> [!NOTE]
> <span data-ttu-id="8fbca-125">Sie können den Berechtigungssatz für eine Sicherheitsgruppe Code können Sie jederzeit mit der rechten Maustaste in die Gruppe ändern der.</span><span class="sxs-lookup"><span data-stu-id="8fbca-125">You can change the permission set for a security code group at any time by right-clicking the group in the .</span></span> <span data-ttu-id="8fbca-126">**NET Configuration 2.0** -Snap-in, indem Sie auf **Eigenschaften**klicken und dann auf die Registerkarte **Berechtigungssatz** .</span><span class="sxs-lookup"><span data-stu-id="8fbca-126">**NET Configuration 2.0** snap-in, clicking **Properties**, and then clicking the **Permission Set** tab.</span></span> 
  
## <a name="assigning-fulltrust-to-forms-at-a-specific-url-or-unc"></a><span data-ttu-id="8fbca-127">Zuweisen von "Voll vertrauenswürdig" an Formulare unter einem bestimmten URL oder UNC</span><span class="sxs-lookup"><span data-stu-id="8fbca-127">Assigning FullTrust to Forms at a Specific URL or UNC</span></span>

<span data-ttu-id="8fbca-128">Sie können Codegruppen unter der **InfoPath-Formularvorlagen** Gruppe erteilen den Berechtigungssatz voll vertrauenswürdig auf Formularvorlagen aus einer bestimmten URL oder UNC-Speicherort erstellen.</span><span class="sxs-lookup"><span data-stu-id="8fbca-128">You can create code groups under the **InfoPath Form Templates** group to grant the full trust permission set to form templates from a particular URL or UNC location.</span></span> <span data-ttu-id="8fbca-129">Nach dem auf diese Weise wird jede Formularvorlage veröffentlicht am angegebenen Speicherort voll vertrauenswürdig ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8fbca-129">After doing this, every form template published to the specified location will run fully trusted.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8fbca-130">Eine Formularvorlage, die aus dem lokalen Computer (Mein Computer Zone Codegruppe) geladen wird, wird von InfoPath mithilfe einer zufällig ausgewählten URL geladen.</span><span class="sxs-lookup"><span data-stu-id="8fbca-130">A form template that is loaded from the local computer (My Computer Zone code group) is loaded by InfoPath using a random URL.</span></span> <span data-ttu-id="8fbca-131">Aus diesem Grund können Sie das folgende Verfahren zum Erteilen Sie der Berechtigungssatzes "voll vertrauenswürdig" zu einer solchen Formularvorlage verwenden.</span><span class="sxs-lookup"><span data-stu-id="8fbca-131">For this reason, you cannot use the following procedure to grant the FullTrust permission set to such a form template.</span></span> <span data-ttu-id="8fbca-132">Erteilen einer lokal installierte Formularvorlage die Berechtigung "voll vertrauenswürdig" festgelegt ist, verwenden Sie eine der der beschriebenen Verfahren im Abschnitt "Bereitstellen von Formularvorlagen, die erfordern voll vertrauenswürdig" neben dem Thema [Bereitstellen von InfoPath-Formularvorlagen mit Code](how-to-deploy-infopath-form-templates-with-code.md) .</span><span class="sxs-lookup"><span data-stu-id="8fbca-132">To grant a locally installed form template the FullTrust permission set, use one of the procedures that are described in the "Deploying Form Templates That Require Full Trust" section of the [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md) topic.</span></span> 
  
### <a name="to-assign-fulltrust-to-infopath-forms-at-a-specific-url-or-unc-location"></a><span data-ttu-id="8fbca-133">So weisen Sie InfoPath-Formularen unter einer bestimmten URL oder UNC die Berechtigung "Voll vertrauenswürdig" zu</span><span class="sxs-lookup"><span data-stu-id="8fbca-133">To assign FullTrust to InfoPath forms at a specific URL or UNC location</span></span>

1. <span data-ttu-id="8fbca-134">Klicken Sie im Menü **Start** auf **Verwaltung**zeigen Sie, und klicken Sie dann auf **Microsoft .NET Framework 2.0-Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="8fbca-134">From the **Start** menu, point to **Administrative Tools**, and then click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
    <span data-ttu-id="8fbca-135">Wenn Sie im **Startmenü** auf **Verwaltung** nicht verfügen, aus der **Control Panel** öffnen Sie **Verwaltung**, und doppelklicken Sie dann auf **Microsoft .NET Framework 2.0-Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="8fbca-135">If you do not have **Administrative Tools** on the **Start** menu, from the **Control Panel** open **Administrative Tools**, and then double-click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
2. <span data-ttu-id="8fbca-136">Klicken Sie unter **Arbeitsplatz**erweitern Sie den Knoten **Laufzeitsicherheitsrichtlinie** , den Knoten **Computer** , Knoten **Codegruppen** , den Knoten **All_Code** , und klicken Sie dann auf den Knoten **InfoPath-Formularvorlagen** .</span><span class="sxs-lookup"><span data-stu-id="8fbca-136">Under **My Computer**, expand the **Runtime Security Policy** node, the **Machine** node, **Code Groups** node, the **All_Code** node, and then click the **InfoPath Form Templates** node.</span></span> 
    
3. <span data-ttu-id="8fbca-137">Klicken Sie in der Liste der **Aufgaben** im rechten Bereich auf **eine untergeordnete Codegruppe hinzufügen**, Name der Codegruppe, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="8fbca-137">In **Tasks** list in the right pane, click **Add a Child Code Group**, name the code group, and then click **Next**.</span></span>
    
4. <span data-ttu-id="8fbca-138">Wählen Sie in der Liste **Wählen Sie den Bedingungstyp für die Codegruppe aus** **URL**aus, und geben Sie die URL oder UNC für den Speicherort der InfoPath managed Code Form Templates, die Sie den Berechtigungssatz **voll vertrauenswürdig** gewähren möchten.</span><span class="sxs-lookup"><span data-stu-id="8fbca-138">In the **Choose the condition type for this code group** list, select **URL**, and then enter the URL or UNC for the location of the InfoPath managed code form templates that you want to grant the **FullTrust** permission set.</span></span> 
    
    <span data-ttu-id="8fbca-p106">Zum Einschränken des Berechtigungssatzes auf eine einzelne Formularvorlage geben Sie den vollständigen Pfad für die jeweilige Formularvorlage ein. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8fbca-p106">To restrict the permission set to a single form template, specify the full path of that particular form template. For example:</span></span>
    
     `\\MyServer\MyShare\MyFormTemplate.xsn`
    
     `http://MySite/MySubsite/MyFormTempate.xsn`
    
    <span data-ttu-id="8fbca-p107">Wenn der Berechtigungssatz allen Formularvorlagen unter dieser URL oder UNC erteilt werden soll, lassen Sie den Namen der Vorlage weg, und fügen Sie ein Sternchen am Ende der URL oder UNC hinzu. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8fbca-p107">To grant the permission set to all form templates in a URL or UNC, omit the name of the template and add an asterisk at the end of the URL or UNC. For example:</span></span>
    
     `\\MyServer\MyShare\*`
    
     `http://MySite/MySubsite/*`
    
5. <span data-ttu-id="8fbca-143">Klicken Sie auf **Weiter**, und klicken Sie auf **vorhandenen Berechtigungssatz verwenden** , und weisen Sie der Codegruppe der Berechtigungssatzes **"voll vertrauenswürdig"** .</span><span class="sxs-lookup"><span data-stu-id="8fbca-143">Click **Next**, and then click **Use existing permission set** and assign the **FullTrust** permission set to the code group.</span></span> 
    
6. <span data-ttu-id="8fbca-144">Klicken Sie auf **Weiter**, und klicken Sie dann auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="8fbca-144">Click **Next**, and then click **Finish**.</span></span>
    
7. <span data-ttu-id="8fbca-145">Um die neuen Einstellungen anzuwenden, schließen Sie, und starten Sie InfoPath.</span><span class="sxs-lookup"><span data-stu-id="8fbca-145">To apply the new settings, close and restart InfoPath.</span></span>
    
> [!NOTE]
> <span data-ttu-id="8fbca-146">Wenn Sie einen restriktiveren oder benutzerdefinierten Berechtigungssatz anwenden möchten, wählen Sie die entsprechende Option anstelle von **voll vertrauenswürdig** in Schritt 4.</span><span class="sxs-lookup"><span data-stu-id="8fbca-146">To apply a more restrictive or custom permission set, select the appropriate option instead of **FullTrust** in step 4.</span></span> 
  
## <a name="creating-a-deployment-package-for-infopath-security-policy"></a><span data-ttu-id="8fbca-147">Erstellen eines Bereitstellungspakets für InfoPath-Sicherheitsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="8fbca-147">Creating a Deployment Package for InfoPath Security Policy</span></span>

<span data-ttu-id="8fbca-148">Nach dem Definieren benutzerdefinierter Sicherheitsrichtlinien für InfoPath managed-Formularvorlagen, können Sie eine Windows Installer-Paket (MSI-Datei) zum Bereitstellen von dieser Codezugriffssicherheits-Richtlinie auf den Computern der Benutzer mithilfe von Gruppenrichtlinien oder Microsoft Systems Management Server erstellen.</span><span class="sxs-lookup"><span data-stu-id="8fbca-148">After defining custom security policy for InfoPath managed-form templates, you can create a Windows Installer Package (.msi) to deploy this security policy on users' computers by using Group Policy or Microsoft Systems Management Server.</span></span>
  
### <a name="to-create-a-deployment-package-for-custom-infopath-security-policy"></a><span data-ttu-id="8fbca-149">So erstellen Sie ein Bereitstellungspaket für benutzerdefinierte InfoPath-Sicherheitsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="8fbca-149">To create a deployment package for custom InfoPath security policy</span></span>

1. <span data-ttu-id="8fbca-150">Klicken Sie im Menü **Start** auf **Verwaltung**zeigen Sie, und klicken Sie dann auf **Microsoft .NET Framework 2.0-Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="8fbca-150">From the **Start** menu, point to **Administrative Tools**, and then click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
    <span data-ttu-id="8fbca-151">Wenn Sie im **Startmenü** auf **Verwaltung** nicht verfügen, aus der **Control Panel** öffnen Sie **Verwaltung**, und doppelklicken Sie dann auf **Microsoft .NET Framework 2.0-Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="8fbca-151">If you do not have **Administrative Tools** on the **Start** menu, from the **Control Panel** open **Administrative Tools**, and then double-click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
2. <span data-ttu-id="8fbca-152">Maustaste auf **Laufzeitsicherheitsrichtlinie**, und klicken Sie dann auf **Bereitstellungspaket erstellen**.</span><span class="sxs-lookup"><span data-stu-id="8fbca-152">Right-click **Runtime Security Policy**, and then click **Create Deployment Package**.</span></span>
    
3. <span data-ttu-id="8fbca-153">Wählen Sie unter **Wählen Sie die Codezugriffssicherheits-Richtlinie zum Bereitstellen von**klicken Sie auf **Computer**, geben Sie den Ordner und den Dateinamen für das Windows Installer-Paket, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="8fbca-153">Under **Select the security policy to deploy**, click **Machine**, specify the folder and file name for the Windows Installer Package, and then click **Next**.</span></span>
    
4. <span data-ttu-id="8fbca-154">Klicken Sie auf **Fertig stellen** , um das Bereitstellungspaket zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8fbca-154">Click **Finish** to create the deployment package.</span></span> 
    
5. <span data-ttu-id="8fbca-155">Informationen zur Verwendung von .NET Framework-Konfigurationstools suchen Sie Hilfe zu Visual Studio oder die MSDN-Website nach ".NET Framework Configuration Tool (Mscorcfg.msc)".</span><span class="sxs-lookup"><span data-stu-id="8fbca-155">For information about how to use the .NET Framework Configuration tool, search Visual Studio Help or the MSDN Web site for ".NET Framework Configuration Tool (Mscorcfg.msc)".</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8fbca-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8fbca-156">See also</span></span>



[<span data-ttu-id="8fbca-157">Informationen zum Sicherheitsmodell für Formularvorlagen mit Code</span><span class="sxs-lookup"><span data-stu-id="8fbca-157">About the Security Model for Form Templates with Code</span></span>](about-the-security-model-for-form-templates-with-code.md)

