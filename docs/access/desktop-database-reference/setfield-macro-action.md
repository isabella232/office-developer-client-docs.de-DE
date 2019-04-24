---
title: SetField-Makroaktion
TOCTitle: SetField macro action
ms:assetid: 66bd26e3-e8c3-b9a1-2f16-f29adc44a345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195227(v=office.15)
ms:contentKeyID: 48545349
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4fbf7252729c7b376da6ebe67f59941c1caf924d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314616"
---
# <a name="setfield-macro-action"></a><span data-ttu-id="d4b28-102">SetField-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="d4b28-102">SetField macro action</span></span>

<span data-ttu-id="d4b28-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d4b28-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d4b28-104">Mit der **FestlegenFeld** -Aktion können Sie einem Feld einen Wert zuweisen.</span><span class="sxs-lookup"><span data-stu-id="d4b28-104">The **SetField** action can be used to assign a value to a field.</span></span>

> [!NOTE]
> <span data-ttu-id="d4b28-105">Die **FestlegenFeld**-Aktion ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d4b28-105">The **SetField** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="d4b28-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="d4b28-106">Setting</span></span>

<span data-ttu-id="d4b28-107">Die **FestlegenFeld**-Aktion kann mit den in der folgenden Tabelle aufgeführten Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d4b28-107">The **SetField** action has the arguments listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d4b28-108">Argument</span><span class="sxs-lookup"><span data-stu-id="d4b28-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="d4b28-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4b28-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d4b28-110"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="d4b28-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="d4b28-111">Eine Zeichenfolge, die das Feld bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d4b28-111">A string that identifies the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4b28-112"><strong>Wert</strong></span><span class="sxs-lookup"><span data-stu-id="d4b28-112"><strong>Value</strong></span></span></p></td>
<td><p><span data-ttu-id="d4b28-113">Ein Ausdruck, der den Wert angibt, der dem Feld zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d4b28-113">An expression that specifies the value to assign to the field.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d4b28-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4b28-114">Remarks</span></span>

<span data-ttu-id="d4b28-115">Die **FestlegenFeld** -Aktion kann nicht außerhalb eines **[DatensatzErstellen](createrecord-data-block.md)** - oder **[BearbeitenDatensatz](editrecord-data-block.md)** -Datenblocks verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d4b28-115">The **SetField** action cannot be used outside of an **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block.</span></span>

