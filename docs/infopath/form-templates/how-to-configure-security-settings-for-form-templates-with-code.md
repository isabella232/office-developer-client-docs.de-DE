---
title: Konfigurieren von Einstellungen für Formularvorlagen mit Code
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Bereitstellungspaket für Sicherheitsrichtlinien [infopath 2007],URLs [InfoPath 2007], Zuweisen von FullTrust,Codezugriffssicherheit [InfoPath 2007],UNCs [InfoPath 2007], Zuweisen von FullTrust, CAS [InfoPath 2007],Sicherheit [InfoPath 2007], Konfigurieren,Codegruppen [InfoPath 2007],FullTrust [InfoPath 2007], Zuweisen zu UNCs,FullTrust [InfoPath 2007], Zuweisen zu URLs
localization_priority: Normal
ms.assetid: 24d1a322-581f-497e-b97b-bd02c4516551
description: Sie können den Berechtigungssatz, der auf eine Formularvorlage für verwalteten InfoPath-Code angewendet wird, mithilfe des .NET Configuration-Snap-Ins anpassen.
ms.openlocfilehash: 77f3546d976bb5ea353aa3fbe58ba7af6cd92a6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300160"
---
# <a name="configure-security-settings-for-form-templates-with-code"></a><span data-ttu-id="5bab5-104">Konfigurieren von Einstellungen für Formularvorlagen mit Code</span><span class="sxs-lookup"><span data-stu-id="5bab5-104">Configure Security Settings for Form Templates with Code</span></span>

<span data-ttu-id="5bab5-105">Sie können den Berechtigungssatz, der auf eine Formularvorlage für verwalteten InfoPath-Code angewendet wird, mithilfe des .NET Configuration-Snap-Ins anpassen.</span><span class="sxs-lookup"><span data-stu-id="5bab5-105">You can customize the permission set that is applied to an InfoPath managed code form template by using the .NET Configuration snap-in.</span></span>
  
<span data-ttu-id="5bab5-106">Die von InfoPath gehostete Common Language Runtime (CLR)  sucht auf der Computerrichtlinienebene unter der Gruppe All_Code nach einer vordefinierten Codegruppe namens InfoPath-Formularvorlagen.</span><span class="sxs-lookup"><span data-stu-id="5bab5-106">The common language runtime (CLR) hosted by InfoPath will look for a predefined code group named  *InfoPath Form Templates*  at the Machine policy level under the All_Code group.</span></span> <span data-ttu-id="5bab5-107">Die CLR wenden die Berechtigungssätze, die unter dieser Gruppe definiert sind, auf die Anwendungsdomäne (AppDomain) an, in der der Formularcode ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5bab5-107">The CLR will apply the permission sets that are defined under that group to the application domain (AppDomain) where the form code runs.</span></span> <span data-ttu-id="5bab5-108">Auf diese Weise können Sie die Berechtigungssätze anpassen, die Formularvorlagen mit verwalteten Code von InfoPath gewährt werden.</span><span class="sxs-lookup"><span data-stu-id="5bab5-108">This enables you to customize the permission sets that are granted to InfoPath managed code form templates.</span></span> <span data-ttu-id="5bab5-109">Sie können z. B. eine Formularvorlage erteilen, die aus der Berechtigung https://MySite für den Zugriff auf Active Directory heruntergeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="5bab5-109">For example, you can grant a form template downloaded from https://MySite permission to access the Active Directory.</span></span> 
  
<span data-ttu-id="5bab5-110">Zur Anwendung benutzerdefinierter Sicherheitsrichtlinien, die mithilfe des Snap-Ins .NET-Konfiguration definiert wurden, müssen diese auf allen Clientcomputern bereitgestellt werden, auf denen die Formularvorlage ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5bab5-110">For custom security policy defined by using the .NET Configuration snap-in to be applied, it must be deployed on all the client computers where the form template will run.</span></span>
  
<span data-ttu-id="5bab5-111">Weitere Informationen zum Sicherheitsmodell für Formularvorlagen mit verwalteten Code in InfoPath finden Sie unter Informationen zum Sicherheitsmodell für [Formularvorlagen mit Code](about-the-security-model-for-form-templates-with-code.md)</span><span class="sxs-lookup"><span data-stu-id="5bab5-111">For more information about the security model for InfoPath managed code form templates, see [About the Security Model for Form Templates with Code](about-the-security-model-for-form-templates-with-code.md)</span></span>
  
