---
title: Zugreifen auf Project Online benutzerdefinierte Enterprise-Felder
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 25509631-fa14-49d8-b594-cfacf5355c38
description: 'Project Online ist ein Office 365-Dienst, den geschäftlichen Anforderungen Unternehmen erweitern können. Eine Erweiterung Bereich ist benutzerdefinierte Enterprise-Felder (ECFs). ECFs sind typisierten Wertfelder, die Projekte, Aufgaben und Ressourcen hinzugefügt werden können. In der folgenden Tabelle sind ECFs, die mit Projekten, Ressourcen und Aufgaben zuordnen, und enthält ein Beispiel für einen Wert für eine Instanz dieser ECF:'
ms.openlocfilehash: d6c8f97ffc887b33e5d81af8e463cf10502845dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796175"
---
# <a name="accessing-project-online-enterprise-custom-fields"></a><span data-ttu-id="1e2b2-106">Zugreifen auf Project Online benutzerdefinierte Enterprise-Felder</span><span class="sxs-lookup"><span data-stu-id="1e2b2-106">Accessing Project Online enterprise custom fields</span></span>

<span data-ttu-id="1e2b2-107">Project Online ist ein Office 365-Dienst, den geschäftlichen Anforderungen Unternehmen erweitern können.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-107">Project Online is an Office 365 service that companies can extend to meet business needs.</span></span> <span data-ttu-id="1e2b2-108">Eine Erweiterung Bereich ist benutzerdefinierte Enterprise-Felder (ECFs).</span><span class="sxs-lookup"><span data-stu-id="1e2b2-108">One extension area is Enterprise Custom Fields (ECFs).</span></span> <span data-ttu-id="1e2b2-109">ECFs sind typisierten Wertfelder, die Projekte, Aufgaben und Ressourcen hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-109">ECFs are typed value fields that can be added to projects, resources, and tasks.</span></span> <span data-ttu-id="1e2b2-110">In der folgenden Tabelle sind ECFs, die mit Projekten, Ressourcen und Aufgaben zuordnen, und enthält ein Beispiel für einen Wert für eine Instanz dieser ECF:</span><span class="sxs-lookup"><span data-stu-id="1e2b2-110">The following table lists ECFs that associate with projects, resources, and tasks, and provides an example of a value for an instance of that ECF:</span></span>
  
