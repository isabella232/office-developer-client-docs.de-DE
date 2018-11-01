---
title: Makroereignis 'Vor Löschung'
TOCTitle: Before Delete Macro Event
ms:assetid: 1a8d3457-5c59-d13e-ada9-6ecd33dfd5b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845672(v=office.15)
ms:contentKeyID: 48543520
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm186077
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0ee4878a742454eb1b02f4b9a45c14ad79097c46
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876260"
---
# <a name="before-delete-macro-event"></a><span data-ttu-id="20e72-102">Makroereignis "Vor Löschung"</span><span class="sxs-lookup"><span data-stu-id="20e72-102">Before Delete Macro Event</span></span>

<span data-ttu-id="20e72-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="20e72-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="20e72-104">Das Ereignis **Vor Löschung** tritt ein, wenn ein Datensatz gelöscht wird, jedoch bevor der Commit für die Änderung erfolgt ist.</span><span class="sxs-lookup"><span data-stu-id="20e72-104">The **Before Delete** event occurs when a record is deleted, but before the change is committed.</span></span>

> [!NOTE]
> <span data-ttu-id="20e72-105">[!HINWEIS] Das Ereignis **Vor Löschung** ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="20e72-105">The **Before Delete** event is available only in Data Macros.</span></span>

## <a name="remarks"></a><span data-ttu-id="20e72-106">Hinweise</span><span class="sxs-lookup"><span data-stu-id="20e72-106">Remarks</span></span>

<span data-ttu-id="20e72-107">Mit dem Ereignis **Vor Löschung** führen Sie sämtliche Aktionen vor dem Löschen eines Datensatzes aus.</span><span class="sxs-lookup"><span data-stu-id="20e72-107">Use the **Before Delete** event to perform any actions that you want to occur before a record is deleted.</span></span> <span data-ttu-id="20e72-108">Das Ereignis **Vor Änderung** wird häufig verwendet, um Überprüfungen auszuführen und benutzerdefinierte Fehlermeldungen auszugeben.</span><span class="sxs-lookup"><span data-stu-id="20e72-108">The **Before Change** is commonly used to perform validation and to raise custom error messages.</span></span>

<span data-ttu-id="20e72-109">Sie können einen Wert in den Datensatz gelöscht wird, mithilfe der folgenden Syntax zugreifen:</span><span class="sxs-lookup"><span data-stu-id="20e72-109">You can access a value in the record to be deleted by using the following syntax:</span></span>

`[Old].[Field Name]`

<span data-ttu-id="20e72-110">Um den Wert des QuantityInStock-Felds im zu löschenden Datensatz zugreifen möchten, verwenden Sie beispielsweise die folgende Syntax:</span><span class="sxs-lookup"><span data-stu-id="20e72-110">For example, to access the value of the QuantityInStock field in the record to be deleted, use the following syntax:</span></span>

`[Old].[QuantityInStock]`

<span data-ttu-id="20e72-111">Am Ende des Ereignisses **Vor Löschung** werden die Werte im zu löschenden Datensatz dauerhaft gelöscht.</span><span class="sxs-lookup"><span data-stu-id="20e72-111">The values contained in the record to be deleted are deleted permanently when the **Before Delete** event ends.</span></span>

<span data-ttu-id="20e72-112">Sie können das Ereignis **Vor Löschung** mit der **Auslösenfehler** -Aktion abbrechen.</span><span class="sxs-lookup"><span data-stu-id="20e72-112">You can cancel the **Before Delete** event by using the **RaiseError** action.</span></span> <span data-ttu-id="20e72-113">Wenn ein Fehler ausgelöst wird, werden die Änderungen, die im Ereignis **Vor Löschung** enthaltenen verworfen.</span><span class="sxs-lookup"><span data-stu-id="20e72-113">When an error is raised, the changes contained in the **Before Delete** event are discarded.</span></span>

