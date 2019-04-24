---
title: SaveObject-Makroaktion
TOCTitle: SaveObject macro action
ms:assetid: 85716dfc-f76f-ca47-cc40-f8f88162f85a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196789(v=office.15)
ms:contentKeyID: 48546060
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm116962
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: cf6fe02616134f864a0e07092951ab9cf49aadbc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308932"
---
# <a name="saveobject-macro-action"></a><span data-ttu-id="d414c-102">SaveObject-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="d414c-102">SaveObject macro action</span></span>

<span data-ttu-id="d414c-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d414c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d414c-p101">You can use the **SaveObject** action to save either a specified Access object or the active object if none is specified. You can also save the active object with a new name in some cases (this functions the same as the **Save As** command on the **Quick Access Toolbar**).</span><span class="sxs-lookup"><span data-stu-id="d414c-p101">You can use the **SaveObject** action to save either a specified Access object or the active object if none is specified. You can also save the active object with a new name in some cases (this functions the same as the **Save As** command on the **Quick Access Toolbar**).</span></span>

> [!NOTE]
> <span data-ttu-id="d414c-106">Diese Aktion ist nicht zulässig, wenn die Datenbank nicht vertrauenswürdig ist.</span><span class="sxs-lookup"><span data-stu-id="d414c-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="d414c-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="d414c-107">Setting</span></span>

<span data-ttu-id="d414c-108">Die **SpeichernObjekt**-Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="d414c-108">The **SaveObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d414c-109">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="d414c-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="d414c-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d414c-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d414c-111"><strong>Objekttyp</strong></span><span class="sxs-lookup"><span data-stu-id="d414c-111"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="d414c-112">Der Objekttyp, der gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d414c-112">The type of object you want to save.</span></span> <span data-ttu-id="d414c-113">Klicken Sie im Feld <strong>Objekttyp</strong> im Abschnitt <strong>Aktionsargumente</strong> des Bereichs <strong>Makro-Generator</strong> auf <strong>Tabelle</strong>, <strong>Abfrage</strong>, <strong>Formular</strong>, <strong>Bericht</strong>, <strong>Makro</strong>, <strong>Datenzugriffsseite</strong>, <strong>Serversicht</strong>, <strong>Diagramm</strong>, <strong>Gespeicherte Prozedur</strong> oder <strong>Funktion</strong>.</span><span class="sxs-lookup"><span data-stu-id="d414c-113">Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="d414c-114">Lassen Sie dieses Argument leer, um das aktive Objekt auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="d414c-114">To select the active object, leave this argument blank.</span></span> <span data-ttu-id="d414c-115">Wenn Sie einen Objekttyp in diesem Argument auswählen, müssen Sie den Namen eines vorhandenen Objekts im Argument <strong>Objektname</strong> auswählen.</span><span class="sxs-lookup"><span data-stu-id="d414c-115">If you select an object type in this argument, you must select an existing object's name in the <strong>Object Name</strong> argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d414c-116"><strong>Objektname</strong></span><span class="sxs-lookup"><span data-stu-id="d414c-116"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="d414c-117">Der Name des zu speichernden Objekts.</span><span class="sxs-lookup"><span data-stu-id="d414c-117">The name of the object to be saved.</span></span> <span data-ttu-id="d414c-118">Im Feld <strong>Objektname</strong> werden alle Objekte in der Datenbank des Typs angezeigt, der vom Argument <strong>Objekttyp</strong> ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="d414c-118">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="d414c-119">Wenn Sie das Argument <strong>Objekttyp</strong> leer lassen, können Sie dieses Argument leer lassen, um das aktive Objekt zu speichern, oder in einigen Fällen einen neuen Namen in dieses Argument eingeben, um das aktive Objekt mit diesem Namen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="d414c-119">If you leave the <strong>Object Type</strong> argument blank, you can leave this argument blank to save the active object, or, in some cases, enter a new name in this argument to save the active object with this name.</span></span> <span data-ttu-id="d414c-120">Wenn Sie einen neuen Namen eingeben, muss der Name den Standardnamenskonventionen für Microsoft Access-Objekte entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d414c-120">If you enter a new name, the name must follow the standard naming conventions for Microsoft Access objects.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d414c-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d414c-121">Remarks</span></span>

<span data-ttu-id="d414c-122">The **SaveObject** action works on all database objects that the user can explicitly open and save.</span><span class="sxs-lookup"><span data-stu-id="d414c-122">The **SaveObject** action works on all database objects that the user can explicitly open and save.</span></span> <span data-ttu-id="d414c-123">The specified object must be open for the **SaveObject** action to have any effect on the object.</span><span class="sxs-lookup"><span data-stu-id="d414c-123">The specified object must be open for the **SaveObject** action to have any effect on the object.</span></span> <span data-ttu-id="d414c-124">This action has the same effect as selecting an object and then saving it by clicking **Save** on the **Quick Access Toolbar**.</span><span class="sxs-lookup"><span data-stu-id="d414c-124">This action has the same effect as selecting an object and then saving it by clicking **Save** on the **Quick Access Toolbar**.</span></span> 

