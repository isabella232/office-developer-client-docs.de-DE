---
title: CloseWindow-Makroaktion
TOCTitle: CloseWindow macro action
ms:assetid: ba96bc26-7f3f-fd3d-8d3a-e18bfe90cdf0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822510(v=office.15)
ms:contentKeyID: 48547377
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm64319
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f9bffbd129d8fb4fc1334dbd884556d98e7f140c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929321"
---
# <a name="closewindow-macro-action"></a><span data-ttu-id="38680-102">CloseWindow-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="38680-102">CloseWindow macro action</span></span>


<span data-ttu-id="38680-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="38680-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="38680-104">Die **Fensterschließen** -Aktion können Sie um eine angegebene Access Dokumentregisterkarte oder die aktive Dokumentregisterkarte zu schließen, wenn keines angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="38680-104">You can use the **CloseWindow** action to close either a specified Access document tab or the active document tab if none is specified.</span></span>

## <a name="setting"></a><span data-ttu-id="38680-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="38680-105">Setting</span></span>

<span data-ttu-id="38680-106">Die **FensterSchließen** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="38680-106">The **CloseWindow** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="38680-107">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="38680-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="38680-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="38680-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="38680-109"><strong>Objekttyp</strong></span><span class="sxs-lookup"><span data-stu-id="38680-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="38680-p101">Der Typ des Objekts, dessen Dokumentregisterkarte Sie schließen möchten. Klicken Sie im Feld Objekttyp im Abschnitt Aktionsargumente des Bereichs Makro-Generator auf Tabelle, Abfrage, Formular, Bericht, Makro, Modul, Datenzugriffsseite, Serversicht, Diagramm, Gespeicherte Prozedur oder Funktion. Lassen Sie dieses Argument leer, um die aktive Dokumentregisterkarte auszuwählen. 

</span><span class="sxs-lookup"><span data-stu-id="38680-p101">The type of object whose document tab you want to close. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. To select the active document tab, leave this argument blank.</span></span></p>

> [!NOTE]
> <span data-ttu-id="38680-113">Wenn Sie ein Modul im Visual Basic-Editor schließen, müssen Sie **Modul** im Argument **Objekttyp** verwenden.</span><span class="sxs-lookup"><span data-stu-id="38680-113">If you are closing a module in the Visual Basic Editor, you must use **Module** in the **Object Type** argument.</span></span>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38680-114"><strong>Objektname</strong></span><span class="sxs-lookup"><span data-stu-id="38680-114"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="38680-p102">Der Name des Objekts, das geschlossen werden soll. Im Feld <strong>Objektname</strong> werden alle Objekte in der Datenbank des Typs angezeigt, der mit dem Argument <strong>Objekttyp</strong> ausgewählt wird. Klicken Sie auf das zu schließende Objekt. Wenn Sie das Argument <strong>Objekttyp</strong> leer lassen, müssen Sie auch dieses Argument leer lassen.</span><span class="sxs-lookup"><span data-stu-id="38680-p102">The name of the object to be closed. The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument. Click the object to close. If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38680-119"><strong>Save</strong></span><span class="sxs-lookup"><span data-stu-id="38680-119"><strong>Save</strong></span></span></p></td>
<td><p><span data-ttu-id="38680-p103">Gibt an, ob beim Schließen des Objekts Änderungen am Objekt gespeichert werden sollen. Klicken Sie auf <strong>Ja</strong> (Objekt speichern), auf <strong>Nein</strong> (Objekt schließen, ohne es zu speichern) oder auf <strong>Eingabeaufforderung</strong> (der Benutzer wird gefragt, ob das Objekt gespeichert werden soll). Die Standardeinstellung ist <strong>Eingabeaufforderung</strong>.</span><span class="sxs-lookup"><span data-stu-id="38680-p103">Whether to save changes to the object when it is closed. Click <strong>Yes</strong> (save the object), <strong>No</strong> (close the object without saving it), or <strong>Prompt</strong> (prompt the user whether or not to save the object). The default is <strong>Prompt</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="38680-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="38680-123">Remarks</span></span>

<span data-ttu-id="38680-p104">Die **FensterSchließen** -Aktion funktioniert für alle Datenbankobjekte, die der Benutzer explizit öffnen oder schließen kann. Diese Aktion wirkt sich genauso aus, als wenn Sie ein Objekt auswählen und es dann schließen, indem Sie mit der rechten Maustaste auf die Dokumentregisterkarte des Objekts klicken und dann auf **Schließen** im Kontextmenü klicken, oder indem Sie auf die Schaltfläche **Schließen** für das Objekt klicken.</span><span class="sxs-lookup"><span data-stu-id="38680-p104">The **CloseWindow** action works on all database objects that the user can explicitly open or close. This action has the same effect as selecting an object and then closing it by right-clicking the object's document tab and then clicking **Close** on the shortcut menu, or clicking the **Close** button for the object.</span></span>

<span data-ttu-id="38680-p105">Wenn das Argument **Speichern** auf **Eingabeaufforderung** festgelegt ist und das Objekt vor dem Ausführen der **FensterSchließen** -Aktion noch nicht gespeichert wurde, wird der Benutzer in einem Dialogfeld aufgefordert, das Objekt zu speichern, bevor es vom Makro geschlossen wird. Wenn Sie das Argument **Warnmeldungen An** der **Warnmeldungen** -Aktion auf **Nein** festgelegt haben, wird das Dialogfeld nicht angezeigt, und das Objekt wird automatisch gespeichert.</span><span class="sxs-lookup"><span data-stu-id="38680-p105">If the **Save** argument is set to **Prompt** and the object hasn't already been saved before the **CloseWindow** action is carried out, a dialog box prompts the user to save the object before the macro closes it. If you have set the **Warnings On** argument of the **SetWarnings** action to **No**, the dialog box is not displayed and the object is automatically saved.</span></span>

<span data-ttu-id="38680-128">Verwenden Sie die **CloseWindow** -Methode des **DoCmd** -Objekts, um die **FensterSchließen** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="38680-128">To run the **CloseWindow** action in a Visual Basic for Applications (VBA) module, use the **CloseWindow** method of the **DoCmd** object.</span></span>

