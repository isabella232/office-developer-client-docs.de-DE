---
title: InheritTypeEnum (Access PC-Datenbank-Referenz)
TOCTitle: InheritTypeEnum
ms:assetid: aa505c66-5871-10a8-35a7-cb30bb5dc21a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249787(v=office.15)
ms:contentKeyID: 48546944
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 031c47aff666bf10f0e2aa597ccd0143ed3d6209
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473166"
---
# <a name="inherittypeenum"></a><span data-ttu-id="eaeb3-102">InheritTypeEnum</span><span class="sxs-lookup"><span data-stu-id="eaeb3-102">InheritTypeEnum</span></span>


<span data-ttu-id="eaeb3-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="eaeb3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="eaeb3-104">Gibt an, wie Objekte Berechtigungen erben, die mit [SetPermissions](setpermissions-method-adox.md) festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="eaeb3-104">Specifies how objects will inherit permissions set with [SetPermissions](setpermissions-method-adox.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eaeb3-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="eaeb3-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="eaeb3-106">Wert</span><span class="sxs-lookup"><span data-stu-id="eaeb3-106">Value</span></span></p></th>
<th><p><span data-ttu-id="eaeb3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eaeb3-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eaeb3-108"><strong>adInheritBoth</strong></span><span class="sxs-lookup"><span data-stu-id="eaeb3-108"><strong>adInheritBoth</strong></span></span></p></td>
<td><p><span data-ttu-id="eaeb3-109">3</span><span class="sxs-lookup"><span data-stu-id="eaeb3-109">3</span></span></p></td>
<td><p><span data-ttu-id="eaeb3-110">Objekte und andere Container, die im primären Objekt enthalten sind, erben den Eintrag.</span><span class="sxs-lookup"><span data-stu-id="eaeb3-110">Both objects and other containers contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eaeb3-111"><strong>adInheritContainers</strong></span><span class="sxs-lookup"><span data-stu-id="eaeb3-111"><strong>adInheritContainers</strong></span></span></p></td>
<td><p><span data-ttu-id="eaeb3-112">2</span><span class="sxs-lookup"><span data-stu-id="eaeb3-112">2</span></span></p></td>
<td><p><span data-ttu-id="eaeb3-113">Andere Container, die im primären Objekt enthalten sind, erben den Eintrag.</span><span class="sxs-lookup"><span data-stu-id="eaeb3-113">Other containers that are contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eaeb3-114"><strong>adInheritNone</strong></span><span class="sxs-lookup"><span data-stu-id="eaeb3-114"><strong>adInheritNone</strong></span></span></p></td>
<td><p><span data-ttu-id="eaeb3-115">0</span><span class="sxs-lookup"><span data-stu-id="eaeb3-115">0</span></span></p></td>
<td><p><span data-ttu-id="eaeb3-p101">Standardeinstellung. Es tritt keine Vererbung auf.</span><span class="sxs-lookup"><span data-stu-id="eaeb3-p101">Default. No inheritance occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eaeb3-118"><strong>adInheritNoPropagate</strong></span><span class="sxs-lookup"><span data-stu-id="eaeb3-118"><strong>adInheritNoPropagate</strong></span></span></p></td>
<td><p><span data-ttu-id="eaeb3-119">4</span><span class="sxs-lookup"><span data-stu-id="eaeb3-119">4</span></span></p></td>
<td><p><span data-ttu-id="eaeb3-120">Die Flags <strong>adInheritObjects</strong> und <strong>adInheritContainers</strong> werden nicht an einen vererbten Eintrag weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="eaeb3-120">The <strong>adInheritObjects</strong> and <strong>adInheritContainers</strong> flags are not propagated to an inherited entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eaeb3-121"><strong>Flags adInheritObjects</strong></span><span class="sxs-lookup"><span data-stu-id="eaeb3-121"><strong>adInheritObjects</strong></span></span></p></td>
<td><p><span data-ttu-id="eaeb3-122">1</span><span class="sxs-lookup"><span data-stu-id="eaeb3-122">1</span></span></p></td>
<td><p><span data-ttu-id="eaeb3-123">Nicht-Container-Objekte innerhalb des Containers erben die Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="eaeb3-123">Non-container objects in the container inherit the permissions.</span></span></p></td>
</tr>
</tbody>
</table>

