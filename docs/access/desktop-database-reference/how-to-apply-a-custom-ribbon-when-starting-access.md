---
<span data-ttu-id="8c8cc-101">Titel: Anwenden einer benutzerdefinierten Multifunktionsleiste beim Starten von Access TOCTitle: Anwenden einer benutzerdefinierten Multifunktionsleiste beim Starten von Access <<<<<<< HEAD Ms:assetid: 9e8ddf95-35aa-4e57-8422-d770da14711e Ms:mtpsurl: https://msdn.microsoft.com/library/Ff198313(v=office.15) Ms:contentKeyID: 48546659 ms.date: 09/18 / 2015 === Beschreibung: Gewusst wie: Anwenden von benutzerdefinierten Menüleisten beim Öffnen einer Datenbank in Access 2013.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-101">title: Apply a custom ribbon when starting Access TOCTitle: Apply a custom ribbon when starting Access <<<<<<< HEAD ms:assetid: 9e8ddf95-35aa-4e57-8422-d770da14711e ms:mtpsurl: https://msdn.microsoft.com/library/Ff198313(v=office.15) ms:contentKeyID: 48546659 ms.date: 09/18/2015 ======= description: How to apply customized ribbons when opening a database in Access 2013.</span></span> <span data-ttu-id="8c8cc-102">MS:AssetId: 9e8ddf95-35aa-4e57-8422-d770da14711e Ms:mtpsurl: https://msdn.microsoft.com/library/Ff198313(v=office.15) Ms:contentKeyID: 48546659 ms.date: 10/16/2018</span><span class="sxs-lookup"><span data-stu-id="8c8cc-102">ms:assetid: 9e8ddf95-35aa-4e57-8422-d770da14711e ms:mtpsurl: https://msdn.microsoft.com/library/Ff198313(v=office.15) ms:contentKeyID: 48546659 ms.date: 10/16/2018</span></span>
>>>>>>> <span data-ttu-id="8c8cc-103">Master-Shape Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="8c8cc-103">master mtps_version: v=office.15</span></span>
---

# <a name="apply-a-custom-ribbon-when-starting-access"></a><span data-ttu-id="8c8cc-104">Anwenden einer benutzerdefinierten Multifunktionsleiste beim Starten von Access</span><span class="sxs-lookup"><span data-stu-id="8c8cc-104">Apply a custom ribbon when starting Access</span></span>

<span data-ttu-id="8c8cc-105">**Gilt für:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8c8cc-105">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="8c8cc-p102">Das Menüband verwendet textbasiertes, deklaratives XML-Markup, das die Erstellung und Anpassung des Menübands vereinfacht. Mit ein paar XML-Zeilen können Sie genau die passende Benutzeroberfläche für den Benutzer erstellen. Access bietet eine enorme Flexibilität beim Anpassen der Menüband-Benutzeroberfläche. So können Sie das Anpassungsmarkup zum Beispiel in einer Tabelle speichern, in eine VBA-Prozedur einbetten, in einer anderen Access-Datenbank speichern oder mit einem Excel-Arbeitsblatt verknüpfen. Dieses Thema beschreibt, wie angepasste Menübänder beim Öffnen einer Datenbank angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-p102">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon. With a few lines of XML, you can create just the right interface for the user. Access provides tremendous flexibility in customizing the ribbon UI. For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet. This topic describes how to apply customized ribbons when opening a database.</span></span>

<span data-ttu-id="8c8cc-111"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="8c8cc-111"><<<<<<< HEAD</span></span>
## <a name="making-the-ribbon-customization-xml-available"></a><span data-ttu-id="8c8cc-112">XML für die Menübandanpassung verfügbar machen</span><span class="sxs-lookup"><span data-stu-id="8c8cc-112">Making the Ribbon Customization XML Available</span></span>

### <a name="storing-ribbon-extensibility-xml-in-a-table"></a><span data-ttu-id="8c8cc-113">Speichern der Menübanderweiterungs-XML in einer Tabelle</span><span class="sxs-lookup"><span data-stu-id="8c8cc-113">Storing Ribbon Extensibility XML in a Table</span></span>

