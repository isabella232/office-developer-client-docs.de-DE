---
title: CopyObject-Makroaktion
TOCTitle: CopyObject macro action
ms:assetid: 746f61df-d5db-284a-0897-75820c2be11f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195876(v=office.15)
ms:contentKeyID: 48545661
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12836
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2d1fb13d04691b7bf5e0aafcc484cfc4f471e1e1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715886"
---
# <a name="copyobject-macro-action"></a><span data-ttu-id="966d1-102">CopyObject-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="966d1-102">CopyObject macro action</span></span>

<span data-ttu-id="966d1-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="966d1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="966d1-p101">Sie können die **KopierenObjekt** -Aktion verwenden, um das angegebene Datenbankobjekt in eine andere Access-Datenbank oder innerhalb derselben Datenbank oder desselben Access-Projekts unter einem neuen Namen zu kopieren. Sie können ein vorhandenes Objekt beispielsweise in eine andere Datenbank kopieren oder dort sichern oder schnell durch einige Änderungen ein ähnliches Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="966d1-p101">You can use the **CopyObject** action to copy the specified database object to a different Access database or to the same database or Access project under a new name. For example, you can copy or back up an existing object in another database or quickly create a similar object with a few changes.</span></span>

> [!NOTE]
> <span data-ttu-id="966d1-106">[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist.</span><span class="sxs-lookup"><span data-stu-id="966d1-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="966d1-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="966d1-107">Setting</span></span>

<span data-ttu-id="966d1-108">Die **KopierenObjekt** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="966d1-108">The **CopyObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="966d1-109">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="966d1-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="966d1-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="966d1-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="966d1-111"><strong>Zieldatenbank</strong></span><span class="sxs-lookup"><span data-stu-id="966d1-111"><strong>Destination Database</strong></span></span></p></td>
<td><p><span data-ttu-id="966d1-p102">Ein gültiger Pfad und Dateiname für die Zieldatenbank. Geben Sie den Pfad und den Dateinamen im Feld Zieldatenbank im Abschnitt Aktionsargumente des Bereichs Makro-Generator ein. Lassen Sie dieses Argument leer, wenn die aktuelle Datenbank ausgewählt werden soll. 

</span><span class="sxs-lookup"><span data-stu-id="966d1-p102">A valid path and file name for the destination database. Enter the path and file name in the <strong>Destination Database</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. Leave this argument blank if you want to select the current database.</span></span></p><p><span data-ttu-id="966d1-115"><strong>Hinweis</strong>: dieses Argument ist nur in der Umgebung für Access-Datenbank verfügbar.</span><span class="sxs-lookup"><span data-stu-id="966d1-115"><strong>NOTE</strong>: This argument is only available in the Access database environment.</span></span> <span data-ttu-id="966d1-116">Wenn Sie diese Aktion in einer Umgebung für Access-Projekt (ADP) verwenden, muss das Argument Zieldatenbank leer sein.</span><span class="sxs-lookup"><span data-stu-id="966d1-116">When using this action in an Access project environment (.adp), the Destination Database argument must be blank.</span></span></p>
<p><span data-ttu-id="966d1-117">Wenn Sie ein Makro, das die <strong>KopierenObjekt</strong>-Aktion enthält, in einer Bibliotheksdatenbank ausführen und dieses Argument leer lassen, wird dieses Objekt von Microsoft Office Access 2007 in die Bibliotheksdatenbank kopiert.</span><span class="sxs-lookup"><span data-stu-id="966d1-117">If you run a macro containing the <strong>CopyObject</strong> action in a library database and leave this argument blank, Microsoft Office Access 2007 will copy the object into the library database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="966d1-118"><strong>Neuer Name</strong></span><span class="sxs-lookup"><span data-stu-id="966d1-118"><strong>New Name</strong></span></span></p></td>
<td><p><span data-ttu-id="966d1-p104">Ein neuer Name für das Objekt. Lassen Sie dieses Argument beim Kopieren in eine andere Datenbank leer, um den Namen beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="966d1-p104">A new name for the object. When copying to a different database, leave this argument blank to keep the same name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="966d1-121"><strong>Objekttyp (Herkunft)</strong></span><span class="sxs-lookup"><span data-stu-id="966d1-121"><strong>Source Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="966d1-p105">Der Objekttyp, den Sie kopieren möchten. Klicken Sie auf <strong>Tabelle</strong>, <strong>Abfrage</strong>, <strong>Formular</strong>, <strong>Bericht</strong>, <strong>Makro</strong>, <strong>Modul</strong>, <strong>Datenzugriffsseite</strong>, <strong>Serversicht</strong>, <strong>Diagramm</strong>, <strong>Gespeicherte Prozedur</strong> oder <strong>Funktion</strong>. Lassen Sie dieses Argument leer, um das im Navigationsbereich ausgewählte Objekt zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="966d1-p105">The object type you want to copy. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong>. To copy the object selected in the Navigation Pane, leave this argument blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="966d1-125"><strong>Objektname (Herkunft)</strong></span><span class="sxs-lookup"><span data-stu-id="966d1-125"><strong>Source Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="966d1-126">Der Name des zu kopierenden Objekts.</span><span class="sxs-lookup"><span data-stu-id="966d1-126">The name of the object to be copied.</span></span> <span data-ttu-id="966d1-127">Das Feld <strong>Objektname Quelle</strong> zeigt alle Objekte in der Datenbank an, die durch das Argument <strong>Objekttyp Quelle</strong> .</span><span class="sxs-lookup"><span data-stu-id="966d1-127">The <strong>Source Object Name</strong> box shows all objects in the database of the type selected by the <strong>Source Object Type</strong> argument.</span></span> <span data-ttu-id="966d1-128">Klicken Sie im Feld <strong>Objektname Quelle</strong> auf das zu kopierende Objekt.</span><span class="sxs-lookup"><span data-stu-id="966d1-128">In the <strong>Source Object Name</strong> box, click the object to copy.</span></span> <span data-ttu-id="966d1-129">Lassen Sie dieses Argument leer, wenn Sie das Argument <strong>Objekttyp Quelle</strong> leer lassen.</span><span class="sxs-lookup"><span data-stu-id="966d1-129">If you leave the <strong>Source Object Type</strong> argument blank, leave this argument blank also.</span></span> <span data-ttu-id="966d1-130">Wenn Sie ein Makro ausführen, das die <strong>KopierenObjekt</strong>-Aktion in einer Bibliotheksdatenbank enthält, sucht Access zunächst in der Bibliotheksdatenbank und dann in der aktuellen Datenbank nach dem Objekt mit diesem Namen.</span><span class="sxs-lookup"><span data-stu-id="966d1-130">If you run a macro containing the <strong>CopyObject</strong> action in a library database, Access first looks for the object with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="966d1-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="966d1-131">Remarks</span></span>

<span data-ttu-id="966d1-132">Sie müssen für diese Aktion für mindestens eines der Argumente **Zieldatenbank** und **Neuer Name** einen Wert eingeben.</span><span class="sxs-lookup"><span data-stu-id="966d1-132">You must enter a value for either one or both of the **Destination Database** and **New Name** arguments for this action.</span></span>

<span data-ttu-id="966d1-p107">Wenn Sie die Argumente Objekttyp (Herkunft) und Objektname (Herkunft) leer lassen, wird das im Navigationsbereich ausgewählte Objekt von Access kopiert. Zum Auswählen eines Objekts im Navigationsbereich können Sie die AuswählenObjekt-Aktion verwenden, wobei das Argument Im Navigationsbereich auf Ja festgelegt sein muss.</span><span class="sxs-lookup"><span data-stu-id="966d1-p107">If you leave the **Source Object Type** and **Source Object Name** arguments blank, Access copies the object selected in the Navigation Pane. To select an object in the Navigation Pane, you can use the **SelectObject** action with the In Navigation Pane argument set to **Yes**.</span></span>

<span data-ttu-id="966d1-135">Die **KopierenObjekt** -Aktion ist mit dem manuellen Ausführen der folgenden Schritte vergleichbar:</span><span class="sxs-lookup"><span data-stu-id="966d1-135">The **CopyObject** action is similar to performing the following steps manually:</span></span>

1. <span data-ttu-id="966d1-136">Wählen Sie ein Objekt im Navigationsbereich aus.</span><span class="sxs-lookup"><span data-stu-id="966d1-136">Select an object in the Navigation Pane.</span></span>

2. <span data-ttu-id="966d1-137">Klicken Sie auf der Registerkarte Home in der Gruppe Clipboard auf Copy.</span><span class="sxs-lookup"><span data-stu-id="966d1-137">On the Home tab, in the Clipboard group, click Copy.</span></span>

3. <span data-ttu-id="966d1-p108">Klicken Sie auf derselben Registerkarte auf **Einfügen**.Das Dialogfeld **Einfügen als** wird angezeigt, damit Sie dem Objekt einen neuen Namen zuweisen können. Diese Schritte werden von der **KopierenObjekt** -Aktion automatisch ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="966d1-p108">On the same tab, click **Paste**.The **Paste As** dialog box appears so that you can give the object a new name. The **CopyObject** action performs all of these steps automatically.</span></span>

> [!NOTE]
> <span data-ttu-id="966d1-140">[!HINWEIS] Beim Kopieren von Datenzugriffsseiten kopiert die **KopierenObjekt** -Aktion nur die Verknüpfung zur zugeordneten HTM-Datei und nicht die Datei selbst.</span><span class="sxs-lookup"><span data-stu-id="966d1-140">When copying data access pages, the **CopyObject** action copies only the link to the associated .htm file, not the file itself.</span></span>

<span data-ttu-id="966d1-p109">Der Pfad und der Dateiname der Zieldatenbank müssen vorhanden sein, bevor das Makro die **KopierenObjekt** -Aktion ausführt. Wenn sie nicht vorhanden sind, zeigt Access eine Fehlermeldung an.</span><span class="sxs-lookup"><span data-stu-id="966d1-p109">The path and file name of the destination database must exist before the macro runs the **CopyObject** action. If they don't exist, Access displays an error message.</span></span>

<span data-ttu-id="966d1-143">Verwenden Sie die **CopyObject** -Methode des **DoCmd** -Objekts, um die **KopierenObjekt** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="966d1-143">To run the **CopyObject** action in a Visual Basic for Applications (VBA) module, use the **CopyObject** method of the **DoCmd** object.</span></span>

<span data-ttu-id="966d1-p110">Sie können ein Objekt, das im Navigationsbereich ausgewählt wurde, oder ein derzeit geöffnetes Objekt auch manuell kopieren, indem Sie auf die Registerkarte **Datei** und dann auf **Speichern unter** klicken. Dieser Befehl erstellt nur in der aktuellen Datenbank eine Kopie des Objekts. Geben Sie im Dialogfeld **Speichern unter** den Namen für die Kopie ein, und wählen Sie den zu speichernden Objekttyp aus. Falls das ursprüngliche Objekt bereits gespeichert wurde und Sie es in der aktuellen Datenbank unter einem neuen Namen speichern, bleibt die ursprüngliche Version mit dem alten Namen weiterhin vorhanden.</span><span class="sxs-lookup"><span data-stu-id="966d1-p110">You can also manually copy an object selected in the Navigation Pane, or an object that is currently open, by clicking the **File** tab and then clicking **Save As**. This command will make a copy of the object in the current database only. In the **Save As** dialog box, enter the name for the copy, and choose what type of object you want to save it as. If the original object has already been saved and you save it in the current database with a new name, the original version still exists with its old name.</span></span>

<span data-ttu-id="966d1-148">So kopieren Sie ein Objekt manuell in eine andere Access-Datenbank:</span><span class="sxs-lookup"><span data-stu-id="966d1-148">To manually copy an object to a different Access database:</span></span>

1. <span data-ttu-id="966d1-149">Klicken Sie auf der Registerkarte **Externe Daten** in der Gruppe **Exportieren** auf **Mehr**, und klicken Sie dann auf **Access-Datenbank**.</span><span class="sxs-lookup"><span data-stu-id="966d1-149">On the **External Data** tab, in the **Export** group, click **More** and then click **Access Database**.</span></span>

2. <span data-ttu-id="966d1-150">Geben Sie im Dialogfeld **Exportieren - Access-Datenbank** den Dateinamen der Zieldatenbank ein.-oder-Klicken Sie auf **Durchsuchen**, um das Dialogfeld **Datei speichern** anzuzeigen, suchen Sie die Zieldatenbank, und klicken Sie dann auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="966d1-150">In the **Export - Access Database** dialog box, enter the file name of the destination database.-or-Click **Browse** to display the **File Save** dialog box, locate the destination database, and then click **Save**.</span></span>

3. <span data-ttu-id="966d1-p111">Klicken Sie im Dialogfeld **Exportieren - Access-Datenbank** auf **OK**. Das Dialogfeld **Exportieren** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="966d1-p111">In the **Export - Access Database** dialog box, click **OK**. The **Export** dialog box appears.</span></span>

4. <span data-ttu-id="966d1-p112">Geben Sie im Dialogfeld **Exportieren** einen Namen für das Objekt in der Zieldatenbank ein. Wählen Sie eine beliebige anwendbare Option für Tabellen aus, z. B. **Definitionen und Daten exportieren** oder **Nur Definitionen**. Klicken Sie auf **OK**, wenn Sie den Vorgang abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="966d1-p112">In the **Export** dialog box, enter a name for the object in the destination database. Choose any applicable options, such as **Export Definition and Data** or **Definition Only** for tables. When you are finished, click **OK**.</span></span>

