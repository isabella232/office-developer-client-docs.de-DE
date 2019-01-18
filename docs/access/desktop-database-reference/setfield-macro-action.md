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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722319"
---
# <a name="setfield-macro-action"></a><span data-ttu-id="4e8a5-102">SetField-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="4e8a5-102">SetField macro action</span></span>

<span data-ttu-id="4e8a5-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4e8a5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4e8a5-104">Mit der **FestlegenFeld** -Aktion können Sie einem Feld einen Wert zuweisen.</span><span class="sxs-lookup"><span data-stu-id="4e8a5-104">The **SetField** action can be used to assign a value to a field.</span></span>

> [!NOTE]
> <span data-ttu-id="4e8a5-105">[!HINWEIS] Die **FestlegenFeld** -Aktion ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4e8a5-105">The **SetField** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="4e8a5-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="4e8a5-106">Setting</span></span>

<span data-ttu-id="4e8a5-107">Die **FestlegenFeld** -Aktion kann mit den in der folgenden Tabelle aufgeführten Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4e8a5-107">The **SetField** action has the arguments listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4e8a5-108">Argument</span><span class="sxs-lookup"><span data-stu-id="4e8a5-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="4e8a5-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4e8a5-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4e8a5-110"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="4e8a5-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="4e8a5-111">Eine Zeichenfolge, die das Feld bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="4e8a5-111">A string that identifies the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e8a5-112"><strong>Wert</strong></span><span class="sxs-lookup"><span data-stu-id="4e8a5-112"><strong>Value</strong></span></span></p></td>
<td><p><span data-ttu-id="4e8a5-113">Ein Ausdruck, der angibt, den Wert in das Feld zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="4e8a5-113">An expression that specifies the value to assign to the field.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4e8a5-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4e8a5-114">Remarks</span></span>

<span data-ttu-id="4e8a5-115">Die **FestlegenFeld** -Aktion kann nicht außerhalb eines **[DatensatzErstellen](createrecord-data-block.md)** - oder **[BearbeitenDatensatz](editrecord-data-block.md)** -Datenblocks verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4e8a5-115">The **SetField** action cannot be used outside of an **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block.</span></span>