## <a name="creating-a-code-group-for-infopath-form-templates"></a><span data-ttu-id="5bab5-112">Erstellen einer Codegruppe für InfoPath-Formularvorlagen</span><span class="sxs-lookup"><span data-stu-id="5bab5-112">Creating a Code Group for InfoPath Form Templates</span></span>

<span data-ttu-id="5bab5-113">Mit dem folgenden Verfahren wird eine Codegruppe erstellt, die keine Berechtigungen für Formularvorlagen mit verwaltetem Code von InfoPath erteilt (mit Ausnahme der auf Ihrem lokalen Computer installierten oder registrierten), unter der Sie InfoPath-Formularvorlagen, die sich in bestimmten URLs oder UNCs befinden, Berechtigungssätze zuweisen können.</span><span class="sxs-lookup"><span data-stu-id="5bab5-113">The following procedure will create a code group that grants no permissions to InfoPath managed code form templates (except those that are installed or registered on your local computer) under which you can assign permission sets to InfoPath form templates located at specific URLs or UNCs.</span></span> <span data-ttu-id="5bab5-114">Informationen zum Erstellen und Zuweisen von Berechtigungssätzen zu Codegruppen innerhalb der Codegruppe finden Sie  `InfoPath Form Templates` im folgenden Verfahren.</span><span class="sxs-lookup"><span data-stu-id="5bab5-114">For information about how to create and assign permission sets to code groups within the  `InfoPath Form Templates` code group, see the following procedure.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5bab5-115">Im Gegensatz zum **Microsoft .NET Framework 1.1-Konfigurationstool,** das mit dem Microsoft .NET Framework 1.1 Redistributable Package installiert ist, wird **die Microsoft .NET Framework 2.0-Konfiguration** nur mit dem Microsoft .NET Framework 2.0 Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="5bab5-115">Unlike the **Microsoft .NET Framework 1.1 Configuration** tool that is installed with the Microsoft .NET Framework 1.1 Redistributable Package, the **Microsoft .NET Framework 2.0 Configuration** is installed only with the Microsoft .NET Framework 2.0 Software Development Kit (SDK).</span></span> 
  
### <a name="to-create-a-custom-security-code-group-for-infopath-managed-code-forms"></a><span data-ttu-id="5bab5-116">So erstellen Sie eine benutzerdefinierte Sicherheitscodegruppe für InfoPath-Formulare mit verwaltetem Code</span><span class="sxs-lookup"><span data-stu-id="5bab5-116">To create a custom security code group for InfoPath managed code forms</span></span>

1. <span data-ttu-id="5bab5-117">Zeigen Sie im Menü **Start** auf **Verwaltung**, und klicken Sie dann auf **Microsoft .NET Framework 2.0-Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="5bab5-117">From the **Start** menu, point to **Administrative Tools**, and then click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
    <span data-ttu-id="5bab5-118">Wenn Sie nicht über Administrative **Tools** im  Menü **Start** verfügen, öffnen Sie in der Systemsteuerung administrative **Tools,** und doppelklicken Sie dann auf Microsoft **.NET Framework 2.0-Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="5bab5-118">If you do not have **Administrative Tools** on the **Start** menu, from the **Control Panel** open **Administrative Tools**, and then double-click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
2. <span data-ttu-id="5bab5-119">Erweitern Sie unter Mein **Computer** den  Knoten  Laufzeitsicherheitsrichtlinie, den Knoten **Computer,** Codegruppen, den Knoten **All_Code,** und klicken Sie dann mit der rechten Maustaste auf den Knoten  **All_Code,** und klicken Sie auf **Neu,** um das Dialogfeld Codegruppe erstellen zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5bab5-119">Under **My Computer**, expand the **Runtime Security Policy** node, the **Machine** node, **Code Groups** node, the **All_Code** node, and then right-click the **All_Code** node and click **New** to open the **Create Code Group** dialog box.</span></span> 
    
3. <span data-ttu-id="5bab5-120">Nennen Sie die neue Codegruppe  `InfoPath Form Templates` (dieser Text muss exakt sein), und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="5bab5-120">Name the new code group  `InfoPath Form Templates` (this text must be exact), and then click **Next**.</span></span>
    
