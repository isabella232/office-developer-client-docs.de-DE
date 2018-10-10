---
title: Ausblenden des Menübands beim Starten von Access
TOCTitle: Hide the ribbon when Access starts
ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15)
ms:contentKeyID: 48548817
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b2b3e28157662a585fa03353da92a598b96bd2c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473315"
---
# <a name="hide-the-ribbon-when-access-starts"></a><span data-ttu-id="5e585-102">Ausblenden des Menübands beim Starten von Access</span><span class="sxs-lookup"><span data-stu-id="5e585-102">Hide the ribbon when Access starts</span></span>

<span data-ttu-id="5e585-103">**Gilt für:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5e585-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="5e585-p101">Standardmäßig stellt Microsoft Access keine Methode zum Ausblenden des Menübands bereit. In diesem Thema wird erläutert, wie Sie ein benutzerdefiniertes Menüband laden, in dem alle integrierten Registerkarten ausgeblendet sind.</span><span class="sxs-lookup"><span data-stu-id="5e585-p101">By default, Microsoft Access does not provide a method for hiding the ribbon. This topic describes how to load a customized ribbon that hides all of the built-in tabs.</span></span>

<span data-ttu-id="5e585-106">Damit beim Start von Access ein benutzerdefiniertes Menüband geladen wird, sollten Sie die Einstellungen für dieses Menüband in einer Tabelle mit der Bezeichnung **USysRibbons** speichern.</span><span class="sxs-lookup"><span data-stu-id="5e585-106">To load the customized ribbon when Access starts, you should store its settings in a table named **USysRibbons**.</span></span>

<span data-ttu-id="5e585-p102">Die Tabelle **USysRibbons** muss unter Verwendung bestimmter Spaltennamen erstellt werden, damit die Anpassungen des Menübands implementiert werden. In der folgenden Tabelle sind die Einstellungen beschrieben, die beim Erstellen der Tabelle **USysRibbons** verwendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5e585-p102">The **USysRibbons** table must be created using specific column names in order for the ribbon customizations to be implemented. The following table lists the settings to use when creating the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5e585-109">Spaltenname</span><span class="sxs-lookup"><span data-stu-id="5e585-109">Column Name</span></span></p></th>
<th><p><span data-ttu-id="5e585-110">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5e585-110">Data Type</span></span></p></th>
<th><p><span data-ttu-id="5e585-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e585-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5e585-112"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="5e585-112"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="5e585-113">Text</span><span class="sxs-lookup"><span data-stu-id="5e585-113">Text</span></span></p></td>
<td><p><span data-ttu-id="5e585-114">Enthält den Namen des benutzerdefinierten Menübands, das dieser Anpassung zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5e585-114">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e585-115"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="5e585-115"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="5e585-116">Memo</span><span class="sxs-lookup"><span data-stu-id="5e585-116">Memo</span></span></p></td>
<td><p><span data-ttu-id="5e585-117">Enthält die Menübanderewiterungs-XML (RibbonX) zur Definition der Menübandanpassung.</span><span class="sxs-lookup"><span data-stu-id="5e585-117">Contains the Ribbon Extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5e585-118">In der folgenden Tabelle werden die Einstellungen zum Anpassen des Menübands aufgelistet, die in der **USysRibbons** -Tabelle gespeichert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5e585-118">The following table lists the ribbon customization settings to store in the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5e585-119">Spaltenname</span><span class="sxs-lookup"><span data-stu-id="5e585-119">Column Name</span></span></p></th>
<th><p><span data-ttu-id="5e585-120">Wert</span><span class="sxs-lookup"><span data-stu-id="5e585-120">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5e585-121"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="5e585-121"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="5e585-122">HideTheRibbon</span><span class="sxs-lookup"><span data-stu-id="5e585-122">HideTheRibbon</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e585-123"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="5e585-123"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="5e585-124">&lt;CustomUI Xmlns =&quot;https://schemas.microsoft.com/office/2006/01/CustomUI&quot; &gt; &lt;des Menübands StartFromScratch =&quot;true&quot;/&gt;&lt;/CustomUI&gt;</span><span class="sxs-lookup"><span data-stu-id="5e585-124">&lt;CustomUI xmlns=&quot;https://schemas.microsoft.com/office/2006/01/CustomUI&quot;&gt; &lt;ribbon startFromScratch=&quot;true&quot;/&gt;&lt;/CustomUI&gt;</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="applying-a-custom-ribbon-when-access-starts"></a><span data-ttu-id="5e585-125">Anwenden eines benutzerdefinierten Menübands beim Starten von Access</span><span class="sxs-lookup"><span data-stu-id="5e585-125">Applying a Custom Ribbon When Access Starts</span></span>

<span data-ttu-id="5e585-126">Wenn Sie ein benutzerdefiniertes Menüband so anwenden möchten, dass es beim Starten der Anwendung zur Verfügung steht, führen Sie folgende Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="5e585-126">To apply a custom ribbon so that it is available when the application starts, use the following procedure:</span></span>

1.  <span data-ttu-id="5e585-127">Führen Sie den oben beschriebenen Vorgang aus, um das benutzerdefinierte Menüband in der Anwendung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="5e585-127">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="5e585-128">Schließen Sie die Anwendung, und starten Sie sie dann neu.</span><span class="sxs-lookup"><span data-stu-id="5e585-128">Close and then restart the application.</span></span>

3.  <span data-ttu-id="5e585-129">Klicken Sie auf der **Microsoft Office-Schaltfläche**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") , und klicken Sie dann auf **Access-Optionen**.</span><span class="sxs-lookup"><span data-stu-id="5e585-129">Click the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") and then click **Access Options**.</span></span>

4.  <span data-ttu-id="5e585-130">Klicken Sie auf die Option **Aktuelle Datenbank**, und klicken Sie dann im Abschnitt **Menüband- und Symbolleistenoptionen** auf die Liste **Name des Menübands**. Wählen Sie **HideTheRibbon** aus.</span><span class="sxs-lookup"><span data-stu-id="5e585-130">Click the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, click the **Ribbon Name** list and select **HideTheRibbon**.</span></span>

5.  <span data-ttu-id="5e585-131">Schließen Sie die Anwendung, und starten Sie sie neu.</span><span class="sxs-lookup"><span data-stu-id="5e585-131">Close and then restart the application.</span></span>

> [!NOTE]
> <span data-ttu-id="5e585-132">[!HINWEIS] Weitere Informationen über die Menüband-Benutzeroberfläche in anderen Office-Anwendungen finden Sie unter [Übersicht über das Office Fluent-Menüband](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="5e585-132">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