|<span data-ttu-id="1e2b2-111">ECF-Name</span><span class="sxs-lookup"><span data-stu-id="1e2b2-111">ECF Name</span></span>|<span data-ttu-id="1e2b2-112">ECF-Typ</span><span class="sxs-lookup"><span data-stu-id="1e2b2-112">ECF Type</span></span>|<span data-ttu-id="1e2b2-113">Zuordnung</span><span class="sxs-lookup"><span data-stu-id="1e2b2-113">Association</span></span>|<span data-ttu-id="1e2b2-114">Beispielwert</span><span class="sxs-lookup"><span data-stu-id="1e2b2-114">Example Value</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1e2b2-115">Begründung</span><span class="sxs-lookup"><span data-stu-id="1e2b2-115">Justification</span></span>  <br/> |<span data-ttu-id="1e2b2-116">TEXT</span><span class="sxs-lookup"><span data-stu-id="1e2b2-116">TEXT</span></span>  <br/> |<span data-ttu-id="1e2b2-117">Project</span><span class="sxs-lookup"><span data-stu-id="1e2b2-117">Project</span></span>  <br/> |<span data-ttu-id="1e2b2-118">Endbenutzer können meine Daten und Gesundheitsdaten mit Ergebnissen, die eine Testversion Integrität und eine individuelle Aktion enthalten aufzeichnen Plan bald besser Integrität.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-118">An end user can record vital statistics and health data, with results that include a health evaluation and an individualized action plan towards better health.</span></span>  <br/> |
|<span data-ttu-id="1e2b2-119">Schweregrads</span><span class="sxs-lookup"><span data-stu-id="1e2b2-119">Risk Rating</span></span>  <br/> |<span data-ttu-id="1e2b2-120">TEXT</span><span class="sxs-lookup"><span data-stu-id="1e2b2-120">TEXT</span></span>  <br/> |<span data-ttu-id="1e2b2-121">Project</span><span class="sxs-lookup"><span data-stu-id="1e2b2-121">Project</span></span>  <br/> |<span data-ttu-id="1e2b2-122">Low</span><span class="sxs-lookup"><span data-stu-id="1e2b2-122">Low</span></span>  <br/> |
|<span data-ttu-id="1e2b2-123">ROI</span><span class="sxs-lookup"><span data-stu-id="1e2b2-123">ROI</span></span>  <br/> |<span data-ttu-id="1e2b2-124">ANZAHL</span><span class="sxs-lookup"><span data-stu-id="1e2b2-124">NUMBER</span></span>  <br/> |<span data-ttu-id="1e2b2-125">Project</span><span class="sxs-lookup"><span data-stu-id="1e2b2-125">Project</span></span>  <br/> |<span data-ttu-id="1e2b2-126">2.10</span><span class="sxs-lookup"><span data-stu-id="1e2b2-126">2.10</span></span>  <br/> |
|<span data-ttu-id="1e2b2-127">Gesamtkosten</span><span class="sxs-lookup"><span data-stu-id="1e2b2-127">Total Cost</span></span>  <br/> |<span data-ttu-id="1e2b2-128">KOSTEN</span><span class="sxs-lookup"><span data-stu-id="1e2b2-128">COST</span></span>  <br/> |<span data-ttu-id="1e2b2-129">Project</span><span class="sxs-lookup"><span data-stu-id="1e2b2-129">Project</span></span>  <br/> |<span data-ttu-id="1e2b2-130">$1,031,514</span><span class="sxs-lookup"><span data-stu-id="1e2b2-130">$1,031,514</span></span>  <br/> |
|<span data-ttu-id="1e2b2-131">Starten Sie Team</span><span class="sxs-lookup"><span data-stu-id="1e2b2-131">Launch Team</span></span>  <br/> |<span data-ttu-id="1e2b2-132">TEXT</span><span class="sxs-lookup"><span data-stu-id="1e2b2-132">TEXT</span></span>  <br/> |<span data-ttu-id="1e2b2-133">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1e2b2-133">Resources</span></span>  <br/> |<span data-ttu-id="1e2b2-134">Ja</span><span class="sxs-lookup"><span data-stu-id="1e2b2-134">Yes</span></span>  <br/> |
|<span data-ttu-id="1e2b2-135">Position-Rolle</span><span class="sxs-lookup"><span data-stu-id="1e2b2-135">Position Role</span></span>  <br/> |<span data-ttu-id="1e2b2-136">TEXT</span><span class="sxs-lookup"><span data-stu-id="1e2b2-136">TEXT</span></span>  <br/> |<span data-ttu-id="1e2b2-137">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1e2b2-137">Resources</span></span>  <br/> |<span data-ttu-id="1e2b2-138">Tester</span><span class="sxs-lookup"><span data-stu-id="1e2b2-138">Tester</span></span>  <br/> |
|<span data-ttu-id="1e2b2-139">Kennzeichnungsstatus</span><span class="sxs-lookup"><span data-stu-id="1e2b2-139">Flag Status</span></span>  <br/> |<span data-ttu-id="1e2b2-140">KENNZEICHNUNG</span><span class="sxs-lookup"><span data-stu-id="1e2b2-140">FLAG</span></span>  <br/> |<span data-ttu-id="1e2b2-141">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="1e2b2-141">Task</span></span>  <br/> |<span data-ttu-id="1e2b2-142">Nein</span><span class="sxs-lookup"><span data-stu-id="1e2b2-142">No</span></span>  <br/> |
|<span data-ttu-id="1e2b2-143">Integrität</span><span class="sxs-lookup"><span data-stu-id="1e2b2-143">Health</span></span>  <br/> |<span data-ttu-id="1e2b2-144">TEXT</span><span class="sxs-lookup"><span data-stu-id="1e2b2-144">TEXT</span></span>  <br/> |<span data-ttu-id="1e2b2-145">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="1e2b2-145">Task</span></span>  <br/> |<span data-ttu-id="1e2b2-146">Nicht angegeben</span><span class="sxs-lookup"><span data-stu-id="1e2b2-146">Not specified</span></span>  <br/> |
   
