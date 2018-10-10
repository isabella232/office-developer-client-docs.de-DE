---
title: ÖffnenSicht-Makroaktion
TOCTitle: OpenView Macro Action
ms:assetid: 4d3b7e6d-4b81-4fbe-7222-24d745350321
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193569(v=office.15)
ms:contentKeyID: 48544726
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm50135
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ad607f852f5af21bc2979bd635286b86d18489a5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473906"
---
# <a name="openview-macro-action"></a><span data-ttu-id="32bca-102">ÖffnenSicht-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="32bca-102">OpenView Macro Action</span></span>


<span data-ttu-id="32bca-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="32bca-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="32bca-p101">In einem Access-Projekt können Sie die **ÖffnenSicht** -Aktion zum Öffnen einer Sicht in der Datenblattansicht, der Entwurfsansicht oder der Seitenansicht verwenden. Wenn die benannte Ansicht in der Datenblattansicht geöffnet wird, wird sie mit dieser Aktion ausgeführt. Für diese Ansicht können Sie die Dateneingabe auswählen und die in der Ansicht angezeigten Datensätze einschränken.</span><span class="sxs-lookup"><span data-stu-id="32bca-p101">In an Access project, you can use the **OpenView** action to open a view in Datasheet view, Design view, or Print Preview. This action runs the named view when opened in Datasheet view. You can select data entry for the view and restrict the records that the view displays.</span></span>


> [!NOTE]
> <P><span data-ttu-id="32bca-p102">[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. Informationen zur Aktivierung von Makros finden Sie unter den Links im Abschnitt See Also dieses Artikels.</span><span class="sxs-lookup"><span data-stu-id="32bca-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="32bca-109">Einstellung</span><span class="sxs-lookup"><span data-stu-id="32bca-109">Setting</span></span>

<span data-ttu-id="32bca-110">Die **ÖffnenSicht** -Aktion verwendet die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="32bca-110">The **OpenView** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="32bca-111">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="32bca-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="32bca-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="32bca-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32bca-113"><strong>Sichtname</strong></span><span class="sxs-lookup"><span data-stu-id="32bca-113"><strong>View Name</strong></span></span></p></td>
<td><p><span data-ttu-id="32bca-114">Der Name der Ansicht zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="32bca-114">The name of the view to open.</span></span> <span data-ttu-id="32bca-115">Das Feld <strong>Sichtname</strong> im Abschnitt <strong>Aktionsargument</strong> des Makro-Generators zeigt alle Ansichten in der aktuellen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="32bca-115">The <strong>View Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all views in the current database.</span></span> <span data-ttu-id="32bca-116">Dies ist ein erforderliches Argument.</span><span class="sxs-lookup"><span data-stu-id="32bca-116">This is a required argument.</span></span> <span data-ttu-id="32bca-117">Wenn Sie ein Makro, das die <strong>ÖffnenSicht</strong>-Aktion enthält, in einer Bibliotheksdatenbank ausführen, sucht Microsoft Access zuerst in der Bibliotheksdatenbank und dann in der aktuellen Datenbank nach dem Diagramm mit diesem Namen.</span><span class="sxs-lookup"><span data-stu-id="32bca-117">If you run a macro containing the <strong>OpenView</strong> action in a library database, Microsoft Access first looks for the view with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32bca-118"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="32bca-118"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="32bca-p104">Die Ansicht, in der die Sicht geöffnet wird. Klicken Sie im Feld <strong>Ansicht</strong> auf <strong>Datenblatt</strong>, <strong>Entwurf</strong>, <strong>Seitenansicht</strong>, <strong>PivotTable</strong> oder <strong>PivotChart</strong>. Die Standardeinstellung ist <strong>Datenblatt</strong>.</span><span class="sxs-lookup"><span data-stu-id="32bca-p104">The view in which the view will open. Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32bca-122"><strong>Data Mode</strong></span><span class="sxs-lookup"><span data-stu-id="32bca-122"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="32bca-p105">Der Dateneingabemodus für die Sicht. Dies gilt nur für Sichten, die in der Datenblattansicht geöffnet werden. Klicken Sie auf <strong>Hinzufügen</strong> (der Benutzer kann neue Datensätze hinzufügen, jedoch keine vorhandenen Datensätze anzeigen oder bearbeiten), <strong>Bearbeiten</strong> (der Benutzer kann vorhandene Datensätze anzeigen oder bearbeiten und neue Datensätze hinzufügen) oder <strong>Nur lesen</strong> (der Benutzer kann die Datensätze nur anzeigen). Die Standardeinstellung ist <strong>Bearbeiten</strong>.</span><span class="sxs-lookup"><span data-stu-id="32bca-p105">The data entry mode for the view. This applies only to views opened in Datasheet view. Click <strong>Add</strong> (the user can add new records but can't view or edit existing records), <strong>Edit</strong> (the user can view or edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records). The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="32bca-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="32bca-127">Remarks</span></span>

<span data-ttu-id="32bca-128">Diese Aktion ist mit dem Doppelklicken auf eine Ansicht im Navigationsbereich, dem Klicken mit der rechten Maustaste auf die Ansicht im Navigationsbereich und dem Klicken auf den gewünschten Befehl vergleichbar.</span><span class="sxs-lookup"><span data-stu-id="32bca-128">This action is similar to double-clicking a view in the Navigation Pane, or right-clicking the view in the Navigation Pane and then clicking the command you want.</span></span>

<span data-ttu-id="32bca-129">**Tipps**</span><span class="sxs-lookup"><span data-stu-id="32bca-129">**Tips**</span></span>

  - <span data-ttu-id="32bca-p106">Sie können eine Tabelle aus dem Navigationsbereich in ein Aktionszeile-Makro ziehen. Dadurch wird automatisch eine **ÖffnenSicht** -Aktion erstellt, die die Tabelle in der Datenblattansicht öffnet.</span><span class="sxs-lookup"><span data-stu-id="32bca-p106">You can drag a view from the Navigation Pane to a macro action row. This automatically creates an **OpenView** action that opens the view in Datasheet view.</span></span>

  - <span data-ttu-id="32bca-132">Wenn Sie die Systemmeldungen nicht anzeigen möchten, die normalerweise angezeigt werden, wenn eine Ansicht ausgeführt wird (sie melden, dass es sich um eine Sicht handelt und wie viele Datensätze betroffen sind), können Sie die **Warnmeldungen** -Aktion verwenden, um die Anzeige dieser Meldungen zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="32bca-132">If you don't want to display the system messages that normally appear when a view is run (indicating it is a view and showing how many records will be affected), you can use the **SetWarning** action to suppress the display of these messages.</span></span>

<span data-ttu-id="32bca-133">Verwenden Sie die **OpenView** -Methode des **DoCmd** -Objekts, um die **ÖffnenSicht** -Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="32bca-133">To run the **OpenView** action in a Visual Basic for Applications (VBA) module, use the **OpenView** method of the **DoCmd** object.</span></span>

