---
<span data-ttu-id="19f14-101">Titel: Anwenden einer benutzerdefinierten Multifunktionsleiste zu einem Formular oder Bericht TOCTitle: Anwenden einer benutzerdefinierten Multifunktionsleiste zu einem Formular oder Bericht <<<<<<< HEAD Ms:assetid: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84 Ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15) Ms:contentKeyID: 48545865 ms.date: 09/18/2015 === === Beschreibung: Gewusst wie: Anwenden von benutzerdefinierten Menüleisten beim Laden eines Formulars oder Berichts in Access 2013.</span><span class="sxs-lookup"><span data-stu-id="19f14-101">title: Apply a custom ribbon to a form or report TOCTitle: Apply a custom ribbon to a form or report <<<<<<< HEAD ms:assetid: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84 ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15) ms:contentKeyID: 48545865 ms.date: 09/18/2015 ======= description: How to apply customized ribbons when loading a form or report in Access 2013.</span></span>
<span data-ttu-id="19f14-102">MS:AssetId: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84 Ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15) Ms:contentKeyID: 48545865 ms.date: 10/16/2018</span><span class="sxs-lookup"><span data-stu-id="19f14-102">ms:assetid: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84 ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15) ms:contentKeyID: 48545865 ms.date: 10/16/2018</span></span>
>>>>>>> <span data-ttu-id="19f14-103">Master-Shape Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="19f14-103">master mtps_version: v=office.15</span></span>
---

# <a name="apply-a-custom-ribbon-to-a-form-or-report"></a><span data-ttu-id="19f14-104">Anwenden einer benutzerdefinierten Multifunktionsleiste zu einem Formular oder Bericht</span><span class="sxs-lookup"><span data-stu-id="19f14-104">Apply a custom ribbon to a form or report</span></span>

<span data-ttu-id="19f14-105"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="19f14-105"><<<<<<< HEAD</span></span>

<span data-ttu-id="19f14-106">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="19f14-106">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="19f14-p102">Das Menüband verwendet textbasiertes, deklaratives XML-Markup, das die Erstellung und Anpassung des Menübands vereinfacht. Mit ein paar XML-Zeilen können Sie genau die passende Benutzeroberfläche für den Benutzer erstellen. Access bietet Flexibilität beim Anpassen der Menüband-Benutzeroberfläche. So können Sie das Anpassungsmarkup zum Beispiel in einer Tabelle speichern, in eine VBA-Prozedur einbetten, in einer anderen Access-Datenbank speichern oder mit einem Excel-Arbeitsblatt verknüpfen. Dieses Thema beschreibt, wie angepasste Menübänder beim Laden eines Formulars oder eines Berichts angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="19f14-p102">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon. With a few lines of XML, you can create just the right interface for the user. Access provides flexibility in customizing the ribbon user interface. For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet. This topic describes how to apply customized ribbons when loading a form or report.</span></span>

## <a name="making-the-ribbon-customization-xml-available"></a><span data-ttu-id="19f14-112">XML für die Menübandanpassung verfügbar machen</span><span class="sxs-lookup"><span data-stu-id="19f14-112">Making the Ribbon Customization XML Available</span></span>

<span data-ttu-id="19f14-113">**Speichern der Menübanderweiterungs-XML in einer Tabelle**</span><span class="sxs-lookup"><span data-stu-id="19f14-113">**Storing Ribbon Extensibility XML in a Table**</span></span>

<span data-ttu-id="19f14-p103">Eine Möglichkeit zum Verfügbarmachen der Menübandanpassungen ist, sie in einer Tabelle zu speichern. Wenn Sie die Anpassungen in einer Tabelle mit dem Namen **USysRibbons** speichern, können die Anpassungen ohne Makros oder VBA-Code implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="19f14-p103">One method that you can use to make ribbon customizations available is to store them in a table. If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="19f14-p104">**USysRibbons** ist eine vom Benutzer erstellte Systemtabelle. Die Tabelle muss mit bestimmten Spaltennamen erstellt werden, damit die Menübandanpassungen implementiert werden können. In der folgenden Tabelle sind die Einstellungen aufgeführt, die beim Erstellen der **USysRibbons** -Tabelle verwendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="19f14-p104">**USysRibbons** is a user-created system table. The table must be created using specific column names in order for the ribbon customizations to be implemented. The following table lists the settings to use when creating the **USysRibbons** table.</span></span>
=======
<span data-ttu-id="19f14-119">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="19f14-119">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="19f14-120">Das Menüband verwendet textbasiertes, deklaratives XML-Markup, das die Erstellung und Anpassung des Menübands vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="19f14-120">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon.</span></span> <span data-ttu-id="19f14-121">Mit ein paar XML-Zeilen können Sie genau die passende Benutzeroberfläche für den Benutzer erstellen.</span><span class="sxs-lookup"><span data-stu-id="19f14-121">With a few lines of XML, you can create just the right interface for the user.</span></span> <span data-ttu-id="19f14-122">Access bietet Flexibilität beim Anpassen der Menüband-Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="19f14-122">Access provides flexibility in customizing the ribbon user interface.</span></span> 