<span data-ttu-id="1e2b2-147">ECFs werden auf der Project Web Application (PWA)-Instanz von Projekt, Ressource oder Vorgang externe definiert.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-147">ECFs are defined at the Project Web Application (PWA) instance, external from any project, resource, or task.</span></span> <span data-ttu-id="1e2b2-148">Noch, können sie ein Projekt, Ressource oder Vorgang zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-148">Yet, they can become associated with a project, resource, or task.</span></span> <span data-ttu-id="1e2b2-149">Dieser Artikel bietet eine grundlegende Aufstellung verwenden ein Beispiel für benutzerdefinierte Felder und liegt der Schwerpunkt auf Abrufen ECF Werte.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-149">This article provides an introductory look at custom fields using a sample application and focuses on retrieving ECF values.</span></span> 
  
<span data-ttu-id="1e2b2-150">Sie können das vollständige Beispiel unter herunterladen https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-150">You can download the complete sample at https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields.</span></span>
  
<span data-ttu-id="1e2b2-151">Project Online unterstützt darüber hinaus lokale benutzerdefinierte Felder als nur-Lese-Entitäten, die speziell für die bestimmten Projekt, Ressource oder Vorgang.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-151">Additionally, Project Online supports local custom fields as read-only entities specific to the specific project, resource, or task.</span></span> <span data-ttu-id="1e2b2-152">Weitere Informationen über lokale benutzerdefinierte Felder, finden Sie im Beispiel https://github.com/OfficeDev/Project-CSOM-Read-Local-CustomFields\.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-152">For more information on local custom fields, see the sample https://github.com/OfficeDev/Project-CSOM-Read-Local-CustomFields\.</span></span>
  
## <a name="background-materials"></a><span data-ttu-id="1e2b2-153">Hintergrund Materialien (engl.)</span><span class="sxs-lookup"><span data-stu-id="1e2b2-153">Background materials</span></span>

<span data-ttu-id="1e2b2-154">[Entwickeln einer Project Online-Anwendung mit dem clientseitigen Objektmodell](developing-a-project-online-application-using-the-client-side-object-model.md), ein vorherigen Artikel bietet Hintergrundinformationen und die ursprüngliche Ausrichtung für die Entwicklung von Anwendungen mit CSOM.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-154">A previous article, [Developing a Project Online application using the client-side object model](developing-a-project-online-application-using-the-client-side-object-model.md), provides background and the initial orientation for developing applications using CSOM.</span></span> <span data-ttu-id="1e2b2-155">Finden Sie in diesem Artikel finden Sie die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="1e2b2-155">Refer to this article for the following items:</span></span>
  
- <span data-ttu-id="1e2b2-156">Hintergrundinformationen zu Project, eigenständigen und Cloud-basierte Versionen</span><span class="sxs-lookup"><span data-stu-id="1e2b2-156">Background information about Project, stand-alone and cloud-based editions</span></span> 
    
- <span data-ttu-id="1e2b2-157">Entwicklungsumgebung (Visual Studio-Editionen und Softwarebibliotheken)</span><span class="sxs-lookup"><span data-stu-id="1e2b2-157">Development environment (Visual Studio editions and software libraries)</span></span>
    
- <span data-ttu-id="1e2b2-158">Visual Studio-Projekt-Setup für eine mithilfe der CSOM-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1e2b2-158">Visual Studio project setup for a .NET application using the CSOM library</span></span>
    
- <span data-ttu-id="1e2b2-159">Herstellen einer Verbindung mit Project Online-Dienst</span><span class="sxs-lookup"><span data-stu-id="1e2b2-159">Connecting to the Project Online service</span></span>
    
