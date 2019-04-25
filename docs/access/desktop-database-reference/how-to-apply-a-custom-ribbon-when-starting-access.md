---
title: Anwenden eines benutzerdefinierten Menübands beim Starten von Access
TOCTitle: Apply a custom ribbon when starting Access
description: Anwenden eines benutzerdefinierten Menübands beim Öffnen einer Datenbank in Access 2013.
ms:assetid: 9e8ddf95-35aa-4e57-8422-d770da14711e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198313(v=office.15)
ms:contentKeyID: 48546659
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 0acd99a498a74f098b08814e9f11d49b28bae097
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291957"
---
# <a name="apply-a-custom-ribbon-when-starting-access"></a><span data-ttu-id="5f939-103">Anwenden eines benutzerdefinierten Menübands beim Starten von Access</span><span class="sxs-lookup"><span data-stu-id="5f939-103">Apply a custom ribbon when starting Access</span></span>

<span data-ttu-id="5f939-104">**Gilt für:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5f939-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5f939-p101">Das Menüband verwendet textbasiertes, deklaratives XML-Markup, das die Erstellung und Anpassung des Menübands vereinfacht. Mit ein paar XML-Zeilen können Sie genau die passende Benutzeroberfläche für den Benutzer erstellen. Access bietet eine enorme Flexibilität beim Anpassen der Menüband-Benutzeroberfläche. So können Sie das Anpassungsmarkup zum Beispiel in einer Tabelle speichern, in eine VBA-Prozedur einbetten, in einer anderen Access-Datenbank speichern oder mit einem Excel-Arbeitsblatt verknüpfen. Dieses Thema beschreibt, wie angepasste Menübänder beim Öffnen einer Datenbank angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="5f939-p101">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon. With a few lines of XML, you can create just the right interface for the user. Access provides tremendous flexibility in customizing the ribbon UI. For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet. This topic describes how to apply customized ribbons when opening a database.</span></span>

## <a name="make-the-ribbon-customization-xml-available"></a><span data-ttu-id="5f939-110">XML für die Menübandanpassung verfügbar machen</span><span class="sxs-lookup"><span data-stu-id="5f939-110">Make the ribbon customization XML available</span></span>

### <a name="store-ribbon-extensibility-xml-in-a-table"></a><span data-ttu-id="5f939-111">Speichern der Menübanderweiterungs-XML in einer Tabelle</span><span class="sxs-lookup"><span data-stu-id="5f939-111">Store ribbon extensibility XML in a table</span></span>

<span data-ttu-id="5f939-p102">Eine Möglichkeit zum Verfügbarmachen der Menübandanpassungen ist, sie in einer Tabelle zu speichern. Wenn Sie die Anpassungen in einer Tabelle mit dem Namen **USysRibbons** speichern, können die Anpassungen ohne Makros oder VBA-Code implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="5f939-p102">One method that you can use to make ribbon customizations available is to store them in a table. If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="5f939-114">**USysRibbons** ist eine vom Benutzer erstellte Systemtabelle.</span><span class="sxs-lookup"><span data-stu-id="5f939-114">**USysRibbons** is a user-created system table.</span></span> <span data-ttu-id="5f939-115">Die Tabelle muss mit bestimmten Spaltennamen erstellt werden, damit die Menübandanpassungen implementiert werden können.</span><span class="sxs-lookup"><span data-stu-id="5f939-115">The table must be created using specific column names in order for the ribbon customizations to be implemented.</span></span> 

<span data-ttu-id="5f939-116">Die folgende Tabelle enthält die zu verwendenden Einstellungen zum Erstellen der **USysRibbons**-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="5f939-116">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5f939-117">Spaltenname</span><span class="sxs-lookup"><span data-stu-id="5f939-117">Column name</span></span></p></th>
<th><p><span data-ttu-id="5f939-118">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5f939-118">Data type</span></span></p></th>
<th><p><span data-ttu-id="5f939-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f939-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f939-120"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="5f939-120"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="5f939-121">Text</span><span class="sxs-lookup"><span data-stu-id="5f939-121">Text</span></span></p></td>
<td><p><span data-ttu-id="5f939-122">Enthält den Namen des benutzerdefinierten Menübands, das dieser Anpassung zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5f939-122">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f939-123"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="5f939-123"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="5f939-124">Memo</span><span class="sxs-lookup"><span data-stu-id="5f939-124">Memo</span></span></p></td>
<td><p><span data-ttu-id="5f939-125">Enthält die Menübanderweiterungs-XML (RibbonX) zur Definition der Menübandanpassung.</span><span class="sxs-lookup"><span data-stu-id="5f939-125">Contains the Ribbon Extensibility XML (RibbonX) that  defines the ribbon customization.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="load-ribbon-extensibility-xml-programmatically"></a><span data-ttu-id="5f939-126">Menübanderweiterungs-XML programmatisch laden</span><span class="sxs-lookup"><span data-stu-id="5f939-126">Load ribbon extensibility XML programmatically</span></span>

