---
title: Veröffentlichen von Formularen mit Code
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: caafab24-6413-4731-813d-cba3ae9ea97e
description: Jeder Websitesammlungsadministrator kann Formulare mit Code direkt aus dem InfoPath Designer-Veröffentlichungs-Assistenten in einer Formularbibliothek auf SharePoint. Der Code wird in einer Sandkastenumgebung ausgeführt, damit der Server nicht durch bösartigen Code geschädigt werden kann. Dies wird als Veröffentlichen einer Sandkastenlösung oder Veröffentlichen in der SharePoint-Sandkasteninfrastruktur bezeichnet.
ms.openlocfilehash: f8f8a48ea6810b5331198f6ddc112b3bd38ab886
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428326"
---
# <a name="publishing-forms-with-code"></a><span data-ttu-id="5df8b-105">Veröffentlichen von Formularen mit Code</span><span class="sxs-lookup"><span data-stu-id="5df8b-105">Publishing Forms with Code</span></span>

<span data-ttu-id="5df8b-106">Jeder Websitesammlungsadministrator kann Formulare mit Code direkt aus dem InfoPath Designer-Veröffentlichungs-Assistenten in einer Formularbibliothek auf SharePoint.</span><span class="sxs-lookup"><span data-stu-id="5df8b-106">Any site collection administrator can publish forms with code directly from the InfoPath Designer publishing wizard to a form library on SharePoint.</span></span> <span data-ttu-id="5df8b-107">Der Code wird in einer Sandkastenumgebung ausgeführt, damit der Server nicht durch bösartigen Code geschädigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5df8b-107">The code is executed in a sandboxed environment so that malicious code cannot harm the server.</span></span> <span data-ttu-id="5df8b-108">Dies wird als Veröffentlichen einer Sandkastenlösung oder Veröffentlichen in der SharePoint-Sandkasteninfrastruktur bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="5df8b-108">This is referred to as publishing a sandboxed solution or publishing to the SharePoint sandbox infrastructure.</span></span>
  
<span data-ttu-id="5df8b-109">InfoPath 2010 und SharePoint Server 2010 unterstützen auch vom Administrator bereitgestellte Lösungen.</span><span class="sxs-lookup"><span data-stu-id="5df8b-109">InfoPath 2010 and SharePoint Server 2010 also support administrator-deployed solutions.</span></span> <span data-ttu-id="5df8b-110">Ein Formulardesigner veröffentlicht in einem lokalen Speicher Formulare mit Code, die später von einem SharePoint-Farmadministrator überprüft und hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="5df8b-110">A form designer publishes forms with code to a local store which are later reviewed and uploaded by a SharePoint farm administrator.</span></span> <span data-ttu-id="5df8b-111">Der Code wird als voll vertrauenswürdig eingestuft und kann Funktionalität enthalten, für die erhöhte Berechtigungen wie beispielsweise Datei-E/A erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="5df8b-111">The code is given full trust, and can incorporate functionality requiring elevated privileges such as file IO.</span></span>
  
## <a name="comparing-sandboxed-and-administrator-approved-solutions"></a><span data-ttu-id="5df8b-112">Vergleich zwischen Sandkastenlösungen und vom Administrator genehmigten Lösungen</span><span class="sxs-lookup"><span data-stu-id="5df8b-112">Comparing Sandboxed and Administrator-approved Solutions</span></span>

<span data-ttu-id="5df8b-113">In der folgenden Tabelle werden die Unterschiede zwischen dem Veröffentlichen von Sandkastenlösungen und von vom Administrator genehmigten Lösungen beschrieben. </span><span class="sxs-lookup"><span data-stu-id="5df8b-113">The following table summarizes the differences between publishing sandboxed and administrator-approved solutions.</span></span> 
  
