---
title: Zugreifen auf benutzerdefinierte Project Online-Enterprise-Felder
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
ms.assetid: 25509631-fa14-49d8-b594-cfacf5355c38
description: 'Project Online ist ein Office 365-Dienst, den Unternehmen erweitern können, um Geschäftsanforderungen zu erfüllen. Ein Erweiterungsbereich sind benutzerdefinierte Enterprise-Felder (Enterprise Custom Fields, ECFs). ECFs sind typbehaftete Wertfelder, die Projekten, Ressourcen und Aufgaben hinzugefügt werden können. In der folgenden Tabelle sind ECFs, die mit Projekten, Ressourcen und Aufgaben verknüpft sind, und jeweils ein Beispiel eines Werts für eine Instanz des jeweiligen ECF aufgelistet:'
localization_priority: Priority
ms.openlocfilehash: 9f754f1446890ae021bf6f7000ffba11e2a2df33
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355083"
---
# <a name="accessing-project-online-enterprise-custom-fields"></a><span data-ttu-id="0b0a7-106">Zugreifen auf benutzerdefinierte Project Online-Enterprise-Felder</span><span class="sxs-lookup"><span data-stu-id="0b0a7-106">Accessing Project Online enterprise custom fields</span></span>

<span data-ttu-id="0b0a7-107">Project Online ist ein Office 365-Dienst, den Unternehmen erweitern können, um Geschäftsanforderungen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-107">Project Online is an Office 365 service that companies can extend to meet business needs.</span></span> <span data-ttu-id="0b0a7-108">Ein Erweiterungsbereich sind benutzerdefinierte Enterprise-Felder (Enterprise Custom Fields, ECFs).</span><span class="sxs-lookup"><span data-stu-id="0b0a7-108">One extension area is Enterprise Custom Fields (ECFs).</span></span> <span data-ttu-id="0b0a7-109">ECFs sind typbehaftete Wertfelder, die Projekten, Ressourcen und Aufgaben hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-109">ECFs are typed value fields that can be added to projects, resources, and tasks.</span></span> <span data-ttu-id="0b0a7-110">In der folgenden Tabelle sind ECFs, die mit Projekten, Ressourcen und Aufgaben verknüpft sind, und jeweils ein Beispiel eines Werts für eine Instanz des jeweiligen ECF aufgelistet:</span><span class="sxs-lookup"><span data-stu-id="0b0a7-110">The following table lists ECFs that associate with projects, resources, and tasks, and provides an example of a value for an instance of that ECF:</span></span>
  
