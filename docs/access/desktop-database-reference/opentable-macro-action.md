---
title: ÖffnenTabelle-Makroaktion
TOCTitle: OpenTable Macro Action
ms:assetid: 4220ad3a-d064-0034-2806-ec1a447cebac
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192909(v=office.15)
ms:contentKeyID: 48544469
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm149011
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 729c1f14d49b3f80ec6307ce775066d3291b96de
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474505"
---
# <a name="opentable-macro-action"></a><span data-ttu-id="36dc4-102">ÖffnenTabelle-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="36dc4-102">OpenTable Macro Action</span></span>


<span data-ttu-id="36dc4-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="36dc4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="36dc4-p101">Sie können die **ÖffnenTabelle** -Aktion verwenden, um eine Tabelle in der Datenblattansicht, der Entwurfsansicht oder der Seitenansicht zu öffnen. Sie können auch einen Dateneingabemodus für die Tabelle auswählen.</span><span class="sxs-lookup"><span data-stu-id="36dc4-p101">You can use the **OpenTable** action to open a table in Datasheet view, Design view, or Print Preview. You can also select a data entry mode for the table.</span></span>

## <a name="setting"></a><span data-ttu-id="36dc4-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="36dc4-106">Setting</span></span>

<span data-ttu-id="36dc4-107">Die **ÖffnenTabelle** -Aktion verwendet die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="36dc4-107">The **OpenTable** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="36dc4-108">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="36dc4-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="36dc4-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36dc4-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="36dc4-110"><strong>Tabellenname</strong></span><span class="sxs-lookup"><span data-stu-id="36dc4-110"><strong>Table Name</strong></span></span></p></td>
<td><p><span data-ttu-id="36dc4-111">Der Name der zu öffnenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="36dc4-111">The name of the table to open.</span></span> <span data-ttu-id="36dc4-112">Das Feld <strong>Tabellenname</strong> im Abschnitt <strong>Aktionsargument</strong> des Makro-Generators zeigt alle Tabellen in der aktuellen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="36dc4-112">The <strong>Table Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all tables in the current database.</span></span> <span data-ttu-id="36dc4-113">Dies ist ein erforderliches Argument.</span><span class="sxs-lookup"><span data-stu-id="36dc4-113">This is a required argument.</span></span> <span data-ttu-id="36dc4-114">Wenn Sie ein Makro in einer Bibliotheksdatenbank ausführen, das die <strong>ÖffnenTabelle</strong>-Aktion enthält, sucht Microsoft Access zunächst in der Bibliotheksdatenbank nach der Tabelle mit diesem Namen und dann in der aktuellen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="36dc4-114">If you run a macro containing the <strong>OpenTable</strong> action in a library database, Microsoft Microsoft Access looks for the table with this name first in the library database, then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36dc4-115"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="36dc4-115"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="36dc4-p103">Die Ansicht, in der die Tabelle geöffnet wird. Klicken Sie im Feld <strong>Ansicht</strong> auf <strong>Datenblatt</strong>, <strong>Entwurf</strong>, <strong>Seitenansicht</strong>, <strong>PivotTable</strong> oder <strong>PivotChart</strong>. Die Standardeinstellung ist <strong>Datenblatt</strong>.</span><span class="sxs-lookup"><span data-stu-id="36dc4-p103">The view in which the table will open. Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36dc4-119"><strong>Data Mode</strong></span><span class="sxs-lookup"><span data-stu-id="36dc4-119"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="36dc4-p104">Der Dateneingabemodus für die Tabelle. Dies gilt nur für Tabellen, die in der Datenblattansicht geöffnet werden. Klicken Sie auf <strong>Hinzufügen</strong> (der Benutzer kann neue Datensätze hinzufügen, aber vorhandene Datensätze nicht bearbeiten), <strong>Bearbeiten</strong> (der Benutzer kann vorhandene Datensätze bearbeiten und neue Datensätze hinzufügen) oder <strong>Nur lesen</strong> (der Benutzer kann die Datensätze nur anzeigen). Die Standardeinstellung ist <strong>Bearbeiten</strong>.</span><span class="sxs-lookup"><span data-stu-id="36dc4-p104">The data entry mode for the table. This applies only to tables opened in Datasheet view. Click <strong>Add</strong> (the user can add new records but can't edit existing records), <strong>Edit</strong> (the user can edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records). The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="36dc4-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="36dc4-124">Remarks</span></span>

<span data-ttu-id="36dc4-125">Diese Aktion ist mit dem Doppelklicken auf die Tabelle im Navigationsbereich, dem Klicken mit der rechten Maustaste auf die Tabelle im Navigationsbereich und dem Auswählen einer Ansicht vergleichbar.</span><span class="sxs-lookup"><span data-stu-id="36dc4-125">This action is similar to double-clicking the table in the Navigation Pane, or right-clicking the table in the Navigation Pane and selecting a view.</span></span>


> [!TIP]
> <P><span data-ttu-id="36dc4-p105">[!TIPP] Sie können eine Tabelle aus dem Navigationsbereich in ein Aktionszeile-Makro ziehen. Dadurch wird automatisch eine <STRONG>ÖffnenTabelle</STRONG> -Aktion erstellt, die die Tabelle in der Datenblattansicht öffnet.</span><span class="sxs-lookup"><span data-stu-id="36dc4-p105">You can drag a table from the Navigation Pane to a macro action row. This automatically creates an <STRONG>OpenTable</STRONG> action that opens the table in Datasheet view.</span></span></P>



<span data-ttu-id="36dc4-128">Verwenden Sie die **OpenTable** -Methode des **DoCmd** -Objekts, um die **ÖffnenTabelle** -Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="36dc4-128">To run the **OpenTable** action in a Visual Basic for Applications (VBA) module, use the **OpenTable** method of the **DoCmd** object.</span></span>

