---
title: DeleteObject-Makroaktion
TOCTitle: DeleteObject macro action
ms:assetid: a8deb2a7-4e73-8696-b8c1-3a3939d813f7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821415(v=office.15)
ms:contentKeyID: 48546912
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm152112
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 3ed8580d95128dae475a6d5fe3963f7daaad53f0
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997259"
---
# <a name="deleteobject-macro-action"></a><span data-ttu-id="d8a5e-102">DeleteObject-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="d8a5e-102">DeleteObject macro action</span></span>

<span data-ttu-id="d8a5e-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d8a5e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d8a5e-104">Sie können die **LöschenObjekt** -Aktion verwenden, um ein angegebenes Datenbankobjekt zu löschen.</span><span class="sxs-lookup"><span data-stu-id="d8a5e-104">You can use the **DeleteObject** action to delete a specified database object.</span></span>

> [!NOTE]
> <span data-ttu-id="d8a5e-105">[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist.</span><span class="sxs-lookup"><span data-stu-id="d8a5e-105">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="d8a5e-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="d8a5e-106">Setting</span></span>

<span data-ttu-id="d8a5e-107">Die **LöschenObjekt** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="d8a5e-107">The **DeleteObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d8a5e-108">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="d8a5e-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="d8a5e-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d8a5e-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d8a5e-110"><strong>Objekttyp</strong></span><span class="sxs-lookup"><span data-stu-id="d8a5e-110"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="d8a5e-p101">Der Typ des Objekts, das gelöscht werden soll. Klicken Sie im Feld Objekttyp im Bereich Aktionsargumente des Bereichs Makro-Generator auf Tabelle, Abfrage, Formular, Bericht, Makro, Modul, Datenzugriffsseite, Serversicht, Diagramm, Gespeicherte Prozedur oder Funktion. Lassen Sie dieses Argument leer, um das im Navigationsbereich ausgewählte Objekt zu löschen.</span><span class="sxs-lookup"><span data-stu-id="d8a5e-p101">The type of object to delete. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. To delete the object selected in the Navigation Pane, leave this argument blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8a5e-114"><strong>Objektname</strong></span><span class="sxs-lookup"><span data-stu-id="d8a5e-114"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="d8a5e-115">Der Name des zu löschenden Objekts.</span><span class="sxs-lookup"><span data-stu-id="d8a5e-115">The name of the object to delete.</span></span> <span data-ttu-id="d8a5e-116">Im Feld <strong>Objektname</strong> werden alle Objekte in der Datenbank mit dem Objekttyp angezeigt, der mit dem <strong>Objekttyp</strong> -Argument ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="d8a5e-116">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="d8a5e-117">Lassen Sie dieses Feld leer, wenn Sie im Feld <strong>Objekttyp</strong> leer lassen.</span><span class="sxs-lookup"><span data-stu-id="d8a5e-117">If you leave the <strong>Object Type</strong> box blank, leave this box blank also.</span></span> <span data-ttu-id="d8a5e-118">Wenn Sie ein Makro ausführen, das die <strong>LöschenObjekt</strong>-Aktion in einer Bibliotheksdatenbank enthält, sucht Microsoft Office Access 2007 zuerst in der Bibliotheksdatenbank und dann in der aktuellen Datenbank nach dem Objekt mit diesem Namen.</span><span class="sxs-lookup"><span data-stu-id="d8a5e-118">If you run a macro containing the <strong>DeleteObject</strong> action in a library database, Microsoft Office Access 2007 first looks for the object with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>

> [!WARNING]
> <span data-ttu-id="d8a5e-119">[!VORSICHT] Wenn Sie die Felder **Objekttyp** und **Objektname** leer lassen, löscht Access beim Auftreten der **LöschenObjekt** -Aktion das im Navigationsbereich ausgewählte Objekt, ohne eine Warnmeldung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d8a5e-119">If you leave the **Object Type** and **Object Name** boxes blank, Access deletes the object selected in the Navigation Pane without displaying a warning message when it encounters the **DeleteObject** action.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8a5e-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d8a5e-120">Remarks</span></span>

<span data-ttu-id="d8a5e-p103">Sie können die **LöschenObjekt** -Aktion verwenden, um temporäre Objekte zu löschen, die beim Ausführen des Makros erstellt wurden. Beispielsweise können Sie die **ÖffnenAbfrage** -Aktion verwenden, um eine Tabellenerstellungsabfrage zum Erstellen einer temporären Tabelle auszuführen. Wenn die temporäre Tabelle nicht mehr verwendet wird, können Sie sie mithilfe der **LöschenObjekt** -Aktion löschen.</span><span class="sxs-lookup"><span data-stu-id="d8a5e-p103">You can use the **DeleteObject** action to delete temporary objects you have created while running the macro. For example, you could use the **OpenQuery** action to run a make-table query that creates a temporary table. When you are finished using the temporary table, you can use the **DeleteObject** action to delete it.</span></span>

<span data-ttu-id="d8a5e-124">Diese Aktion wirkt sich genauso aus, wie wenn Sie ein Objekt im Navigationsbereich auswählen und anschließend die ENTF-TASTE drücken, oder wenn Sie mit der rechten Maustaste auf das Objekt im Navigationsbereich klicken und dann auf **Löschen** klicken.</span><span class="sxs-lookup"><span data-stu-id="d8a5e-124">This action has the same effect as selecting an object in the Navigation Pane and then pressing the DEL key, or right-clicking the object in the Navigation Pane and clicking **Delete**.</span></span>

<span data-ttu-id="d8a5e-125">Verwenden Sie die **DeleteObject** -Methode des **DoCmd** -Objekts, um die **LöschenObjekt** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d8a5e-125">To run the **DeleteObject** action in a Visual Basic for Applications module, you can use the **DeleteObject** method of the **DoCmd** object.</span></span>

