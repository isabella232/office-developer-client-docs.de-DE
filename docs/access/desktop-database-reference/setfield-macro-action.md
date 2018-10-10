---
title: FestlegenFeld-Makroaktion
TOCTitle: SetField Macro Action
ms:assetid: 66bd26e3-e8c3-b9a1-2f16-f29adc44a345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195227(v=office.15)
ms:contentKeyID: 48545349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7050065ccb42d5e6cc9347f32df056891f4ed078
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474955"
---
# <a name="setfield-macro-action"></a><span data-ttu-id="fd86d-102">FestlegenFeld-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="fd86d-102">SetField Macro Action</span></span>


<span data-ttu-id="fd86d-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fd86d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fd86d-104">Mit der **FestlegenFeld** -Aktion können Sie einem Feld einen Wert zuweisen.</span><span class="sxs-lookup"><span data-stu-id="fd86d-104">The **SetField** action can be used to assign a value to a field.</span></span>


> [!NOTE]
> <P><span data-ttu-id="fd86d-105">[!HINWEIS] Die <STRONG>FestlegenFeld</STRONG> -Aktion ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fd86d-105">The <STRONG>SetField</STRONG> action is available only in Data Macros.</span></span></P>



## <a name="setting"></a><span data-ttu-id="fd86d-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="fd86d-106">Setting</span></span>

<span data-ttu-id="fd86d-107">Die **FestlegenFeld** -Aktion kann mit den in der folgenden Tabelle aufgeführten Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd86d-107">The **SetField** action has the arguments listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fd86d-108">Argument</span><span class="sxs-lookup"><span data-stu-id="fd86d-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="fd86d-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fd86d-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fd86d-110"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="fd86d-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="fd86d-111">Eine Zeichenfolge, die das Feld bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="fd86d-111">A string that identifies the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd86d-112"><strong>Wert</strong></span><span class="sxs-lookup"><span data-stu-id="fd86d-112"><strong>Value</strong></span></span></p></td>
<td><p><span data-ttu-id="fd86d-113">Ein Ausdruck, der angibt, den Wert in das Feld zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="fd86d-113">An expression that specifies the value to assign to the field.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="fd86d-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fd86d-114">Remarks</span></span>

<span data-ttu-id="fd86d-115">Die **FestlegenFeld** -Aktion kann nicht außerhalb eines **[DatensatzErstellen](createrecord-data-block.md)** - oder **[BearbeitenDatensatz](editrecord-data-block.md)** -Datenblocks verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd86d-115">The **SetField** action cannot be used outside of an **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block.</span></span>