<span data-ttu-id="8c8cc-p103">Eine Möglichkeit zum Verfügbarmachen der Menübandanpassungen ist, sie in einer Tabelle zu speichern. Wenn Sie die Anpassungen in einer Tabelle mit dem Namen **USysRibbons** speichern, können die Anpassungen ohne Makros oder VBA-Code implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-p103">One method that you can use to make ribbon customizations available is to store them in a table. If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="8c8cc-p104">**USysRibbons** ist eine vom Benutzer erstellte Systemtabelle. Die Tabelle muss mit bestimmten Spaltennamen erstellt werden, damit die Menübandanpassungen implementiert werden können. In der folgenden Tabelle sind die Einstellungen aufgeführt, die beim Erstellen der **USysRibbons** -Tabelle verwendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-p104">**USysRibbons** is a user-created system table. The table must be created using specific column names in order for the ribbon customizations to be implemented. The following table lists the settings to use when creating the **USysRibbons** table.</span></span>
=======
## <a name="make-the-ribbon-customization-xml-available"></a><span data-ttu-id="8c8cc-119">Anpassung der Multifunktionsleiste XML verfügbar machen</span><span class="sxs-lookup"><span data-stu-id="8c8cc-119">Make the ribbon customization XML available</span></span>

### <a name="store-ribbon-extensibility-xml-in-a-table"></a><span data-ttu-id="8c8cc-120">Menüband-Erweiterbarkeits-XML in einer Tabelle speichern</span><span class="sxs-lookup"><span data-stu-id="8c8cc-120">Store ribbon extensibility XML in a table</span></span>

<span data-ttu-id="8c8cc-p105">Eine Möglichkeit zum Verfügbarmachen der Menübandanpassungen ist, sie in einer Tabelle zu speichern. Wenn Sie die Anpassungen in einer Tabelle mit dem Namen **USysRibbons** speichern, können die Anpassungen ohne Makros oder VBA-Code implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-p105">One method that you can use to make ribbon customizations available is to store them in a table. If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="8c8cc-123">**USysRibbons** ist eine vom Benutzer erstellte Systemtabelle.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-123">**USysRibbons** is a user-created system table.</span></span> <span data-ttu-id="8c8cc-124">Die Tabelle muss mit bestimmten Spaltennamen für die menübandanpassungen implementiert werden erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-124">The table must be created using specific column names for the ribbon customizations to be implemented.</span></span> 

<span data-ttu-id="8c8cc-125">In der folgenden Tabelle sind die Einstellungen beschrieben, die beim Erstellen der Tabelle **USysRibbons** verwendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-125">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>
>>>>>>> <span data-ttu-id="8c8cc-126">master</span><span class="sxs-lookup"><span data-stu-id="8c8cc-126">master</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<span data-ttu-id="8c8cc-127"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="8c8cc-127"><<<<<<< HEAD</span></span>
<th><p><span data-ttu-id="8c8cc-128">Spaltenname</span><span class="sxs-lookup"><span data-stu-id="8c8cc-128">Column Name</span></span></p></th>
<th><p><span data-ttu-id="8c8cc-129">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8c8cc-129">Data Type</span></span></p></th>
=======
<th><p><span data-ttu-id="8c8cc-130">Spaltenname</span><span class="sxs-lookup"><span data-stu-id="8c8cc-130">Column name</span></span></p></th>
<th><p><span data-ttu-id="8c8cc-131">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8c8cc-131">Data type</span></span></p></th><span data-ttu-id="8c8cc-132">
>>>>>>>Master-Shape</span><span class="sxs-lookup"><span data-stu-id="8c8cc-132">
>>>>>>> master</span></span>
<th><p><span data-ttu-id="8c8cc-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8c8cc-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c8cc-134"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="8c8cc-134"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="8c8cc-135">Text</span><span class="sxs-lookup"><span data-stu-id="8c8cc-135">Text</span></span></p></td>
<td><p><span data-ttu-id="8c8cc-136">Enthält den Namen des benutzerdefinierten Menübands, das dieser Anpassung zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-136">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c8cc-137"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="8c8cc-137"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="8c8cc-138">Memo</span><span class="sxs-lookup"><span data-stu-id="8c8cc-138">Memo</span></span></p></td>
<span data-ttu-id="8c8cc-139"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="8c8cc-139"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="8c8cc-140">Enthält die Menübanderewiterungs-XML (RibbonX) zur Definition der Menübandanpassung.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-140">Contains the Ribbon Extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
=======
<td><p><span data-ttu-id="8c8cc-141">Enthält die Menüband-Erweiterbarkeits-XML (RibbonX), die die menübandanpassung definiert wird.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-141">Contains the ribbon extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td><span data-ttu-id="8c8cc-142">
>>>>>>>Master-Shape</span><span class="sxs-lookup"><span data-stu-id="8c8cc-142">
>>>>>>> master</span></span>
</tr>
</tbody>
</table>