||<span data-ttu-id="5df8b-114">**Sandkastenlösungen**</span><span class="sxs-lookup"><span data-stu-id="5df8b-114">**Sandboxed Solutions**</span></span>|<span data-ttu-id="5df8b-115">**Vom Administrator genehmigte Lösungen**</span><span class="sxs-lookup"><span data-stu-id="5df8b-115">**Administrator-approved Solutions**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5df8b-116">**Erforderliche Berechtigungen**</span><span class="sxs-lookup"><span data-stu-id="5df8b-116">**Permissions Required**</span></span> <br/> |<span data-ttu-id="5df8b-117">Kann von jedem Websitesammlungsadministrator veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="5df8b-117">Can be published by any site collection administrator.</span></span>  <br/> |<span data-ttu-id="5df8b-118">Kann von einem Farmadministrator bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5df8b-118">Can be deployed by a farm administrator.</span></span>  <br/> |
|<span data-ttu-id="5df8b-119">**Publishing**</span><span class="sxs-lookup"><span data-stu-id="5df8b-119">**Publishing**</span></span> <br/> |<span data-ttu-id="5df8b-120">Kann direkt über InfoPath veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="5df8b-120">Can be published directly from InfoPath.</span></span>  <br/> |<span data-ttu-id="5df8b-121">Kann mithilfe der Zentraladministration oder des Befehlszeilentools stsadm bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5df8b-121">Can be deployed using Central Administration or the stsadm command-line tool.</span></span>  <br/> |
|<span data-ttu-id="5df8b-122">**Schutz**</span><span class="sxs-lookup"><span data-stu-id="5df8b-122">**Protection**</span></span> <br/> |<span data-ttu-id="5df8b-p104">Code wird in einer Sandkastenumgebung ausgeführt. Dadurch wird der Server vor bösartigem Code geschützt.</span><span class="sxs-lookup"><span data-stu-id="5df8b-p104">Code is run in a sandboxed environment. This helps protect the server from malicious code.</span></span>  <br/> |<span data-ttu-id="5df8b-125">Code kann mit voller Vertrauenswürdigkeit ausgeführt werden und auf alle Ressourcen auf dem Server zugreifen.</span><span class="sxs-lookup"><span data-stu-id="5df8b-125">Code can run with full trust and access any resource on the server.</span></span>  <br/> |
|<span data-ttu-id="5df8b-126">**Empfohlene Verwendung**</span><span class="sxs-lookup"><span data-stu-id="5df8b-126">**Recommended Use**</span></span> <br/> |<span data-ttu-id="5df8b-127">Formulare, für die nur in geringem Umfang Code benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="5df8b-127">Forms that only require a small amount of code.</span></span>  <br/> |<span data-ttu-id="5df8b-128">Formulare, die viele Codezeilen enthalten.</span><span class="sxs-lookup"><span data-stu-id="5df8b-128">Forms that contain many lines of code.</span></span>  <br/> |
   
### <a name="publishing-form-templates-as-sandboxed-solutions"></a><span data-ttu-id="5df8b-129">Veröffentlichen von Formularvorlagen als Sandkastenlösungen</span><span class="sxs-lookup"><span data-stu-id="5df8b-129">Publishing Form Templates as Sandboxed Solutions</span></span>

<span data-ttu-id="5df8b-130">Das Veröffentlichen eines Formulars mit Code als Sandkastenlösung ist nicht anders als das Veröffentlichen eines anderen Formulars in einer Dokumentbibliothek.</span><span class="sxs-lookup"><span data-stu-id="5df8b-130">Publishing a form with code as a sandboxed solution is no different from publishing any other form to a document library.</span></span> <span data-ttu-id="5df8b-131">Verwenden Sie einfach wie gewohnt den Veröffentlichungs-Assistenten, und das Formular wird auf den Server hochgeladen und kann im Sandkasten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5df8b-131">Just use the publishing wizard as usual and your form will be uploaded to the server and will operate in the sandbox.</span></span>
  
<span data-ttu-id="5df8b-132">Beachten Sie, dass es bestimmte Einschränkungen für die Bereitstellung Ihres Formulars als Sandkastenlösung gibt:</span><span class="sxs-lookup"><span data-stu-id="5df8b-132">Note that there are certain restrictions to deploying your form as a sandboxed solution:</span></span>
  
