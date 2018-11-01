---
title: Anwenden eines benutzerdefinierten Menübands auf ein Formular oder einen Bericht
TOCTitle: Apply a custom ribbon to a form or report
description: Informationen zum Anwenden von benutzerdefinierten Menüleisten beim Laden eines Formulars oder Berichts in Access 2013.
ms:assetid: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15)
ms:contentKeyID: 48545865
ms.date: 10/16/2018
mtps_version: v=office.15
ms.openlocfilehash: e494985054ffd91440f3aff6eb671b781a5f65d7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888825"
---
# <a name="apply-a-custom-ribbon-to-a-form-or-report"></a><span data-ttu-id="ccab7-103">Anwenden eines benutzerdefinierten Menübands auf ein Formular oder einen Bericht</span><span class="sxs-lookup"><span data-stu-id="ccab7-103">Apply a custom ribbon to a form or report</span></span>

<span data-ttu-id="ccab7-104">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ccab7-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ccab7-105">Das Menüband verwendet textbasiertes, deklaratives XML-Markup, das die Erstellung und Anpassung des Menübands vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="ccab7-105">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon.</span></span> <span data-ttu-id="ccab7-106">Mit ein paar XML-Zeilen können Sie genau die passende Benutzeroberfläche für den Benutzer erstellen.</span><span class="sxs-lookup"><span data-stu-id="ccab7-106">With a few lines of XML, you can create just the right interface for the user.</span></span> <span data-ttu-id="ccab7-107">Access bietet Flexibilität beim Anpassen der Menüband-Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="ccab7-107">Access provides flexibility in customizing the ribbon user interface.</span></span> 

<span data-ttu-id="ccab7-108">So können Sie das Anpassungsmarkup zum Beispiel in einer Tabelle speichern, in eine VBA-Prozedur einbetten, in einer anderen Access-Datenbank speichern oder mit einem Excel-Arbeitsblatt verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="ccab7-108">For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet.</span></span> <span data-ttu-id="ccab7-109">Dieses Thema beschreibt, wie angepasste Menübänder beim Laden eines Formulars oder eines Berichts angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="ccab7-109">This topic describes how to apply customized ribbons when loading a form or report.</span></span>

## <a name="make-the-ribbon-customization-xml-available"></a><span data-ttu-id="ccab7-110">Anpassung der Multifunktionsleiste XML verfügbar machen</span><span class="sxs-lookup"><span data-stu-id="ccab7-110">Make the ribbon customization XML available</span></span>

### <a name="store-ribbon-extensibility-xml-in-a-table"></a><span data-ttu-id="ccab7-111">Menüband-Erweiterbarkeits-XML in einer Tabelle speichern</span><span class="sxs-lookup"><span data-stu-id="ccab7-111">Store ribbon extensibility XML in a table</span></span>

<span data-ttu-id="ccab7-p103">Eine Möglichkeit zum Verfügbarmachen der Menübandanpassungen ist, sie in einer Tabelle zu speichern. Wenn Sie die Anpassungen in einer Tabelle mit dem Namen **USysRibbons** speichern, können die Anpassungen ohne Makros oder VBA-Code implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="ccab7-p103">One method that you can use to make ribbon customizations available is to store them in a table. If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="ccab7-114">**USysRibbons** ist eine vom Benutzer erstellte Systemtabelle.</span><span class="sxs-lookup"><span data-stu-id="ccab7-114">**USysRibbons** is a user-created system table.</span></span> <span data-ttu-id="ccab7-115">Die Tabelle muss mit bestimmten Spaltennamen für die menübandanpassungen implementiert werden erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ccab7-115">The table must be created using specific column names for the ribbon customizations to be implemented.</span></span> 

<span data-ttu-id="ccab7-116">In der folgenden Tabelle sind die Einstellungen beschrieben, die beim Erstellen der Tabelle **USysRibbons** verwendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="ccab7-116">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ccab7-117">Spaltenname</span><span class="sxs-lookup"><span data-stu-id="ccab7-117">Column name</span></span></p></th>
<th><p><span data-ttu-id="ccab7-118">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ccab7-118">Data type</span></span></p></th>
<th><p><span data-ttu-id="ccab7-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ccab7-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ccab7-120"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="ccab7-120"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="ccab7-121">Text</span><span class="sxs-lookup"><span data-stu-id="ccab7-121">Text</span></span></p></td>
<td><p><span data-ttu-id="ccab7-122">Enthält den Namen des benutzerdefinierten Menübands, das dieser Anpassung zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ccab7-122">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccab7-123"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="ccab7-123"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="ccab7-124">Memo</span><span class="sxs-lookup"><span data-stu-id="ccab7-124">Memo</span></span></p></td>
<td><p><span data-ttu-id="ccab7-125">Enthält die Menüband-Erweiterbarkeits-XML (RibbonX), die die menübandanpassung definiert wird.</span><span class="sxs-lookup"><span data-stu-id="ccab7-125">Contains the ribbon extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="load-ribbon-extensibility-xml-programmatically"></a><span data-ttu-id="ccab7-126">Menüband-Erweiterbarkeits-XML programmgesteuert laden</span><span class="sxs-lookup"><span data-stu-id="ccab7-126">Load ribbon extensibility XML programmatically</span></span>

