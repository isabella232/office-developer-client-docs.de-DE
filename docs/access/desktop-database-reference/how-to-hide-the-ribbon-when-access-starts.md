---
title: Ausblenden des Menübands beim Starten von Access
TOCTitle: Hide the ribbon when Access starts
description: Informationen zum Laden eines benutzerdefinierten Menübands, in dem alle integrierten Registerkarten in Access 2013 ausgeblendet sind.
ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15)
ms:contentKeyID: 48548817
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 384a575ae5e15b75ba7b0b891529c695cc3de599
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537829"
---
# <a name="hide-the-ribbon-when-access-starts"></a><span data-ttu-id="cd315-103">Ausblenden des Menübands beim Starten von Access</span><span class="sxs-lookup"><span data-stu-id="cd315-103">Hide the ribbon when Access starts</span></span>

<span data-ttu-id="cd315-104">**Gilt für:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="cd315-104">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="cd315-p101">Standardmäßig stellt Microsoft Access keine Methode zum Ausblenden des Menübands bereit. In diesem Thema wird erläutert, wie Sie ein benutzerdefiniertes Menüband laden, in dem alle integrierten Registerkarten ausgeblendet sind.</span><span class="sxs-lookup"><span data-stu-id="cd315-p101">By default, Microsoft Access does not provide a method for hiding the ribbon. This topic describes how to load a customized ribbon that hides all of the built-in tabs.</span></span>

<span data-ttu-id="cd315-107">Damit beim Start von Access ein benutzerdefiniertes Menüband geladen wird, sollten Sie die Einstellungen für dieses Menüband in einer Tabelle mit der Bezeichnung **USysRibbons** speichern.</span><span class="sxs-lookup"><span data-stu-id="cd315-107">To load the customized ribbon when Access starts, you should store its settings in a table named **USysRibbons**.</span></span>

<span data-ttu-id="cd315-108">Die Tabelle **USysRibbons** muss unter Verwendung bestimmter Spaltennamen erstellt werden, damit die Anpassungen des Menübands implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="cd315-108">The **USysRibbons** table must be created using specific column names for the ribbon customizations to be implemented.</span></span> 

<span data-ttu-id="cd315-109">Die folgende Tabelle enthält die zu verwendenden Einstellungen zum Erstellen der **USysRibbons**-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="cd315-109">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cd315-110">Spaltenname</span><span class="sxs-lookup"><span data-stu-id="cd315-110">Column name</span></span></p></th>
<th><p><span data-ttu-id="cd315-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="cd315-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="cd315-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cd315-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd315-113"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="cd315-113"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="cd315-114">Text</span><span class="sxs-lookup"><span data-stu-id="cd315-114">Text</span></span></p></td>
<td><p><span data-ttu-id="cd315-115">Enthält den Namen des benutzerdefinierten Menübands, das dieser Anpassung zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cd315-115">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd315-116"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="cd315-116"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="cd315-117">Memo</span><span class="sxs-lookup"><span data-stu-id="cd315-117">Memo</span></span></p></td>
<td><p><span data-ttu-id="cd315-118">Enthält die Menübanderweiterungs-XML (RibbonX) zur Definition der Menübandanpassung.</span><span class="sxs-lookup"><span data-stu-id="cd315-118">Contains the ribbon extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="cd315-119">In der folgenden Tabelle sind die Einstellungen für die Menübandanpassung aufgeführt, die in der **USysRibbons**-Tabelle gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cd315-119">The following table lists the ribbon customization settings to store in the **USysRibbons** table.</span></span>

|<span data-ttu-id="cd315-120">Spaltenname</span><span class="sxs-lookup"><span data-stu-id="cd315-120">Column name</span></span>|<span data-ttu-id="cd315-121">Wert</span><span class="sxs-lookup"><span data-stu-id="cd315-121">Value</span></span>|
|:----------|:----|
|<span data-ttu-id="cd315-122">**RibbonName**</span><span class="sxs-lookup"><span data-stu-id="cd315-122">**RibbonName**</span></span>|<span data-ttu-id="cd315-123">HideTheRibbon</span><span class="sxs-lookup"><span data-stu-id="cd315-123">HideTheRibbon</span></span>|
|<span data-ttu-id="cd315-124">**RibbonXML**</span><span class="sxs-lookup"><span data-stu-id="cd315-124">**RibbonXML**</span></span>|`<CustomUI xmlns="http://schemas.microsoft.com/office/2006/01/CustomUI"> <ribbon startFromScratch="true"/></CustomUI>`|


## <a name="apply-a-custom-ribbon-when-access-starts"></a><span data-ttu-id="cd315-125">Anwenden eines benutzerdefinierten Menübands beim Starten von Access</span><span class="sxs-lookup"><span data-stu-id="cd315-125">Apply a custom ribbon when Access starts</span></span>

<span data-ttu-id="cd315-126">Wenn Sie ein benutzerdefiniertes Menüband so anwenden möchten, dass es beim Starten der Anwendung zur Verfügung steht, führen Sie folgende Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="cd315-126">To apply a custom ribbon so that it is available when the application starts, use the following procedure:</span></span>

1.  <span data-ttu-id="cd315-127">Führen Sie den oben beschriebenen Vorgang aus, um das benutzerdefinierte Menüband in der Anwendung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="cd315-127">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="cd315-128">Schließen Sie die Anwendung, und starten Sie sie dann neu.</span><span class="sxs-lookup"><span data-stu-id="cd315-128">Close and then restart the application.</span></span>

3.  <span data-ttu-id="cd315-129">Klicken Sie auf die **Microsoft Office-Schaltfläche**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102"), und wählen Sie dann **Access-Optionen** aus.</span><span class="sxs-lookup"><span data-stu-id="cd315-129">Choose the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102"), and then choose **Access Options**.</span></span>

4.  <span data-ttu-id="cd315-130">Klicken Sie auf die Option **Aktuelle Datenbank**, und klicken Sie dann im Abschnitt **Menüband- und Symbolleistenoptionen** auf die Liste **Menübandname**. Wählen Sie dann **HideTheRibbon** aus.</span><span class="sxs-lookup"><span data-stu-id="cd315-130">Choose the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, choose the **Ribbon Name** list and select **HideTheRibbon**.</span></span>

5.  <span data-ttu-id="cd315-131">Schließen Sie die Anwendung, und starten Sie sie neu.</span><span class="sxs-lookup"><span data-stu-id="cd315-131">Close and then restart the application.</span></span>

> [!NOTE]
> <span data-ttu-id="cd315-132">Weitere Informationen über die Menüband-Benutzeroberfläche in anderen Office-Anwendungen finden Sie unter [Übersicht über das Office Fluent-Menüband](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="cd315-132">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