- <span data-ttu-id="5df8b-133">Muss ein InfoPath-Formular sein.</span><span class="sxs-lookup"><span data-stu-id="5df8b-133">Must be an InfoPath form.</span></span>
    
- <span data-ttu-id="5df8b-134">Als Programmiersprache muss C# oder Visual Basic verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5df8b-134">Must use C# or Visual Basic as the programming language.</span></span>
    
- <span data-ttu-id="5df8b-135">An E-Mail-Datenverbindungen kann nicht übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="5df8b-135">Cannot submit to email data connections.</span></span>
    
- <span data-ttu-id="5df8b-136">Es ist nicht möglich, Eigenschaften für Webpart-zu-Webpart-Verbindungen heraufzustufen.</span><span class="sxs-lookup"><span data-stu-id="5df8b-136">Cannot have properties promoted for part-to-part connections.</span></span>
    
- <span data-ttu-id="5df8b-137">Es dürfen keine Steuerelemente für verwaltete Metadaten oder Datenverbindungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5df8b-137">Must not have any managed meta-data controls or data connections.</span></span>
    
<span data-ttu-id="5df8b-138">Damit Websitesammlungsadministratoren Sandkastenlösungen auf Microsoft SharePoint Server 2010 oder einem Server verwenden können, der Microsoft SharePoint Foundation 2010 ausgeführt wird, muss der Farmadministrator den Windows SharePoint-Benutzercodedienst starten.</span><span class="sxs-lookup"><span data-stu-id="5df8b-138">To enable site collection administrators to use sandboxed solutions on Microsoft SharePoint Server 2010 or a server that runs Microsoft SharePoint Foundation 2010, the farm administrator must start the Windows SharePoint User Code service.</span></span>
  
### <a name="to-start-the-windows-sharepoint-user-code-service"></a><span data-ttu-id="5df8b-139">So starten Sie den Windows SharePoint-Benutzercodedienst</span><span class="sxs-lookup"><span data-stu-id="5df8b-139">To start the Windows SharePoint User Code service</span></span>

1. <span data-ttu-id="5df8b-140">Öffnen Sie die Zentraladministration.</span><span class="sxs-lookup"><span data-stu-id="5df8b-140">Open Central Administration.</span></span>
    
2. <span data-ttu-id="5df8b-141">Klicken Sie unter **Systemdienste** auf **Dienste auf dem Server verwalten**.</span><span class="sxs-lookup"><span data-stu-id="5df8b-141">Under **System Services**, click **Manage services on server**.</span></span>
    
3. <span data-ttu-id="5df8b-142">Starten Sie den **Microsoft SharePoint Foundation-Benutzercodedienst**.</span><span class="sxs-lookup"><span data-stu-id="5df8b-142">Start the **Microsoft SharePoint Foundation User Code Service**.</span></span>
    
### <a name="to-publish-a-sandboxed-solution"></a><span data-ttu-id="5df8b-143">So veröffentlichen Sie eine Sandkastenlösung</span><span class="sxs-lookup"><span data-stu-id="5df8b-143">To publish a sandboxed solution</span></span>

1. <span data-ttu-id="5df8b-144">Öffnen Sie die Formularvorlage in InfoPath Designer.</span><span class="sxs-lookup"><span data-stu-id="5df8b-144">Open the form template in the InfoPath designer.</span></span>
    
2. <span data-ttu-id="5df8b-145">Klicken Sie **auf die** Registerkarte Datei, und klicken  **SharePoint auf** der Registerkarte Veröffentlichen in der Backstage auf Server.</span><span class="sxs-lookup"><span data-stu-id="5df8b-145">Click the **File** tab, and then click **SharePoint Server** on the **Publish** tab in the Backstage.</span></span> 
    
