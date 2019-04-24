---
title: RenameObject-Makroaktion
TOCTitle: RenameObject macro action
ms:assetid: fee04eb0-23c0-5d57-b903-e1ae54f2d25e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837293(v=office.15)
ms:contentKeyID: 48548948
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm165893
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ce16b86ea06e041d490d0c68917daf18bd80dbb6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306720"
---
# <a name="renameobject-macro-action"></a><span data-ttu-id="40447-102">RenameObject-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="40447-102">RenameObject macro action</span></span>

<span data-ttu-id="40447-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="40447-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="40447-104">Zum Umbenennen eines angegebenen Datenbankobjekts können Sie die **UmbenennenObjekt** -Aktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="40447-104">You can use the **RenameObject** action to rename a specified database object.</span></span>

> [!NOTE]
> <span data-ttu-id="40447-105">[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist.</span><span class="sxs-lookup"><span data-stu-id="40447-105">This action will not be allowed if the database is not trusted.</span></span>

## <a name="setting"></a><span data-ttu-id="40447-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="40447-106">Setting</span></span>

<span data-ttu-id="40447-107">Die **UmbenennenObjekt**-Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="40447-107">The **RenameObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="40447-108">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="40447-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="40447-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="40447-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40447-110"><strong>Neuer Name</strong></span><span class="sxs-lookup"><span data-stu-id="40447-110"><strong>New Name</strong></span></span></p></td>
<td><p><span data-ttu-id="40447-111">Ein neuer Name für das Database-Objekt.</span><span class="sxs-lookup"><span data-stu-id="40447-111">A new name for the database object.</span></span> <span data-ttu-id="40447-112">Geben Sie den Objektnamen im Feld <strong>neuer Name</strong> im Abschnitt <strong>Aktionsargumente</strong> des Bereichs Makro-Generator ein.</span><span class="sxs-lookup"><span data-stu-id="40447-112">Enter the object name in the <strong>New Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="40447-113">Dies ist ein erforderliches Argument.</span><span class="sxs-lookup"><span data-stu-id="40447-113">This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40447-114"><strong>Objekttyp</strong></span><span class="sxs-lookup"><span data-stu-id="40447-114"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="40447-p102">Der Objekttyp, den Sie umbenennen möchten. Klicken Sie auf <strong>Tabelle</strong>, <strong>Abfrage</strong>, <strong>Formular</strong>, <strong>Bericht</strong>, <strong>Makro</strong>, <strong>Modul</strong>, <strong>Datenzugriffsseite</strong>, <strong>Serversicht</strong>, <strong>Diagramm</strong>, <strong>Gespeicherte Prozedur</strong> oder <strong>Funktion</strong>. Lassen Sie dieses Argument leer, um das im Navigationsbereich ausgewählte Objekt umzubenennen.</span><span class="sxs-lookup"><span data-stu-id="40447-p102">The type of object you want to rename. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong>. To rename the object selected in the Navigation Pane, leave this argument blank.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40447-118"><strong>Alter Name</strong></span><span class="sxs-lookup"><span data-stu-id="40447-118"><strong>Old Name</strong></span></span></p></td>
<td><p><span data-ttu-id="40447-119">Der Name des Objekts, das Sie umbenennen möchten.</span><span class="sxs-lookup"><span data-stu-id="40447-119">The name of the object to be renamed.</span></span> <span data-ttu-id="40447-120">Im Feld <strong>Alter Name</strong> werden alle Objekte in der Datenbank mit dem Typ angezeigt, der vom Argument <strong>Objekttyp</strong> ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="40447-120">The <strong>Old Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="40447-121">Wenn Sie das Argument <strong>Objekttyp</strong> leer lassen, müssen Sie auch dieses Argument leer lassen.</span><span class="sxs-lookup"><span data-stu-id="40447-121">If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p><p><span data-ttu-id="40447-122"><strong>Hinweis</strong>: Wenn Sie ein Makro ausführen, das die <STRONG>Rename</STRONG> -Aktion in einer Bibliotheksdatenbank enthält, sucht Microsoft Access zunächst in der Bibliotheksdatenbank und dann in der aktuellen Datenbank nach dem Objekt mit diesem Namen.</span><span class="sxs-lookup"><span data-stu-id="40447-122"><strong>NOTE</strong>: If you run a macro containing the <STRONG>Rename</STRONG> action in a library database, Microsoft Access first looks for the object with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="40447-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40447-123">Remarks</span></span>

<span data-ttu-id="40447-124">Der neue Name des Datenbankobjekts muss den Standardnamenskonventionen für Access-Objekte entsprechen.</span><span class="sxs-lookup"><span data-stu-id="40447-124">The new name of the database object must follow the standard naming conventions for Access objects.</span></span>

<span data-ttu-id="40447-125">Sie können ein geöffnetes Objekt nicht umbenennen.</span><span class="sxs-lookup"><span data-stu-id="40447-125">You can't rename an open object.</span></span>

<span data-ttu-id="40447-p104">Wenn Sie die Argumente **Objekttyp** und **Alter Name** leer lassen, wird das im Navigationsbereich ausgewählte Objekt in Access automatisch umbenannt. Zum Auswählen eines Objekts im Navigationsbereich können Sie die **AuswählenObjekt** -Aktion mit dem Argument **Im Navigationsbereich** verwenden, das auf **Ja** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="40447-p104">If you leave the **Object Type** and **Old Name** arguments blank, Access renames the object selected in the Navigation Pane. To select an object in the Navigation Pane, you can use the **SelectObject** action with the **In Navigation Pane** argument set to **Yes**.</span></span>

<span data-ttu-id="40447-p105">Sie können ein Objekt auch umbenennen, indem Sie im Navigationsbereich mit der rechten Maustaste darauf klicken, dann auf **Umbenennen** klicken und einen neuen Namen eingeben. Mit der **UmbenennenObjekt** -Aktion müssen Sie das Objekt nicht zuerst im Navigationsbereich auswählen und das Makro beenden, um den neuen Namen einzugeben.</span><span class="sxs-lookup"><span data-stu-id="40447-p105">You can also rename an object by right-clicking it in the Navigation Pane, clicking **Rename**, and entering a new name. With the **RenameObject** action, you don't have to select the object first in the Navigation Pane, and you don't have to stop the macro to enter the new name.</span></span>

<span data-ttu-id="40447-130">Diese Aktion unterscheidet sich von der **KopierenObjekt** -Aktion, bei der eine Kopie des Objekts unter einem neuen Namen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="40447-130">This action differs from the **CopyObject** action, which creates a copy of the object under a new name.</span></span>

<span data-ttu-id="40447-131">Verwenden Sie die **Rename** -Methode des **DoCmd** -Objekts, um die **UmbenennenObjekt** -Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="40447-131">To run the **RenameObject** action in a Visual Basic for Applications (VBA) module, use the **Rename** method of the **DoCmd** object.</span></span>

