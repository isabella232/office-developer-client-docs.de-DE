---
title: Gruppieren-Makroanweisung
TOCTitle: Group Macro Statement
ms:assetid: 42aa4afa-ab5d-9dcc-2182-786f025e316d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192918(v=office.15)
ms:contentKeyID: 48544481
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 35f9ad1d445dbddaa5487e28da60b9202a72dae1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879851"
---
# <a name="group-macro-statement"></a><span data-ttu-id="f59b2-102">Gruppieren-Makroanweisung</span><span class="sxs-lookup"><span data-stu-id="f59b2-102">Group Macro Statement</span></span>


<span data-ttu-id="f59b2-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f59b2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f59b2-104">Die **Group** -Anweisung können Sie einen Block von Aktionen innerhalb eines Makros angeben, die Sie erweitern oder reduzieren können.</span><span class="sxs-lookup"><span data-stu-id="f59b2-104">The **Group** statement enables you to specify a block of actions within a macro that you can expand or collapse.</span></span>

## <a name="setting"></a><span data-ttu-id="f59b2-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="f59b2-105">Setting</span></span>

<span data-ttu-id="f59b2-106">Die **Gruppieren** -Aktion kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f59b2-106">The **Group** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f59b2-107">Argument</span><span class="sxs-lookup"><span data-stu-id="f59b2-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="f59b2-108">Eingabe erforderlich</span><span class="sxs-lookup"><span data-stu-id="f59b2-108">Required</span></span></p></th>
<th><p><span data-ttu-id="f59b2-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f59b2-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f59b2-110"><strong>Beschreibung</strong></span><span class="sxs-lookup"><span data-stu-id="f59b2-110"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="f59b2-111">Nein</span><span class="sxs-lookup"><span data-stu-id="f59b2-111">No</span></span></p></td>
<td><p><span data-ttu-id="f59b2-112">Eine Zeichenfolge, die nach dem Reduzieren als Titel einer Gruppe angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f59b2-112">A string that appears as the title of a group when it is collapsed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f59b2-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f59b2-113">Remarks</span></span>

<span data-ttu-id="f59b2-p101">Mit der **Gruppieren** -Anweisung wird kein Bereich eines Makros definiert, der einzeln ausgeführt werden kann. Verwenden Sie die **[Untermakro](submacro-macro-statement.md)** -Anweisung im **Makro-Designer**-Fenster, um eine Reihe von Aktionen zu definieren, die einzeln ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="f59b2-p101">The **Group** statment does not define a region of a macro that can be executed separately. Use the **[Submacro](submacro-macro-statement.md)** statment to define a set of actions to be executed separately in the **Macro Designer** window.</span></span>

