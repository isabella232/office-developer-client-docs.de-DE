---
title: BearbeitenDatensatz-Datenblock
TOCTitle: EditRecord Data Block
ms:assetid: fe9f55eb-d7ed-1914-65a9-fa2fcb332b98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837277(v=office.15)
ms:contentKeyID: 48548940
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 07763e32e0f8687816dc39298f91733ca814d275
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472680"
---
# <a name="editrecord-data-block"></a><span data-ttu-id="c43d3-102">BearbeitenDatensatz-Datenblock</span><span class="sxs-lookup"><span data-stu-id="c43d3-102">EditRecord Data Block</span></span>

<span data-ttu-id="c43d3-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c43d3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c43d3-104">Mit dem **BearbeitenDatensatz** -Datenblock können Sie die Werte in einem vorhandenen Datensatz ändern.</span><span class="sxs-lookup"><span data-stu-id="c43d3-104">You can use the **EditRecord** data block to change the values contained in an existing record.</span></span>

> [!NOTE]
> <span data-ttu-id="c43d3-105">[!HINWEIS] Der **BearbeitenDatensatz** -Datenblock ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c43d3-105">The **EditRecord** data block is available only in Data Macros.</span></span>


## <a name="setting"></a><span data-ttu-id="c43d3-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="c43d3-106">Setting</span></span>

<span data-ttu-id="c43d3-107">Der **BearbeitenDatensatz** -Datenblock kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c43d3-107">The **EditRecord** data block has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c43d3-108">Argument</span><span class="sxs-lookup"><span data-stu-id="c43d3-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="c43d3-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c43d3-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c43d3-110"><strong>Alias</strong></span><span class="sxs-lookup"><span data-stu-id="c43d3-110"><strong>Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="c43d3-p101">Eine Zeichenfolge, mit der der zu bearbeitende Datensatz gekennzeichnet wird. Wenn das <em>Alias</em>-Argument nicht angegeben ist, wird der aktuelle Datensatz bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="c43d3-p101">A string that identifies the record to edit. If the <em>Alias</em> argument is not specified, then the current record is edited.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="c43d3-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c43d3-113">Remarks</span></span>

<span data-ttu-id="c43d3-p102">Nach der **BearbeitenDatensatz** -Anweisung können Sie einen Block von Befehlen einfügen, die ausgeführt werden, bevor für die Änderungen am Datensatz ein Commit erfolgt. In einem **BearbeitenDatensatz** -Datenblock sind die folgenden Aktionen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c43d3-p102">After **EditRecord** statement, you can insert a block of commands that will execute before the changes to the record are comitted. The following actions are available in a **EditRecord** data block.</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c43d3-116"><a href="cancelrecordchange-macro-action.md">AbbrechenDatensatzänderung-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="c43d3-116"><a href="cancelrecordchange-macro-action.md">CancelRecordChange Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c43d3-117"><a href="comment-macro-statement.md">Kommentar-Makroanweisung</a></span><span class="sxs-lookup"><span data-stu-id="c43d3-117"><a href="comment-macro-statement.md">Comment Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c43d3-118"><a href="group-macro-statement.md">Gruppieren-Makroanweisung</a></span><span class="sxs-lookup"><span data-stu-id="c43d3-118"><a href="group-macro-statement.md">Group Macro Statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c43d3-119"><a href="if-then-else-macro-block.md">If... Im Anschluss: Else-Makroanweisung</a></span><span class="sxs-lookup"><span data-stu-id="c43d3-119"><a href="if-then-else-macro-block.md">If...Then...Else Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c43d3-120"><a href="setfield-macro-action.md">FestlegenFeld-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="c43d3-120"><a href="setfield-macro-action.md">SetField Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c43d3-121"><a href="setlocalvar-macro-action.md">FestlegenLokaleVar-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="c43d3-121"><a href="setlocalvar-macro-action.md">SetLocalVar Macro Action</a></span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c43d3-122">Mit der **FestlegenFeld** -Aktion geben Sie die neuen Werte eines Felds im bearbeiteten Datensatz an.</span><span class="sxs-lookup"><span data-stu-id="c43d3-122">Use the **SetField** action to specify the new values of a field in the edited record.</span></span>

<span data-ttu-id="c43d3-123">Anschließend können Sie mit einer **Wenn...Dann...Sonst** -Anweisung Vorgänge auf der Grundlage einer Bedingung ausführen.</span><span class="sxs-lookup"><span data-stu-id="c43d3-123">You can use an **If...Then...Else** statment to perform operations based on a condition.</span></span>

<span data-ttu-id="c43d3-p103">Wenn Sie das Bearbeiten eines Datensatzes abbrechen möchten, verwenden Sie die **AbbrechenDatensatzänderung** -Aktion. Damit verhindern Sie, dass für die Änderungen ein Commit ausgeführt wird, und der **BearbeitenDatensatz** -Datenblock wird beendet.</span><span class="sxs-lookup"><span data-stu-id="c43d3-p103">To cancel the editing of a record, use the **CancelRecordChange** action. This prevents the changes from being committed and exits the **EditRecord** data block.</span></span>

<span data-ttu-id="c43d3-126">Über die lokale Variable **LetztesErstellenDatensatzID** in einem **DatensatzErstellen** -Datenblock können Sie mit dem zuletzt erstellten Datensatz arbeiten.</span><span class="sxs-lookup"><span data-stu-id="c43d3-126">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="c43d3-127">Verwenden Sie beispielsweise die folgende Syntax, um des Felds AssignedTo die zuletzt erstellte Datensatz zu verweisen:</span><span class="sxs-lookup"><span data-stu-id="c43d3-127">For example, use the following syntax to refer to the AssignedTo field of the most recently created record:</span></span>

`[LastCreateRecordIdentity].[AssignedTo]`

<span data-ttu-id="c43d3-128">Der DatensatzErstellen-Datenblock kann nur in den Datenmakroereignissen **[Nach Eingabe](after-insert-macro-event.md)**, **[Nach Aktualisierung](after-update-macro-event.md)** und **[Nach Aktualisierung](after-update-macro-event.md)** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c43d3-128">The CreateRecord data block can only be used in the **[After Insert](after-insert-macro-event.md)**, **[After Update](after-update-macro-event.md)**, and **[After Update](after-update-macro-event.md)** data macro events.</span></span>

