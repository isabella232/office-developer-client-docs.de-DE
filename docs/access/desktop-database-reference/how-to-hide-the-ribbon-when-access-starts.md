---
<span data-ttu-id="7fc17-101">Titel: Ausblenden des Menübands beim Starten von Access TOCTitle: Ausblenden des Menübands beim Starten von Access <<<<<<< HEAD Ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574 Ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15) Ms:contentKeyID: 48548817 ms.date: 09/18/2015 === Beschreibung: wie ein benutzerdefiniertes Menüband geladen, die alle integrierten Registerkarten in Access 2013 ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="7fc17-101">title: Hide the ribbon when Access starts TOCTitle: Hide the ribbon when Access starts <<<<<<< HEAD ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574 ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15) ms:contentKeyID: 48548817 ms.date: 09/18/2015 ======= description: How to load a customized ribbon that hides all of the built-in tabs in Access 2013.</span></span>
<span data-ttu-id="7fc17-102">MS:AssetId: f98bab58-8094-1c56-f70b-ced2e7849574 Ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15) Ms:contentKeyID: 48548817 ms.date: 10/16/2018</span><span class="sxs-lookup"><span data-stu-id="7fc17-102">ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574 ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15) ms:contentKeyID: 48548817 ms.date: 10/16/2018</span></span>
>>>>>>> <span data-ttu-id="7fc17-103">Master-Shape Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="7fc17-103">master mtps_version: v=office.15</span></span>
---

# <a name="hide-the-ribbon-when-access-starts"></a><span data-ttu-id="7fc17-104">Ausblenden des Menübands beim Starten von Access</span><span class="sxs-lookup"><span data-stu-id="7fc17-104">Hide the ribbon when Access starts</span></span>

<span data-ttu-id="7fc17-105">**Gilt für:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7fc17-105">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="7fc17-p102">Standardmäßig stellt Microsoft Access keine Methode zum Ausblenden des Menübands bereit. In diesem Thema wird erläutert, wie Sie ein benutzerdefiniertes Menüband laden, in dem alle integrierten Registerkarten ausgeblendet sind.</span><span class="sxs-lookup"><span data-stu-id="7fc17-p102">By default, Microsoft Access does not provide a method for hiding the ribbon. This topic describes how to load a customized ribbon that hides all of the built-in tabs.</span></span>

<span data-ttu-id="7fc17-108">Damit beim Start von Access ein benutzerdefiniertes Menüband geladen wird, sollten Sie die Einstellungen für dieses Menüband in einer Tabelle mit der Bezeichnung **USysRibbons** speichern.</span><span class="sxs-lookup"><span data-stu-id="7fc17-108">To load the customized ribbon when Access starts, you should store its settings in a table named **USysRibbons**.</span></span>

<span data-ttu-id="7fc17-109"><<<<<<< HEAD die **USysRibbons** -Tabelle mithilfe von bestimmten Spaltennamen in der Reihenfolge für die menübandanpassungen implementiert werden erstellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="7fc17-109"><<<<<<< HEAD The **USysRibbons** table must be created using specific column names in order for the ribbon customizations to be implemented.</span></span> <span data-ttu-id="7fc17-110">In der folgenden Tabelle sind die Einstellungen beschrieben, die beim Erstellen der Tabelle **USysRibbons** verwendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="7fc17-110">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>
<span data-ttu-id="7fc17-111">=== Die **USysRibbons** -Tabelle muss mit bestimmten Spaltennamen für die menübandanpassungen implementiert werden erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7fc17-111">======= The **USysRibbons** table must be created using specific column names for the ribbon customizations to be implemented.</span></span> 