|<span data-ttu-id="0b0a7-111">ECF-Name</span><span class="sxs-lookup"><span data-stu-id="0b0a7-111">ECF Name</span></span>|<span data-ttu-id="0b0a7-112">ECF-Typ</span><span class="sxs-lookup"><span data-stu-id="0b0a7-112">ECF Type</span></span>|<span data-ttu-id="0b0a7-113">Zuweisung</span><span class="sxs-lookup"><span data-stu-id="0b0a7-113">Association</span></span>|<span data-ttu-id="0b0a7-114">Beispielwert</span><span class="sxs-lookup"><span data-stu-id="0b0a7-114">Example Value</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0b0a7-115">Justification</span><span class="sxs-lookup"><span data-stu-id="0b0a7-115">Justification</span></span>  <br/> |<span data-ttu-id="0b0a7-116">TEXT</span><span class="sxs-lookup"><span data-stu-id="0b0a7-116">TEXT</span></span>  <br/> |<span data-ttu-id="0b0a7-117">Project</span><span class="sxs-lookup"><span data-stu-id="0b0a7-117">Project</span></span>  <br/> |<span data-ttu-id="0b0a7-118">Ein Endbenutzer kann wichtige Statistiken und Zustandsdaten erfassen, mit Ergebnissen, die eine Zustandsbewertung und einen individualisierten Aktionsplan in Richtung Zustandsverbesserung beinhalten.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-118">An end user can record vital statistics and health data, with results that include a health evaluation and an individualized action plan towards better health.</span></span>  <br/> |
|<span data-ttu-id="0b0a7-119">Risikobewertung</span><span class="sxs-lookup"><span data-stu-id="0b0a7-119">Risk Rating</span></span>  <br/> |<span data-ttu-id="0b0a7-120">TEXT</span><span class="sxs-lookup"><span data-stu-id="0b0a7-120">TEXT</span></span>  <br/> |<span data-ttu-id="0b0a7-121">Project</span><span class="sxs-lookup"><span data-stu-id="0b0a7-121">Project</span></span>  <br/> |<span data-ttu-id="0b0a7-122">Niedrig</span><span class="sxs-lookup"><span data-stu-id="0b0a7-122">Low</span></span>  <br/> |
|<span data-ttu-id="0b0a7-123">ROI</span><span class="sxs-lookup"><span data-stu-id="0b0a7-123">ROI</span></span>  <br/> |<span data-ttu-id="0b0a7-124">NUMBER</span><span class="sxs-lookup"><span data-stu-id="0b0a7-124">NUMBER</span></span>  <br/> |<span data-ttu-id="0b0a7-125">Project</span><span class="sxs-lookup"><span data-stu-id="0b0a7-125">Project</span></span>  <br/> |<span data-ttu-id="0b0a7-126">2.10</span><span class="sxs-lookup"><span data-stu-id="0b0a7-126">2.10</span></span>  <br/> |
|<span data-ttu-id="0b0a7-127">Total Cost</span><span class="sxs-lookup"><span data-stu-id="0b0a7-127">Total Cost</span></span>  <br/> |<span data-ttu-id="0b0a7-128">COST</span><span class="sxs-lookup"><span data-stu-id="0b0a7-128">COST</span></span>  <br/> |<span data-ttu-id="0b0a7-129">Project</span><span class="sxs-lookup"><span data-stu-id="0b0a7-129">Project</span></span>  <br/> |<span data-ttu-id="0b0a7-130">$1.031.514</span><span class="sxs-lookup"><span data-stu-id="0b0a7-130">$1,031,514</span></span>  <br/> |
|<span data-ttu-id="0b0a7-131">Launch Team</span><span class="sxs-lookup"><span data-stu-id="0b0a7-131">Launch Team</span></span>  <br/> |<span data-ttu-id="0b0a7-132">TEXT</span><span class="sxs-lookup"><span data-stu-id="0b0a7-132">TEXT</span></span>  <br/> |<span data-ttu-id="0b0a7-133">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0b0a7-133">Resources</span></span>  <br/> |<span data-ttu-id="0b0a7-134">Ja</span><span class="sxs-lookup"><span data-stu-id="0b0a7-134">Yes</span></span>  <br/> |
|<span data-ttu-id="0b0a7-135">Position Role</span><span class="sxs-lookup"><span data-stu-id="0b0a7-135">Position Role</span></span>  <br/> |<span data-ttu-id="0b0a7-136">TEXT</span><span class="sxs-lookup"><span data-stu-id="0b0a7-136">TEXT</span></span>  <br/> |<span data-ttu-id="0b0a7-137">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0b0a7-137">Resources</span></span>  <br/> |<span data-ttu-id="0b0a7-138">Tester</span><span class="sxs-lookup"><span data-stu-id="0b0a7-138">Tester</span></span>  <br/> |
|<span data-ttu-id="0b0a7-139">Flag Status</span><span class="sxs-lookup"><span data-stu-id="0b0a7-139">Flag Status</span></span>  <br/> |<span data-ttu-id="0b0a7-140">FLAG</span><span class="sxs-lookup"><span data-stu-id="0b0a7-140">FLAG</span></span>  <br/> |<span data-ttu-id="0b0a7-141">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="0b0a7-141">Task</span></span>  <br/> |<span data-ttu-id="0b0a7-142">No</span><span class="sxs-lookup"><span data-stu-id="0b0a7-142">No</span></span>  <br/> |
|<span data-ttu-id="0b0a7-143">Health</span><span class="sxs-lookup"><span data-stu-id="0b0a7-143">Health</span></span>  <br/> |<span data-ttu-id="0b0a7-144">TEXT</span><span class="sxs-lookup"><span data-stu-id="0b0a7-144">TEXT</span></span>  <br/> |<span data-ttu-id="0b0a7-145">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="0b0a7-145">Task</span></span>  <br/> |<span data-ttu-id="0b0a7-146">Nicht angegeben</span><span class="sxs-lookup"><span data-stu-id="0b0a7-146">Not specified</span></span>  <br/> |
   
