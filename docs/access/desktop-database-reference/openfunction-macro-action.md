---
title: OpenFunction-Makroaktion
TOCTitle: OpenFunction macro action
ms:assetid: 0446dbb9-c342-9225-27ba-b8a6892030e1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844833(v=office.15)
ms:contentKeyID: 48543005
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89179
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2a9a96b22669889cf4dc51984fc3d3c9f7623428
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930224"
---
# <a name="openfunction-macro-action"></a><span data-ttu-id="a1643-102">OpenFunction-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="a1643-102">OpenFunction macro action</span></span>


<span data-ttu-id="a1643-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a1643-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a1643-p101">In einem Access-Projekt können Sie mithilfe der **ÖffnenFunktion** -Aktion eine benutzerdefinierte Funktion in der Datenblattansicht, in der Entwurfsansicht der Inlinefunktion, in der SQL-Texteditor-Ansicht (für eine benutzerdefinierte Skalarfunktion oder Tabellenfunktion) oder in der Seitenansicht öffnen. Mit dieser Aktion wird die benutzerdefinierte Funktion beim Öffnen in der Datenblattansicht ausgeführt. Sie können für die benutzerdefinierte Funktion auch den Dateneingabemodus auswählen und die von der benutzerdefinierten Funktion angezeigten Datensätze einschränken.</span><span class="sxs-lookup"><span data-stu-id="a1643-p101">In an Access project, you can use the **OpenFunction** action to open a user-defined function in Datasheet view, inline function Design view, SQL Text Editor view (for a scalar or table user-defined function), or Print Preview. This action runs the user-defined function when opened in Datasheet view. You can also select the data entry mode for the user-defined function and restrict the records that the user-defined function displays.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a1643-p102">[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. Informationen zur Aktivierung von Makros finden Sie unter den Links im Abschnitt See Also dieses Artikels.</span><span class="sxs-lookup"><span data-stu-id="a1643-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="a1643-109">Einstellung</span><span class="sxs-lookup"><span data-stu-id="a1643-109">Setting</span></span>

<span data-ttu-id="a1643-110">Die **ÖffnenFunktion** -Aktion verwendet die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="a1643-110">The **OpenFunction** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a1643-111">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="a1643-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="a1643-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1643-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1643-113"><strong>Funktionsname</strong></span><span class="sxs-lookup"><span data-stu-id="a1643-113"><strong>Function Name</strong></span></span></p></td>
<td><p><span data-ttu-id="a1643-114">Der Name der benutzerdefinierten Funktion zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a1643-114">The name of the user-defined function to open.</span></span> <span data-ttu-id="a1643-115">Feld <strong>Funktionsname</strong> im Abschnitt <strong>Aktionsargument</strong> des Makro-Generators werden alle benutzerdefinierten Funktionen in der aktuellen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="a1643-115">The <strong>Function Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all user-defined functions in the current database.</span></span> <span data-ttu-id="a1643-116">Dies ist ein Argument erforderlich. Wenn Sie ein Makro mit der <strong>ÖffnenFunktion</strong> -Aktion in einer Bibliotheksdatenbank ausführen, sucht Microsoft Access zuerst die Funktion mit diesem Namen in der Bibliotheksdatenbank und dann in der aktuellen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="a1643-116">This is a required argument.If you run a macro containing the <strong>Function</strong> action in a library database, Microsoft Access first looks for the function with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1643-117"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="a1643-117"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="a1643-p104">Die Ansicht, in der die benutzerdefinierte Funktion geöffnet wird. Klicken Sie im Feld <strong>Ansicht</strong> auf <strong>Datenblatt</strong>, <strong>Entwurf</strong>, <strong>Seitenansicht</strong>, <strong>PivotTable</strong> oder <strong>PivotChart</strong>. Die Standardeinstellung ist <strong>Datenblatt</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1643-p104">The view in which the user-defined function will open. Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1643-121"><strong>Data Mode</strong></span><span class="sxs-lookup"><span data-stu-id="a1643-121"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="a1643-p105">Der Dateneingabemodus für die benutzerdefinierte Funktion. Dieser gilt nur für benutzerdefinierte Funktionen, die in der Datenblattansicht geöffnet sind. Klicken Sie auf <strong>Hinzufügen</strong> (der Benutzer kann neue Datensätze hinzufügen, vorhandene Datensätze jedoch nicht anzeigen oder bearbeiten), <strong>Bearbeiten</strong> (der Benutzer kann vorhandene Datensätze anzeigen oder bearbeiten und neue Datensätze hinzufügen) oder <strong>Schreibgeschützt</strong> (der Benutzer kann Datensätze nur anzeigen). Die Standardeinstellung ist <strong>Bearbeiten</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1643-p105">The data entry mode for the user-defined function. This applies only to user-defined functions opened in Datasheet view. Click <strong>Add</strong> (the user can add new records but can't view or edit existing records), <strong>Edit</strong> (the user can view or edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records). The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a1643-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a1643-126">Remarks</span></span>