## <a name="preliminaries-class-level-declarations"></a><span data-ttu-id="1e2b2-160">Hinweise (auf Klassenebene Deklarationen)</span><span class="sxs-lookup"><span data-stu-id="1e2b2-160">Preliminaries (class-level declarations)</span></span>

<span data-ttu-id="1e2b2-161">Die Klasse für diese Anwendung definiert zwei Datenelemente: der Projektkontext und das PwaECF Wörterbuch.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-161">The class for this application defines two data items: the project context and the pwaECF dictionary.</span></span>
  
<span data-ttu-id="1e2b2-162">Das Projekt Context-Objekt ist Teil der Project-CSOM und verbindet die Anwendung und die PWA-Instanz.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-162">The project context object is part of the Project CSOM, and connects the application and the PWA instance.</span></span> <span data-ttu-id="1e2b2-163">Alle Anfragen an den Dienst verwenden den Projektkontext.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-163">All requests to the service use the project context.</span></span>
  
```cs
private static ProjectContext projContext = 
     new ProjectContext("https://Contoso216.sharepoint.com/sites/pwa");

```

<span data-ttu-id="1e2b2-164">Der Kontext benötigt den Verbindungsendpunkt zum Erstellen einer Instanz in einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-164">The context needs the connection endpoint to create an instance in an application.</span></span> <span data-ttu-id="1e2b2-165">Der Verbindungsendpunkt ist die URL der PWA-Instanz.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-165">The connection endpoint is the URL of your PWA instance.</span></span> 
  
<span data-ttu-id="1e2b2-166">Das Wörterbuch PwaECF speichert das Projekt, die auf der PWA-Ebene ECFs definiert haben.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-166">The pwaECF dictionary stores the project ECFs defined at the PWA level.</span></span> <span data-ttu-id="1e2b2-167">Das Wörterbuch verwendet die ECF. InternalName als Schlüssel und das benutzerdefiniertes Objekt als Wert.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-167">The dictionary uses the ECF.InternalName as the key, and the CustomField object as the value.</span></span> <span data-ttu-id="1e2b2-168">Das Wörterbuch ist in der ListPWACustomFields-Methode aufgefüllt und dann als einen Verweis in der Main-Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-168">The dictionary is populated in the ListPWACustomFields method, and then used as a reference in the Main method.</span></span> 
  
```cs
    //Dictionary of ECFs
        static Dictionary<String, CustomField> pwaECF = new Dictionary<string, CustomField>();

```

## <a name="main-method"></a><span data-ttu-id="1e2b2-169">Main-Methode</span><span class="sxs-lookup"><span data-stu-id="1e2b2-169">Main method</span></span>

<span data-ttu-id="1e2b2-170">Die Main-Methode verwaltet den Ablauf der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-170">The Main method manages the application flow.</span></span> <span data-ttu-id="1e2b2-171">Als initialisiert Main mit einer anderen Anwendung, die die Project Online-CSOM verwenden den Projekt-Kontext.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-171">As with other applications that use the Project Online CSOM, Main initializes the project context.</span></span> 
  
1. <span data-ttu-id="1e2b2-172">Rufen Sie ab und Listen Sie der ECFs in Project Online PWA auf.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-172">Retrieve and list the ECFs in the Project Online PWA.</span></span>
    
   <span data-ttu-id="1e2b2-173">Diese Funktionalität ist in der ListPWACustomFields-Methode implementiert.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-173">This functionality is implemented in the ListPWACustomFields method.</span></span>
    