<span data-ttu-id="0b0a7-147">ECFs sind in der Project Web Application-Instanz (PWA-Instanz) definiert, außerhalb von jedem Projekt, jeder Ressource oder jeder Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-147">ECFs are defined at the Project Web Application (PWA) instance, external from any project, resource, or task.</span></span> <span data-ttu-id="0b0a7-148">Dennoch können sie mit einem Projekt, einer Ressource oder einer Aufgabe verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-148">Yet, they can become associated with a project, resource, or task.</span></span> <span data-ttu-id="0b0a7-149">Dieser Artikel bietet eine einführende Sicht auf benutzerdefinierte Felder anhand einer Beispielanwendung und konzentriert sich auf das Abrufen von ECF-Werten.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-149">This article provides an introductory look at custom fields using a sample application and focuses on retrieving ECF values.</span></span> 
  
<span data-ttu-id="0b0a7-150">Sie können das vollständige Beispiel aus https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields herunterladen.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-150">You can download the complete sample at https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields.</span></span>
  
<span data-ttu-id="0b0a7-151">Darüber hinaus unterstützt Project Online lokale benutzerdefinierte Felder als schreibgeschützte Einheiten, die speziell für das jeweilige Objekt (Projekt, Ressource oder Aufgabe) gelten.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-151">Additionally, Project Online supports local custom fields as read-only entities specific to the specific project, resource, or task.</span></span> <span data-ttu-id="0b0a7-152">Weitere Informationen zu lokalen benutzerdefinierten Feldern finden Sie im Beispiel https://github.com/OfficeDev/Project-CSOM-Read-Local-CustomFields\.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-152">For more information on local custom fields, see the sample https://github.com/OfficeDev/Project-CSOM-Read-Local-CustomFields\.</span></span>
  
## <a name="background-materials"></a><span data-ttu-id="0b0a7-153">Hintergrundmaterial</span><span class="sxs-lookup"><span data-stu-id="0b0a7-153">Background materials</span></span>

<span data-ttu-id="0b0a7-154">Ein vorheriger Artikel, [Entwickeln einer Project Online-Anwendung mit dem clientseitigen Objektmodell](developing-a-project-online-application-using-the-client-side-object-model.md), bietet Hintergrundinformationen und die erste Orientierung für die Entwicklung von Anwendungen mit CSOM.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-154">A previous article, [Developing a Project Online application using the client-side object model](developing-a-project-online-application-using-the-client-side-object-model.md), provides background and the initial orientation for developing applications using CSOM.</span></span> <span data-ttu-id="0b0a7-155">In diesem Artikel finden Sie die folgenden Punkte:</span><span class="sxs-lookup"><span data-stu-id="0b0a7-155">Refer to this article for the following items:</span></span>
  
- <span data-ttu-id="0b0a7-156">Hintergrundinformationen zu Project, eigenständige und cloudbasierte Editionen</span><span class="sxs-lookup"><span data-stu-id="0b0a7-156">Background information about Project, stand-alone and cloud-based editions</span></span> 
    
- <span data-ttu-id="0b0a7-157">Entwicklungsumgebung (Visual Studio-Editionen und Softwarebibliotheken)</span><span class="sxs-lookup"><span data-stu-id="0b0a7-157">Development environment (Visual Studio editions and software libraries)</span></span>
    
- <span data-ttu-id="0b0a7-158">Einrichten eines Visual Studio-Projekts für eine .NET-Anwendung mit der CSOM-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0b0a7-158">Visual Studio project setup for a .NET application using the CSOM library</span></span>
    
- <span data-ttu-id="0b0a7-159">Herstellen einer Verbindung mit dem Project Online-Dienst</span><span class="sxs-lookup"><span data-stu-id="0b0a7-159">Connecting to the Project Online service</span></span>
    
## <a name="preliminaries-class-level-declarations"></a><span data-ttu-id="0b0a7-160">Vorbereitungen (Deklarationen auf Klassenebene)</span><span class="sxs-lookup"><span data-stu-id="0b0a7-160">Preliminaries (class-level declarations)</span></span>

<span data-ttu-id="0b0a7-161">Die Klasse für diese Anwendung definiert zwei Datenelemente: den Projektkontext und das pwaECF-Wörterbuch.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-161">The class for this application defines two data items: the project context and the pwaECF dictionary.</span></span>
  
