---
title: Cancel-Methode (ADO)
TOCTitle: Cancel method (ADO)
ms:assetid: 747edc04-a5cc-3631-2d0b-82e7e41a76b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249476(v=office.15)
ms:contentKeyID: 48545662
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231032
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 791803bb8935ffab24e5aed7e4e6a77360e82b65
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296675"
---
# <a name="cancel-method-ado"></a><span data-ttu-id="1db00-102">Cancel-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="1db00-102">Cancel method (ADO)</span></span>

<span data-ttu-id="1db00-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1db00-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1db00-104">Die Ausführung eines ausstehenden asynchronen Methodenaufrufs wird abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="1db00-104">Cancels execution of a pending, asynchronous method call.</span></span>

## <a name="syntax"></a><span data-ttu-id="1db00-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1db00-105">Syntax</span></span>

<span data-ttu-id="1db00-106">- *Objekt*. Abbrechen</span><span class="sxs-lookup"><span data-stu-id="1db00-106">*object*.Cancel</span></span>

## <a name="remarks"></a><span data-ttu-id="1db00-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1db00-107">Remarks</span></span>

<span data-ttu-id="1db00-108">Verwenden Sie die **Cancel**-Methode, um die Ausführung eines asynchronen Methodenaufrufs (d. h. einer mit der Option **adAsyncConnect**, **adAsyncExecute** oder **adAsyncFetch** aufgerufenen Methode) zu beenden.</span><span class="sxs-lookup"><span data-stu-id="1db00-108">Use the **Cancel** method to terminate execution of an asynchronous method call (that is, a method invoked with the **adAsyncConnect**, **adAsyncExecute**, or **adAsyncFetch** option).</span></span>

<span data-ttu-id="1db00-109">In der folgenden Tabelle wird gezeigt, welcher Task beendet wird, wenn Sie die **Cancel** -Methode für einen bestimmten Objekttyp verwenden.</span><span class="sxs-lookup"><span data-stu-id="1db00-109">The following table shows what task is terminated when you use the **Cancel** method on a particular type of object.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><br />
<span data-ttu-id="1db00-110"><em>Objekt</em></span><span class="sxs-lookup"><span data-stu-id="1db00-110">If <em>object</em> is a</span></span></p></th>
<th><p><span data-ttu-id="1db00-111">Der letzte asynchrone Aufruf dieser Methode wird beendet</span><span class="sxs-lookup"><span data-stu-id="1db00-111">The last asynchronous call to this method is terminated</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1db00-112"><a href="command-object-ado.md">Befehl</a></span><span class="sxs-lookup"><span data-stu-id="1db00-112"><a href="command-object-ado.md">Command</a></span></span></p></td>
<td><p><span data-ttu-id="1db00-113"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">Execute</a></span><span class="sxs-lookup"><span data-stu-id="1db00-113"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">Execute</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1db00-114"><a href="connection-object-ado.md">Connection</a></span><span class="sxs-lookup"><span data-stu-id="1db00-114"><a href="connection-object-ado.md">Connection</a></span></span></p></td>
<td><p><span data-ttu-id="1db00-115"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">Execute</a> oder <a href="open-method-ado-connection.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="1db00-115"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">Execute</a> or <a href="open-method-ado-connection.md">Open</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1db00-116"><a href="record-object-ado.md">Record</a></span><span class="sxs-lookup"><span data-stu-id="1db00-116"><a href="record-object-ado.md">Record</a></span></span></p></td>
<td><p><span data-ttu-id="1db00-117"><a href="copyrecord-method-ado.md">CopyRecord</a>, <a href="deleterecord-method-ado.md">DeleteRecord</a>, <a href="moverecord-method-ado.md">MoveRecord</a> oder <a href="open-method-ado-record.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="1db00-117"><a href="copyrecord-method-ado.md">CopyRecord</a>, <a href="deleterecord-method-ado.md">DeleteRecord</a>, <a href="moverecord-method-ado.md">MoveRecord</a>, or <a href="open-method-ado-record.md">Open</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1db00-118"><a href="recordset-object-ado.md">Recordset</a></span><span class="sxs-lookup"><span data-stu-id="1db00-118"><a href="recordset-object-ado.md">Recordset</a></span></span></p></td>
<td><p><span data-ttu-id="1db00-119"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="1db00-119"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1db00-120"><a href="stream-object-ado.md">Stream</a></span><span class="sxs-lookup"><span data-stu-id="1db00-120"><a href="stream-object-ado.md">Stream</a></span></span></p></td>
<td><p><span data-ttu-id="1db00-121"><a href="open-method-ado-stream.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="1db00-121"><a href="open-method-ado-stream.md">Open</a></span></span></p></td>
</tr>
</tbody>
</table>

