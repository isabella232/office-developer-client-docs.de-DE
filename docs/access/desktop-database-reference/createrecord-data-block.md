---
title: DatensatzErstellen-Datenblock
TOCTitle: CreateRecord data block
ms:assetid: e18f47f8-2aad-9a14-ad63-ab603a4d5b07
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835671(v=office.15)
ms:contentKeyID: 48548263
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 63e189143e77f9fcc42fa8d48c3ebfb2feda6633
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719816"
---
# <a name="createrecord-data-block"></a><span data-ttu-id="1f782-102">DatensatzErstellen-Datenblock</span><span class="sxs-lookup"><span data-stu-id="1f782-102">CreateRecord data block</span></span>


<span data-ttu-id="1f782-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1f782-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1f782-104">Mit dem **DatensatzErstellen** -Datenblock können Sie einen neuen Datensatz in der angegebenen Tabelle erstellen.</span><span class="sxs-lookup"><span data-stu-id="1f782-104">You can use the **CreateRecord** data block to create a new record in the specified table.</span></span>

> [!NOTE]
> <span data-ttu-id="1f782-105">[!HINWEIS] Der **DatensatzErstellen** -Datenblock ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1f782-105">The **CreateRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="1f782-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="1f782-106">Setting</span></span>

<span data-ttu-id="1f782-107">Der **DatensatzLöschen** -Datenblock kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1f782-107">The **CreateRecord** data block has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f782-108">Argument</span><span class="sxs-lookup"><span data-stu-id="1f782-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="1f782-109">Eingabe erforderlich</span><span class="sxs-lookup"><span data-stu-id="1f782-109">Required</span></span></p></th>
<th><p><span data-ttu-id="1f782-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f782-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f782-111"><strong>Datensatz erstellen in</strong></span><span class="sxs-lookup"><span data-stu-id="1f782-111"><strong>Create a Record In</strong></span></span></p></td>
<td><p><span data-ttu-id="1f782-112">Ja</span><span class="sxs-lookup"><span data-stu-id="1f782-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="1f782-113">Der Name der Tabelle, in der der neue Datensatz erstellt werden soll</span><span class="sxs-lookup"><span data-stu-id="1f782-113">The name of the table to create the new record in.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f782-114"><strong>Alias</strong></span><span class="sxs-lookup"><span data-stu-id="1f782-114"><strong>Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="1f782-115">Nein</span><span class="sxs-lookup"><span data-stu-id="1f782-115">No</span></span></p></td>
<td><p><span data-ttu-id="1f782-116">Eine Zeichenfolge zur Kennzeichnung des Datensatzes</span><span class="sxs-lookup"><span data-stu-id="1f782-116">An string that identifies the record.</span></span> <span data-ttu-id="1f782-117">Sie können den Alias des Datensatzes zur Kennzeichnung verwenden</span><span class="sxs-lookup"><span data-stu-id="1f782-117">You can use the record's alias to identify</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1f782-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1f782-118">Remarks</span></span>

<span data-ttu-id="1f782-119">Der mit **DatensatzErstellen** erstellte Datensatz wird automatisch als aktueller Datensatz festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1f782-119">The record created by **CreateRecord** automatically becomes the current record.</span></span>

<span data-ttu-id="1f782-120">Nach der **DatensatzErstellen** -Anweisung können Sie einen Block von Befehlen einfügen, die ausgeführt wird, bevor ein Commit für der neue Datensatz ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1f782-120">After **CreateRecord** statement, you can insert a block of commands that will execute before the new record is committed.</span></span> <span data-ttu-id="1f782-121">In einem **DatensatzErstellen** -Datenblock sind die folgenden Aktionen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1f782-121">The following actions are available in a **CreateRecord** data block.</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f782-122"><a href="cancelrecordchange-macro-action.md">CancelRecordChange-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="1f782-122"><a href="cancelrecordchange-macro-action.md">CancelRecordChange macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f782-123"><a href="comment-macro-statement.md">Kommentar-Makroanweisung</a></span><span class="sxs-lookup"><span data-stu-id="1f782-123"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f782-124"><a href="group-macro-statement.md">Gruppieren-Makroanweisung</a></span><span class="sxs-lookup"><span data-stu-id="1f782-124"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f782-125"><a href="if-then-else-macro-block.md">If... Im Anschluss: Else-makroanweisung</a></span><span class="sxs-lookup"><span data-stu-id="1f782-125"><a href="if-then-else-macro-block.md">If...Then...Else macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f782-126"><a href="setfield-macro-action.md">SetField-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="1f782-126"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f782-127"><a href="setlocalvar-macro-action.md">SetLocalVar-Makroaktion</a></span><span class="sxs-lookup"><span data-stu-id="1f782-127"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1f782-128">Wenn mit der **DatensatzErstellen** -Aktion ein Datensatz erstellt wurde, geben Sie mit der **FestlegenFeld** -Aktion den Wert eines Felds im neuen Datensatz an.</span><span class="sxs-lookup"><span data-stu-id="1f782-128">After the **CreateRecord** action creates a record, use the **SetField** action to specify a value of a field in the new record.</span></span>

<span data-ttu-id="1f782-129">Anschließend können Sie mit einer **Wenn...Dann...Sonst** -Anweisung Vorgänge auf der Grundlage einer Bedingung ausführen.</span><span class="sxs-lookup"><span data-stu-id="1f782-129">You can use an **If...Then...Else** statment to perform operations based on a condition.</span></span>

<span data-ttu-id="1f782-p103">Wenn Sie das Erstellen eines Datensatzes abbrechen möchten, verwenden Sie die **AbbrechenDatensatzänderung** -Aktion. Damit verhindern Sie, dass für die Änderungen ein Commit ausgeführt wird, und der **DatensatzErstellen** -Datenblock wird beendet.</span><span class="sxs-lookup"><span data-stu-id="1f782-p103">To cancel the creation of a record, use the **CancelRecordChange** action. This prevents the changes from being committed and exits the **CreateRecord** data block.</span></span>

<span data-ttu-id="1f782-132">Nachdem der neue Datensatz ein Commit ausgeführt wird, können Sie die lokale Variable **LastCreateRecordIdentity** den Eintrag entwickelt verwenden.</span><span class="sxs-lookup"><span data-stu-id="1f782-132">Once the new record is committed, you can use the **LastCreateRecordIdentity** local variable to work with the record.</span></span> <span data-ttu-id="1f782-133">Verwenden Sie beispielsweise die folgende Syntax, um des Felds AssignedTo die zuletzt erstellte Datensatz zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="1f782-133">For example, use the following syntax to refer to the AssignedTo field of the most recently created record.</span></span>

`[LastCreateRecordIdentity].[AssignedTo]`

<span data-ttu-id="1f782-134">Der **DatensatzErstellen** -Datenblock kann nur in den Datenmakroereignissen **[Nach Eingabe](after-insert-macro-event.md)**, **[Nach Aktualisierung](after-update-macro-event.md)** und **[Nach Aktualisierung](after-update-macro-event.md)** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1f782-134">The **CreateRecord** data block can only be used in the **[After Insert](after-insert-macro-event.md)**, **[After Update](after-update-macro-event.md)**, and **[After Update](after-update-macro-event.md)** data macro events.</span></span>