<span data-ttu-id="5f939-p104">Mit der **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** -Methode können Sie Menübandanpassungen programmatisch laden. Um das Menüband zu erstellen und der Anwendung zur Verfügung zu stellen, erstellen Sie in der Regel zunächst ein Modul in der Datenbank mit einer Prozedur, die die **LoadCustomUI** -Methode aufruft, sodass der Name des Menübands und das XML-Anpassungsmarkup übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="5f939-p104">You can use the **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** method to load ribbon customizations programmatically. Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>

<span data-ttu-id="5f939-p105">Das XML-Markup kann von einem **Recordset**-Objekt stammen, das aus einer Tabelle, einer datenbankexternen Quelle wie einer XML-Datei, die in eine Zeichenfolge analysiert wird, oder aus einer direkt in die Prozedur eingebetteten XML-Datei stammen kann. Sie können verschiedene Menübänder anhand mehrerer Aufrufe der **LoadCustomUI**-Methode erstellen, wobei verschiedenes XML übergeben wird, solange der Name jedes Menübands und das **id**-Attribut der Registerkarten des Menübands eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="5f939-p105">The XML markup can come from a **Recordset** object created from a table, from a source external to the database such as an XML file that you parse into a string, or from XML markup embedded directly inside the procedure. You can make different ribbons using multiple calls to the **LoadCustomUI** method, passing in different XML markup as long as the name of each ribbon and the **id** attribute of the tabs that make up the ribbon are unique.</span></span>

<span data-ttu-id="5f939-131">Nachdem der Vorgang abgeschlossen ist, erstellen Sie ein AutoExec-Makro, das die Prozedur mithilfe der RunCode-Aktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="5f939-131">After the procedure is complete, you then create an AutoExec macro that calls the procedure by using the RunCode action.</span></span> <span data-ttu-id="5f939-132">Auf diese Weise wird beim Starten der Anwendung die **LoadCustomUI**-Methode automatisch ausgeführt, und alle benutzerdefinierten Menübänder werden für die Anwendung verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="5f939-132">That way, when the application is started, the **LoadCustomUI** method is automatically executed and all of the custom ribbons are made available to the application.</span></span>

## <a name="apply-customized-ribbons-when-access-starts"></a><span data-ttu-id="5f939-133">Anwenden von angepassten Menübändern beim Starten von Access</span><span class="sxs-lookup"><span data-stu-id="5f939-133">Apply customized ribbons when Access starts</span></span>

<span data-ttu-id="5f939-134">Gehen Sie wie folgt vor, um eine benutzerdefiniert Oberfläche anzuwenden, die beim Starten der Anwendung zur Verfügung steht:</span><span class="sxs-lookup"><span data-stu-id="5f939-134">To apply a custom UI so that it is available when the application starts, use the following procedure:</span></span>

1.  <span data-ttu-id="5f939-135">Führen Sie den weiter oben beschriebenen Vorgang aus, um der Anwendung die benutzerdefinierten Menübänder verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="5f939-135">Follow the process described previously to make the customized ribbons available to the application.</span></span>

2.  <span data-ttu-id="5f939-136">Schließen Sie die Anwendung, und starten Sie sie neu.</span><span class="sxs-lookup"><span data-stu-id="5f939-136">Close and then restart the application.</span></span>

3.  <span data-ttu-id="5f939-137">Klicken Sie auf die **Microsoft Office-Schaltfläche**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102"), und wählen Sie dann **Access-Optionen** aus.</span><span class="sxs-lookup"><span data-stu-id="5f939-137">Choose the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") and then choose **Access Options**.</span></span>

4.  <span data-ttu-id="5f939-138">Klicken Sie auf die Option **Aktuelle Datenbank**, und klicken Sie dann im Abschnitt **Menüband- und Symbolleistenoptionen** auf die Liste **Menübandname**. Wählen Sie dann ein Menüband aus.</span><span class="sxs-lookup"><span data-stu-id="5f939-138">Click the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, click the **Ribbon Name** list and select a ribbon.</span></span>

5.  <span data-ttu-id="5f939-p107">Schließen Sie jetzt die Anwendung, und starten Sie sie neu. Die ausgewählte Benutzeroberfläche wird jetzt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5f939-p107">Now close and restart the application. The UI you selected is displayed.</span></span>

> [!NOTE]
> <span data-ttu-id="5f939-141">Weitere Informationen über die Menüband-Benutzeroberfläche in anderen Office-Anwendungen finden Sie unter [Übersicht über das Office Fluent-Menüband](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="5f939-141">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


