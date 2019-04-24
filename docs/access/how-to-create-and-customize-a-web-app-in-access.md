---
title: Erstellen und Anpassen einer Web-App in Access
manager: kelbow
ms.date: 08/18/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: 628745f4-82e9-4838-9726-6f3e506a654f
localization_priority: Priority
ms.openlocfilehash: d7d27e98189a5b6784e4db48c81a545b85f01fc1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306119"
---
# <a name="create-and-customize-a-web-app-in-access"></a><span data-ttu-id="eecda-102">Erstellen und Anpassen einer Web-App in Access</span><span class="sxs-lookup"><span data-stu-id="eecda-102">Create and customize a web app in Access</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eecda-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/de-DE/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="eecda-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/de-DE/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
<span data-ttu-id="eecda-p102">Access 2013 umfasst ein neues Anwendungsmodell, das Experten das schnelle Erstellen webbasierter Anwendungen ermöglicht. In Access sind eine Reihe an Vorlagen enthalten, die Sie für den schnellen Einstieg beim Erstellen Ihrer Anwendung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="eecda-p102">Access 2013 features a new application model that enables subject matter experts to quickly create web-based applications. Included with Access are a set of templates that you can use to jump start creating your application.</span></span>

<span data-ttu-id="eecda-107"><a name="ac15_CreateAndCustomizeWebApp_Prerequisites"> </a></span><span class="sxs-lookup"><span data-stu-id="eecda-107"></span></span>

## <a name="prerequisites-for-building-an-app-with-access-2013"></a><span data-ttu-id="eecda-108">Voraussetzungen für das Erstellen einer App mit Access 2013</span><span class="sxs-lookup"><span data-stu-id="eecda-108">Prerequisites for building an app with Access 2013</span></span>

<span data-ttu-id="eecda-109">Um die Schritte in diesem Beispiel auszuführen, benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="eecda-109">To follow the steps in this example, you need the following:</span></span>
  
- <span data-ttu-id="eecda-110">Access</span><span class="sxs-lookup"><span data-stu-id="eecda-110">Access</span></span>
    
- <span data-ttu-id="eecda-111">Eine SharePoint-Entwicklungsumgebung</span><span class="sxs-lookup"><span data-stu-id="eecda-111">A SharePoint development environment</span></span>
    