2. <span data-ttu-id="1e2b2-174">Projekte mit benutzerdefinierten Feldern und nicht benutzerdefinierten Felder abrufen.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-174">Retrieve projects with custom fields and non-custom fields.</span></span>
    
   <span data-ttu-id="1e2b2-175">Beim Abrufen von Projekten mit ECFs muss der abfrageanforderung mit dem Project Online-Dienst die folgenden Elemente enthalten:</span><span class="sxs-lookup"><span data-stu-id="1e2b2-175">When retrieving projects with ECFs, the query request to the Project Online service needs to include the following items:</span></span> 
    
   - <span data-ttu-id="1e2b2-176">**IncludeCustomFields** &ndash; Dieses Element fordert den Dienst aus, um eine Auflistung von PublishedProjects zurückzugeben, wobei jedes veröffentlichtes Projekt enthält eine Erweiterung, die benutzerdefinierte Felder unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-176">**IncludeCustomFields** &ndash; This item requests the service to return a collection of PublishedProjects where each published project includes an extension that supports custom fields.</span></span> <span data-ttu-id="1e2b2-177">Wenn dieses Element angegeben ist, gibt Project Online PublishedProject-Objekte, die keine benutzerdefinierten Felddaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-177">Unless this item is specified, Project Online returns PublishedProject objects that do not include Custom Field data.</span></span>
    
   - <span data-ttu-id="1e2b2-178">**IncludeCustomFields.CustomFields** &ndash; dieses Element fordert den Dienst auf die Objekte PublishedProject mit CustomFields Daten auffüllen.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-178">**IncludeCustomFields.CustomFields** &ndash; This item requests the service to populate the PublishedProject objects with CustomFields data.</span></span>
    
   <span data-ttu-id="1e2b2-179">Die folgende Anforderung gibt an, das Projekt-Id und Name, als auch die Objekt-Erweiterung für benutzerdefinierte Felder und die Werte für benutzerdefinierte Felder.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-179">The following request specifies the project Id and Name, as well as the object extension for custom fields and the custom field values.</span></span>
    
   ```cs
        var projBlk = projContext.LoadQuery(
        projContext.Projects.Include(
            p => p.Id, 
            p => p.Name,
            p => p.IncludeCustomFields,
            p => p.IncludeCustomFields.CustomFields
        ));
    
   ```

3. <span data-ttu-id="1e2b2-180">Untersuchen Sie jedes Projekt.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-180">Examine each project.</span></span>
    
   <span data-ttu-id="1e2b2-181">Projektobjekte, die in dieser Anwendung verwendet werden der Typ PublishedProject, da die Werte abgerufen und angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-181">The project objects used in this application are the PublishedProject type because the values are retrieved and displayed.</span></span> 
    
   <span data-ttu-id="1e2b2-182">Wenn Sie Datenwerte in einem oder mehreren Projekten aktualisieren müssen, würde das Projekt, das Update momentan ausgecheckt werden, und die Anwendung würde ein DraftProject-Objekt verwenden, um die Werte abzurufen und aktualisieren Sie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-182">If you need to update data values in one or more projects, the project undergoing the update would be checked out and the application would use a DraftProject object to retrieve the values and update the project.</span></span>
    
