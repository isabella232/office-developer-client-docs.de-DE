---
title: Gruppieren-Makroanweisung
TOCTitle: Group macro statement
ms:assetid: 42aa4afa-ab5d-9dcc-2182-786f025e316d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192918(v=office.15)
ms:contentKeyID: 48544481
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2dc25621a49d8fd23078a926d6ec6c5de54e54d9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292111"
---
# <a name="group-macro-statement"></a><span data-ttu-id="fb1f0-102">Gruppieren-Makroanweisung</span><span class="sxs-lookup"><span data-stu-id="fb1f0-102">Group macro statement</span></span>


<span data-ttu-id="fb1f0-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fb1f0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fb1f0-104">Mit der **Group** -Anweisung können Sie einen Block von Aktionen innerhalb eines Makros angeben, den Sie erweitern oder reduzieren möchten.</span><span class="sxs-lookup"><span data-stu-id="fb1f0-104">The **Group** statement enables you to specify a block of actions within a macro that you can expand or collapse.</span></span>

## <a name="setting"></a><span data-ttu-id="fb1f0-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="fb1f0-105">Setting</span></span>

<span data-ttu-id="fb1f0-106">Die **Gruppieren**-Aktion kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fb1f0-106">The **Group** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fb1f0-107">Argument</span><span class="sxs-lookup"><span data-stu-id="fb1f0-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="fb1f0-108">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fb1f0-108">Required</span></span></p></th>
<th><p><span data-ttu-id="fb1f0-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb1f0-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fb1f0-110"><strong>Beschreibung</strong></span><span class="sxs-lookup"><span data-stu-id="fb1f0-110"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="fb1f0-111">Nein</span><span class="sxs-lookup"><span data-stu-id="fb1f0-111">No</span></span></p></td>
<td><p><span data-ttu-id="fb1f0-112">Eine Zeichenfolge, die nach dem Reduzieren als Titel einer Gruppe angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="fb1f0-112">A string that appears as the title of a group when it is collapsed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="fb1f0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb1f0-113">Remarks</span></span>

<span data-ttu-id="fb1f0-p101">Mit der **Gruppieren** -Anweisung wird kein Bereich eines Makros definiert, der einzeln ausgeführt werden kann. Verwenden Sie die **[Untermakro](submacro-macro-statement.md)** -Anweisung im **Makro-Designer**-Fenster, um eine Reihe von Aktionen zu definieren, die einzeln ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="fb1f0-p101">The **Group** statment does not define a region of a macro that can be executed separately. Use the **[Submacro](submacro-macro-statement.md)** statment to define a set of actions to be executed separately in the **Macro Designer** window.</span></span>