<span data-ttu-id="eecda-112">Weitere Informationen über das Einrichten Ihrer SharePoint-Entwicklungsumgebung finden Sie unter [Einrichten einer allgemeinen Entwicklungsumgebung für SharePoint](https://docs.microsoft.com/sharepoint/dev/general-development/set-up-a-general-development-environment-for-sharepoint).</span><span class="sxs-lookup"><span data-stu-id="eecda-112">For more information about setting up your SharePoint development environment, see [Set up a general development environment for SharePoint](https://docs.microsoft.com/sharepoint/dev/general-development/set-up-a-general-development-environment-for-sharepoint).</span></span> 
  
<span data-ttu-id="eecda-113">Weitere Informationen über das Abrufen von Access und SharePoint finden Sie unter [Downloads](https://msdn.microsoft.com/office/apps/fp123627).</span><span class="sxs-lookup"><span data-stu-id="eecda-113">For more information about obtaining Access and SharePoint, see [Downloads](https://msdn.microsoft.com/office/apps/fp123627).</span></span>

<span data-ttu-id="eecda-114"><a name="ac15_CreateAndCustomizeWebApp_CreateTheApp"> </a></span><span class="sxs-lookup"><span data-stu-id="eecda-114"></span></span>

## <a name="create-the-app"></a><span data-ttu-id="eecda-115">Erstellen der App</span><span class="sxs-lookup"><span data-stu-id="eecda-115">Create the app</span></span>

<span data-ttu-id="eecda-p103">Angenommen, Sie möchten eine Access-App erstellen, die Probleme für Ihr Unternehmen verfolgt. Bevor Sie mit dem Erstellen der Tabellen und Ansicht von Grund auf beginnen, sollten Sie nach einer Schemavorlage suchen, die Ihre Anforderungen erfüllt.</span><span class="sxs-lookup"><span data-stu-id="eecda-p103">Suppose you want to create an Access app that tracks issues for your business. Before you start creating the tables and view from scratch, you should search for a schema template that meets your needs.</span></span>
  
### <a name="to-create-the-issue-tracking-app"></a><span data-ttu-id="eecda-118">So erstellen Sie die Problemverfolgungs-App</span><span class="sxs-lookup"><span data-stu-id="eecda-118">To create the issue tracking app</span></span>

1. <span data-ttu-id="eecda-119">Öffnen Sie Access, und wählen Sie **Benutzerdefinierte Web App** aus.</span><span class="sxs-lookup"><span data-stu-id="eecda-119">Open Access and choose **Custom web app**.</span></span>
    
2. <span data-ttu-id="eecda-p104">Geben Sie einen Namen und den Webspeicherort für Ihre App ein. Sie können auch einen Speicherort aus der Liste **Speicherorte** und **Erstellen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="eecda-p104">Enter a name and the web location for your app. You can also choose a location from the **Locations** list and choose **Create**.</span></span>
    
3. <span data-ttu-id="eecda-122">Geben Sie **Probleme** in das Feld **Was möchten Sie verfolgen?** ein, und drücken Sie dann die EINGABETASTE.</span><span class="sxs-lookup"><span data-stu-id="eecda-122">Type **Issues** into the **What would you like to track?** box and then press ENTER.</span></span> 
    
   <span data-ttu-id="eecda-123">Eine Liste der Vorlagen, die für die Problemverfolgung möglicherweise nützlich sind, wird in Abbildung 1 dargestellt.</span><span class="sxs-lookup"><span data-stu-id="eecda-123">A list of templates that might be useful for tracking issues is displayed in Figure 1.</span></span>
    
   <span data-ttu-id="eecda-124">**Abbildung 1. Vorlagen für die Problemverfolgung**</span><span class="sxs-lookup"><span data-stu-id="eecda-124">**Figure 1. Templates that match the search for issues**</span></span>

   <span data-ttu-id="eecda-125">![Vorlagen für die Problemverfolgung](media/odc_Access15_CreateAndCustomizeWebApp_Figure01.JPG "Vorlagen für die Problemverfolgung")</span><span class="sxs-lookup"><span data-stu-id="eecda-125">![Templates that match the search for issues](media/odc_Access15_CreateAndCustomizeWebApp_Figure01.JPG "Templates that match the search for issues")</span></span>
  
4. <span data-ttu-id="eecda-126">Wählen Sie **Probleme** aus.</span><span class="sxs-lookup"><span data-stu-id="eecda-126">Choose **Issues**.</span></span>
    
<span data-ttu-id="eecda-127">Access erstellt einen Satz an Tabellen und Ansichten.</span><span class="sxs-lookup"><span data-stu-id="eecda-127">Access creates a set of tables and views.</span></span>
  
## <a name="explore-the-app"></a><span data-ttu-id="eecda-128">Untersuchen der App</span><span class="sxs-lookup"><span data-stu-id="eecda-128">Explore the app</span></span>
<span data-ttu-id="eecda-129"><a name="ac15_CreateAndCustomizeWebApp_ExploreTheApp"> </a></span><span class="sxs-lookup"><span data-stu-id="eecda-129"></span></span>

<span data-ttu-id="eecda-130">Damit Sie verstehen, ob das Schema und die Ansichten Ihre Anforderungen erfüllen, sollten Sie sie prüfen.</span><span class="sxs-lookup"><span data-stu-id="eecda-130">To understand whether the schema and views meet your needs, you should examine them.</span></span>
  
<span data-ttu-id="eecda-p105">Die durch Auswahl des Schemas für Probleme erstellten Tabellen werden im Kachelbereich angezeigt. Die Tabellen „Probleme“, „Kunde“ und „Mitarbeiter“ bilden den Schwerpunkt der App. In der Tabelle „Probleme“ sind Informationen über jedes Problem gespeichert. Jedes Problem wird durch einen Mitarbeiter geöffnet und auf Veranlassung eines Kunden einem Mitarbeiter zugewiesen. Die Tabellen „Verwandte Probleme“ und „Problemberichte“ spielen eine unterstützende Rolle in der App. Die Tabelle „Verwandte Probleme“ ermöglicht Ihnen, ein Problem mit einem anderen zu verknüpfen. Die Tabelle „Problemberichte“ speichert mehrere Kommentare für ein einzelnes Problem.</span><span class="sxs-lookup"><span data-stu-id="eecda-p105">The tables created by selecting the Issues schema are displayed in the Tile Pane. The Issues, Customer, and Employees tables are the main focus of the app. The Issues table stores information about each issue. Each issue is opened by and assigned to an employee on behalf of a customer. The Related Issues and Issue Comments tables play a supporting role in the app. The Related Issues table enables you to link one issue to another. The Issue Comments table stores multiple comments for a single issue.</span></span>
  
<span data-ttu-id="eecda-p106">In einer Access-Desktop-PC-Datenbank (.accdb) werden die Beziehungen zwischen Tabellen im Fenster **Beziehungen** verwaltet. Access 2013-Apps verwalten Beziehungen durch die Verwendung von Feldern, die auf den Datentyp **Nachschlagen** festgelegt sind. Im Folgenden überprüfen wir die Beziehungen für die Tabelle „Probleme", indem wir mit der rechten Maustaste auf die Kachel **Probleme** klicken und **Tabelle bearbeiten** auswählen.</span><span class="sxs-lookup"><span data-stu-id="eecda-p106">In an Access desktop (.accdb) database, the relationships between tables are managed in the **Relationships** window. Access 2013 apps manage relationships by using fields set to the **Lookup** data type. Let's examine the relationships for the Issues table by right-clicking the **Issues** tile and selecting **Edit Table**.</span></span>
  
<span data-ttu-id="eecda-p107">Das Feld **Kunde** steht im Zusammenhang mit der Tabelle **Kunden**. Wählen Sie zum Überprüfen der Beziehung das Feld **Kunde** und dann die Option zum Ändern der Nachschlagefunktion aus. Der Nachschlage-Assistent wird analog zur Darstellung in Abbildung 2 angezeigt.</span><span class="sxs-lookup"><span data-stu-id="eecda-p107">The **Customer** field is related to the **Customers** table. To examine the relationship, select the **Customer** field and then select **Modify Lookups**. The **Lookup Wizard** is displayed, as shown in Figure 2.</span></span> 
  
<span data-ttu-id="eecda-144">**Abbildung 2. Der die Beziehung zur Tabelle „Kunden“ anzeigende Nachschlage-Assistent**</span><span class="sxs-lookup"><span data-stu-id="eecda-144">**Figure 2. Lookup Wizard displaying the relationship to the Customers table**</span></span>

<span data-ttu-id="eecda-145">![Nachschlage-Assistent zeigt die Beziehung an](media/odc_Access15_CreateAndCustomizeWebApp_Figure02.jpg "Nachschlage-Assistenten zeigt die Beziehung an")</span><span class="sxs-lookup"><span data-stu-id="eecda-145">![Lookup Wizard displaying the relationship](media/odc_Access15_CreateAndCustomizeWebApp_Figure02.jpg "Lookup Wizard displaying the relationship")</span></span>
  
<span data-ttu-id="eecda-146">Das Dialogfeld „Nachschlage-Assistent" zeigt, dass das Feld **Kunde** mit der Tabelle **Kunden** verknüpft ist und dass **Anzeigename Vorname Nachname** von der Tabelle **Kunden** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="eecda-146">The Lookup Wizard dialog box shows that the **Customer** field is linked to the **Customers** table and to return the **Display Name First Last** field from the **Customers** table.</span></span> 
  
<span data-ttu-id="eecda-p108">Die Felder **Geöffnet von**, **Zugewiesen an** und **Geändert von** stehen mit der Tabelle **Mitarbeiter** im Zusammenhang. Verschiedene andere Felder sind auch auf den Datentyp **Nachschlagen** festgelegt. In diesen Fällen wird der Datentyp „Nachschlagen" zum Angeben bestimmter, im Feld zulässiger Werte verwendet.</span><span class="sxs-lookup"><span data-stu-id="eecda-p108">The **Opened By**, **Assigned To**, and **Changed By** fields are related to the **Employees** table. Several other fields are also set to the **Lookup** data type. In these cases, the Lookup data type is used to specify the specific values to allow for in the field.</span></span> 
  
<span data-ttu-id="eecda-p109">Schließen Sie die Tabelle **Probleme**, und überprüfen Sie den Kachelbereich. Die oberen drei Kacheln für die Tabellen **Probleme**, **Kunden** und **Mitarbeiter** werden analog zur Darstellung in Abbildung 3 anders dargestellt als die unteren zwei Kacheln für die Tabellen **Verwandte Probleme** und **Problemberichte**.</span><span class="sxs-lookup"><span data-stu-id="eecda-p109">Close the **Issues** table and examine the Tile Pane. The top three tiles, for the **Issues**, **Customers**, and **Employees** tables, are displayed differently than the bottom two tiles for the **Related Issues** and **Issue Comments** table, as shown in Figure 3.</span></span> 
  
<span data-ttu-id="eecda-152">**Abbildung 3. Kachelbereich für das Schema „Probleme“**</span><span class="sxs-lookup"><span data-stu-id="eecda-152">**Figure 3. Tile Pane for the Issues schema**</span></span>

<span data-ttu-id="eecda-153">![Kachelbereich für das Schema „Probleme“](media/odc_Access15_CreateAndCustomizeWebApp_Figure03.jpg "Kachelbereich für das Schema „Probleme“")</span><span class="sxs-lookup"><span data-stu-id="eecda-153">![Tile Pane for the Issues schema](media/odc_Access15_CreateAndCustomizeWebApp_Figure03.jpg "Tile Pane for the Issues schema")</span></span>
  
<span data-ttu-id="eecda-154">Die Tabellen **Verwandte Probleme** und **Problemberichte** sind abgeblendet, da sie dem Benutzer im Webbrowser nicht angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="eecda-154">The **Related Issues** and **Issue Comments** tables are dimmed because they are to be hidden from the user in the web browser.</span></span> 
  
<span data-ttu-id="eecda-p110">Wir verwenden die App nun zum Verfolgen einiger Probleme. Klicken Sie dafür auf **App starten** zum Öffnen der App in Ihrem Webbrowser.</span><span class="sxs-lookup"><span data-stu-id="eecda-p110">Let's use the app to track some issues. To do this, click **Launch App** to open the app in your web browser.</span></span> 
  
<span data-ttu-id="eecda-p111">Die App öffnet die Ansicht **Problemliste** der Tabelle „Probleme". Vor dem Hinzufügen eines Problems empfiehlt es sich, einige Kunden und Mitarbeiter hinzuzufügen. Klicken Sie auf die Kachel **Kunden** zum Hinzufügen von Kunden.</span><span class="sxs-lookup"><span data-stu-id="eecda-p111">The app opens the **Issues List** view of the Issues table. Before adding an issue, it would be a good idea to add some customers and employees. Click the **Customers** tile to start adding customers.</span></span> 
  
<span data-ttu-id="eecda-160">Verwenden Sie die Ansichtsauswahl zum Auswählen einer der drei verfügbaren Ansichten für die Tabelle **Kunden**, die analog zur Darstellung in Abbildung 4 als **Liste**, **Datenblatt** und **Gruppen** bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="eecda-160">Use the View Selector to choose one of three views available for the **Customers** table, labeled **List**, **Datasheet**, and **Groups** as shown in Figure 4.</span></span> 
  
<span data-ttu-id="eecda-161">**Abbildung 4. Ansichtsauswahl**</span><span class="sxs-lookup"><span data-stu-id="eecda-161">**Figure 4. View Selector**</span></span>

<span data-ttu-id="eecda-162">![Ansichtsauswahl](media/odc_Access15_CreateAndCustomizeWebApp_Figure04.jpg "Ansichtsauswahl")</span><span class="sxs-lookup"><span data-stu-id="eecda-162">![View Selector](media/odc_Access15_CreateAndCustomizeWebApp_Figure04.jpg "View Selector")</span></span>
  
<span data-ttu-id="eecda-p112">Durch das Auswählen von **Liste** wird die Ansicht **Kundenliste** aktiviert, die eine Ansicht vom Typ „Detailinformationen" ist. „Detailinformationen" ist eine der durch Access automatisch generierten Ansichten, wenn Sie eine Tabelle erstellen. Das Hauptmerkmal einer Ansicht vom Typ „Detailinformationen" ist der Listenbereich, der im linken Bereich der Ansicht angezeigt wird. Der Listenbereich wird zum Filtern und Navigieren der in der Ansicht enthaltenen Datensätze verwendet. Für das Implementieren einer durchsuchbaren Liste in einer Access-Desktop-PC-Datenbank müsste benutzerdefinierter Code geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="eecda-p112">Choosing **List** activates the **Customers List** view, which is a List Details view. List Details is one of the views Access automatically generates when you create a table. The main feature that distinguishes a List Details view is the list pane that appears on the left side of the view. The list pane is used to filter and navigate the records contained in the view. In an Access desktop database, implementing a searchable list view would require writing custom code.</span></span> 
  
<span data-ttu-id="eecda-p113">Choosing **Datasheet** opens the **Customers Datasheet** view. Datasheet is the other kind of view Access automatically generates when you create a table. Datasheet views are useful for those who find it easier to enter, sort, and filter data in a spreadsheet-like manner.</span><span class="sxs-lookup"><span data-stu-id="eecda-p113">Choosing **Datasheet** opens the **Customers Datasheet** view. Datasheet is the other kind of view Access automatically generates when you create a table. Datasheet views are useful for those who find it easier to enter, sort, and filter data in a spreadsheet-like manner.</span></span> 
  
<span data-ttu-id="eecda-p114">Durch das Auswählen von „Gruppen“ wird eine Ansicht vom Typ „Zusammenfassung“ geöffnet. Ansichten vom Typ „Zusammenfassung“ können zum Gruppieren von Datensätzen auf Grundlage eines Felds und zum optionalen Berechnen einer Summe oder eines Mittelwerts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eecda-p114">Choosing Groups opens a Summary view. Summary views can be used to group records based on a field and optionally calculate a sum or average.</span></span>
  
<span data-ttu-id="eecda-p115">Verwenden Sie beim Hinzufügen von Kunden die Aktionsleiste zum Hinzufügen, Bearbeiten, Speichern, Löschen von Datensätzen und zum Abbrechen von Bearbeitungen. Bei der Aktionsleiste handelt es sich um eine anpassbare Symbolleiste, die analog zur Darstellung in Abbildung 5 in jeder Ansicht oben angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="eecda-p115">As you're adding customers, use the Action Bar to add records, edit records, save records, delete records, and cancel edits. The Action Bar is a customizable toolbar that appears at the top of each view, as shown in Figure 5.</span></span>
  
<span data-ttu-id="eecda-175">**Abbildung 5. Aktionsleiste**</span><span class="sxs-lookup"><span data-stu-id="eecda-175">**Figure 5. Action Bar**</span></span>

<span data-ttu-id="eecda-176">![Aktionsleiste](media/odc_Access15_CreateAndCustomizeWebApp_Figure05.jpg "Aktionsleiste")</span><span class="sxs-lookup"><span data-stu-id="eecda-176">![Action Bar](media/odc_Access15_CreateAndCustomizeWebApp_Figure05.jpg "Action Bar")</span></span>
  
<span data-ttu-id="eecda-p116">Sobald Sie einige Kunden und Mitarbeiter hinzugefügt haben, öffnen Sie die Ansicht „Problemliste", und fügen Sie ein Problem hinzu. Wenn Sie den Namen eines Kunden in das Feld „Kunde" eingeben, wird analog zur Darstellung in Abbildung 6 mindestens ein Kundenname angezeigt.</span><span class="sxs-lookup"><span data-stu-id="eecda-p116">Once you've added some customers and employees open the Issues List view and start adding an issue. As you type the name of a customer into the into the Customer box, one or more of the customer names will appear, as shown in Figure 6.</span></span>
  
<span data-ttu-id="eecda-179">**Abbildung 6. AutoVervollständigen-Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="eecda-179">**Figure 6. AutoComplete control**</span></span>

<span data-ttu-id="eecda-180">![AutoVervollständigen-Steuerelement](media/odc_Access15_CreateAndCustomizeWebApp_Figure06.jpg "AutoVervollständigen-Steuerelement")</span><span class="sxs-lookup"><span data-stu-id="eecda-180">![AutoComplete control](media/odc_Access15_CreateAndCustomizeWebApp_Figure06.jpg "AutoComplete control")</span></span>
  
<span data-ttu-id="eecda-p117">Das Feld „Kunde" ist ein AutoVervollständigen-Steuerelement. Das AutoVervollständigen-Steuerelement zeigt eine Liste von Datensätzen an, die mit dem, was Sie in das Feld eingeben, übereinstimmen. Dadurch wird die Genauigkeit der Dateneingabe sichergestellt.</span><span class="sxs-lookup"><span data-stu-id="eecda-p117">The Customer box is an AutoComplete control. The AutoComplete control displays a list of records that match what you're typing into the box. This helps ensure the accuracy of data entry.</span></span>
  
## <a name="customize-the-app"></a><span data-ttu-id="eecda-184">Anpassen der App</span><span class="sxs-lookup"><span data-stu-id="eecda-184">Customize the app</span></span>
<span data-ttu-id="eecda-185"><a name="ac15_CreateAndCustomizeWebApp_CustomizeTheApp"> </a></span><span class="sxs-lookup"><span data-stu-id="eecda-185"></span></span>

<span data-ttu-id="eecda-p118">Da Sie die App nun begutachtet haben, stellen Sie fest, dass die Ansicht „Problemliste" keine Kontaktinformationen für den Kunden enthält. Im Folgenden passen wir die App an, um der Tabelle „Probleme" die geschäftliche Telefonnummer des Kunden hinzuzufügen, während das Problem erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="eecda-p118">Now that you've taken a tour of the app, you notice that the Issues List view doesn't contain contact information for the customer. Let's customize the app to add the customer's work phone to the Issues table as the issue is being created.</span></span>
  
### <a name="to-add-a-field-to-the-issues-table"></a><span data-ttu-id="eecda-188">So fügen Sie der Tabelle „Probleme“ ein Feld hinzu</span><span class="sxs-lookup"><span data-stu-id="eecda-188">To add a field to the Issues table</span></span>

1. <span data-ttu-id="eecda-189">Öffnen Sie die App in Access.</span><span class="sxs-lookup"><span data-stu-id="eecda-189">Open the app in Access.</span></span>
    
2. <span data-ttu-id="eecda-190">Wählen Sie die Kachel **Probleme**, das Symbol **Einstellungen/Aktion** und dann **Tabelle bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="eecda-190">Choose the **Issues** tile, choose the **Settings/Action** icon, and then choose **Edit Table**.</span></span>
    
3. <span data-ttu-id="eecda-191">Geben Sie **Telefonnummer** in die erste leere Zelle in der Spalte **Feldname** ein.</span><span class="sxs-lookup"><span data-stu-id="eecda-191">Enter **Contact Number** in the first blank cell in the **Field Name** column.</span></span> 
    
4. <span data-ttu-id="eecda-192">Wählen Sie **Kurzer Text** in der Spalte **Datentyp** aus.</span><span class="sxs-lookup"><span data-stu-id="eecda-192">Choose **Short Text** in the **Data Type** column.</span></span> 
    
5. <span data-ttu-id="eecda-193">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="eecda-193">Choose **Save**.</span></span>
    
6. <span data-ttu-id="eecda-194">Schließen Sie die Tabelle „Probleme“.</span><span class="sxs-lookup"><span data-stu-id="eecda-194">Close the Issues table.</span></span>
    
<span data-ttu-id="eecda-195">Da nun ein Feld zum Speichern der Telefonnummer vorhanden ist, erstellen wir nun ein Datenmakro zum Nachschlagen der Kontaktinformationen.</span><span class="sxs-lookup"><span data-stu-id="eecda-195">Now that we have field in which to store the phone number, let's create a data macro to look up the contact information.</span></span>
  
### <a name="to-create-the-data-macro-to-look-up-contact-information"></a><span data-ttu-id="eecda-196">So erstellen Sie das Datenmakro zum Nachschlagen von Kontaktinformationen</span><span class="sxs-lookup"><span data-stu-id="eecda-196">To create the data macro to look up contact information</span></span>

1. <span data-ttu-id="eecda-197">Wählen Sie in der Gruppe **Erstellen** die Option **Erweitert** und dann **Datenmakro** aus.</span><span class="sxs-lookup"><span data-stu-id="eecda-197">In the **Create** group, choose **Advanced**, and then choose **Data Macro**.</span></span>
    
2. <span data-ttu-id="eecda-198">Wählen Sie **Parameter erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="eecda-198">Choose **Create Parameter**.</span></span>
    
3. <span data-ttu-id="eecda-p119">Geben Sie **CustID** in das Feld **Name** ein. Wählen Sie im Dropdownmenü **Typ** die Option **Zahl (Gleitkomma)** aus.</span><span class="sxs-lookup"><span data-stu-id="eecda-p119">In the **Name** box, enter **CustID**. In the **Type** dropdown, choose **Number (Floating Decimal).**</span></span>
    
4. <span data-ttu-id="eecda-201">Wählen Sie **LookupRecord** im Dropdownmenü **Neue Aktion hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="eecda-201">From the **Add New Action** dropdown, choose **LookupRecord**.</span></span> 
    
5. <span data-ttu-id="eecda-202">Wählen Sie **Kunden** im Dropdownmenü **Datensatz nachschlagen in** aus.</span><span class="sxs-lookup"><span data-stu-id="eecda-202">In the **Look Up A Record In** dropdown, choose **Customers**.</span></span> 
    
6. <span data-ttu-id="eecda-203">Geben Sie **[Customers].[ID]=[CustID]** in das Feld **Bedingung** ein.</span><span class="sxs-lookup"><span data-stu-id="eecda-203">In the **Where Condition** box, enter **[Customers].[ID]=[CustID]**.</span></span> 
    
7. <span data-ttu-id="eecda-204">Wählen Sie **SetReturnVar** im Dropdownmenü **Neue Aktion hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="eecda-204">Choose **SetReturnVar** from the **Add New Action** dropdown.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="eecda-p120">Es werden zwei Dropdownmenüs vom Typ **Neue Aktion hinzufügen** im Block **LookupRecord** und ein weiteres außerhalb des Blocks **LookupRecord** angezeigt. Sie sollten analog zur Darstellung in Abbildung 7 das Dropdownmenü **Neue Aktion hinzufügen** im Block **LookupRecord** verwenden.</span><span class="sxs-lookup"><span data-stu-id="eecda-p120">You'll see two **Add New Action** dropdowns, one within the **LookupRecord** block, and another outside the **LookupRecord** block. You should choose the **Add New Action** dropdown within the **LookupRecord** block, as shown in Figure 7.</span></span> 
  
   <span data-ttu-id="eecda-207">**Abbildung 7. Dropdown „Neue Aktion hinzufügen“**</span><span class="sxs-lookup"><span data-stu-id="eecda-207">**Figure 7. Add New Action dropdown**</span></span>

   <span data-ttu-id="eecda-208">![Dropdown „Neue Aktion hinzufügen“](media/odc_Access15_CreateAndCustomizeWebApp_Figure07.jpg "Dropdown „Neue Aktion hinzufügen“")</span><span class="sxs-lookup"><span data-stu-id="eecda-208">![Add New Action dropdown](media/odc_Access15_CreateAndCustomizeWebApp_Figure07.jpg "Add New Action dropdown")</span></span>
  
8. <span data-ttu-id="eecda-209">Geben Sie **ContactPhone** in das Feld **Name** ein.</span><span class="sxs-lookup"><span data-stu-id="eecda-209">In the **Name** box, enter **ContactPhone**.</span></span> 
    
9. <span data-ttu-id="eecda-210">Geben Sie **[Customers].[Work Phone]** in das Feld **Ausdruck** ein.</span><span class="sxs-lookup"><span data-stu-id="eecda-210">In the **Expression** box, enter **[Customers].[Work Phone]**.</span></span> 
    
10. <span data-ttu-id="eecda-p121">Wählen Sie **Speichern** aus. Geben Sie **GetContactPhone** in das Feld **Makroname** ein, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="eecda-p121">Choose **Save**. Enter **GetContactPhone** in the **Macro Name** box and then choose **OK**.</span></span>
    
    <span data-ttu-id="eecda-213">Das Makro sollte dem Makro in Abbildung 8 gleichen.</span><span class="sxs-lookup"><span data-stu-id="eecda-213">The macro should resemble the macro shown in Figure 8.</span></span>
    
    <span data-ttu-id="eecda-214">**Abbildung 8. GetContactPhone-Datenmakro**</span><span class="sxs-lookup"><span data-stu-id="eecda-214">**Figure 8. GetContactPhone data macro**</span></span>

    <span data-ttu-id="eecda-215">![GetContactPhone-Datenmakro](media/odc_Access15_CreateAndCustomizeWebApp_Figure08.jpg "GetContactPhone-Datenmakro")</span><span class="sxs-lookup"><span data-stu-id="eecda-215">![GetContactPhone data macro](media/odc_Access15_CreateAndCustomizeWebApp_Figure08.jpg "GetContactPhone data macro")</span></span>
  
11. <span data-ttu-id="eecda-216">Schließen Sie die Entwurfsansicht für das Makro.</span><span class="sxs-lookup"><span data-stu-id="eecda-216">Close macro Design View.</span></span>
    
<span data-ttu-id="eecda-217">Nun können wir dem Formular „Problemliste" das Feld **Telefonnummer** hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="eecda-217">Now we're ready to add the **Contact Number** field to the Issues List form.</span></span> 
  
### <a name="to-add-the-contact-number-field-to-the-issues-list-form"></a><span data-ttu-id="eecda-218">So fügen Sie das Feld „Telefonnummer“ zum Formular „Problemliste“ hinzu</span><span class="sxs-lookup"><span data-stu-id="eecda-218">To add the Contact Number field to the Issues List form</span></span>

1. <span data-ttu-id="eecda-p122">Wählen Sie die Tabelle **Probleme** aus. Dadurch wird das Formular „Problemliste" ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="eecda-p122">Choose the **Issues** table. This chooses the Issues list form.</span></span> 
    
2. <span data-ttu-id="eecda-221">Wählen Sie in der Ansichtsauswahl **Liste**, das Symbol **Einstellungen/Aktion** und anschließend **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="eecda-221">In the View selector, choose **List**, choose the **Settings/Action** icon, and then choose **Edit**.</span></span>
    
3. <span data-ttu-id="eecda-222">Ziehen Sie das Feld **Telefonnummer** aus dem Bereich **Feldliste** zur Position auf dem Formular, wo die Telefonnummer angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="eecda-222">Drag the **Contact Number** field form the **Field List** pane to the location on the form where you want the contact number to be displayed.</span></span> 
    
4. <span data-ttu-id="eecda-223">Wählen Sie das Textfeld **Telefonnummer** aus, und klicken Sie dann auf **Daten**.</span><span class="sxs-lookup"><span data-stu-id="eecda-223">Choose the **Contact Number** text box, and then click **Data**.</span></span> 
    
5. <span data-ttu-id="eecda-224">Geben Sie **CustomerContact** in das Feld **Steuerelementname** ein, und schließen Sie dann das Popup **Daten**.</span><span class="sxs-lookup"><span data-stu-id="eecda-224">In the **Control Name** box, enter **CustomerContact** and then close the **Data** popup.</span></span> 
    
6. <span data-ttu-id="eecda-225">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="eecda-225">Choose **Save**.</span></span>
    
<span data-ttu-id="eecda-p123">Nun sollten wir ein Benutzeroberflächenmakro schreiben, welches das Feld **Telefon (geschäftlich)** aus der Tabelle **Kunden** in das Feld **Telefonnummer** der Tabelle **Probleme** kopiert. Das Ereignis **Nach Aktualisierung** des Steuerelements **CustomerAutocomplete** ist ein geeigneter Ort für das Makro.</span><span class="sxs-lookup"><span data-stu-id="eecda-p123">Now we should write a user interface (UI) macro that copies the **Work Phone** field from the **Customers** table into the **Contact Phone** field of the **Issues** table. The **After Update** event of the **CustomerAutocomplete** control is a good location for the macro.</span></span> 
  
### <a name="to-create-the-afterupdate-macro"></a><span data-ttu-id="eecda-228">So erstellen Sie das AfterUpdate-Makro</span><span class="sxs-lookup"><span data-stu-id="eecda-228">To create the AfterUpdate macro</span></span>

1. <span data-ttu-id="eecda-229">Wählen Sie das Steuerelement **CustomerAutocomplete**, die Schaltfläche **Aktionen** und dann **Nach Aktualisierung** aus.</span><span class="sxs-lookup"><span data-stu-id="eecda-229">Choose the **CustomerAutocomplete** control, choose the **Actions** button, and then choose **After Update**.</span></span> 
    
    <span data-ttu-id="eecda-230">In der Entwurfsansicht für das Makro wird ein leeres Makro geöffnet.</span><span class="sxs-lookup"><span data-stu-id="eecda-230">A blank macro is opened in macro Design View.</span></span>
    
2. <span data-ttu-id="eecda-231">Wählen Sie **RunDataMacro** im Dropdownmenü **Neue Aktion hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="eecda-231">From the **Add New Action** dropdown, choose **RunDataMacro**.</span></span> 
    
3. <span data-ttu-id="eecda-232">Wählen Sie **GetContactPhone** im Dropdownmenü **Makroname** aus.</span><span class="sxs-lookup"><span data-stu-id="eecda-232">In the **Macro Name** dropdown, choose **GetContactPhone**.</span></span> 
    
4. <span data-ttu-id="eecda-233">Geben Sie **[CustomerAutocomplete]** in das Feld **CustID** ein.</span><span class="sxs-lookup"><span data-stu-id="eecda-233">In the **CustID** box, enter **[CustomerAutocomplete]**.</span></span> 
    
5. <span data-ttu-id="eecda-234">Geben Sie **Telefon** in das Feld **SetLocalVar** ein.</span><span class="sxs-lookup"><span data-stu-id="eecda-234">In the **SetLocalVar** box, enter **Phone**.</span></span> 
    
    <span data-ttu-id="eecda-235">Wenn Sie das zuvor erstellte GetContactPhone-Datenmakro auswählen, hat Access den Parameternamen und Rückgabewert für das Makro automatisch ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="eecda-235">When you chose the GetContactPhone data macro that was created earlier, Access automatically filled in the parameter name and return variable for the macro.</span></span>
    
    <span data-ttu-id="eecda-236">Die Telefonnummer für den Kunden wird in einer Variablen namens „Phone“ gespeichert.</span><span class="sxs-lookup"><span data-stu-id="eecda-236">The phone number for the customer is stored in a variable named Phone.</span></span>
    
6. <span data-ttu-id="eecda-237">Wählen Sie **SetProperty** im Dropdownmenü **Neue Aktion hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="eecda-237">From the **Add New Action** dropdown, choose **SetProperty**.</span></span> 
    
7. <span data-ttu-id="eecda-238">Geben Sie **CustomerContact** in das Feld **Steuerelementname** ein.</span><span class="sxs-lookup"><span data-stu-id="eecda-238">In the **Control Name** box, enter **CustomerContact**.</span></span> 
    
8. <span data-ttu-id="eecda-239">Wählen Sie **Wert** im Dropdownmenü **Eigenschaft** aus.</span><span class="sxs-lookup"><span data-stu-id="eecda-239">In the **Property** dropdown, choose **Value**.</span></span> 
    
9. <span data-ttu-id="eecda-240">Geben Sie **=[Phone]** in das Feld **Wert** ein.</span><span class="sxs-lookup"><span data-stu-id="eecda-240">In the **Value** box, enter **=[Phone]**.</span></span> 
    
10. <span data-ttu-id="eecda-241">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="eecda-241">Choose **Save**.</span></span>
    
    <span data-ttu-id="eecda-242">Das Makro sollte dem Makro in Abbildung 9 gleichen.</span><span class="sxs-lookup"><span data-stu-id="eecda-242">The macro should resemble the macro shown in Figure 9.</span></span>
    
    <span data-ttu-id="eecda-243">**Abbildung 9. AfterUpdate-Makro**</span><span class="sxs-lookup"><span data-stu-id="eecda-243">**Figure 9. After Update macro**</span></span>

    <span data-ttu-id="eecda-244">![AfterUpdate-Makro](media/odc_Access15_CreateAndCustomizeWebApp_Figure09.jpg "AfterUpdate-Makro")</span><span class="sxs-lookup"><span data-stu-id="eecda-244">![After Update macro](media/odc_Access15_CreateAndCustomizeWebApp_Figure09.jpg "After Update macro")</span></span>
  
11. <span data-ttu-id="eecda-245">Schließen Sie die Entwurfsansicht für das Makro.</span><span class="sxs-lookup"><span data-stu-id="eecda-245">Close macro Design View.</span></span>
    
12. <span data-ttu-id="eecda-p124">Schließen Sie die Ansicht „Problemliste“. Wählen Sie **Ja** aus, wenn Sie dazu aufgefordert werden, Ihre Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="eecda-p124">Close the Issues List view. Choose **Yes** when you are prompted to save your changes.</span></span> 
    
<span data-ttu-id="eecda-248">Jetzt können Sie die Anpassung formulieren.</span><span class="sxs-lookup"><span data-stu-id="eecda-248">Now we're ready to text the customization.</span></span> <span data-ttu-id="eecda-249">Klicken Sie auf **App starten**, um die App in Ihrem Webbrowser zu öffnen, und fügen Sie dann ein neues Problem ein.</span><span class="sxs-lookup"><span data-stu-id="eecda-249">Click **Launch App** to open the app in your web browser and then add a new issue.</span></span> <span data-ttu-id="eecda-250">Das Feld **Telefonnummer** wird automatisch aktualisiert, nachdem der Kundenname analog zur Darstellung in Abbildung 10 eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="eecda-250">The **Contact Number** box updates automatically after the customer name is entered,  as shown in Figure 10.</span></span> 
  
<span data-ttu-id="eecda-251">**Abbildung 10. Mit Telefonnummer aktualisierte Ansicht vom Typ „Probleme“**</span><span class="sxs-lookup"><span data-stu-id="eecda-251">**Figure 10. Issues view updated with phone number**</span></span>

<span data-ttu-id="eecda-252">![Mit Telefonnummer aktualisierte Ansicht vom Typ „Probleme“](media/odc_Access15_CreateAndCustomizeWebApp_Figure10.jpg "Mit Telefonnummer aktualisierte Ansicht vom Typ „Probleme“")</span><span class="sxs-lookup"><span data-stu-id="eecda-252">![Issues view updated with phone number](media/odc_Access15_CreateAndCustomizeWebApp_Figure10.jpg "Issues view updated with phone number")</span></span>
  
## <a name="conclusion"></a><span data-ttu-id="eecda-253">Schlussbemerkung</span><span class="sxs-lookup"><span data-stu-id="eecda-253">Conclusion</span></span>

<span data-ttu-id="eecda-p126">Die Verwendung einer der in enthaltenen Schemavorlagen ist eine gute Einstiegsmöglichkeit für das Erstellen einer Access-Web-App. Die automatisch für Sie erstellten Ansichten verfügen über eine erweiterte Funktionalität, für die das Implementieren von benutzerdefiniertem Code in einer Access-Desktop-PC-Datenbank erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="eecda-p126">Using one of the schema templates included with is a good way to jump start the creation of an Access web app. The views that are automatically created for you contain advanced functionally that requires custom code to implement in a Access desktop database.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="eecda-256">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eecda-256">See also</span></span>

- [<span data-ttu-id="eecda-257">Neuigkeiten für Access 2013-Entwickler</span><span class="sxs-lookup"><span data-stu-id="eecda-257">What's new for Access 2013 developers</span></span>](https://msdn.microsoft.com/library/df778f51-d65e-4c30-b618-65003ceb39b3%28Office.15%29.aspx) 
- [<span data-ttu-id="eecda-258">Benutzerdefinierte Web-App-Referenz für Access</span><span class="sxs-lookup"><span data-stu-id="eecda-258">Access custom web app reference</span></span>](access-custom-web-app-reference.md)
  

