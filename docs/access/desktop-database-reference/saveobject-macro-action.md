---
title: SpeichernObjekt-Makroaktion
TOCTitle: SaveObject Macro Action
ms:assetid: 85716dfc-f76f-ca47-cc40-f8f88162f85a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196789(v=office.15)
ms:contentKeyID: 48546060
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm116962
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 107b9b97b22f01b1caaf09ae10936abd8484684f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474597"
---
# <a name="saveobject-macro-action"></a><span data-ttu-id="a4fb8-102">SpeichernObjekt-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="a4fb8-102">SaveObject Macro Action</span></span>


<span data-ttu-id="a4fb8-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a4fb8-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a4fb8-104">Die **Speichernobjekt** -Aktion können Sie eine angegebene Access-Objekt oder das aktive Objekt speichern, wenn keines angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-104">You can use the **SaveObject** action to save either a specified Access object or the active object if none is specified.</span></span> <span data-ttu-id="a4fb8-105">Sie können auch das aktive Objekt unter einem neuen Namen in einigen Fällen speichern (diese Funktion identisch mit dem Befehl **Speichern unter** auf der **Symbolleiste für den Schnellzugriff**).</span><span class="sxs-lookup"><span data-stu-id="a4fb8-105">You can also save the active object with a new name in some cases (this functions the same as the **Save As** command on the **Quick Access Toolbar**).</span></span>


