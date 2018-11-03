---
title: Gruppieren-Makroanweisung
TOCTitle: Group macro statement
ms:assetid: 42aa4afa-ab5d-9dcc-2182-786f025e316d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192918(v=office.15)
ms:contentKeyID: 48544481
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c82169ac430496587c6ebab5e439d70bc9319b5e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930889"
---
# <a name="group-macro-statement"></a><span data-ttu-id="d8403-102">Gruppieren-Makroanweisung</span><span class="sxs-lookup"><span data-stu-id="d8403-102">Group macro statement</span></span>


<span data-ttu-id="d8403-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d8403-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d8403-104">Die **Group** -Anweisung können Sie einen Block von Aktionen innerhalb eines Makros angeben, die Sie erweitern oder reduzieren können.</span><span class="sxs-lookup"><span data-stu-id="d8403-104">The **Group** statement enables you to specify a block of actions within a macro that you can expand or collapse.</span></span>

## <a name="setting"></a><span data-ttu-id="d8403-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="d8403-105">Setting</span></span>

<span data-ttu-id="d8403-106">Die **Gruppieren** -Aktion kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8403-106">The **Group** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d8403-107">Argument</span><span class="sxs-lookup"><span data-stu-id="d8403-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="d8403-108">Eingabe erforderlich</span><span class="sxs-lookup"><span data-stu-id="d8403-108">Required</span></span></p></th>
<th><p><span data-ttu-id="d8403-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d8403-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d8403-110"><strong>Beschreibung</strong></span><span class="sxs-lookup"><span data-stu-id="d8403-110"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="d8403-111">Nein</span><span class="sxs-lookup"><span data-stu-id="d8403-111">No</span></span></p></td>
<td><p><span data-ttu-id="d8403-112">Eine Zeichenfolge, die nach dem Reduzieren als Titel einer Gruppe angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d8403-112">A string that appears as the title of a group when it is collapsed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d8403-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d8403-113">Remarks</span></span>

<span data-ttu-id="d8403-p101">Mit der **Gruppieren** -Anweisung wird kein Bereich eines Makros definiert, der einzeln ausgeführt werden kann. Verwenden Sie die **[Untermakro](submacro-macro-statement.md)** -Anweisung im **Makro-Designer**-Fenster, um eine Reihe von Aktionen zu definieren, die einzeln ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="d8403-p101">The **Group** statment does not define a region of a macro that can be executed separately. Use the **[Submacro](submacro-macro-statement.md)** statment to define a set of actions to be executed separately in the **Macro Designer** window.</span></span>