<span data-ttu-id="0b0a7-162">Das Projektkontextobjekt ist Bestandteil des Project-CSOM und verbindet die Anwendung und die PWA-Instanz.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-162">The project context object is part of the Project CSOM, and connects the application and the PWA instance.</span></span> <span data-ttu-id="0b0a7-163">Alle Anforderungen an den Dienst verwenden den Projektkontext.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-163">All requests to the service use the project context.</span></span>
  
```cs
private static ProjectContext projContext = 
     new ProjectContext("https://Contoso216.sharepoint.com/sites/pwa");

```

<span data-ttu-id="0b0a7-164">Der Kontext benötigt den Verbindungsendpunkt, um eine Instanz in einer Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-164">The context needs the connection endpoint to create an instance in an application.</span></span> <span data-ttu-id="0b0a7-165">Der Verbindungsendpunkt ist die URL Ihrer PWA-Instanz.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-165">The connection endpoint is the URL of your PWA instance.</span></span> 
  
<span data-ttu-id="0b0a7-166">Das pwaECF-Wörterbuch speichert die Projekt-ECFs, die auf der PWA-Ebene definiert sind.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-166">The pwaECF dictionary stores the project ECFs defined at the PWA level.</span></span> <span data-ttu-id="0b0a7-167">Das Wörterbuch verwendet "ECF.InternalName" als Schlüssel und das "CustomField"-Objekt als Wert.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-167">The dictionary uses the ECF.InternalName as the key, and the CustomField object as the value.</span></span> <span data-ttu-id="0b0a7-168">Das Wörterbuch wird mit der "ListPWACustomFields"-Methode aufgefüllt und dann als Referenz in der "Main"-Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-168">The dictionary is populated in the ListPWACustomFields method, and then used as a reference in the Main method.</span></span> 
  
```cs
    //Dictionary of ECFs
        static Dictionary<String, CustomField> pwaECF = new Dictionary<string, CustomField>();

```

## <a name="main-method"></a><span data-ttu-id="0b0a7-169">"Main"-Methode</span><span class="sxs-lookup"><span data-stu-id="0b0a7-169">Main method</span></span>

<span data-ttu-id="0b0a7-170">Die "Main"-Methode verwaltet den Datenfluss der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-170">The Main method manages the application flow.</span></span> <span data-ttu-id="0b0a7-171">Wie bei anderen Anwendungen, in denen das Project Online-CSOM verwendet wird, initialisiert "Main" den Projektkontext.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-171">As with other applications that use the Project Online CSOM, Main initializes the project context.</span></span> 
  
1. <span data-ttu-id="0b0a7-172">Rufen und Sie die ECFs in der Project Online-PWA-Instanz ab, und listen Sie sie auf.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-172">Retrieve and list the ECFs in the Project Online PWA.</span></span>
    
   <span data-ttu-id="0b0a7-173">Diese Funktionalität ist in der "ListPWACustomFields"-Methode implementiert.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-173">This functionality is implemented in the ListPWACustomFields method.</span></span>
    
