---
title: SelectObject-Makroaktion
TOCTitle: SelectObject macro action
ms:assetid: a90539a0-c5a0-e997-9c25-e0972d28f2a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821420(v=office.15)
ms:contentKeyID: 48546914
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm41840
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f134a43aaa56a1b206330175658f92e5076a4a14
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919290"
---
# <a name="selectobject-macro-action"></a><span data-ttu-id="59472-102">SelectObject-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="59472-102">SelectObject macro action</span></span>


<span data-ttu-id="59472-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="59472-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="59472-104">Sie können die **AuswählenObjekt** -Aktion zur Auswahl eines bestimmten Datenbankobjekts verwenden.</span><span class="sxs-lookup"><span data-stu-id="59472-104">You can use the **SelectObject** action to select a specified database object.</span></span>

## <a name="setting"></a><span data-ttu-id="59472-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="59472-105">Setting</span></span>

<span data-ttu-id="59472-106">Die **AuswählenObjekt** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="59472-106">The **SelectObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="59472-107">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="59472-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="59472-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="59472-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="59472-109"><strong>Objekttyp</strong></span><span class="sxs-lookup"><span data-stu-id="59472-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="59472-p101">Der Typ des auszuwählenden Datenbankobjekts. Klicken Sie im Feld <strong>Objekttyp</strong> im Abschnitt <strong>Aktionsargumente</strong> des Bereichs <strong>Makro-Generator</strong> auf <strong>Tabelle</strong>, <strong>Abfrage</strong>, <strong>Formular</strong>, <strong>Bericht</strong>, <strong>Makro</strong>, <strong>Datenzugriffsseite</strong>, <strong>Serversicht</strong>, <strong>Diagramm</strong>, <strong>Gespeicherte Prozedur</strong> oder <strong>Funktion</strong>. Dies ist ein erforderliches Argument.</span><span class="sxs-lookup"><span data-stu-id="59472-p101">The type of database object to select. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59472-113"><strong>Objektname</strong></span><span class="sxs-lookup"><span data-stu-id="59472-113"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="59472-p102">Der Name des auszuwählenden Objekts. Im Feld Objektname werden alle Objekte in der Datenbank angezeigt, die dem vom Argument Objekttyp ausgewählten Typ entsprechen. Das ist ein erforderliches Argument, es sei denn, Sie legen das Argument Im Navigationsbereich auf Ja fest.</span><span class="sxs-lookup"><span data-stu-id="59472-p102">The name of the object to select. The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument. This is a required argument, unless you set the In Navigation Pane argument to <strong>Yes</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="59472-117">Die Objektnamen für <STRONG>Serversicht</STRONG>, <STRONG>Diagramm</STRONG> oder <STRONG>Gespeicherte Prozedur</STRONG>-Objekte werden im Feld <STRONG>Objektname</STRONG> eines Access-Projekts (ADP) nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="59472-117">The object names for <STRONG>Server View</STRONG>, <STRONG>Diagram</STRONG>, or <STRONG>Stored Procedure</STRONG> objects are not displayed in the <STRONG>Object Name</STRONG> box of an Access project (.adp).</span></span></P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59472-118"><strong>Im Navigationsbereich</strong></span><span class="sxs-lookup"><span data-stu-id="59472-118"><strong>In Navigation Pane</strong></span></span></p></td>
<td><p><span data-ttu-id="59472-p103">Gibt an, ob Microsoft Access das Objekt im Navigationsbereich auswählt. Klicken Sie auf <strong>Ja</strong> (um das Objekt im Navigationsbereich auszuwählen) oder <strong>Nein</strong> (um das Objekt nicht im Navigationsbereich auszuwählen). Die Standardeinstellung ist <strong>Nein</strong>.</span><span class="sxs-lookup"><span data-stu-id="59472-p103">Specifies whether Microsoft Access selects the object in the Navigation Pane. Click <strong>Yes</strong> (to select the object in the Navigation Pane) or <strong>No</strong> (not to select the object in the Navigation Pane). The default is <strong>No</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="59472-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="59472-122">Remarks</span></span>