4. <span data-ttu-id="5bab5-121">Legen Sie den Bedingungstyp für die Codegruppe **Gesamter Code** fest, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="5bab5-121">Set the condition type for the code group to **All Code**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="5bab5-122">Klicken Sie auf **Vorhandenen Berechtigungssatz verwenden**, weisen Sie den Berechtigungssatz **Nothing** der Codegruppe zu, klicken Sie auf **Weiter** und anschließend auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="5bab5-122">Click **Use existing permission set**, assign the **Nothing** permission set to the code group, click **Next**, and then click **Finish**.</span></span>
    
6. <span data-ttu-id="5bab5-123">Um die neuen Einstellungen anzuwenden, schließen und starten Sie InfoPath neu.</span><span class="sxs-lookup"><span data-stu-id="5bab5-123">To apply the new settings, close and restart InfoPath.</span></span>
    
<span data-ttu-id="5bab5-124">Wenn es Ihnen lieber ist, können Sie den Berechtigungssatz für alle Formularvorlagen  mit verwalteten Code in InfoPath verwalten, indem Sie der Codegruppe **InfoPath-Formularvorlagen** einen anderen Berechtigungssatz als den Berechtigungssatz Nothing zuweisen.</span><span class="sxs-lookup"><span data-stu-id="5bab5-124">If you prefer, you can manage the permission set for all InfoPath managed code form templates by assigning a permission set other than the **Nothing** permission set to the **InfoPath Form Templates** code group.</span></span> 
> [!NOTE]
> <span data-ttu-id="5bab5-125">Sie können den Berechtigungssatz für eine Sicherheitscodegruppe jederzeit ändern, indem Sie mit der rechten Maustaste auf die Gruppe in klicken.</span><span class="sxs-lookup"><span data-stu-id="5bab5-125">You can change the permission set for a security code group at any time by right-clicking the group in the .</span></span> <span data-ttu-id="5bab5-126">**NET Configuration 2.0** Snap-In, klicken Sie auf **Eigenschaften** und dann auf die Registerkarte **Berechtigungssatz.**</span><span class="sxs-lookup"><span data-stu-id="5bab5-126">**NET Configuration 2.0** snap-in, clicking **Properties**, and then clicking the **Permission Set** tab.</span></span> 
  
## <a name="assigning-fulltrust-to-forms-at-a-specific-url-or-unc"></a><span data-ttu-id="5bab5-127">Zuweisen von "Voll vertrauenswürdig" an Formulare unter einem bestimmten URL oder UNC</span><span class="sxs-lookup"><span data-stu-id="5bab5-127">Assigning FullTrust to Forms at a Specific URL or UNC</span></span>

<span data-ttu-id="5bab5-128">Sie können Codegruppen unter der **Gruppe InfoPath-Formularvorlagen** erstellen, um formularvorlagen von einer bestimmten URL oder einem bestimmten UNC-Speicherort den voll vertrauenswürdigen Berechtigungssatz zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="5bab5-128">You can create code groups under the **InfoPath Form Templates** group to grant the full trust permission set to form templates from a particular URL or UNC location.</span></span> <span data-ttu-id="5bab5-129">Danach wird jede am angegebenen Speicherort veröffentlichte Formularvorlage vollständig vertrauenswürdig ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5bab5-129">After doing this, every form template published to the specified location will run fully trusted.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5bab5-130">Eine Formularvorlage, die vom lokalen Computer geladen wird (Codegruppe Meine Computerzone), wird von InfoPath mithilfe einer zufälligen URL geladen.</span><span class="sxs-lookup"><span data-stu-id="5bab5-130">A form template that is loaded from the local computer (My Computer Zone code group) is loaded by InfoPath using a random URL.</span></span> <span data-ttu-id="5bab5-131">Aus diesem Grund können Sie das folgende Verfahren nicht verwenden, um den Berechtigungssatz FullTrust für eine solche Formularvorlage zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="5bab5-131">For this reason, you cannot use the following procedure to grant the FullTrust permission set to such a form template.</span></span> <span data-ttu-id="5bab5-132">Um einer lokal installierten Formularvorlage den Berechtigungssatz FullTrust zu erteilen, verwenden Sie eines der Verfahren, die im Abschnitt "Bereitstellen von Formularvorlagen, die voll vertrauenswürdig sind" im Thema Bereitstellen von [InfoPath-Formularvorlagen](how-to-deploy-infopath-form-templates-with-code.md) mit Code beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="5bab5-132">To grant a locally installed form template the FullTrust permission set, use one of the procedures that are described in the "Deploying Form Templates That Require Full Trust" section of the [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md) topic.</span></span> 
  
