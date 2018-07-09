---
title: Project-Programmieraufgaben
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: ac5544e7-ff7a-4af5-ac1b-33a49bc6be0d
description: Dieser Abschnitt enthält außerdem-Toarticles, die zeigen, wie Sie die JavaScript-Bibliothek für das clientseitige Objektmodell (CSOM) verwenden, und führen andere Programmieraufgaben für Project Server 2013 und Project Online. Beispiele für Programmieraufgaben sind Erstellen einer Project Server in SharePoint gehostete app, Erstellen von Workflows für das bedarfsmanagement; Programmieren von Project Server-Anwendungen mit Windows Communication Foundation (WCF); Anpassen des Menübands von Project Web App; Erstellen von Project Server-Webparts Erstellen von Project Server-Ereignishandler und remoteereignisempfänger; und Massen Aktualisieren von benutzerdefinierten Feldern und Erstellen von Projektwebsites für Project Online.
ms.openlocfilehash: 79ff301b825b4eea073d5d1896e27be9e0090ba6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796304"
---
# <a name="project-programming-tasks"></a><span data-ttu-id="f8599-104">Project-Programmieraufgaben</span><span class="sxs-lookup"><span data-stu-id="f8599-104">Project programming tasks</span></span>

<span data-ttu-id="f8599-105">Dieser Abschnitt enthält einige "Gewusst wie" Artikel, die zeigen, wie Sie die JavaScript-Bibliothek für das clientseitige Objektmodell (CSOM) verwenden, und führen andere Programmieraufgaben für Project Server 2013 und Project Online.</span><span class="sxs-lookup"><span data-stu-id="f8599-105">This section includes some "how-to" articles that show how to use the JavaScript library for the client-side object model (CSOM), and perform other programming tasks for Project Server 2013 and Project Online.</span></span> <span data-ttu-id="f8599-106">Beispiele für Programmieraufgaben sind Erstellen einer Project Server in SharePoint gehostete app, Erstellen von Workflows für das bedarfsmanagement; Programmieren von Project Server-Anwendungen mit Windows Communication Foundation (WCF); Anpassen des Menübands von Project Web App; Erstellen von Project Server-Webparts Erstellen von Project Server-Ereignishandler und remoteereignisempfänger; und Massen Aktualisieren von benutzerdefinierten Feldern und Erstellen von Projektwebsites für Project Online.</span><span class="sxs-lookup"><span data-stu-id="f8599-106">Examples of programming tasks include creating a SharePoint-hosted Project Server app, creating workflows for demand management; programming Project Server applications with the Windows Communication Foundation (WCF); customizing the Project Web App ribbon; creating Project Server Web Parts; creating Project Server event handlers and remote event receivers; and bulk updating custom fields and creating project sites for Project Online.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f8599-107">Informationen zum Programmieren mit der JS Grid-Steuerelement finden Sie unter [JS Grid-Steuerelement](http://msdn.microsoft.com/de-de/library/ee535898%28office.14%29.aspx) in der SharePoint 2010-Entwicklerreferenz.</span><span class="sxs-lookup"><span data-stu-id="f8599-107">For information about programming with the JS Grid control, see [JS Grid Control](http://msdn.microsoft.com/de-de/library/ee535898%28office.14%29.aspx) in the SharePoint 2010 developer reference.</span></span> <span data-ttu-id="f8599-108">Der Verweis verwaltetem Code finden Sie unter [Microsoft.SharePoint.JSGrid-Namespace](http://msdn.microsoft.com/de-de/library/microsoft.sharepoint.jsgrid%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="f8599-108">For the managed code reference, see [Microsoft.SharePoint.JSGrid Namespace](http://msdn.microsoft.com/de-de/library/microsoft.sharepoint.jsgrid%28Office.15%29.aspx).</span></span> <span data-ttu-id="f8599-109">Die Websteuerelemente JS Grid-Steuerelement finden Sie unter [JSGrid-Klasse](http://msdn.microsoft.com/de-de/library/microsoft.sharepoint.webcontrols.jsgrid%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="f8599-109">For the JS Grid control web controls, see [JSGrid class](http://msdn.microsoft.com/de-de/library/microsoft.sharepoint.webcontrols.jsgrid%28Office.15%29.aspx).</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="f8599-110">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="f8599-110">In this section</span></span>

[<span data-ttu-id="f8599-111">Erste Schritte beim Entwickeln von Project Server-workflows</span><span class="sxs-lookup"><span data-stu-id="f8599-111">Getting started developing Project Server workflows</span></span>](getting-started-developing-project-server-workflows.md)
  
[<span data-ttu-id="f8599-112">Massen-Update für benutzerdefinierte Felder und Erstellen von Projektwebsites in einem Workflow in Project Online</span><span class="sxs-lookup"><span data-stu-id="f8599-112">Bulk update custom fields and create project sites from a workflow in Project Online</span></span>](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)
  
[<span data-ttu-id="f8599-113">Erstellen, abrufen, aktualisieren und Löschen von Projekten mit dem Project Server-JavaScript-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="f8599-113">Create, retrieve, update, and delete projects by using the Project Server JavaScript object model</span></span>](create-retrieve-update-delete-projects-using-project-server-javascript.md)
  
<span data-ttu-id="f8599-114">[Erstellen einer SharePoint gehosteten Project Server-add-in](create-a-sharepoint-hosted-project-server-add-in.md) : enthält den Abschnitt zum Ändern der Project Web App-Multifunktionsleiste</span><span class="sxs-lookup"><span data-stu-id="f8599-114">[Create a SharePoint-hosted Project Server add-in](create-a-sharepoint-hosted-project-server-add-in.md) : includes a section on how to modify the Project Web App ribbon</span></span> 
  
## <a name="reference"></a><span data-ttu-id="f8599-115">Referenz</span><span class="sxs-lookup"><span data-stu-id="f8599-115">Reference</span></span>

[<span data-ttu-id="f8599-116">Übersicht über Project PSI-Verweis</span><span class="sxs-lookup"><span data-stu-id="f8599-116">Project PSI reference overview</span></span>](project-psi-reference-overview.md)
  
## <a name="see-also"></a><span data-ttu-id="f8599-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8599-117">See also</span></span>



[<span data-ttu-id="f8599-118">Client-seitigen Objektmodell (CSOM) für Project 2013</span><span class="sxs-lookup"><span data-stu-id="f8599-118">Client-side object model (CSOM) for Project 2013</span></span>](client-side-object-model-csom-for-project-2013.md)