<span data-ttu-id="8c8cc-143"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="8c8cc-143"><<<<<<< HEAD</span></span>
### <a name="loading-ribbon-extensibility-xml-programmatically"></a><span data-ttu-id="8c8cc-144">Menübanderweiterungs-XML programmatisch laden</span><span class="sxs-lookup"><span data-stu-id="8c8cc-144">Loading Ribbon Extensibility XML Programmatically</span></span>

<span data-ttu-id="8c8cc-p107">Mit der **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** -Methode können Sie Menübandanpassungen programmatisch laden. Um das Menüband zu erstellen und der Anwendung zur Verfügung zu stellen, erstellen Sie in der Regel zunächst ein Modul in der Datenbank mit einer Prozedur, die die **LoadCustomUI** -Methode aufruft, sodass der Name des Menübands und das XML-Anpassungsmarkup übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-p107">You can use the **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** method to load ribbon customizations programmatically. Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>

<span data-ttu-id="8c8cc-p108">Das XML-Markup kann von einem **Recordset** -Objekt stammen, das aus einer Tabelle, einer datenbankexternen Quelle wie einer XML-Datei, die in eine Zeichenfolge analysiert wird, oder aus einer direkt in die Prozedur eingebetteten XML-Datei stammen kann. Sie können verschiedene Menübänder anhand mehrerer Aufrufe der **LoadCustomUI** -Methode erstellen, wobei verschiedenes XML übergeben wird, solange der Name jedes Menübands und das **id** -Attribut der Registerkarten des Menübands eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-p108">The XML markup can come from a **Recordset** object created from a table, from a source external to the database such as an XML file that you parse into a string, or from XML markup embedded directly inside the procedure. You can make different ribbons using multiple calls to the **LoadCustomUI** method, passing in different XML markup as long as the name of each ribbon and the **id** attribute of the tabs that make up the ribbon are unique.</span></span>

<span data-ttu-id="8c8cc-p109">Nach Abschluss der Prozedur erstellen Sie ein AutoExec-Makro, das die Prozedur über die RunCode-Aktion aufruft. Auf diese Weise wird beim Starten der Anwendung die **LoadCustomUI** -Methode automatisch ausgeführt, und alle benutzerdefinierten Menübänder werden für die Anwendung verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-p109">After the procedure is complete, you then create an AutoExec macro that calls the procedure by using the RunCode action. That way, when the application is started, the **LoadCustomUI** method is automatically executed and all of the custom ribbons are made available to the application.</span></span>

## <a name="applying-customized-ribbons-when-access-starts"></a><span data-ttu-id="8c8cc-151">Anwenden von benutzerdefinierten Menübändern beim Starten von Access</span><span class="sxs-lookup"><span data-stu-id="8c8cc-151">Applying Customized Ribbons When Access Starts</span></span>
=======
### <a name="load-ribbon-extensibility-xml-programmatically"></a><span data-ttu-id="8c8cc-152">Menüband-Erweiterbarkeits-XML programmgesteuert laden</span><span class="sxs-lookup"><span data-stu-id="8c8cc-152">Load ribbon extensibility XML programmatically</span></span>

<span data-ttu-id="8c8cc-p110">Mit der **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** -Methode können Sie Menübandanpassungen programmatisch laden. Um das Menüband zu erstellen und der Anwendung zur Verfügung zu stellen, erstellen Sie in der Regel zunächst ein Modul in der Datenbank mit einer Prozedur, die die **LoadCustomUI** -Methode aufruft, sodass der Name des Menübands und das XML-Anpassungsmarkup übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-p110">You can use the **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** method to load ribbon customizations programmatically. Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>

<span data-ttu-id="8c8cc-p111">Das XML-Markup kann von einem **Recordset** -Objekt stammen, das aus einer Tabelle, einer datenbankexternen Quelle wie einer XML-Datei, die in eine Zeichenfolge analysiert wird, oder aus einer direkt in die Prozedur eingebetteten XML-Datei stammen kann. Sie können verschiedene Menübänder anhand mehrerer Aufrufe der **LoadCustomUI** -Methode erstellen, wobei verschiedenes XML übergeben wird, solange der Name jedes Menübands und das **id** -Attribut der Registerkarten des Menübands eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-p111">The XML markup can come from a **Recordset** object created from a table, from a source external to the database such as an XML file that you parse into a string, or from XML markup embedded directly inside the procedure. You can make different ribbons using multiple calls to the **LoadCustomUI** method, passing in different XML markup as long as the name of each ribbon and the **id** attribute of the tabs that make up the ribbon are unique.</span></span>