<span data-ttu-id="59472-p104">Die **AuswählenObjekt** -Aktion funktioniert mit allen Access-Objekten, die den Fokus erhalten können. Diese Aktion weist den Fokus dem angegebenen Objekt zu und zeigt dem Objekt an, ob es ausgeblendet ist. Wenn das Objekt ein Formular ist, wird die **Sichtbar** -Eigenschaft des Formulars von der **AuswählenObjekt** -Aktion auf **Ja** festgelegt, und das Formular wird in den Modus zurückgesetzt, der durch die Formulareigenschaften festgelegt ist (beispielsweise gebundenes Formular oder Popupformular).</span><span class="sxs-lookup"><span data-stu-id="59472-p104">The **SelectObject** action works with any Access object that can receive the focus. This action gives the specified object the focus and shows the object if it's hidden. If the object is a form, the **SelectObject** action sets the form's **Visible** property to **Yes** and returns the form to the mode set by its form properties (for example, as a modal or pop-up form).</span></span>

<span data-ttu-id="59472-p105">Wenn das Objekt in einem der anderen Access-Fenster nicht geöffnet ist, können Sie es auswählen, indem Sie das Argument **Im Navigationsbereich** auf **Ja** festlegen. Wenn Sie das Argument **Im Navigationsbereich** auf **Nein** festlegen, wird eine Fehlermeldung angezeigt, sobald Sie versuchen, ein Objekt auszuwählen, das nicht geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="59472-p105">If the object isn't open in one of the other Access windows, you can select it in the Navigation Pane by setting the **In Navigation Pane** argument to **Yes**. If you set the **In Navigation Pane** argument to **No**, an error message appears when you try to select an object that isn't open.</span></span>

<span data-ttu-id="59472-p106">Diese Aktion verwenden Sie unter Umständen häufig, um ein Objekt auszuwählen, für das Sie weitere Aktionen durchführen möchten. Wenn Access z. B. für die Verwendung von überlappenden Fenstern anstatt von Dokumenten mit Registerkarten konfiguriert ist, können Sie beispielsweise ein Objekt wiederherstellen, das minimiert wurde (indem Sie die **WiederherstellenFenster** -Aktion verwenden), oder ein Fenster maximieren, das ein Objekt enthält, mit dem Sie arbeiten möchten (indem Sie die **MaximierenFenster** -Aktion verwenden).</span><span class="sxs-lookup"><span data-stu-id="59472-p106">Often, you might use this action to select an object on which you want to perform additional actions. For example, if you have Access configured to use overlapping windows instead of tabbed documents, you may want to restore an object that has been minimized (by using the **RestoreWindow** action) or maximize a window that contains an object you want to work with (by using the **MaximizeWindow** action).</span></span>

<span data-ttu-id="59472-p107">Wenn Sie ein Formular auswählen, können Sie die Aktionen **GeheZuSteuerelement**, **GeheZuDatensatz** und **GeheZuSeite** verwenden, um zu verschiedenen Formularbereichen zu wechseln. Die **GeheZuDatensatz** -Aktion funktioniert außerdem für Datenblätter.</span><span class="sxs-lookup"><span data-stu-id="59472-p107">If you select a form, you can use the **GoToControl**, **GoToRecord**, and **GoToPage** actions to move to specific areas on the form. The **GoToRecord** action also works for datasheets.</span></span>

<span data-ttu-id="59472-132">Verwenden Sie die **SelectObject** -Methode des **DoCmd** -Objekts, um die **AuswählenObjekt** -Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="59472-132">To run the **SelectObject** action in a Visual Basic for Applications (VBA) module, use the **SelectObject** method of the **DoCmd** object.</span></span>