3. <span data-ttu-id="5df8b-146">Geben Sie die URL der SharePoint-Website ein, auf der das Formular veröffentlicht werden soll, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="5df8b-146">Enter the URL of the SharePoint site to publish to, and then click **Next**.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="5df8b-147">Sie müssen ein Websitesammlungsadministrator auf dieser Website sein, um diese Formularvorlage als Sandkastenlösung zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="5df8b-147">You must be a site collection administrator on this site to publish this form template as a sandboxed solution.</span></span> 
  
4. <span data-ttu-id="5df8b-148">Wählen Sie **Formularbibliothek** aus, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="5df8b-148">Select **Form Library**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="5df8b-149">Wählen Sie **Neue Formularbibliothek erstellen** aus, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="5df8b-149">Select **Create a new form library**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="5df8b-150">Geben Sie den Namen und die Beschreibungen für die Formularbibliothek ein, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="5df8b-150">Enter the name and descriptions for your form library, and then click **Next**.</span></span>
    
7. <span data-ttu-id="5df8b-151">Klicken Sie auf **Veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="5df8b-151">Click **Publish**.</span></span>
    
<span data-ttu-id="5df8b-152">Beispiellösungen, die Szenarien veranschaulichen, die für als Sandkastenlösungen veröffentlichte Formularvorlagen geeignet sind, finden Sie unter [Beispiel sandkastenlösungen](sample-sandboxed-solutions.md).</span><span class="sxs-lookup"><span data-stu-id="5df8b-152">For example solutions that demonstrate scenarios that are appropriate for form templates published as sandboxed solutions, see [Sample Sandboxed Solutions](sample-sandboxed-solutions.md).</span></span>
  
### <a name="publishing-form-templates-as-administrator-deployed-solutions"></a><span data-ttu-id="5df8b-153">Veröffentlichen von Formularvorlagen als vom Administrator bereitgestellte Lösungen</span><span class="sxs-lookup"><span data-stu-id="5df8b-153">Publishing Form Templates as Administrator-Deployed Solutions</span></span>

<span data-ttu-id="5df8b-154">Das Veröffentlichen eines Formulars als vom Administrator genehmigte Vorlage wird empfohlen, wenn das Formular zahlreiche Datenverbindungen enthält, wenn Sicherheit durch volle Vertrauenswürdigkeit erforderlich ist oder wenn Sie eine farmweite Vorlage benötigen.</span><span class="sxs-lookup"><span data-stu-id="5df8b-154">Publishing your form as an administrator-approved template is recommended if your form has many data connections, if it requires full-trust security, or if you require a farm-wide template.</span></span>
  
<span data-ttu-id="5df8b-155">Ein Farmadministrator muss verschiedene Schritte ausführen, bevor eine vom Administrator bereitgestellte Lösung in SharePoint verfügbar ist. Sie als Entwickler müssen die Lösung vorbereiten, bevor der Administrator hinzugezogen wird.</span><span class="sxs-lookup"><span data-stu-id="5df8b-155">There are several steps that a farm administrator must complete before an administrator-deployed solution is available on SharePoint, and you as the developer must prepare the solution before the administrator is engaged.</span></span>
  
<span data-ttu-id="5df8b-156">Wenn das Formular als voll vertrauenswürdig bereitgestellt werden soll, müssen Sie zuerst die Sicherheitsstufe wie im folgenden Verfahren beschrieben festlegen.</span><span class="sxs-lookup"><span data-stu-id="5df8b-156">First, if your form is going to be deployed as full trust, you must set the security level as described in the following procedure.</span></span>
  
### <a name="to-set-the-security-level-of-a-form-template-to-full-trust"></a><span data-ttu-id="5df8b-157">So legen Sie die Sicherheitsstufe einer Formularvorlage auf "Voll vertrauenswürdig" fest</span><span class="sxs-lookup"><span data-stu-id="5df8b-157">To set the security level of a form template to full trust</span></span>

1. <span data-ttu-id="5df8b-158">Öffnen Sie die Formularvorlage in InfoPath Designer.</span><span class="sxs-lookup"><span data-stu-id="5df8b-158">Open the form template in the InfoPath designer.</span></span>
    