<span data-ttu-id="19f14-123">So können Sie das Anpassungsmarkup zum Beispiel in einer Tabelle speichern, in eine VBA-Prozedur einbetten, in einer anderen Access-Datenbank speichern oder mit einem Excel-Arbeitsblatt verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="19f14-123">For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet.</span></span> <span data-ttu-id="19f14-124">Dieses Thema beschreibt, wie angepasste Menübänder beim Laden eines Formulars oder eines Berichts angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="19f14-124">This topic describes how to apply customized ribbons when loading a form or report.</span></span>

## <a name="make-the-ribbon-customization-xml-available"></a><span data-ttu-id="19f14-125">Anpassung der Multifunktionsleiste XML verfügbar machen</span><span class="sxs-lookup"><span data-stu-id="19f14-125">Make the ribbon customization XML available</span></span>

### <a name="store-ribbon-extensibility-xml-in-a-table"></a><span data-ttu-id="19f14-126">Menüband-Erweiterbarkeits-XML in einer Tabelle speichern</span><span class="sxs-lookup"><span data-stu-id="19f14-126">Store ribbon extensibility XML in a table</span></span>

<span data-ttu-id="19f14-p107">Eine Möglichkeit zum Verfügbarmachen der Menübandanpassungen ist, sie in einer Tabelle zu speichern. Wenn Sie die Anpassungen in einer Tabelle mit dem Namen **USysRibbons** speichern, können die Anpassungen ohne Makros oder VBA-Code implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="19f14-p107">One method that you can use to make ribbon customizations available is to store them in a table. If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="19f14-129">**USysRibbons** ist eine vom Benutzer erstellte Systemtabelle.</span><span class="sxs-lookup"><span data-stu-id="19f14-129">**USysRibbons** is a user-created system table.</span></span> <span data-ttu-id="19f14-130">Die Tabelle muss mit bestimmten Spaltennamen für die menübandanpassungen implementiert werden erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="19f14-130">The table must be created using specific column names for the ribbon customizations to be implemented.</span></span> 

<span data-ttu-id="19f14-131">In der folgenden Tabelle sind die Einstellungen beschrieben, die beim Erstellen der Tabelle **USysRibbons** verwendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="19f14-131">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>
>>>>>>> <span data-ttu-id="19f14-132">master</span><span class="sxs-lookup"><span data-stu-id="19f14-132">master</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<span data-ttu-id="19f14-133"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="19f14-133"><<<<<<< HEAD</span></span>
<th><p><span data-ttu-id="19f14-134">Spaltenname</span><span class="sxs-lookup"><span data-stu-id="19f14-134">Column Name</span></span></p></th>
<th><p><span data-ttu-id="19f14-135">Datentyp</span><span class="sxs-lookup"><span data-stu-id="19f14-135">Data Type</span></span></p></th>
=======
<th><p><span data-ttu-id="19f14-136">Spaltenname</span><span class="sxs-lookup"><span data-stu-id="19f14-136">Column name</span></span></p></th>
<th><p><span data-ttu-id="19f14-137">Datentyp</span><span class="sxs-lookup"><span data-stu-id="19f14-137">Data type</span></span></p></th><span data-ttu-id="19f14-138">
>>>>>>>Master-Shape</span><span class="sxs-lookup"><span data-stu-id="19f14-138">
>>>>>>> master</span></span>
<th><p><span data-ttu-id="19f14-139">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="19f14-139">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="19f14-140"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="19f14-140"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="19f14-141">Text</span><span class="sxs-lookup"><span data-stu-id="19f14-141">Text</span></span></p></td>
<span data-ttu-id="19f14-142"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="19f14-142"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="19f14-143">Enthält den Namen des benutzerdefinierten Menübands, das dieser Anpassung zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="19f14-143">Contains the name of the custom ribbon to be associated with this customization</span></span></p></td>
=======
<td><p><span data-ttu-id="19f14-144">Enthält den Namen des benutzerdefinierten Menübands, das dieser Anpassung zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="19f14-144">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td><span data-ttu-id="19f14-145">
>>>>>>>Master-Shape</span><span class="sxs-lookup"><span data-stu-id="19f14-145">
>>>>>>> master</span></span>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19f14-146"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="19f14-146"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="19f14-147">Memo</span><span class="sxs-lookup"><span data-stu-id="19f14-147">Memo</span></span></p></td>
<span data-ttu-id="19f14-148"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="19f14-148"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="19f14-149">Enthält die Menübanderweiterungs-XML (RibbonX) zur Definition der Menübandanpassung.</span><span class="sxs-lookup"><span data-stu-id="19f14-149">Contains the ribbon Extensibility XML (RibbonX) that defines the ribbon customization</span></span></p></td>
=======
<td><p><span data-ttu-id="19f14-150">Enthält die Menüband-Erweiterbarkeits-XML (RibbonX), die die menübandanpassung definiert wird.</span><span class="sxs-lookup"><span data-stu-id="19f14-150">Contains the ribbon extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td><span data-ttu-id="19f14-151">
>>>>>>>Master-Shape</span><span class="sxs-lookup"><span data-stu-id="19f14-151">
>>>>>>> master</span></span>
</tr>
</tbody>
</table>


