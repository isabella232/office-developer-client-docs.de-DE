---
title: DatensatzLöschen-Makroaktion
TOCTitle: DeleteRecord Macro Action
ms:assetid: c656a72c-c037-76a5-dc07-f6eccb6590dd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823132(v=office.15)
ms:contentKeyID: 48547624
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 536369082a5abb94914d78d8bc64c5f9b45e8b0d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474877"
---
# <a name="deleterecord-macro-action"></a><span data-ttu-id="2f216-102">DatensatzLöschen-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="2f216-102">DeleteRecord Macro Action</span></span>

<span data-ttu-id="2f216-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2f216-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2f216-104">Mit der **DatensatzLöschen** -Aktion können Sie einen Datensatz löschen.</span><span class="sxs-lookup"><span data-stu-id="2f216-104">You can use the **DeleteRecord** action to delete a record.</span></span>

## <a name="setting"></a><span data-ttu-id="2f216-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="2f216-105">Setting</span></span>

<span data-ttu-id="2f216-106">Der **DatensatzLöschen** -Datenblock kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2f216-106">The **CreateRecord** data block has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2f216-107">Argument</span><span class="sxs-lookup"><span data-stu-id="2f216-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="2f216-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f216-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f216-109"><strong>Datensatzalias</strong></span><span class="sxs-lookup"><span data-stu-id="2f216-109"><strong>Record Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="2f216-p101">Eine Zeichenfolge, mit der der zu löschende Datensatz gekennzeichnet wird. Wenn das <em>Alias</em>-Argument nicht angegeben ist, wird der aktuelle Datensatz gelöscht.</span><span class="sxs-lookup"><span data-stu-id="2f216-p101">A string that identifies the record to delete. If the <em>Alias</em> argument is not specified, then the current record is deleted.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="2f216-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2f216-112">Remarks</span></span>

<span data-ttu-id="2f216-113">Über die lokale Variable **LetztesErstellenDatensatzID** in einem **DatensatzErstellen** -Datenblock können Sie mit dem zuletzt erstellten Datensatz arbeiten.</span><span class="sxs-lookup"><span data-stu-id="2f216-113">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="2f216-114">Beispielsweise verwenden Sie die folgende Syntax, um auf die zuletzt erstellte Datensatz zu verweisen:</span><span class="sxs-lookup"><span data-stu-id="2f216-114">For example, use the following syntax to refer to the most recently created record:</span></span>

`[LastCreateRecordIdentity]`