<span data-ttu-id="20e72-114">In der folgenden Tabelle sind Makros ausgeführt, die im Ereignis **Vor Löschung** verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="20e72-114">The following table lists macro commands that can be used in the **Before Delete** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="20e72-115">Befehlstyp</span><span class="sxs-lookup"><span data-stu-id="20e72-115">Command Type</span></span></p></th>
<th><p><span data-ttu-id="20e72-116">Command</span><span class="sxs-lookup"><span data-stu-id="20e72-116">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20e72-117">Programmablauf</span><span class="sxs-lookup"><span data-stu-id="20e72-117">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="20e72-118"><a href="comment-macro-statement.md">Kommentar-Makroanweisung</a></span><span class="sxs-lookup"><span data-stu-id="20e72-118"><a href="comment-macro-statement.md">Comment Macro Statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20e72-119">Programmablauf</span><span class="sxs-lookup"><span data-stu-id="20e72-119">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="20e72-120"><a href="group-macro-statement.md">Gruppieren-Makroanweisung</a></span><span class="sxs-lookup"><span data-stu-id="20e72-120"><a href="group-macro-statement.md">Group Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20e72-121">Programmablauf</span><span class="sxs-lookup"><span data-stu-id="20e72-121">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="20e72-122"><a href="if-then-else-macro-block.md">If... Im Anschluss: Makroblock</a></span><span class="sxs-lookup"><span data-stu-id="20e72-122"><a href="if-then-else-macro-block.md">If...Then...Else Macro Block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20e72-123">Datenblock</span><span class="sxs-lookup"><span data-stu-id="20e72-123">Data Block</span></span></p></td>
<td><p><span data-ttu-id="20e72-124"><a href="lookuprecord-data-block.md">NachschlagenDatensatz-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="20e72-124"><a href="lookuprecord-data-block.md">LookupRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20e72-125">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="20e72-125">Data Action</span></span></p></td>
<td><p><span data-ttu-id="20e72-126"><a href="clearmacroerror-macro-action.md">Löschenmakrofehler-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="20e72-126"><a href="clearmacroerror-macro-action.md">ClearMacroError Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20e72-127">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="20e72-127">Data Action</span></span></p></td>
<td><p><span data-ttu-id="20e72-128"><a href="onerror-macro-action.md">BeiFehler-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="20e72-128"><a href="onerror-macro-action.md">OnError Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20e72-129">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="20e72-129">Data Action</span></span></p></td>
<td><p><span data-ttu-id="20e72-130"><a href="raiseerror-macro-action.md">Auslösenfehler-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="20e72-130"><a href="raiseerror-macro-action.md">RaiseError Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20e72-131">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="20e72-131">Data Action</span></span></p></td>
<td><p><span data-ttu-id="20e72-132"><a href="setlocalvar-macro-action.md">FestlegenLokaleVar-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="20e72-132"><a href="setlocalvar-macro-action.md">SetLocalVar Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20e72-133">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="20e72-133">Data Action</span></span></p></td>
<td><p><span data-ttu-id="20e72-134"><a href="stopmacro-macro-action.md">StoppMakro-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="20e72-134"><a href="stopmacro-macro-action.md">StopMacro Macro Action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="20e72-135">Zum Erstellen eines Datenmakros, mit dem das Ereignis **Vor Löschung** erfasst wird, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="20e72-135">To create a Data macro that captures the **Before Delete** event, use the following steps.</span></span>

1.  <span data-ttu-id="20e72-136">Öffnen Sie die Tabelle, für die Sie das Ereignis **Vor Löschung** erfassen möchten.</span><span class="sxs-lookup"><span data-stu-id="20e72-136">Open the table for which you want to capture the **Before Delete** event.</span></span>

2.  <span data-ttu-id="20e72-137">Klicken Sie auf der Registerkarte **Tabelle** in der Gruppe **Vorabereignisse** wählen Sie **Vor dem Löschen**.</span><span class="sxs-lookup"><span data-stu-id="20e72-137">On the **Table** tab, in the **Before Events** group, select **Before Delete**.</span></span>