<span data-ttu-id="19f14-152"><<<<<<< HEAD **programmgesteuert Laden von Menüband-Erweiterbarkeits-XML**</span><span class="sxs-lookup"><span data-stu-id="19f14-152"><<<<<<< HEAD **Loading Ribbon Extensibility XML Programmatically**</span></span>

<span data-ttu-id="19f14-p109">Mit der **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** -Methode können Sie Menübandanpassungen programmatisch laden. Um das Menüband zu erstellen und der Anwendung zur Verfügung zu stellen, erstellen Sie in der Regel zunächst ein Modul in der Datenbank mit einer Prozedur, die die **LoadCustomUI** -Methode aufruft, sodass der Name des Menübands und das XML-Anpassungsmarkup übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="19f14-p109">You can use the **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** method to load ribbon customizations programmatically. Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>
=======
### <a name="load-ribbon-extensibility-xml-programmatically"></a><span data-ttu-id="19f14-155">Menüband-Erweiterbarkeits-XML programmgesteuert laden</span><span class="sxs-lookup"><span data-stu-id="19f14-155">Load ribbon extensibility XML programmatically</span></span>

<span data-ttu-id="19f14-p110">Mit der **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** -Methode können Sie Menübandanpassungen programmatisch laden. Um das Menüband zu erstellen und der Anwendung zur Verfügung zu stellen, erstellen Sie in der Regel zunächst ein Modul in der Datenbank mit einer Prozedur, die die **LoadCustomUI** -Methode aufruft, sodass der Name des Menübands und das XML-Anpassungsmarkup übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="19f14-p110">You can use the **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** method to load ribbon customizations programmatically. Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>
>>>>>>> <span data-ttu-id="19f14-158">master</span><span class="sxs-lookup"><span data-stu-id="19f14-158">master</span></span>

<span data-ttu-id="19f14-p111">Das XML-Markup kann von einem **Recordset** -Objekt stammen, das aus einer Tabelle, einer datenbankexternen Quelle wie einer XML-Datei, die in eine Zeichenfolge analysiert wird, oder aus einer direkt in die Prozedur eingebetteten XML-Datei stammen kann. Sie können verschiedene Menübänder anhand mehrerer Aufrufe der **LoadCustomUI** -Methode erstellen, wobei verschiedenes XML übergeben wird, solange der Name jedes Menübands und das **id** -Attribut der Registerkarten des Menübands eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="19f14-p111">The XML markup can come from a **Recordset** object created from a table, from a source external to the database such as an XML file that you parse into a string, or from XML markup embedded directly inside the procedure. You can make different ribbons using multiple calls to the **LoadCustomUI** method, passing in different XML markup as long as the name of each ribbon and the **id** attribute of the tabs that make up the ribbon are unique.</span></span>

<span data-ttu-id="19f14-p112">Nach Abschluss der Prozedur erstellen Sie ein AutoExec-Makro, das die Prozedur über die RunCode-Aktion aufruft. Auf diese Weise wird beim Starten der Anwendung die **LoadCustomUI** -Methode automatisch ausgeführt, und alle benutzerdefinierten Menübänder werden für die Anwendung verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="19f14-p112">After the procedure is complete, you then create an AutoExec macro that calls the procedure by using the RunCode action. That way, when the application is started, the **LoadCustomUI** method is automatically executed and all of the custom ribbons are made available to the application.</span></span>

