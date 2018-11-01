---
title: UmbenennenObjekt-Makroaktion
TOCTitle: RenameObject Macro Action
ms:assetid: fee04eb0-23c0-5d57-b903-e1ae54f2d25e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837293(v=office.15)
ms:contentKeyID: 48548948
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm165893
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0590b586e2640df629cfeacbb28caca6f87ccb34
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878913"
---
# <a name="renameobject-macro-action"></a><span data-ttu-id="6fbbe-102">UmbenennenObjekt-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="6fbbe-102">RenameObject Macro Action</span></span>


<span data-ttu-id="6fbbe-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6fbbe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6fbbe-104">Zum Umbenennen eines angegebenen Datenbankobjekts können Sie die **UmbenennenObjekt** -Aktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="6fbbe-104">You can use the **RenameObject** action to rename a specified database object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="6fbbe-p101">[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. Informationen zur Aktivierung von Makros finden Sie unter den Links im Abschnitt See Also dieses Artikels.</span><span class="sxs-lookup"><span data-stu-id="6fbbe-p101">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="6fbbe-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="6fbbe-107">Setting</span></span>

<span data-ttu-id="6fbbe-108">Die **UmbenennenObjekt** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="6fbbe-108">The **RenameObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6fbbe-109">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="6fbbe-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="6fbbe-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6fbbe-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6fbbe-111"><strong>Neuer Name</strong></span><span class="sxs-lookup"><span data-stu-id="6fbbe-111"><strong>New Name</strong></span></span></p></td>
<td><p><span data-ttu-id="6fbbe-p102">Ein neuer Name für das Datenbankobjekt. Geben Sie den Objektnamen im Feld Neuer Name im Bereich Aktionsargument des Bereichs Makro-Generator ein. Dies ist ein erforderliches Argument.</span><span class="sxs-lookup"><span data-stu-id="6fbbe-p102">A new name for the database object. Enter the object name in the <strong>New Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fbbe-115"><strong>Objekttyp</strong></span><span class="sxs-lookup"><span data-stu-id="6fbbe-115"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="6fbbe-p103">Der Objekttyp, den Sie umbenennen möchten. Klicken Sie auf <strong>Tabelle</strong>, <strong>Abfrage</strong>, <strong>Formular</strong>, <strong>Bericht</strong>, <strong>Makro</strong>, <strong>Modul</strong>, <strong>Datenzugriffsseite</strong>, <strong>Serversicht</strong>, <strong>Diagramm</strong>, <strong>Gespeicherte Prozedur</strong> oder <strong>Funktion</strong>. Lassen Sie dieses Argument leer, um das im Navigationsbereich ausgewählte Objekt umzubenennen.</span><span class="sxs-lookup"><span data-stu-id="6fbbe-p103">The type of object you want to rename. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong>. To rename the object selected in the Navigation Pane, leave this argument blank.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6fbbe-119"><strong>Alter Name</strong></span><span class="sxs-lookup"><span data-stu-id="6fbbe-119"><strong>Old Name</strong></span></span></p></td>
<td><p><span data-ttu-id="6fbbe-p104">Der Name des Objekts, das Sie umbenennen möchten. Im Feld <strong>Alter Name</strong> werden alle Objekte in der Datenbank mit dem Typ angezeigt, der vom Argument <strong>Objekttyp</strong> ausgewählt wurde. Wenn Sie das Argument <strong>Objekttyp</strong> leer lassen, müssen Sie auch dieses Argument leer lassen. 

</span><span class="sxs-lookup"><span data-stu-id="6fbbe-p104">The name of the object to be renamed. The <strong>Old Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument. If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="6fbbe-123">Wenn Sie ein Makro ausführen, das die <STRONG>AusgabeIn</STRONG>-Aktion in einer Bibliotheksdatenbank enthält, sucht Access zuerst in der Bibliotheksdatenbank und dann in der aktuellen Datenbank nach dem Objekt mit diesem Namen.</span><span class="sxs-lookup"><span data-stu-id="6fbbe-123">If you run a macro containing the <STRONG>Rename</STRONG> action in a library database, Microsoft Access first looks for the object with this name in the library database, and then in the current database.</span></span></P>


<p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6fbbe-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6fbbe-124">Remarks</span></span>

<span data-ttu-id="6fbbe-125">Der neue Name des Datenbankobjekts muss den Standardnamenskonventionen für Access-Objekte entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6fbbe-125">The new name of the database object must follow the standard naming conventions for Access objects.</span></span>

<span data-ttu-id="6fbbe-126">Sie können ein geöffnetes Objekt nicht umbenennen.</span><span class="sxs-lookup"><span data-stu-id="6fbbe-126">You can't rename an open object.</span></span>

<span data-ttu-id="6fbbe-p105">Wenn Sie die Argumente **Objekttyp** und **Alter Name** leer lassen, wird das im Navigationsbereich ausgewählte Objekt in Access automatisch umbenannt. Zum Auswählen eines Objekts im Navigationsbereich können Sie die **AuswählenObjekt** -Aktion mit dem Argument **Im Navigationsbereich** verwenden, das auf **Ja** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6fbbe-p105">If you leave the **Object Type** and **Old Name** arguments blank, Access renames the object selected in the Navigation Pane. To select an object in the Navigation Pane, you can use the **SelectObject** action with the **In Navigation Pane** argument set to **Yes**.</span></span>

<span data-ttu-id="6fbbe-p106">Sie können ein Objekt auch umbenennen, indem Sie im Navigationsbereich mit der rechten Maustaste darauf klicken, dann auf **Umbenennen** klicken und einen neuen Namen eingeben. Mit der **UmbenennenObjekt** -Aktion müssen Sie das Objekt nicht zuerst im Navigationsbereich auswählen und das Makro beenden, um den neuen Namen einzugeben.</span><span class="sxs-lookup"><span data-stu-id="6fbbe-p106">You can also rename an object by right-clicking it in the Navigation Pane, clicking **Rename**, and entering a new name. With the **RenameObject** action, you don't have to select the object first in the Navigation Pane, and you don't have to stop the macro to enter the new name.</span></span>

<span data-ttu-id="6fbbe-131">Diese Aktion unterscheidet sich von der **KopierenObjekt** -Aktion, bei der eine Kopie des Objekts unter einem neuen Namen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="6fbbe-131">This action differs from the **CopyObject** action, which creates a copy of the object under a new name.</span></span>

<span data-ttu-id="6fbbe-132">Verwenden Sie die **Rename** -Methode des **DoCmd** -Objekts, um die **UmbenennenObjekt** -Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="6fbbe-132">To run the **RenameObject** action in a Visual Basic for Applications (VBA) module, use the **Rename** method of the **DoCmd** object.</span></span>

