---
title: InheritTypeEnum (Access PC-Datenbank-Referenz)
TOCTitle: InheritTypeEnum
ms:assetid: aa505c66-5871-10a8-35a7-cb30bb5dc21a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249787(v=office.15)
ms:contentKeyID: 48546944
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: bf7d7ceac1e4822344ce4f7ad8a05e09c0429dff
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860567"
---
# <a name="inherittypeenum"></a><span data-ttu-id="e7522-102">InheritTypeEnum</span><span class="sxs-lookup"><span data-stu-id="e7522-102">InheritTypeEnum</span></span>

<span data-ttu-id="e7522-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e7522-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e7522-104">Gibt an, wie Objekte Berechtigungen erben, die mit [SetPermissions](setpermissions-method-adox.md) festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="e7522-104">Specifies how objects will inherit permissions set with [SetPermissions](setpermissions-method-adox.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e7522-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="e7522-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="e7522-106">Wert</span><span class="sxs-lookup"><span data-stu-id="e7522-106">Value</span></span></p></th>
<th><p><span data-ttu-id="e7522-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e7522-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e7522-108"><strong>adInheritBoth</strong></span><span class="sxs-lookup"><span data-stu-id="e7522-108"><strong>adInheritBoth</strong></span></span></p></td>
<td><p><span data-ttu-id="e7522-109">3</span><span class="sxs-lookup"><span data-stu-id="e7522-109">3</span></span></p></td>
<td><p><span data-ttu-id="e7522-110">Objekte und andere Container, die im primären Objekt enthalten sind, erben den Eintrag.</span><span class="sxs-lookup"><span data-stu-id="e7522-110">Both objects and other containers contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7522-111"><strong>adInheritContainers</strong></span><span class="sxs-lookup"><span data-stu-id="e7522-111"><strong>adInheritContainers</strong></span></span></p></td>
<td><p><span data-ttu-id="e7522-112">2</span><span class="sxs-lookup"><span data-stu-id="e7522-112">2</span></span></p></td>
<td><p><span data-ttu-id="e7522-113">Andere Container, die im primären Objekt enthalten sind, erben den Eintrag.</span><span class="sxs-lookup"><span data-stu-id="e7522-113">Other containers that are contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7522-114"><strong>adInheritNone</strong></span><span class="sxs-lookup"><span data-stu-id="e7522-114"><strong>adInheritNone</strong></span></span></p></td>
<td><p><span data-ttu-id="e7522-115">0</span><span class="sxs-lookup"><span data-stu-id="e7522-115">0</span></span></p></td>
<td><p><span data-ttu-id="e7522-p101">Standardeinstellung. Es tritt keine Vererbung auf.</span><span class="sxs-lookup"><span data-stu-id="e7522-p101">Default. No inheritance occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7522-118"><strong>adInheritNoPropagate</strong></span><span class="sxs-lookup"><span data-stu-id="e7522-118"><strong>adInheritNoPropagate</strong></span></span></p></td>
<td><p><span data-ttu-id="e7522-119">4</span><span class="sxs-lookup"><span data-stu-id="e7522-119">4</span></span></p></td>
<td><p><span data-ttu-id="e7522-120">Die Flags <strong>adInheritObjects</strong> und <strong>adInheritContainers</strong> werden nicht an einen vererbten Eintrag weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="e7522-120">The <strong>adInheritObjects</strong> and <strong>adInheritContainers</strong> flags are not propagated to an inherited entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7522-121"><strong>Flags adInheritObjects</strong></span><span class="sxs-lookup"><span data-stu-id="e7522-121"><strong>adInheritObjects</strong></span></span></p></td>
<td><p><span data-ttu-id="e7522-122">1</span><span class="sxs-lookup"><span data-stu-id="e7522-122">1</span></span></p></td>
<td><p><span data-ttu-id="e7522-123">Nicht-Container-Objekte innerhalb des Containers erben die Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="e7522-123">Non-container objects in the container inherit the permissions.</span></span></p></td>
</tr>
</tbody>
</table>