2. <span data-ttu-id="0b0a7-174">Rufen Sie Projekte mit benutzerdefinierten Feldern und nicht-benutzerdefinierten Feldern ab.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-174">Retrieve projects with custom fields and non-custom fields.</span></span>
    
   <span data-ttu-id="0b0a7-175">Werden Projekte mit ECFs abgerufen, muss die Abfrageanforderung an den Project Online-Dienst die folgenden Elemente enthalten:</span><span class="sxs-lookup"><span data-stu-id="0b0a7-175">When retrieving projects with ECFs, the query request to the Project Online service needs to include the following items:</span></span> 
    
   - <span data-ttu-id="0b0a7-176">**IncludeCustomFields** &ndash; Dieses Element fordert den Dienst auf, eine Sammlung veröffentlichter Projekte ("PublishedProject"-Objekte) zurückzugeben, wobei jedes veröffentlichte Projekt eine Erweiterung enthält, die benutzerdefinierte Felder unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-176">**IncludeCustomFields** &ndash; This item requests the service to return a collection of PublishedProjects where each published project includes an extension that supports custom fields.</span></span> <span data-ttu-id="0b0a7-177">Ist dieses Element nicht angegeben, gibt Project Online "PublishedProject"-Objekte zurück, die keine Daten aus benutzerdefinierten Feldern enthalten.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-177">Unless this item is specified, Project Online returns PublishedProject objects that do not include Custom Field data.</span></span>
    
   - <span data-ttu-id="0b0a7-178">**IncludeCustomFields.CustomFields** &ndash; Dieses Element fordert den Dienst auf, die "PublishedProject"-Objekte mit "CustomFields"-Daten auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-178">**IncludeCustomFields.CustomFields** &ndash; This item requests the service to populate the PublishedProject objects with CustomFields data.</span></span>
    
   <span data-ttu-id="0b0a7-179">Die folgende Anforderung gibt die Projekt-ID und den Projektnamen sowie die Objekterweiterung für benutzerdefinierte Felder und die Werte der benutzerdefinierten Felder an.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-179">The following request specifies the project Id and Name, as well as the object extension for custom fields and the custom field values.</span></span>
    
   ```cs
        var projBlk = projContext.LoadQuery(
        projContext.Projects.Include(
            p => p.Id, 
            p => p.Name,
            p => p.IncludeCustomFields,
            p => p.IncludeCustomFields.CustomFields
        ));
    
   ```

3. <span data-ttu-id="0b0a7-180">Überprüfen Sie jedes Projekt.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-180">Examine each project.</span></span>
    
   <span data-ttu-id="0b0a7-181">Die in dieser Anwendung verwendeten Projektobjekte entsprechen dem "PublishedProject"-Typ, weil die Werte abgerufen und angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-181">The project objects used in this application are the PublishedProject type because the values are retrieved and displayed.</span></span> 
    
   <span data-ttu-id="0b0a7-182">Wenn Sie Datenwerte in einem oder mehreren Projekten aktualisieren müssen, würde das zu aktualisierende Projekt ausgecheckt, und würde die Anwendung ein "DraftProject"-Objekt verwenden, um die Werte abzurufen und das Projekt zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-182">If you need to update data values in one or more projects, the project undergoing the update would be checked out and the application would use a DraftProject object to retrieve the values and update the project.</span></span>
    
4. <span data-ttu-id="0b0a7-183">Zugreifen auf die ECF-Einträge für ein Projekt</span><span class="sxs-lookup"><span data-stu-id="0b0a7-183">Accessing the ECF entries for a project</span></span>
    
   <span data-ttu-id="0b0a7-184">In jeder ECF-Instanz wird der Feldwert von den restlichen ECF-Informationen getrennt.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-184">Each ECF instance separates the field value from the rest of the ECF information.</span></span> <span data-ttu-id="0b0a7-185">Der Feldwert wird als Teil eines Schlüssel-Wert-Paares gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-185">The field value is stored as part of a key/value pair.</span></span> <span data-ttu-id="0b0a7-186">Die restlichen Informationen werden in einem "CustomField"-Objekt gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-186">The rest of the information is stored in a CustomField object.</span></span>
    
   <span data-ttu-id="0b0a7-187">Zugreifen auf ECF-Werte in einem Projekt besteht aus zwei Teilen:</span><span class="sxs-lookup"><span data-stu-id="0b0a7-187">Accessing ECF values in a project consists of two parts:</span></span>
    
   - <span data-ttu-id="0b0a7-188">Durchlaufen der "CustomFields"-Sammlung</span><span class="sxs-lookup"><span data-stu-id="0b0a7-188">Cycling through the CustomFields collection</span></span>
    
   - <span data-ttu-id="0b0a7-189">Zugreifen auf den richtigen Eintrag mit zwei Konstrukten</span><span class="sxs-lookup"><span data-stu-id="0b0a7-189">Accessing the proper entry using two constructs.</span></span>
    
   <span data-ttu-id="0b0a7-190">In jedem Projekt werden zugewiesene ECF Einträge an zwei Stellen gespeichert: in einer "CustomFields"-Sammlung, die durchlaufen werden kann, und in den Feldwerten als Bestandteile von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-190">Each project stores associated ECF entries in two places, a CustomFields collection that is enumerable and and the field values as part of key/value pairs.</span></span> <span data-ttu-id="0b0a7-191">In den Schlüssel-Wert-Paaren ist der interne Name (internalName) der Schlüssel und der Feldwert der Wert.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-191">In the key/value pairs, the internalName is the key and the field value is the value.</span></span> <span data-ttu-id="0b0a7-192">Verwenden Sie ein Wörterbuch, um die Feldwerte zu speichern und auf sie zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-192">Use a dictionary to hold and access the field values.</span></span> 
    
   <span data-ttu-id="0b0a7-193">Die ECF-Eigenschaften werden, anders als die Feldwerte, in "CustomField"-Objekten gespeichert, ein Objekt pro Projekt.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-193">The ECF properties, other than the field values, are stored in CustomField objects, one object per project.</span></span> <span data-ttu-id="0b0a7-194">Verwenden Sie eine "CustomFields"-Sammlung, um auf die ECFs zuzugreifen, die mit einem einzelnen Projekt verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-194">Use a CustomFields collection to access the ECFs associated with an individual project.</span></span> 
    