<span data-ttu-id="19f14-163"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="19f14-163"><<<<<<< HEAD</span></span>
## <a name="assigning-custom-ribbons-to-forms-or-reports"></a><span data-ttu-id="19f14-164">Zuweisen benutzerdefinierter Menübänder zu Formularen oder Berichten</span><span class="sxs-lookup"><span data-stu-id="19f14-164">Assigning Custom Ribbons to Forms or Reports</span></span>
=======
## <a name="assign-custom-ribbons-to-forms-or-reports"></a><span data-ttu-id="19f14-165">Weisen Sie benutzerdefinierter Menübänder zu Formularen oder Berichten zu</span><span class="sxs-lookup"><span data-stu-id="19f14-165">Assign custom ribbons to forms or reports</span></span>
>>>>>>> <span data-ttu-id="19f14-166">master</span><span class="sxs-lookup"><span data-stu-id="19f14-166">master</span></span>

1.  <span data-ttu-id="19f14-167">Führen Sie den oben beschriebenen Vorgang aus, um das benutzerdefinierte Menüband in der Anwendung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="19f14-167">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="19f14-168">Öffnen Sie das Formular oder den Bericht in der Entwurfsansicht.</span><span class="sxs-lookup"><span data-stu-id="19f14-168">Open the form or report in Design view.</span></span>

<span data-ttu-id="19f14-169"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="19f14-169"><<<<<<< HEAD</span></span>
3.  <span data-ttu-id="19f14-170">Klicken Sie auf der Registerkarte „Entwurf" auf **Eigenschaftenblatt**.</span><span class="sxs-lookup"><span data-stu-id="19f14-170">On the Design tab, click **Property Sheet**.</span></span>

4.  <span data-ttu-id="19f14-171">Klicken Sie auf der Registerkarte **Alle** des Eigenschaftenfensters auf die Liste **Name des Menübands**, und wählen Sie anschließend ein Menüband aus.</span><span class="sxs-lookup"><span data-stu-id="19f14-171">On the **All** tab of the Property window, click the **Ribbon Name** list and then select a ribbon.</span></span>
=======
3.  <span data-ttu-id="19f14-172">Wählen Sie auf der Registerkarte Entwurf **Eigenschaftenblatt**.</span><span class="sxs-lookup"><span data-stu-id="19f14-172">On the Design tab, choose **Property Sheet**.</span></span>

4.  <span data-ttu-id="19f14-173">Wählen Sie auf der Registerkarte **Alle** des Eigenschaftenfensters aus der Liste **Name** des Menübands, und wählen Sie ein Menüband aus.</span><span class="sxs-lookup"><span data-stu-id="19f14-173">On the **All** tab of the Property window, choose the **Ribbon Name** list and then select a ribbon.</span></span>
>>>>>>> <span data-ttu-id="19f14-174">master</span><span class="sxs-lookup"><span data-stu-id="19f14-174">master</span></span>

5.  <span data-ttu-id="19f14-p113">Speichern und schließen Sie das Formular oder den Bericht, und öffnen Sie das Formular oder den Bericht dann erneut. Die ausgewählte Menüband-Benutzeroberfläche wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="19f14-p113">Save, close, and then reopen the form or report. The ribbon UI you selected is displayed.</span></span>


> [!NOTE]
> <span data-ttu-id="19f14-177">[!HINWEIS] Die in der Menüband-Benutzeroberfläche angezeigten Registerkarten sind additiv.</span><span class="sxs-lookup"><span data-stu-id="19f14-177">The tabs displayed in the ribbon UI are additive.</span></span> <span data-ttu-id="19f14-178">D. h., es sei denn, Sie insbesondere die Registerkarten ausblenden oder *von vorne beginnen* -Attribut auf **True**festgelegt, die Registerkarten angezeigt, in einem Formular oder des Berichts Menüband-Benutzeroberfläche sind zusätzlich zu den vorhandenen Registerkarten.</span><span class="sxs-lookup"><span data-stu-id="19f14-178">That is, unless you specifically hide the tabs or set the *Start from Scratch* attribute to **True**, the tabs displayed in a form's or report's ribbon user interface are in addition to the existing tabs.</span></span>

> [!NOTE]
> <span data-ttu-id="19f14-179">[!HINWEIS] Weitere Informationen über die Menüband-Benutzeroberfläche in anderen Office-Anwendungen finden Sie unter [Übersicht über das Office Fluent-Menüband](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="19f14-179">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