<span data-ttu-id="7fc17-112">In der folgenden Tabelle sind die Einstellungen beschrieben, die beim Erstellen der Tabelle **USysRibbons** verwendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="7fc17-112">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>
>>>>>>> <span data-ttu-id="7fc17-113">master</span><span class="sxs-lookup"><span data-stu-id="7fc17-113">master</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<span data-ttu-id="7fc17-114"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="7fc17-114"><<<<<<< HEAD</span></span>
<th><p><span data-ttu-id="7fc17-115">Spaltenname</span><span class="sxs-lookup"><span data-stu-id="7fc17-115">Column Name</span></span></p></th>
<th><p><span data-ttu-id="7fc17-116">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7fc17-116">Data Type</span></span></p></th>
=======
<th><p><span data-ttu-id="7fc17-117">Spaltenname</span><span class="sxs-lookup"><span data-stu-id="7fc17-117">Column name</span></span></p></th>
<th><p><span data-ttu-id="7fc17-118">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7fc17-118">Data type</span></span></p></th><span data-ttu-id="7fc17-119">
>>>>>>>Master-Shape</span><span class="sxs-lookup"><span data-stu-id="7fc17-119">
>>>>>>> master</span></span>
<th><p><span data-ttu-id="7fc17-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7fc17-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7fc17-121"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="7fc17-121"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="7fc17-122">Text</span><span class="sxs-lookup"><span data-stu-id="7fc17-122">Text</span></span></p></td>
<td><p><span data-ttu-id="7fc17-123">Enthält den Namen des benutzerdefinierten Menübands, das dieser Anpassung zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7fc17-123">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7fc17-124"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="7fc17-124"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="7fc17-125">Memo</span><span class="sxs-lookup"><span data-stu-id="7fc17-125">Memo</span></span></p></td>
<span data-ttu-id="7fc17-126"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="7fc17-126"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="7fc17-127">Enthält die Menübanderewiterungs-XML (RibbonX) zur Definition der Menübandanpassung.</span><span class="sxs-lookup"><span data-stu-id="7fc17-127">Contains the Ribbon Extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
=======
<td><p><span data-ttu-id="7fc17-128">Enthält die Menüband-Erweiterbarkeits-XML (RibbonX), die die menübandanpassung definiert wird.</span><span class="sxs-lookup"><span data-stu-id="7fc17-128">Contains the ribbon extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td><span data-ttu-id="7fc17-129">
>>>>>>>Master-Shape</span><span class="sxs-lookup"><span data-stu-id="7fc17-129">
>>>>>>> master</span></span>
</tr>
</tbody>
</table>

<span data-ttu-id="7fc17-130"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="7fc17-130"><<<<<<< HEAD</span></span>

<span data-ttu-id="7fc17-131">In der folgenden Tabelle werden die Einstellungen zum Anpassen des Menübands aufgelistet, die in der **USysRibbons** -Tabelle gespeichert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="7fc17-131">The following table lists the ribbon customization settings to store in the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7fc17-132">Spaltenname</span><span class="sxs-lookup"><span data-stu-id="7fc17-132">Column Name</span></span></p></th>
<th><p><span data-ttu-id="7fc17-133">Wert</span><span class="sxs-lookup"><span data-stu-id="7fc17-133">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7fc17-134"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="7fc17-134"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="7fc17-135">HideTheRibbon</span><span class="sxs-lookup"><span data-stu-id="7fc17-135">HideTheRibbon</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7fc17-136"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="7fc17-136"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="7fc17-137">&lt;CustomUI Xmlns =&quot;https://schemas.microsoft.com/office/2006/01/CustomUI&quot; &gt; &lt;des Menübands StartFromScratch =&quot;true&quot;/&gt;&lt;/CustomUI&gt;</span><span class="sxs-lookup"><span data-stu-id="7fc17-137">&lt;CustomUI xmlns=&quot;https://schemas.microsoft.com/office/2006/01/CustomUI&quot;&gt; &lt;ribbon startFromScratch=&quot;true&quot;/&gt;&lt;/CustomUI&gt;</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="applying-a-custom-ribbon-when-access-starts"></a><span data-ttu-id="7fc17-138">Anwenden eines benutzerdefinierten Menübands beim Starten von Access</span><span class="sxs-lookup"><span data-stu-id="7fc17-138">Applying a Custom Ribbon When Access Starts</span></span>
=======
<br/>

<span data-ttu-id="7fc17-139">In der folgenden Tabelle werden die Einstellungen zum Anpassen des Menübands aufgelistet, die in der **USysRibbons** -Tabelle gespeichert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="7fc17-139">The following table lists the ribbon customization settings to store in the **USysRibbons** table.</span></span>