5. <span data-ttu-id="0b0a7-195">In jedem Projekt werden die zugehörigen ECFs in einer Sammlung gespeichert, in der jeder Eintrag aus einem Schlüssel – der interne Name des ECF – und einem Objekt besteht, das den Wert des ECF enthält.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-195">Each project stores the associated ECFs in a collection where each ECF entry consists of a key--the internal name of the ECF--and an object that holds the value of the ECF.</span></span> <span data-ttu-id="0b0a7-196">Überführen Sie die Sammlung in ein Wörterbuch, um auf einzelne Einträge zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-196">Transfer the collection to a dictionary to access individual entries.</span></span> <span data-ttu-id="0b0a7-197">Die Deklaration folgt.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-197">The declaration follows.</span></span>
    
   ```cs
    Dictionary<string, object> projDict = pubProj.IncludeCustomFields.FieldValues;
    
   ```

   <span data-ttu-id="0b0a7-198">Der Wert in einem Wörterbucheintrags entspricht dem Datentyp des ECF.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-198">The value in a dictionary entry corresponds to the data type of the ECF.</span></span> <span data-ttu-id="0b0a7-199">Das Objekt für jedes ECF wird einem Typ aus einer Reihe von Typen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-199">The object for each ECF maps to one of a variety of types.</span></span> <span data-ttu-id="0b0a7-200">Für die meisten ECFs werden einfache Typen verwendet, die in Standardvariablen passen.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-200">Most ECFs use simple types that fit into standard variables.</span></span> <span data-ttu-id="0b0a7-201">Im folgenden Fragment wird gezeigt, dass verschiedene Typen eine minimale Verarbeitung erfordern:</span><span class="sxs-lookup"><span data-stu-id="0b0a7-201">The following fragment shows that minimal processing is involved for several types:</span></span>
    
   ```cs
    switch (cf.FieldType)
    {
        case CustomFieldType.COST:
            decimal costValue = (decimal)oVal;
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                costValue.ToString("C"));
            break;
        case CustomFieldType.DATE:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.FINISHDATE:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.DURATION:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.FLAG:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.NUMBER:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
    
   ```

   <span data-ttu-id="0b0a7-202">Die Nachschlagetabelle von TEXT-Werten erfordert jedoch zusätzliche Verarbeitungsschritte.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-202">The lookup table of TEXT values, however, requires additional processing.</span></span> <span data-ttu-id="0b0a7-203">Die Anwendung ruft die entsprechende Nachschlagetabelle aus dem Dienst ab und gibt die ECF-Instanz (mit einem oder mehreren Werten) aus, indem sie die Nachschlagetabelle durchläuft.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-203">The application retrieves the appropriate lookup table from the service, and outputs the ECF instance (with single or multiple values) by traversing the lookup table.</span></span> <span data-ttu-id="0b0a7-204">Im folgenden Codefragment wird die Verarbeitung von TEXT-ECFs gezeigt, einschließlich derjenigen mit einfachen Werten und derjenigen mit Nachschlagetabellen:</span><span class="sxs-lookup"><span data-stu-id="0b0a7-204">The following code fragment shows processing of TEXT ECFs, including those with simple values and those using lookup tables:</span></span> 
    
   ```cs
    case CustomFieldType.TEXT:
        if (!cf.LookupTable.ServerObjectIsNull.HasValue ||
            (cf.LookupTable.ServerObjectIsNull.HasValue && 
            cf.LookupTable.ServerObjectIsNull.Value))
        { //No lookup table
            Console.WriteLine("\tFieldType:\t{0}\n\tText:\t{1}", cf.FieldType, 
                oVal.ToString());
        }
        else
        { //Lookup table
            Console.WriteLine("\tFieldType:\t{0} - using Lookup Table", cf.FieldType);
            String[] entries = (String[])oVal;
            foreach (String entry in entries)
            {
                var luEntry = projContext.LoadQuery(cf.LookupTable.Entries
                    .Where(e => e.InternalName == entry));
                projContext.ExecuteQuery();
                Console.WriteLine("\tLookup Value:\t{0}", luEntry.First().FullValue);  
            }
        }
        break;
    
   ```

   <span data-ttu-id="0b0a7-205">Diese Anwendung gibt schlicht den Wert oder die Werte aus. Allerdings ist es möglich, mehr Bedeutung aus den Datenwerten zu gewinnen.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-205">This application simply outputs the value(s); however, it is possible to get more meaning from the data value(s).</span></span>
    