<span data-ttu-id="d414c-125">Leaving the **Object Type** argument blank and entering a new name in the **Object Name** argument has the same effect as clicking **Save As** on the **Quick Access Toolbar**, and entering a new name for the active object.</span><span class="sxs-lookup"><span data-stu-id="d414c-125">Leaving the **Object Type** argument blank and entering a new name in the **Object Name** argument has the same effect as clicking **Save As** on the **Quick Access Toolbar**, and entering a new name for the active object.</span></span> <span data-ttu-id="d414c-126">Using the **SaveObject** action enables you to specify an object to save and to perform a **Save As** command from a macro.</span><span class="sxs-lookup"><span data-stu-id="d414c-126">Using the **SaveObject** action enables you to specify an object to save and to perform a **Save As** command from a macro.</span></span>

> [!NOTE]
> <span data-ttu-id="d414c-127">[!HINWEIS] Zum Speichern der folgenden Objekte unter einem neuen Namen können Sie die **SpeichernObjekt** -Aktion nicht verwenden:</span><span class="sxs-lookup"><span data-stu-id="d414c-127">You can't use the **SaveObject** action to save any of the following with a new name:</span></span>
> - <span data-ttu-id="d414c-128">Ein Formular in der Formularansicht oder Datenblattansicht</span><span class="sxs-lookup"><span data-stu-id="d414c-128">A form in Form view or Datasheet view</span></span>
> - <span data-ttu-id="d414c-129">Ein Bericht in der Seitenansicht</span><span class="sxs-lookup"><span data-stu-id="d414c-129">A report in Print Preview</span></span>
> - <span data-ttu-id="d414c-130">Ein Modul</span><span class="sxs-lookup"><span data-stu-id="d414c-130">A module</span></span>
> - <span data-ttu-id="d414c-131">Eine Serveransicht in der Datenblattansicht oder-Vorschau</span><span class="sxs-lookup"><span data-stu-id="d414c-131">A server view in Datasheet view or Print Preview</span></span>
> - <span data-ttu-id="d414c-132">Eine Datenzugriffsseite in der Seitenansicht</span><span class="sxs-lookup"><span data-stu-id="d414c-132">A data access page in Page view</span></span>
> - <span data-ttu-id="d414c-133">Eine Tabelle in der Datenblattansicht oder der Seitenansicht</span><span class="sxs-lookup"><span data-stu-id="d414c-133">A table in Datasheet view or Print Preview</span></span>
> - <span data-ttu-id="d414c-134">Eine Abfrage in der Datenblattansicht oder der Seitenansicht</span><span class="sxs-lookup"><span data-stu-id="d414c-134">A query in Datasheet view or Print Preview</span></span>
> - <span data-ttu-id="d414c-135">Eine gespeicherte Prozedur in der Datenblattansicht oder der Seitenansicht</span><span class="sxs-lookup"><span data-stu-id="d414c-135">A stored procedure in Datasheet view or Print Preview</span></span>

<span data-ttu-id="d414c-136">Die **SpeichernObjekt** -Aktion, unabhängig davon, ob in einem in der aktuellen Datenbank ausgeführten Makro oder in einer Bibliotheksdatenbank ausgeführt, speichert immer das angegebene Objekt oder das aktive Objekt in der Datenbank, in der das Objekt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d414c-136">The **SaveObject** action, whether it's carried out in a macro run in the current database or in a library database, always saves the specified object or the active object in the database in which the object was created.</span></span>

<span data-ttu-id="d414c-p106">Wenn Sie das aktive Objekt unter einem neuen Namen speichern, der Name jedoch mit dem Namen eines bereits vorhandenen Objekts übereinstimmt, werden Sie in einem Dialogfeld gefragt, ob Sie das vorhandene Objekt überschreiben möchten. Wenn Sie das Argument **Warnungen** der **Warnmeldungen** -Aktion auf **Nein** festgelegt haben, wird das Dialogfeld nicht angezeigt, und das alte Objekt wird automatisch überschrieben.</span><span class="sxs-lookup"><span data-stu-id="d414c-p106">If you save the active object with a new name, but the name is the same as the name of an existing object of this type, a dialog box asks if you want to overwrite the existing object. If you've set the **Warnings On** argument of the **SetWarnings** action to **No**, the dialog box isn't displayed and the old object is automatically overwritten.</span></span>

<span data-ttu-id="d414c-139">Verwenden Sie die **Save** -Methode des **DoCmd** -Objekts, um die **SpeichernObjekt** -Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d414c-139">To run the **SaveObject** action in a Visual Basic for Applications (VBA) module, use the **Save** method of the **DoCmd** object.</span></span>