### <a name="to-assign-fulltrust-to-infopath-forms-at-a-specific-url-or-unc-location"></a><span data-ttu-id="5bab5-133">So weisen Sie InfoPath-Formularen unter einer bestimmten URL oder UNC die Berechtigung "Voll vertrauenswürdig" zu</span><span class="sxs-lookup"><span data-stu-id="5bab5-133">To assign FullTrust to InfoPath forms at a specific URL or UNC location</span></span>

1. <span data-ttu-id="5bab5-134">Zeigen Sie im Menü **Start** auf **Verwaltung**, und klicken Sie dann auf **Microsoft .NET Framework 2.0-Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="5bab5-134">From the **Start** menu, point to **Administrative Tools**, and then click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
    <span data-ttu-id="5bab5-135">Wenn Sie nicht über Administrative **Tools** im  Menü **Start** verfügen, öffnen Sie in der Systemsteuerung administrative **Tools,** und doppelklicken Sie dann auf Microsoft **.NET Framework 2.0-Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="5bab5-135">If you do not have **Administrative Tools** on the **Start** menu, from the **Control Panel** open **Administrative Tools**, and then double-click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
2. <span data-ttu-id="5bab5-136">Erweitern **Sie unter** Mein Computer den Knoten **Laufzeitsicherheitsrichtlinie,** den Knoten **Computer,** Codegruppen, den Knoten **All_Code,** und klicken Sie dann auf den Knoten **InfoPath-Formularvorlagen.** </span><span class="sxs-lookup"><span data-stu-id="5bab5-136">Under **My Computer**, expand the **Runtime Security Policy** node, the **Machine** node, **Code Groups** node, the **All_Code** node, and then click the **InfoPath Form Templates** node.</span></span> 
    
3. <span data-ttu-id="5bab5-137">Klicken Sie in der Liste **Aufgaben** im rechten Bereich auf **Untergeordnete Codegruppe hinzufügen**, benennen Sie die Codegruppe, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="5bab5-137">In **Tasks** list in the right pane, click **Add a Child Code Group**, name the code group, and then click **Next**.</span></span>
    
4. <span data-ttu-id="5bab5-138">Wählen  Sie in der Liste Bedingungstyp für diese Codegruppe auswählen **DIE URL** aus, und geben Sie dann die URL oder UNC für den Speicherort der Formularvorlagen mit verwaltetem Code von InfoPath ein, die Sie dem Berechtigungssatz **FullTrust** erteilen möchten.</span><span class="sxs-lookup"><span data-stu-id="5bab5-138">In the **Choose the condition type for this code group** list, select **URL**, and then enter the URL or UNC for the location of the InfoPath managed code form templates that you want to grant the **FullTrust** permission set.</span></span> 
    
    <span data-ttu-id="5bab5-p106">Zum Einschränken des Berechtigungssatzes auf eine einzelne Formularvorlage geben Sie den vollständigen Pfad für die jeweilige Formularvorlage ein. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="5bab5-p106">To restrict the permission set to a single form template, specify the full path of that particular form template. For example:</span></span>
    
     `\\MyServer\MyShare\MyFormTemplate.xsn`
    
     `https://MySite/MySubsite/MyFormTempate.xsn`
    
    <span data-ttu-id="5bab5-p107">Wenn der Berechtigungssatz allen Formularvorlagen unter dieser URL oder UNC erteilt werden soll, lassen Sie den Namen der Vorlage weg, und fügen Sie ein Sternchen am Ende der URL oder UNC hinzu. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="5bab5-p107">To grant the permission set to all form templates in a URL or UNC, omit the name of the template and add an asterisk at the end of the URL or UNC. For example:</span></span>
    
     `\\MyServer\MyShare\*`
    
     `https://MySite/MySubsite/*`
    
5. <span data-ttu-id="5bab5-143">Klicken Sie auf **Weiter**, dann auf **Vorhandenen Berechtigungssatz verwenden**, und weisen Sie der Codegruppe den Berechtigungssatz **Voll vertrauenswürdig** zu.</span><span class="sxs-lookup"><span data-stu-id="5bab5-143">Click **Next**, and then click **Use existing permission set** and assign the **FullTrust** permission set to the code group.</span></span> 
    
6. <span data-ttu-id="5bab5-144">Klicken Sie auf **Weiter** und dann auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="5bab5-144">Click **Next**, and then click **Finish**.</span></span>
    
