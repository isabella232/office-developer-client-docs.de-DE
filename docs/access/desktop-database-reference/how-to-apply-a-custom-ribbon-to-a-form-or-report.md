---
title: Anwenden einer benutzerdefinierten Multifunktionsleiste zu einem Formular oder Bericht
TOCTitle: Apply a custom ribbon to a form or report
ms:assetid: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15)
ms:contentKeyID: 48545865
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f4fb0155b1a1ed36b6fe924f72a4da385197cc21
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475235"
---
# <a name="apply-a-custom-ribbon-to-a-form-or-report"></a><span data-ttu-id="5147e-102">Anwenden einer benutzerdefinierten Multifunktionsleiste zu einem Formular oder Bericht</span><span class="sxs-lookup"><span data-stu-id="5147e-102">Apply a custom ribbon to a form or report</span></span>


<span data-ttu-id="5147e-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5147e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5147e-p101">Das Menüband verwendet textbasiertes, deklaratives XML-Markup, das die Erstellung und Anpassung des Menübands vereinfacht. Mit ein paar XML-Zeilen können Sie genau die passende Benutzeroberfläche für den Benutzer erstellen. Access bietet Flexibilität beim Anpassen der Menüband-Benutzeroberfläche. So können Sie das Anpassungsmarkup zum Beispiel in einer Tabelle speichern, in eine VBA-Prozedur einbetten, in einer anderen Access-Datenbank speichern oder mit einem Excel-Arbeitsblatt verknüpfen. Dieses Thema beschreibt, wie angepasste Menübänder beim Laden eines Formulars oder eines Berichts angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="5147e-p101">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon. With a few lines of XML, you can create just the right interface for the user. Access provides flexibility in customizing the ribbon user interface. For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet. This topic describes how to apply customized ribbons when loading a form or report.</span></span>

## <a name="making-the-ribbon-customization-xml-available"></a><span data-ttu-id="5147e-109">XML für die Menübandanpassung verfügbar machen</span><span class="sxs-lookup"><span data-stu-id="5147e-109">Making the Ribbon Customization XML Available</span></span>

<span data-ttu-id="5147e-110">**Speichern der Menübanderweiterungs-XML in einer Tabelle**</span><span class="sxs-lookup"><span data-stu-id="5147e-110">**Storing Ribbon Extensibility XML in a Table**</span></span>

<span data-ttu-id="5147e-p102">Eine Möglichkeit zum Verfügbarmachen der Menübandanpassungen ist, sie in einer Tabelle zu speichern. Wenn Sie die Anpassungen in einer Tabelle mit dem Namen **USysRibbons** speichern, können die Anpassungen ohne Makros oder VBA-Code implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="5147e-p102">One method that you can use to make ribbon customizations available is to store them in a table. If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="5147e-p103">**USysRibbons** ist eine vom Benutzer erstellte Systemtabelle. Die Tabelle muss mit bestimmten Spaltennamen erstellt werden, damit die Menübandanpassungen implementiert werden können. In der folgenden Tabelle sind die Einstellungen aufgeführt, die beim Erstellen der **USysRibbons** -Tabelle verwendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5147e-p103">**USysRibbons** is a user-created system table. The table must be created using specific column names in order for the ribbon customizations to be implemented. The following table lists the settings to use when creating the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5147e-116">Spaltenname</span><span class="sxs-lookup"><span data-stu-id="5147e-116">Column Name</span></span></p></th>
<th><p><span data-ttu-id="5147e-117">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5147e-117">Data Type</span></span></p></th>
<th><p><span data-ttu-id="5147e-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5147e-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5147e-119"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="5147e-119"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="5147e-120">Text</span><span class="sxs-lookup"><span data-stu-id="5147e-120">Text</span></span></p></td>
<td><p><span data-ttu-id="5147e-121">Enthält den Namen des benutzerdefinierten Menübands, das dieser Anpassung zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5147e-121">Contains the name of the custom ribbon to be associated with this customization</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5147e-122"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="5147e-122"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="5147e-123">Memo</span><span class="sxs-lookup"><span data-stu-id="5147e-123">Memo</span></span></p></td>
<td><p><span data-ttu-id="5147e-124">Enthält die Menübanderweiterungs-XML (RibbonX) zur Definition der Menübandanpassung.</span><span class="sxs-lookup"><span data-stu-id="5147e-124">Contains the ribbon Extensibility XML (RibbonX) that defines the ribbon customization</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5147e-125">**Menübanderweiterungs-XML programmatisch laden**</span><span class="sxs-lookup"><span data-stu-id="5147e-125">**Loading Ribbon Extensibility XML Programmatically**</span></span>