2. <span data-ttu-id="5df8b-159">Klicken Sie auf die Registerkarte **Datei**, und klicken Sie auf der Registerkarte **Info** auf **Formularoptionen**.</span><span class="sxs-lookup"><span data-stu-id="5df8b-159">Click the **File** tab, on the **Info** tab click **Form Options**.</span></span>
    
3. <span data-ttu-id="5df8b-160">Klicken Sie auf die Kategorie **Sicherheit und Vertrauensstellung**, und deaktivieren Sie dann das Kontrollkästchen **Sicherheitsstufe automatisch ermitteln**.</span><span class="sxs-lookup"><span data-stu-id="5df8b-160">Click the **Security and Trust** category, and then clear the **Automatically determine security level** check box.</span></span> 
    
4. <span data-ttu-id="5df8b-161">Wählen Sie **Voll vertrauenswürdig** aus.</span><span class="sxs-lookup"><span data-stu-id="5df8b-161">Select **Full Trust**.</span></span>
    
<span data-ttu-id="5df8b-162">Veröffentlichen Sie dann das Formular mithilfe des folgenden Verfahrens. Beachten Sie dabei, dass dabei Unterschiede zu einem Standardveröffentlichungsverfahren bestehen.</span><span class="sxs-lookup"><span data-stu-id="5df8b-162">Then, publish the form by using the following procedure, but be aware that there are some differences from a standard publishing procedure.</span></span>
  
### <a name="to-publish-an-administrator-deployed-solution"></a><span data-ttu-id="5df8b-163">So veröffentlichen Sie eine vom Administrator bereitgestellte Lösung</span><span class="sxs-lookup"><span data-stu-id="5df8b-163">To publish an administrator-deployed solution</span></span>

1. <span data-ttu-id="5df8b-164">Geben Sie auf der ersten Seite des Veröffentlichungs-Assistenten den Speicherort der SharePoint Server 2010- oder SharePoint Foundation 2010-Website an, und klicken Sie dann auf **Weiter**. </span><span class="sxs-lookup"><span data-stu-id="5df8b-164">In the first page of the **Publishing Wizard**, specify the location of the SharePoint Server 2010 or SharePoint Foundation 2010 site, and then click **Next**.</span></span>
    
2. <span data-ttu-id="5df8b-165">InfoPath aktiviert automatisch das Kontrollkästchen **Vom Administrator** genehmigte Formularvorlagen auf der zweiten Seite des Assistenten.</span><span class="sxs-lookup"><span data-stu-id="5df8b-165">InfoPath will automatically select the **Administrator-approved form template** check box on the second page of the wizard.</span></span> <span data-ttu-id="5df8b-166">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="5df8b-166">Click **Next**.</span></span>
    
3. <span data-ttu-id="5df8b-167">Die dritte Seite gilt nur für Szenarien mit Bereitstellung durch den Administrator.</span><span class="sxs-lookup"><span data-stu-id="5df8b-167">The third page is unique to administrator-deployed scenarios.</span></span> <span data-ttu-id="5df8b-168">Anstatt einen server SharePoint, veröffentlichen Sie das Formular in einem lokalen Speicher.</span><span class="sxs-lookup"><span data-stu-id="5df8b-168">Instead of selecting a SharePoint Server, publish the form to a local store.</span></span> <span data-ttu-id="5df8b-169">Der SharePoint-Administrator lädt die Datei während des Bereitstellungsvorgangs aus diesem Speicherort hoch.</span><span class="sxs-lookup"><span data-stu-id="5df8b-169">The SharePoint administrator will upload the file from this location during the administrator deployment process.</span></span>
    
4. <span data-ttu-id="5df8b-170">Schließen Sie die restlichen Seiten des Veröffentlichungs-Assistenten ab.</span><span class="sxs-lookup"><span data-stu-id="5df8b-170">Complete the remaining pages of the **Publishing Wizard**.</span></span>
    