<span data-ttu-id="a1643-127">Diese Aktion bewirkt dasselbe, wie wenn Sie auf eine benutzerdefinierte Funktion im Navigationsbereich doppelklicken oder mit der rechten Maustaste auf die Funktion im Navigationsbereich klicken und dann eine Ansicht auswählen.</span><span class="sxs-lookup"><span data-stu-id="a1643-127">This action is similar to double-clicking a user-defined function in the Navigation Pane, or right-clicking the function in the Navigation Pane and selecting a view.</span></span>

<span data-ttu-id="a1643-p106">Wenn Sie zur Entwurfsansicht wechseln, während die benutzerdefinierte Funktion geöffnet ist, wird die Einstellung des Arguments **Datenmodus** für die benutzerdefinierte Funktion entfernt. Diese Einstellung ist nicht wirksam, auch wenn der Benutzer zur Datenblattansicht zurückkehrt.</span><span class="sxs-lookup"><span data-stu-id="a1643-p106">Switching to Design view while the user-defined function is open removes the **Data Mode** argument setting for the user-defined function. This setting is not in effect, even if the user returns to Datasheet view.</span></span>

<span data-ttu-id="a1643-130">**Tipps**</span><span class="sxs-lookup"><span data-stu-id="a1643-130">**Tips**</span></span>

  - <span data-ttu-id="a1643-p107">Sie können eine benutzerdefinierte Funktion im Navigationsbereich auswählen und in die Aktionszeile eines Makros ziehen. Damit wird automatisch eine **ÖffnenFormular** -Aktion erstellt, mit der die benutzerdefinierte Funktion in der Datenblattansicht geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="a1643-p107">You can select a user-defined function in the Navigation Pane and drag it to a macro action row. This automatically creates an **OpenFunction** action that opens the user-defined function in Datasheet view.</span></span>

  - <span data-ttu-id="a1643-133">Wenn Sie nicht möchten, dass die Systemmeldungen angezeigt werden, die normalerweise angezeigt werden (und anzeigen, dass es sich um eine benutzerdefinierte Funktion handelt, und angeben, wie viele Datensätze betroffen sind), wenn eine benutzerdefinierte Funktion ausgeführt wird, können Sie die Anzeige dieser Meldungen mithilfe der **Warnmeldungen** -Aktion unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="a1643-133">If you don't want to display the system messages that normally appear when a user-defined function is run (indicating it is a user-defined function and showing how many records will be affected), you can use the **SetWarning** action to suppress the display of these messages.</span></span>

<span data-ttu-id="a1643-134">Wenn Sie die **ÖffnenFunktion** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) ausführen möchten, verwenden Sie die **OpenFunction** -Methode des **DoCmd** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="a1643-134">To run the **OpenFunction** action in a Visual Basic for Applications (VBA) module, use the **OpenFunction** method of the **DoCmd** object.</span></span>