<span data-ttu-id="5147e-p104">Mit der **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** -Methode können Sie Menübandanpassungen programmatisch laden. Um das Menüband zu erstellen und der Anwendung zur Verfügung zu stellen, erstellen Sie in der Regel zunächst ein Modul in der Datenbank mit einer Prozedur, die die **LoadCustomUI** -Methode aufruft, sodass der Name des Menübands und das XML-Anpassungsmarkup übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="5147e-p104">You can use the **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** method to load ribbon customizations programmatically. Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>

<span data-ttu-id="5147e-p105">Das XML-Markup kann von einem **Recordset** -Objekt stammen, das aus einer Tabelle, einer datenbankexternen Quelle wie einer XML-Datei, die in eine Zeichenfolge analysiert wird, oder aus einer direkt in die Prozedur eingebetteten XML-Datei stammen kann. Sie können verschiedene Menübänder anhand mehrerer Aufrufe der **LoadCustomUI** -Methode erstellen, wobei verschiedenes XML übergeben wird, solange der Name jedes Menübands und das **id** -Attribut der Registerkarten des Menübands eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="5147e-p105">The XML markup can come from a **Recordset** object created from a table, from a source external to the database such as an XML file that you parse into a string, or from XML markup embedded directly inside the procedure. You can make different ribbons using multiple calls to the **LoadCustomUI** method, passing in different XML markup as long as the name of each ribbon and the **id** attribute of the tabs that make up the ribbon are unique.</span></span>

<span data-ttu-id="5147e-p106">Nach Abschluss der Prozedur erstellen Sie ein AutoExec-Makro, das die Prozedur über die RunCode-Aktion aufruft. Auf diese Weise wird beim Starten der Anwendung die **LoadCustomUI** -Methode automatisch ausgeführt, und alle benutzerdefinierten Menübänder werden für die Anwendung verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="5147e-p106">After the procedure is complete, you then create an AutoExec macro that calls the procedure by using the RunCode action. That way, when the application is started, the **LoadCustomUI** method is automatically executed and all of the custom ribbons are made available to the application.</span></span>

## <a name="assigning-custom-ribbons-to-forms-or-reports"></a><span data-ttu-id="5147e-132">Zuweisen benutzerdefinierter Menübänder zu Formularen oder Berichten</span><span class="sxs-lookup"><span data-stu-id="5147e-132">Assigning Custom Ribbons to Forms or Reports</span></span>

1.  <span data-ttu-id="5147e-133">Führen Sie den oben beschriebenen Vorgang aus, um das benutzerdefinierte Menüband in der Anwendung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="5147e-133">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="5147e-134">Öffnen Sie das Formular oder den Bericht in der Entwurfsansicht.</span><span class="sxs-lookup"><span data-stu-id="5147e-134">Open the form or report in Design view.</span></span>

3.  <span data-ttu-id="5147e-135">Klicken Sie auf der Registerkarte „Entwurf" auf **Eigenschaftenblatt**.</span><span class="sxs-lookup"><span data-stu-id="5147e-135">On the Design tab, click **Property Sheet**.</span></span>

4.  <span data-ttu-id="5147e-136">Klicken Sie auf der Registerkarte **Alle** des Eigenschaftenfensters auf die Liste **Name des Menübands**, und wählen Sie anschließend ein Menüband aus.</span><span class="sxs-lookup"><span data-stu-id="5147e-136">On the **All** tab of the Property window, click the **Ribbon Name** list and then select a ribbon.</span></span>

5.  <span data-ttu-id="5147e-p107">Speichern und schließen Sie das Formular oder den Bericht, und öffnen Sie das Formular oder den Bericht dann erneut. Die ausgewählte Menüband-Benutzeroberfläche wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5147e-p107">Save, close, and then reopen the form or report. The ribbon UI you selected is displayed.</span></span>


> [!NOTE]
> <span data-ttu-id="5147e-139">[!HINWEIS] Die in der Menüband-Benutzeroberfläche angezeigten Registerkarten sind additiv.</span><span class="sxs-lookup"><span data-stu-id="5147e-139">The tabs displayed in the ribbon UI are additive.</span></span> <span data-ttu-id="5147e-140">D. h., es sei denn, Sie insbesondere die Registerkarten ausblenden oder *von vorne beginnen* -Attribut auf **True**festgelegt, die Registerkarten angezeigt, in einem Formular oder des Berichts Menüband-Benutzeroberfläche sind zusätzlich zu den vorhandenen Registerkarten.</span><span class="sxs-lookup"><span data-stu-id="5147e-140">That is, unless you specifically hide the tabs or set the *Start from Scratch* attribute to **True**, the tabs displayed in a form's or report's ribbon user interface are in addition to the existing tabs.</span></span>

> [!NOTE]
> <span data-ttu-id="5147e-141">[!HINWEIS] Weitere Informationen über die Menüband-Benutzeroberfläche in anderen Office-Anwendungen finden Sie unter [Übersicht über das Office Fluent-Menüband](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span><span class="sxs-lookup"><span data-stu-id="5147e-141">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