<span data-ttu-id="8c8cc-157">Nach Abschluss der Prozedur erstellen Sie ein AutoExec-Makro, das die Prozedur über die RunCode-Aktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-157">After the procedure is complete, you then create an AutoExec macro that calls the procedure by using the RunCode action.</span></span> <span data-ttu-id="8c8cc-158">Auf diese Weise, wenn die Anwendung gestartet wird, wird automatisch die **LoadCustomUI** -Methode ausgeführt, und alle benutzerdefinierten Multifunktionsleisten der Anwendung zur Verfügung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-158">That way, when the application is started, the **LoadCustomUI** method is automatically executed, and all of the custom ribbons are made available to the application.</span></span>

## <a name="apply-customized-ribbons-when-access-starts"></a><span data-ttu-id="8c8cc-159">Anwenden Sie benutzerdefinierte Multifunktionsleisten beim Starten von Access</span><span class="sxs-lookup"><span data-stu-id="8c8cc-159">Apply customized ribbons when Access starts</span></span>
>>>>>>> <span data-ttu-id="8c8cc-160">master</span><span class="sxs-lookup"><span data-stu-id="8c8cc-160">master</span></span>

<span data-ttu-id="8c8cc-161">Gehen Sie wie folgt vor, um eine benutzerdefiniert Oberfläche anzuwenden, die beim Starten der Anwendung zur Verfügung steht:</span><span class="sxs-lookup"><span data-stu-id="8c8cc-161">To apply a custom UI so that it is available when the application starts, use the following procedure:</span></span>

1.  <span data-ttu-id="8c8cc-162">Führen Sie den weiter oben beschriebenen Vorgang aus, um der Anwendung die benutzerdefinierten Menübänder verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-162">Follow the process described previously to make the customized ribbons available to the application.</span></span>

2.  <span data-ttu-id="8c8cc-163">Schließen Sie die Anwendung, und starten Sie sie neu.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-163">Close and then restart the application.</span></span>

<span data-ttu-id="8c8cc-164"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="8c8cc-164"><<<<<<< HEAD</span></span>
3.  <span data-ttu-id="8c8cc-165">Klicken Sie auf der **Microsoft Office-Schaltfläche**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") , und klicken Sie dann auf **Access-Optionen**.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-165">Click the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") and then click **Access Options**.</span></span>

4.  <span data-ttu-id="8c8cc-166">Klicken Sie auf die Option **Aktuelle Datenbank**, und klicken Sie dann im Abschnitt **Menüband- und Symbolleistenoptionen** auf die Liste **Menübandname**. Wählen Sie dann ein Menüband aus.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-166">Click the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, click the **Ribbon Name** list and select a ribbon.</span></span>
=======
3.  <span data-ttu-id="8c8cc-167">Wählen Sie die **Microsoft Office-Schaltfläche**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") und wählen Sie dann auf **Access-Optionen**.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-167">Choose the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") and then choose **Access Options**.</span></span>

4.  <span data-ttu-id="8c8cc-168">Wählen Sie die Option **Aktuelle Datenbank** und klicken Sie dann im Abschnitt **Menüband- und Symbolleistenoptionen** wählen Sie in der Liste **Name** des Menübands, und wählen Sie ein Menüband aus.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-168">Choose the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, choose the **Ribbon Name** list and select a ribbon.</span></span>
>>>>>>> <span data-ttu-id="8c8cc-169">master</span><span class="sxs-lookup"><span data-stu-id="8c8cc-169">master</span></span>

5.  <span data-ttu-id="8c8cc-p113">Schließen Sie jetzt die Anwendung, und starten Sie sie neu. Die ausgewählte Benutzeroberfläche wird jetzt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-p113">Now close and restart the application. The UI you selected is displayed.</span></span>

> [!NOTE]
> <span data-ttu-id="8c8cc-172">[!HINWEIS] Weitere Informationen über die Menüband-Benutzeroberfläche in anderen Office-Anwendungen finden Sie unter [Übersicht über das Office Fluent-Menüband](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="8c8cc-172">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