4. <span data-ttu-id="1e2b2-183">Zugreifen auf die ECF-Einträge für ein Projekt</span><span class="sxs-lookup"><span data-stu-id="1e2b2-183">Accessing the ECF entries for a project</span></span>
    
   <span data-ttu-id="1e2b2-184">Jede Instanz ECF trennt den Wert des Felds von der restlichen ECF Informationen.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-184">Each ECF instance separates the field value from the rest of the ECF information.</span></span> <span data-ttu-id="1e2b2-185">Der Wert des Felds wird als Teil der Schlüssel/Wert-Paar gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-185">The field value is stored as part of a key/value pair.</span></span> <span data-ttu-id="1e2b2-186">Die restlichen Informationen werden in ein benutzerdefiniertes Objekt gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-186">The rest of the information is stored in a CustomField object.</span></span>
    
   <span data-ttu-id="1e2b2-187">Zugreifen auf die Werte in einem Projekt ECF besteht aus zwei Teilen:</span><span class="sxs-lookup"><span data-stu-id="1e2b2-187">Accessing ECF values in a project consists of two parts:</span></span>
    
   - <span data-ttu-id="1e2b2-188">Durchlaufen der Auflistung CustomFields</span><span class="sxs-lookup"><span data-stu-id="1e2b2-188">Cycling through the CustomFields collection</span></span>
    
   - <span data-ttu-id="1e2b2-189">Zugreifen auf den entsprechenden Eintrag mit zwei Konstrukte.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-189">Accessing the proper entry using two constructs.</span></span>
    
   <span data-ttu-id="1e2b2-190">Jedes Projekt zugeordneten ECF Einträge an zwei Stellen, eine CustomFields-Auflistung, die aufzählbare wird gespeichert und und die Feldwerte im Rahmen der Schlüssel/Wert-Paare.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-190">Each project stores associated ECF entries in two places, a CustomFields collection that is enumerable and and the field values as part of key/value pairs.</span></span> <span data-ttu-id="1e2b2-191">In der Schlüssel/Wert-Paaren die InternalName ist der Schlüssel und der Wert des Felds ist der Wert.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-191">In the key/value pairs, the internalName is the key and the field value is the value.</span></span> <span data-ttu-id="1e2b2-192">Verwenden eines Wörterbuchs halten und auf die Feldwerte zugreifen.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-192">Use a dictionary to hold and access the field values.</span></span> 
    
   <span data-ttu-id="1e2b2-193">Die Eigenschaften ECF als die Feldwerte werden in benutzerdefiniertes-Objekten, ein Objekt pro Projekt gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-193">The ECF properties, other than the field values, are stored in CustomField objects, one object per project.</span></span> <span data-ttu-id="1e2b2-194">Verwenden Sie eine CustomFields-Auflistung, um die einzelnen Projekten zugeordneten ECFs zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-194">Use a CustomFields collection to access the ECFs associated with an individual project.</span></span> 
    
5. <span data-ttu-id="1e2b2-195">Jedes Projekt speichert die zugeordneten ECFs in einer Auflistung, in dem jeder Eintrag ECF besteht aus einem Schlüssel – den internen Namen der ECF – sowie ein Objekt, das den Wert für die ECF enthält.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-195">Each project stores the associated ECFs in a collection where each ECF entry consists of a key--the internal name of the ECF--and an object that holds the value of the ECF.</span></span> <span data-ttu-id="1e2b2-196">Übertragen der Auflistung in ein Wörterbuch auf einzelne Einträge zugreifen.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-196">Transfer the collection to a dictionary to access individual entries.</span></span> <span data-ttu-id="1e2b2-197">Die Deklaration folgt.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-197">The declaration follows.</span></span>
    
   ```cs
    Dictionary<string, object> projDict = pubProj.IncludeCustomFields.FieldValues;
    
   ```

   <span data-ttu-id="1e2b2-198">Der Wert in einen Wörterbucheintrag entspricht den Datentyp der ECF.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-198">The value in a dictionary entry corresponds to the data type of the ECF.</span></span> <span data-ttu-id="1e2b2-199">Das Objekt für jede ECF ordnet einer der verschiedenen Typen.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-199">The object for each ECF maps to one of a variety of types.</span></span> <span data-ttu-id="1e2b2-200">Die meisten ECFs verwenden einfache Typen, die in den Standardvariablen passen.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-200">Most ECFs use simple types that fit into standard variables.</span></span> <span data-ttu-id="1e2b2-201">Das folgende Schemafragment zeigt, dass die minimale Verarbeitung für verschiedene beteiligt ist:</span><span class="sxs-lookup"><span data-stu-id="1e2b2-201">The following fragment shows that minimal processing is involved for several types:</span></span>
    
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

   <span data-ttu-id="1e2b2-202">Die Nachschlagetabelle mit Textwerten, erfordert jedoch die weitere Verarbeitung weiterleitet.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-202">The lookup table of TEXT values, however, requires additional processing.</span></span> <span data-ttu-id="1e2b2-203">Die Anwendung die entsprechenden Nachschlagetabelle vom Dienst abgerufen, und gibt die Instanz ECF (mit einem oder mehreren Werten) durch Durchlaufen der Nachschlagetabelle.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-203">The application retrieves the appropriate lookup table from the service, and outputs the ECF instance (with single or multiple values) by traversing the lookup table.</span></span> <span data-ttu-id="1e2b2-204">Im folgenden Codefragment zeigt die Verarbeitung von TEXT ECFs, einschließlich derjenigen mit einfachen-Werten und Nachschlagetabellen verwenden:</span><span class="sxs-lookup"><span data-stu-id="1e2b2-204">The following code fragment shows processing of TEXT ECFs, including those with simple values and those using lookup tables:</span></span> 
    
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

   <span data-ttu-id="1e2b2-205">Diese Anwendung gibt einfach die Werte; Es ist jedoch möglich, weitere Bedeutung aus der Daten Werte abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-205">This application simply outputs the value(s); however, it is possible to get more meaning from the data value(s).</span></span>
    
