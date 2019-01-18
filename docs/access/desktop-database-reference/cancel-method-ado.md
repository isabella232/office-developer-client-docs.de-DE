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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713233"
---
# <a name="cancel-method-ado"></a><span data-ttu-id="98116-102">Cancel-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="98116-102">Cancel method (ADO)</span></span>

<span data-ttu-id="98116-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="98116-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="98116-104">Bricht die Ausführung eines ausstehenden asynchronen Methodenaufrufs ab.</span><span class="sxs-lookup"><span data-stu-id="98116-104">Cancels execution of a pending, asynchronous method call.</span></span>

## <a name="syntax"></a><span data-ttu-id="98116-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="98116-105">Syntax</span></span>

<span data-ttu-id="98116-106">- *Objekt*. Abbrechen</span><span class="sxs-lookup"><span data-stu-id="98116-106">*object*.Cancel</span></span>

## <a name="remarks"></a><span data-ttu-id="98116-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="98116-107">Remarks</span></span>

<span data-ttu-id="98116-108">Verwenden Sie die **Cancel** -Methode, um die Ausführung eines asynchronen Methodenaufrufs (d. h. einer mit der Option **adAsyncConnect**, **adAsyncExecute** oder **adAsyncFetch** aufgerufenen Methode) zu beenden.</span><span class="sxs-lookup"><span data-stu-id="98116-108">Use the **Cancel** method to terminate execution of an asynchronous method call (that is, a method invoked with the **adAsyncConnect**, **adAsyncExecute**, or **adAsyncFetch** option).</span></span>

<span data-ttu-id="98116-109">In der folgenden Tabelle wird gezeigt, welcher Task beendet wird, wenn Sie die **Cancel** -Methode für einen bestimmten Objekttyp verwenden.</span><span class="sxs-lookup"><span data-stu-id="98116-109">The following table shows what task is terminated when you use the **Cancel** method on a particular type of object.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><br />
<span data-ttu-id="98116-110"><em>Objekt</em></span><span class="sxs-lookup"><span data-stu-id="98116-110">If <em>object</em> is a</span></span></p></th>
<th><p><span data-ttu-id="98116-111">Der letzte asynchrone Aufruf dieser Methode wird beendet</span><span class="sxs-lookup"><span data-stu-id="98116-111">The last asynchronous call to this method is terminated</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="98116-112"><a href="command-object-ado.md">Command</a></span><span class="sxs-lookup"><span data-stu-id="98116-112"><a href="command-object-ado.md">Command</a></span></span></p></td>
<td><p><span data-ttu-id="98116-113"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">Ausführen</a></span><span class="sxs-lookup"><span data-stu-id="98116-113"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">Execute</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98116-114"><a href="connection-object-ado.md">Connection</a></span><span class="sxs-lookup"><span data-stu-id="98116-114"><a href="connection-object-ado.md">Connection</a></span></span></p></td>
<td><p><span data-ttu-id="98116-115"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">Execute</a> oder <a href="open-method-ado-connection.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="98116-115"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">Execute</a> or <a href="open-method-ado-connection.md">Open</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98116-116"><a href="record-object-ado.md">Record</a></span><span class="sxs-lookup"><span data-stu-id="98116-116"><a href="record-object-ado.md">Record</a></span></span></p></td>
<td><p><span data-ttu-id="98116-117"><a href="copyrecord-method-ado.md">CopyRecord</a>, <a href="deleterecord-method-ado.md">DeleteRecord</a>, <a href="moverecord-method-ado.md">MoveRecord</a> oder <a href="open-method-ado-record.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="98116-117"><a href="copyrecord-method-ado.md">CopyRecord</a>, <a href="deleterecord-method-ado.md">DeleteRecord</a>, <a href="moverecord-method-ado.md">MoveRecord</a>, or <a href="open-method-ado-record.md">Open</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98116-118"><a href="recordset-object-ado.md">Recordset</a></span><span class="sxs-lookup"><span data-stu-id="98116-118"><a href="recordset-object-ado.md">Recordset</a></span></span></p></td>
<td><p><span data-ttu-id="98116-119"><a href="open-method-ado-recordset.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="98116-119"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98116-120"><a href="stream-object-ado.md">Stream</a></span><span class="sxs-lookup"><span data-stu-id="98116-120"><a href="stream-object-ado.md">Stream</a></span></span></p></td>
<td><p><span data-ttu-id="98116-121"><a href="open-method-ado-stream.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="98116-121"><a href="open-method-ado-stream.md">Open</a></span></span></p></td>
</tr>
</tbody>
</table>

