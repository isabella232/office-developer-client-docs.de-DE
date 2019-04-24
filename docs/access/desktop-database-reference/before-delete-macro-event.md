---
title: Makroereignis "Vor Löschung"
TOCTitle: Before Delete macro event
ms:assetid: 1a8d3457-5c59-d13e-ada9-6ecd33dfd5b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845672(v=office.15)
ms:contentKeyID: 48543520
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm186077
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2b2a4f978a4af2ba79cab7807f0142d35d7d30c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296913"
---
# <a name="before-delete-macro-event"></a><span data-ttu-id="66db9-102">Makroereignis "Vor Löschung"</span><span class="sxs-lookup"><span data-stu-id="66db9-102">Before Delete macro event</span></span>

<span data-ttu-id="66db9-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="66db9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="66db9-104">Das Ereignis **Vor Löschung** tritt ein, wenn ein Datensatz gelöscht wird, jedoch bevor der Commit für die Änderung erfolgt ist.</span><span class="sxs-lookup"><span data-stu-id="66db9-104">The **Before Delete** event occurs when a record is deleted, but before the change is committed.</span></span>

> [!NOTE]
> <span data-ttu-id="66db9-105">Das Ereignis **Vor Löschung** ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="66db9-105">The **Before Delete** event is available only in Data Macros.</span></span>

## <a name="remarks"></a><span data-ttu-id="66db9-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="66db9-106">Remarks</span></span>

<span data-ttu-id="66db9-107">Mit dem Ereignis **Vor Löschung** führen Sie sämtliche Aktionen vor dem Löschen eines Datensatzes aus.</span><span class="sxs-lookup"><span data-stu-id="66db9-107">Use the **Before Delete** event to perform any actions that you want to occur before a record is deleted.</span></span> <span data-ttu-id="66db9-108">Das Ereignis **Vor Änderung** wird häufig verwendet, um Überprüfungen auszuführen und benutzerdefinierte Fehlermeldungen auszugeben.</span><span class="sxs-lookup"><span data-stu-id="66db9-108">The **Before Change** is commonly used to perform validation and to raise custom error messages.</span></span>

<span data-ttu-id="66db9-109">Mithilfe der folgenden Syntax können Sie auf einen Wert im zu löschenden Datensatz zugreifen:</span><span class="sxs-lookup"><span data-stu-id="66db9-109">You can access a value in the record to be deleted by using the following syntax:</span></span>

`[Old].[Field Name]`

<span data-ttu-id="66db9-110">Verwenden Sie die folgende Syntax, um beispielsweise auf den Wert des QuantityInStock-Felds im zu löschenden Datensatz zuzugreifen:</span><span class="sxs-lookup"><span data-stu-id="66db9-110">For example, to access the value of the QuantityInStock field in the record to be deleted, use the following syntax:</span></span>

`[Old].[QuantityInStock]`

<span data-ttu-id="66db9-111">Am Ende des Ereignisses **Vor Löschung** werden die Werte im zu löschenden Datensatz dauerhaft gelöscht.</span><span class="sxs-lookup"><span data-stu-id="66db9-111">The values contained in the record to be deleted are deleted permanently when the **Before Delete** event ends.</span></span>

<span data-ttu-id="66db9-112">You can cancel the **Before Delete** event by using the **RaiseError** action.</span><span class="sxs-lookup"><span data-stu-id="66db9-112">You can cancel the **Before Delete** event by using the **RaiseError** action.</span></span> <span data-ttu-id="66db9-113">Wenn ein Fehler ausgelöst wird, werden die Änderungen im **BEFORE DELETE** -Ereignis verworfen.</span><span class="sxs-lookup"><span data-stu-id="66db9-113">When an error is raised, the changes contained in the **Before Delete** event are discarded.</span></span>

<span data-ttu-id="66db9-114">In der folgenden Tabelle sind Makros ausgeführt, die im Ereignis **Vor Löschung** verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="66db9-114">The following table lists macro commands that can be used in the **Before Delete** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="66db9-115">Befehlstyp</span><span class="sxs-lookup"><span data-stu-id="66db9-115">Command Type</span></span></p></th>
<th><p><span data-ttu-id="66db9-116">Befehl</span><span class="sxs-lookup"><span data-stu-id="66db9-116">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="66db9-117">Programmablauf</span><span class="sxs-lookup"><span data-stu-id="66db9-117">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="66db9-118"><a href="comment-macro-statement.md">Kommentar-Makroanweisung</a></span><span class="sxs-lookup"><span data-stu-id="66db9-118"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66db9-119">Programmablauf</span><span class="sxs-lookup"><span data-stu-id="66db9-119">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="66db9-120"><a href="group-macro-statement.md">Gruppieren-Makroanweisung</a></span><span class="sxs-lookup"><span data-stu-id="66db9-120"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66db9-121">Programmablauf</span><span class="sxs-lookup"><span data-stu-id="66db9-121">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="66db9-122"><a href="if-then-else-macro-block.md">Wenn...Dann...Sonst-Makroblock</a></span><span class="sxs-lookup"><span data-stu-id="66db9-122"><a href="if-then-else-macro-block.md">If...Then...Else macro block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66db9-123">Datenblock</span><span class="sxs-lookup"><span data-stu-id="66db9-123">Data Block</span></span></p></td>
<td><p><span data-ttu-id="66db9-124"><a href="lookuprecord-data-block.md">LookupRecord-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="66db9-124"><a href="lookuprecord-data-block.md">LookupRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66db9-125">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="66db9-125">Data Action</span></span></p></td>
<td><p><span data-ttu-id="66db9-126"><a href="clearmacroerror-macro-action.md">ClearMacroError-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="66db9-126"><a href="clearmacroerror-macro-action.md">ClearMacroError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66db9-127">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="66db9-127">Data Action</span></span></p></td>
<td><p><span data-ttu-id="66db9-128"><a href="onerror-macro-action.md">OnError-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="66db9-128"><a href="onerror-macro-action.md">OnError macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66db9-129">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="66db9-129">Data Action</span></span></p></td>
<td><p><span data-ttu-id="66db9-130"><a href="raiseerror-macro-action.md">RaiseError-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="66db9-130"><a href="raiseerror-macro-action.md">RaiseError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66db9-131">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="66db9-131">Data Action</span></span></p></td>
<td><p><span data-ttu-id="66db9-132"><a href="setlocalvar-macro-action.md">SetLocalVar-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="66db9-132"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66db9-133">Datenaktion</span><span class="sxs-lookup"><span data-stu-id="66db9-133">Data Action</span></span></p></td>
<td><p><span data-ttu-id="66db9-134"><a href="stopmacro-macro-action.md">StopMacro-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="66db9-134"><a href="stopmacro-macro-action.md">StopMacro macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="66db9-135">Zum Erstellen eines Datenmakros, mit dem das Ereignis **Vor Löschung** erfasst wird, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="66db9-135">To create a Data macro that captures the **Before Delete** event, use the following steps.</span></span>

1.  <span data-ttu-id="66db9-136">Öffnen Sie die Tabelle, für die Sie das Ereignis **Vor Löschung** erfassen möchten.</span><span class="sxs-lookup"><span data-stu-id="66db9-136">Open the table for which you want to capture the **Before Delete** event.</span></span>

2.  <span data-ttu-id="66db9-137">Wählen Sie auf der Registerkarte **Tabelle** in der Gruppe **before-Ereignisse** **vor löschen**aus.</span><span class="sxs-lookup"><span data-stu-id="66db9-137">On the **Table** tab, in the **Before Events** group, select **Before Delete**.</span></span>