|<span data-ttu-id="7fc17-140">Spaltenname</span><span class="sxs-lookup"><span data-stu-id="7fc17-140">Column name</span></span>|<span data-ttu-id="7fc17-141">Wert</span><span class="sxs-lookup"><span data-stu-id="7fc17-141">Value</span></span>|
|:----------|:----|
|<span data-ttu-id="7fc17-142">**RibbonName**</span><span class="sxs-lookup"><span data-stu-id="7fc17-142">**RibbonName**</span></span>|<span data-ttu-id="7fc17-143">HideTheRibbon</span><span class="sxs-lookup"><span data-stu-id="7fc17-143">HideTheRibbon</span></span>|
|<span data-ttu-id="7fc17-144">**RibbonXML**</span><span class="sxs-lookup"><span data-stu-id="7fc17-144">**RibbonXML**</span></span>|`<CustomUI xmlns="https://schemas.microsoft.com/office/2006/01/CustomUI"> <ribbon startFromScratch="true"/></CustomUI>`|


## <a name="apply-a-custom-ribbon-when-access-starts"></a><span data-ttu-id="7fc17-145">Anwenden einer benutzerdefinierten Multifunktionsleiste beim Starten von Access</span><span class="sxs-lookup"><span data-stu-id="7fc17-145">Apply a custom ribbon when Access starts</span></span>
>>>>>>> <span data-ttu-id="7fc17-146">master</span><span class="sxs-lookup"><span data-stu-id="7fc17-146">master</span></span>

<span data-ttu-id="7fc17-147">Wenn Sie ein benutzerdefiniertes Menüband so anwenden möchten, dass es beim Starten der Anwendung zur Verfügung steht, führen Sie folgende Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="7fc17-147">To apply a custom ribbon so that it is available when the application starts, use the following procedure:</span></span>

1.  <span data-ttu-id="7fc17-148">Führen Sie den oben beschriebenen Vorgang aus, um das benutzerdefinierte Menüband in der Anwendung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7fc17-148">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="7fc17-149">Schließen Sie die Anwendung, und starten Sie sie dann neu.</span><span class="sxs-lookup"><span data-stu-id="7fc17-149">Close and then restart the application.</span></span>

<span data-ttu-id="7fc17-150"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="7fc17-150"><<<<<<< HEAD</span></span>
3.  <span data-ttu-id="7fc17-151">Klicken Sie auf der **Microsoft Office-Schaltfläche**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") , und klicken Sie dann auf **Access-Optionen**.</span><span class="sxs-lookup"><span data-stu-id="7fc17-151">Click the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") and then click **Access Options**.</span></span>

4.  <span data-ttu-id="7fc17-152">Klicken Sie auf die Option **Aktuelle Datenbank**, und klicken Sie dann im Abschnitt **Menüband- und Symbolleistenoptionen** auf die Liste **Name des Menübands**. Wählen Sie **HideTheRibbon** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc17-152">Click the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, click the **Ribbon Name** list and select **HideTheRibbon**.</span></span>
=======
3.  <span data-ttu-id="7fc17-153">Wählen Sie die **Microsoft Office-Schaltfläche**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102"), und klicken Sie dann auf **Access-Optionen**.</span><span class="sxs-lookup"><span data-stu-id="7fc17-153">Choose the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102"), and then choose **Access Options**.</span></span>

4.  <span data-ttu-id="7fc17-154">Wählen Sie die Option **Aktuelle Datenbank** und klicken Sie dann im Abschnitt **Menüband- und Symbolleistenoptionen** wählen Sie in der Liste **Name** des Menübands, und **Klicken**.</span><span class="sxs-lookup"><span data-stu-id="7fc17-154">Choose the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, choose the **Ribbon Name** list and select **HideTheRibbon**.</span></span>
>>>>>>> <span data-ttu-id="7fc17-155">master</span><span class="sxs-lookup"><span data-stu-id="7fc17-155">master</span></span>

5.  <span data-ttu-id="7fc17-156">Schließen Sie die Anwendung, und starten Sie sie neu.</span><span class="sxs-lookup"><span data-stu-id="7fc17-156">Close and then restart the application.</span></span>

> [!NOTE]
> <span data-ttu-id="7fc17-157">[!HINWEIS] Weitere Informationen über die Menüband-Benutzeroberfläche in anderen Office-Anwendungen finden Sie unter [Übersicht über das Office Fluent-Menüband](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="7fc17-157">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