7. <span data-ttu-id="5bab5-145">Um die neuen Einstellungen anzuwenden, schließen und starten Sie InfoPath neu.</span><span class="sxs-lookup"><span data-stu-id="5bab5-145">To apply the new settings, close and restart InfoPath.</span></span>
    
> [!NOTE]
> <span data-ttu-id="5bab5-146">Wenn Sie einen restriktiveren oder benutzerdefinierten Berechtigungssatz anwenden möchten, wählen Sie anstelle von **Voll vertrauenswürdig** in Schritt 4 die geeignete Option aus.</span><span class="sxs-lookup"><span data-stu-id="5bab5-146">To apply a more restrictive or custom permission set, select the appropriate option instead of **FullTrust** in step 4.</span></span> 
  
## <a name="creating-a-deployment-package-for-infopath-security-policy"></a><span data-ttu-id="5bab5-147">Erstellen eines Bereitstellungspakets für InfoPath-Sicherheitsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="5bab5-147">Creating a Deployment Package for InfoPath Security Policy</span></span>

<span data-ttu-id="5bab5-148">Nachdem Sie benutzerdefinierte Sicherheitsrichtlinien für verwaltete Formularvorlagen von InfoPath definiert haben, können Sie ein Windows Installer Package (.msi) erstellen, um diese Sicherheitsrichtlinie mithilfe von Gruppenrichtlinien oder Microsoft Systems Management Server auf den Computern der Benutzer zu bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5bab5-148">After defining custom security policy for InfoPath managed-form templates, you can create a Windows Installer Package (.msi) to deploy this security policy on users' computers by using Group Policy or Microsoft Systems Management Server.</span></span>
  
### <a name="to-create-a-deployment-package-for-custom-infopath-security-policy"></a><span data-ttu-id="5bab5-149">So erstellen Sie ein Bereitstellungspaket für benutzerdefinierte InfoPath-Sicherheitsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="5bab5-149">To create a deployment package for custom InfoPath security policy</span></span>

1. <span data-ttu-id="5bab5-150">Zeigen Sie im Menü **Start** auf **Verwaltung**, und klicken Sie dann auf **Microsoft .NET Framework 2.0-Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="5bab5-150">From the **Start** menu, point to **Administrative Tools**, and then click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
    <span data-ttu-id="5bab5-151">Wenn Sie nicht über Administrative **Tools** im  Menü **Start** verfügen, öffnen Sie in der Systemsteuerung administrative **Tools,** und doppelklicken Sie dann auf Microsoft **.NET Framework 2.0-Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="5bab5-151">If you do not have **Administrative Tools** on the **Start** menu, from the **Control Panel** open **Administrative Tools**, and then double-click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
2. <span data-ttu-id="5bab5-152">Klicken Sie mit der rechten Maustaste auf **Laufzeitsicherheitsrichtlinie**, und klicken Sie dann auf **Bereitstellungspaket erstellen**.</span><span class="sxs-lookup"><span data-stu-id="5bab5-152">Right-click **Runtime Security Policy**, and then click **Create Deployment Package**.</span></span>
    
3. <span data-ttu-id="5bab5-153">Klicken Sie unter **Wählen Sie die weiterzugebende Sicherheitsrichtlinienebene aus** auf **Computer**, geben Sie den Ordner und den Dateinamen für das Windows Installer-Paket an, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="5bab5-153">Under **Select the security policy to deploy**, click **Machine**, specify the folder and file name for the Windows Installer Package, and then click **Next**.</span></span>
    
4. <span data-ttu-id="5bab5-154">Klicken Sie auf **Fertig stellen**, um das Bereitstellungspaket zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5bab5-154">Click **Finish** to create the deployment package.</span></span> 
    
5. <span data-ttu-id="5bab5-155">Weitere Informationen zur Verwendung des .NET Framework-Konfigurationstools finden Sie Visual Studio Hilfe oder auf der MSDN-Website nach ".NET Framework Configuration Tool (Mscorcfg.msc)".</span><span class="sxs-lookup"><span data-stu-id="5bab5-155">For information about how to use the .NET Framework Configuration tool, search Visual Studio Help or the MSDN website for ".NET Framework Configuration Tool (Mscorcfg.msc)".</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5bab5-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5bab5-156">See also</span></span>



[<span data-ttu-id="5bab5-157">Informationen zum Sicherheitsmodell für Formularvorlagen mit Code</span><span class="sxs-lookup"><span data-stu-id="5bab5-157">About the Security Model for Form Templates with Code</span></span>](about-the-security-model-for-form-templates-with-code.md)