## <a name="listpwacustomfields"></a><span data-ttu-id="0b0a7-206">ListPWACustomFields</span><span class="sxs-lookup"><span data-stu-id="0b0a7-206">ListPWACustomFields</span></span>

<span data-ttu-id="0b0a7-207">Die "ListPWACustomFields"-Methode ruft die ECFs ab, die mit Projekten verknüpft sind, und listet die ECFs auf.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-207">The ListPWACustomFields method retrieves and lists the ECFs associated with projects.</span></span> <span data-ttu-id="0b0a7-208">Diese Methode listet die ECFs auf, die in der PWA-Instanz registriert sind, die mit einzelnen Projekten verknüpft werden kann.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-208">This method lists the ECFs registered on the PWA instance that can be associated with individual projects.</span></span> <span data-ttu-id="0b0a7-209">Der Einstiegspunkt für Zugreifen auf die ECFs verwendet das "CustomFields"-Element des Projektkontexts, wie in der folgenden Abfrageanforderung:</span><span class="sxs-lookup"><span data-stu-id="0b0a7-209">The entry point for accessing the ECFs uses the CustomFields element of the project context, as in the following query request:</span></span>
  
```cs
// Project ECFs
    var allECFields = 
            projContext.LoadQuery(projContext.CustomFields.Include(
            qp => qp.InternalName,
            qp => qp.Name
        ));
    projContext.ExecuteQuery();

```

<span data-ttu-id="0b0a7-210">Die Methode überprüft nicht, ob für ein Projekt ein bestimmtes ECF verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0b0a7-210">The method does not check to see whether a project uses a specific ECF.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0b0a7-211">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b0a7-211">See also</span></span>

- [<span data-ttu-id="0b0a7-212">Project-Entwicklungsportal</span><span class="sxs-lookup"><span data-stu-id="0b0a7-212">Project Development Portal</span></span>](https://developer.microsoft.com/de-DE/project)
- [<span data-ttu-id="0b0a7-213">Übersicht: Benutzerdefinierte Enterprise-Felder und Nachschlagetabellen</span><span class="sxs-lookup"><span data-stu-id="0b0a7-213">Overview: Enterprise custom fields and lookup tables</span></span>](https://support.office.com/en-us/article/overview-enterprise-custom-fields-and-lookup-tables-f99db553-0b33-4648-93c0-f6a74637d790?ui=en-us&rs=en-us&ad=us)
- <span data-ttu-id="0b0a7-214">[Local and Enterprise Custom Fields](https://msdn.microsoft.com/library/office/ms447495(v=office.14).aspx)</span><span class="sxs-lookup"><span data-stu-id="0b0a7-214">[Local and Enterprise Custom Fields](https://msdn.microsoft.com/library/office/ms447495(v=office.14).aspx)</span></span>
- [<span data-ttu-id="0b0a7-215">Hinzufügen oder Bearbeiten benutzerdefinierter Enterprise-Felder in Project Server 2013</span><span class="sxs-lookup"><span data-stu-id="0b0a7-215">Add or edit enterprise custom fields in Project Server 2013</span></span>](https://docs.microsoft.com/project/add-or-edit-enterprise-custom-fields-in-project-server)
    