> [!NOTE]
> <P><span data-ttu-id="a4fb8-p102">[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. Informationen zur Aktivierung von Makros finden Sie unter den Links im Abschnitt See Also dieses Artikels.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="a4fb8-108">Einstellung</span><span class="sxs-lookup"><span data-stu-id="a4fb8-108">Setting</span></span>

<span data-ttu-id="a4fb8-109">Die **SpeichernObjekt** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-109">The **SaveObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a4fb8-110">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="a4fb8-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="a4fb8-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a4fb8-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a4fb8-112"><strong>Objekttyp</strong></span><span class="sxs-lookup"><span data-stu-id="a4fb8-112"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="a4fb8-p103">Der zu speichernde Objekttyp. Klicken Sie im Feld Objekttyp im Abschnitt Aktionsargumente des Bereichs Makro-Generator auf Tabelle, Abfrage, Formular, Bericht, Makro, Modul, Datenzugriffsseite, Serversicht, Diagramm, Gespeicherte Prozedur oder Funktion. Um das aktive Objekt auszuwählen, lassen Sie dieses Argument leer. Wenn Sie in diesem Argument einen Objekttyp auswählen, müssen Sie einen Namen eines bereits vorhandenen Objekts im Argument Objektname auswählen.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-p103">The type of object you want to save. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. To select the active object, leave this argument blank. If you select an object type in this argument, you must select an existing object's name in the <strong>Object Name</strong> argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4fb8-117"><strong>Objektname</strong></span><span class="sxs-lookup"><span data-stu-id="a4fb8-117"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="a4fb8-118">Der Name des Objekts gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-118">The name of the object to be saved.</span></span> <span data-ttu-id="a4fb8-119">Im Feld <strong>Objektname</strong> werden alle Objekte in der Datenbank mit dem Objekttyp angezeigt, der mit dem <strong>Objekttyp</strong> -Argument ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-119">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="a4fb8-120">Wenn Sie das Argument <strong>Objekttyp</strong> leer lassen, können Sie lassen dieses Argument leer, um das aktive Objekt speichern oder, in einigen Fällen geben Sie einen neuen Namen in dieses Argument auf das aktive Objekt mit diesem Namen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-120">If you leave the <strong>Object Type</strong> argument blank, you can leave this argument blank to save the active object, or, in some cases, enter a new name in this argument to save the active object with this name.</span></span> <span data-ttu-id="a4fb8-121">Wenn Sie einen neuen Namen eingeben, muss der Name den Standardnamenskonventionen für Microsoft Access-Objekte entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-121">If you enter a new name, the name must follow the standard naming conventions for Microsoft Access objects.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a4fb8-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a4fb8-122">Remarks</span></span>

<span data-ttu-id="a4fb8-123">Die **Speichernobjekt** -Aktion funktioniert für alle Datenbankobjekte, die der Benutzer explizit öffnen kann, und speichern.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-123">The **SaveObject** action works on all database objects that the user can explicitly open and save.</span></span> <span data-ttu-id="a4fb8-124">Das angegebene Objekt muss für die **Speichernobjekt** -Aktion haben keinen Einfluss auf das Objekt geöffnet sein.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-124">The specified object must be open for the **SaveObject** action to have any effect on the object.</span></span> <span data-ttu-id="a4fb8-125">Diese Aktion hat dieselbe Wirkung wie das Auswählen eines Objekts und klicken Sie dann speichern, indem Sie auf der **Symbolleiste für den Schnellzugriff**auf **Speichern** .</span><span class="sxs-lookup"><span data-stu-id="a4fb8-125">This action has the same effect as selecting an object and then saving it by clicking **Save** on the **Quick Access Toolbar**.</span></span> <span data-ttu-id="a4fb8-126">Das Argument **Objekttyp** leer lassen und einen neuen Namen eingeben, in das Argument **Objektname** hat dieselbe Wirkung wie das **Speichern unter** auf der **Symbolleiste für den Schnellzugriff**klicken und eingeben einen neuen Namen für das aktive Objekt.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-126">Leaving the **Object Type** argument blank and entering a new name in the **Object Name** argument has the same effect as clicking **Save As** on the **Quick Access Toolbar**, and entering a new name for the active object.</span></span> <span data-ttu-id="a4fb8-127">Verwenden die **Speichernobjekt** -Aktion können Sie ein Objekt angeben, speichern und den Befehl **Speichern unter** aus einem Makro ausführen.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-127">Using the **SaveObject** action enables you to specify an object to save and to perform a **Save As** command from a macro.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a4fb8-128">[!HINWEIS] Zum Speichern der folgenden Objekte unter einem neuen Namen können Sie die <STRONG>SpeichernObjekt</STRONG> -Aktion nicht verwenden:</span><span class="sxs-lookup"><span data-stu-id="a4fb8-128">You can't use the <STRONG>SaveObject</STRONG> action to save any of the following with a new name:</span></span></P>



  - <span data-ttu-id="a4fb8-129">Ein Formular in der Formularansicht oder Datenblattansicht.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-129">A form in Form view or Datasheet view.</span></span>

  - <span data-ttu-id="a4fb8-130">Ein Bericht in der Seitenansicht.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-130">A report in Print Preview.</span></span>

  - <span data-ttu-id="a4fb8-131">Ein Modul.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-131">A module.</span></span>

  - <span data-ttu-id="a4fb8-132">Eine Serversicht in der Datenblattansicht oder Seitenansicht.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-132">A server view in Datasheet view or Print Preview.</span></span>

  - <span data-ttu-id="a4fb8-133">Eine Datenzugriffsseite in der Seitenansicht.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-133">A data access page in Page view.</span></span>

  - <span data-ttu-id="a4fb8-134">Eine Tabelle in der Datenblattansicht oder Seitenansicht.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-134">A table in Datasheet view or Print Preview.</span></span>

  - <span data-ttu-id="a4fb8-135">Eine Abfrage in der Datenblattansicht oder Seitenansicht.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-135">A query in Datasheet view or Print Preview.</span></span>

  - <span data-ttu-id="a4fb8-136">Eine gespeicherte Prozedur in der Datenblattansicht oder Seitenansicht.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-136">A stored procedure in Datasheet view or Print Preview.</span></span>

<span data-ttu-id="a4fb8-137">Die **SpeichernObjekt** -Aktion, unabhängig davon, ob in einem in der aktuellen Datenbank ausgeführten Makro oder in einer Bibliotheksdatenbank ausgeführt, speichert immer das angegebene Objekt oder das aktive Objekt in der Datenbank, in der das Objekt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-137">The **SaveObject** action, whether it's carried out in a macro run in the current database or in a library database, always saves the specified object or the active object in the database in which the object was created.</span></span>

<span data-ttu-id="a4fb8-p106">Wenn Sie das aktive Objekt unter einem neuen Namen speichern, der Name jedoch mit dem Namen eines bereits vorhandenen Objekts übereinstimmt, werden Sie in einem Dialogfeld gefragt, ob Sie das vorhandene Objekt überschreiben möchten. Wenn Sie das Argument **Warnungen** der **Warnmeldungen** -Aktion auf **Nein** festgelegt haben, wird das Dialogfeld nicht angezeigt, und das alte Objekt wird automatisch überschrieben.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-p106">If you save the active object with a new name, but the name is the same as the name of an existing object of this type, a dialog box asks if you want to overwrite the existing object. If you've set the **Warnings On** argument of the **SetWarnings** action to **No**, the dialog box isn't displayed and the old object is automatically overwritten.</span></span>

<span data-ttu-id="a4fb8-140">Verwenden Sie die **Save** -Methode des **DoCmd** -Objekts, um die **SpeichernObjekt** -Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a4fb8-140">To run the **SaveObject** action in a Visual Basic for Applications (VBA) module, use the **Save** method of the **DoCmd** object.</span></span>