<span data-ttu-id="ccab7-p105">Mit der **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** -Methode können Sie Menübandanpassungen programmatisch laden. Um das Menüband zu erstellen und der Anwendung zur Verfügung zu stellen, erstellen Sie in der Regel zunächst ein Modul in der Datenbank mit einer Prozedur, die die **LoadCustomUI** -Methode aufruft, sodass der Name des Menübands und das XML-Anpassungsmarkup übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="ccab7-p105">You can use the **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** method to load ribbon customizations programmatically. Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>

<span data-ttu-id="ccab7-p106">Das XML-Markup kann von einem **Recordset** -Objekt stammen, das aus einer Tabelle, einer datenbankexternen Quelle wie einer XML-Datei, die in eine Zeichenfolge analysiert wird, oder aus einer direkt in die Prozedur eingebetteten XML-Datei stammen kann. Sie können verschiedene Menübänder anhand mehrerer Aufrufe der **LoadCustomUI** -Methode erstellen, wobei verschiedenes XML übergeben wird, solange der Name jedes Menübands und das **id** -Attribut der Registerkarten des Menübands eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="ccab7-p106">The XML markup can come from a **Recordset** object created from a table, from a source external to the database such as an XML file that you parse into a string, or from XML markup embedded directly inside the procedure. You can make different ribbons using multiple calls to the **LoadCustomUI** method, passing in different XML markup as long as the name of each ribbon and the **id** attribute of the tabs that make up the ribbon are unique.</span></span>

<span data-ttu-id="ccab7-p107">Nach Abschluss der Prozedur erstellen Sie ein AutoExec-Makro, das die Prozedur über die RunCode-Aktion aufruft. Auf diese Weise wird beim Starten der Anwendung die **LoadCustomUI** -Methode automatisch ausgeführt, und alle benutzerdefinierten Menübänder werden für die Anwendung verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="ccab7-p107">After the procedure is complete, you then create an AutoExec macro that calls the procedure by using the RunCode action. That way, when the application is started, the **LoadCustomUI** method is automatically executed and all of the custom ribbons are made available to the application.</span></span>

## <a name="assign-custom-ribbons-to-forms-or-reports"></a><span data-ttu-id="ccab7-133">Weisen Sie benutzerdefinierter Menübänder zu Formularen oder Berichten zu</span><span class="sxs-lookup"><span data-stu-id="ccab7-133">Assign custom ribbons to forms or reports</span></span>

1.  <span data-ttu-id="ccab7-134">Führen Sie den oben beschriebenen Vorgang aus, um das benutzerdefinierte Menüband in der Anwendung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ccab7-134">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="ccab7-135">Öffnen Sie das Formular oder den Bericht in der Entwurfsansicht.</span><span class="sxs-lookup"><span data-stu-id="ccab7-135">Open the form or report in Design view.</span></span>

3.  <span data-ttu-id="ccab7-136">Wählen Sie auf der Registerkarte Entwurf **Eigenschaftenblatt**.</span><span class="sxs-lookup"><span data-stu-id="ccab7-136">On the Design tab, choose **Property Sheet**.</span></span>

4.  <span data-ttu-id="ccab7-137">Wählen Sie auf der Registerkarte **Alle** des Eigenschaftenfensters aus der Liste **Name** des Menübands, und wählen Sie ein Menüband aus.</span><span class="sxs-lookup"><span data-stu-id="ccab7-137">On the **All** tab of the Property window, choose the **Ribbon Name** list and then select a ribbon.</span></span>

5.  <span data-ttu-id="ccab7-p108">Speichern und schließen Sie das Formular oder den Bericht, und öffnen Sie das Formular oder den Bericht dann erneut. Die ausgewählte Menüband-Benutzeroberfläche wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ccab7-p108">Save, close, and then reopen the form or report. The ribbon UI you selected is displayed.</span></span>


> [!NOTE]
> <span data-ttu-id="ccab7-140">[!HINWEIS] Die in der Menüband-Benutzeroberfläche angezeigten Registerkarten sind additiv.</span><span class="sxs-lookup"><span data-stu-id="ccab7-140">The tabs displayed in the ribbon UI are additive.</span></span> <span data-ttu-id="ccab7-141">D. h., es sei denn, Sie insbesondere die Registerkarten ausblenden oder *von vorne beginnen* -Attribut auf **True**festgelegt, die Registerkarten angezeigt, in einem Formular oder des Berichts Menüband-Benutzeroberfläche sind zusätzlich zu den vorhandenen Registerkarten.</span><span class="sxs-lookup"><span data-stu-id="ccab7-141">That is, unless you specifically hide the tabs or set the *Start from Scratch* attribute to **True**, the tabs displayed in a form's or report's ribbon user interface are in addition to the existing tabs.</span></span>

> [!NOTE]
> <span data-ttu-id="ccab7-142">[!HINWEIS] Weitere Informationen über die Menüband-Benutzeroberfläche in anderen Office-Anwendungen finden Sie unter [Übersicht über das Office Fluent-Menüband](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="ccab7-142">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


