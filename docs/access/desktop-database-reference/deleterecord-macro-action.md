---
title: DeleteRecord-Makroaktion
TOCTitle: DeleteRecord macro action
ms:assetid: c656a72c-c037-76a5-dc07-f6eccb6590dd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823132(v=office.15)
ms:contentKeyID: 48547624
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8fb20068052972696b09ea0d2165b344e97ea922
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28725952"
---
# <a name="deleterecord-macro-action"></a><span data-ttu-id="4217a-102">DeleteRecord-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="4217a-102">DeleteRecord macro action</span></span>

<span data-ttu-id="4217a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4217a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4217a-104">Mit der **DatensatzLöschen** -Aktion können Sie einen Datensatz löschen.</span><span class="sxs-lookup"><span data-stu-id="4217a-104">You can use the **DeleteRecord** action to delete a record.</span></span>

## <a name="setting"></a><span data-ttu-id="4217a-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="4217a-105">Setting</span></span>

<span data-ttu-id="4217a-106">Der **DatensatzLöschen** -Datenblock kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4217a-106">The **CreateRecord** data block has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4217a-107">Argument</span><span class="sxs-lookup"><span data-stu-id="4217a-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="4217a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4217a-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4217a-109"><strong>Datensatzalias</strong></span><span class="sxs-lookup"><span data-stu-id="4217a-109"><strong>Record Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="4217a-p101">Eine Zeichenfolge, mit der der zu löschende Datensatz gekennzeichnet wird. Wenn das <em>Alias</em>-Argument nicht angegeben ist, wird der aktuelle Datensatz gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4217a-p101">A string that identifies the record to delete. If the <em>Alias</em> argument is not specified, then the current record is deleted.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="4217a-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4217a-112">Remarks</span></span>

<span data-ttu-id="4217a-113">Über die lokale Variable **LetztesErstellenDatensatzID** in einem **DatensatzErstellen** -Datenblock können Sie mit dem zuletzt erstellten Datensatz arbeiten.</span><span class="sxs-lookup"><span data-stu-id="4217a-113">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="4217a-114">Beispielsweise verwenden Sie die folgende Syntax, um auf die zuletzt erstellte Datensatz zu verweisen:</span><span class="sxs-lookup"><span data-stu-id="4217a-114">For example, use the following syntax to refer to the most recently created record:</span></span>

`[LastCreateRecordIdentity]`