## <a name="listpwacustomfields"></a><span data-ttu-id="1e2b2-206">ListPWACustomFields</span><span class="sxs-lookup"><span data-stu-id="1e2b2-206">ListPWACustomFields</span></span>

<span data-ttu-id="1e2b2-207">Die Methode ListPWACustomFields abgerufen und die ECFs Projekten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-207">The ListPWACustomFields method retrieves and lists the ECFs associated with projects.</span></span> <span data-ttu-id="1e2b2-208">Diese Methode enthält die ECFs registriert auf der PWA-Instanz, die einzelnen Projekte zugeordnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-208">This method lists the ECFs registered on the PWA instance that can be associated with individual projects.</span></span> <span data-ttu-id="1e2b2-209">Der Einstiegspunkt für den Zugriff auf die ECFs wird das CustomFields-Element des Projektkontexts, wie in der folgenden abfrageanforderung verwendet:</span><span class="sxs-lookup"><span data-stu-id="1e2b2-209">The entry point for accessing the ECFs uses the CustomFields element of the project context, as in the following query request:</span></span>
  
```cs
// Project ECFs
    var allECFields = 
            projContext.LoadQuery(projContext.CustomFields.Include(
            qp => qp.InternalName,
            qp => qp.Name
        ));
    projContext.ExecuteQuery();

```

<span data-ttu-id="1e2b2-210">Die Methode wird nicht überprüft, um festzustellen, ob ein Projekt mit einer bestimmten ECF verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1e2b2-210">The method does not check to see whether a project uses a specific ECF.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1e2b2-211">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e2b2-211">See also</span></span>

- [<span data-ttu-id="1e2b2-212">Project-Entwicklung-Portal</span><span class="sxs-lookup"><span data-stu-id="1e2b2-212">Project Development Portal</span></span>](http://dev.office.com/project.aspx)
- [<span data-ttu-id="1e2b2-213">Übersicht: Benutzerdefinierte Enterprise-Felder und Nachschlagetabellen</span><span class="sxs-lookup"><span data-stu-id="1e2b2-213">Overview: Enterprise custom fields and lookup tables</span></span>](https://support.office.com/en-us/article/overview-enterprise-custom-fields-and-lookup-tables-f99db553-0b33-4648-93c0-f6a74637d790?ui=en-us&rs=en-us&ad=us)
- <span data-ttu-id="1e2b2-214">[Lokale und benutzerdefinierte Enterprise-Felder](https://msdn.microsoft.com/en-us/library/office/ms447495(v=office.14).aspx)</span><span class="sxs-lookup"><span data-stu-id="1e2b2-214">[Local and Enterprise Custom Fields](https://msdn.microsoft.com/en-us/library/office/ms447495(v=office.14).aspx)</span></span>
- [<span data-ttu-id="1e2b2-215">Hinzufügen oder Bearbeiten von benutzerdefinierten Enterprise-Felder in Project Server 2013</span><span class="sxs-lookup"><span data-stu-id="1e2b2-215">Add or edit enterprise custom fields in Project Server 2013</span></span>](https://docs.microsoft.com/en-us/project/add-or-edit-enterprise-custom-fields-in-project-server)
    

