---
title: InheritTypeEnum (Access PC-Datenbank-Referenz)
TOCTitle: InheritTypeEnum
ms:assetid: aa505c66-5871-10a8-35a7-cb30bb5dc21a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249787(v=office.15)
ms:contentKeyID: 48546944
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ba1a78e49d44bce0c489e4f5259ec9699543e231
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706807"
---
# <a name="inherittypeenum"></a><span data-ttu-id="1d7da-102">InheritTypeEnum</span><span class="sxs-lookup"><span data-stu-id="1d7da-102">InheritTypeEnum</span></span>

<span data-ttu-id="1d7da-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1d7da-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1d7da-104">Gibt an, wie Objekte Berechtigungen erben, die mit [SetPermissions](setpermissions-method-adox.md) festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="1d7da-104">Specifies how objects will inherit permissions set with [SetPermissions](setpermissions-method-adox.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1d7da-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="1d7da-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="1d7da-106">Wert</span><span class="sxs-lookup"><span data-stu-id="1d7da-106">Value</span></span></p></th>
<th><p><span data-ttu-id="1d7da-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1d7da-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d7da-108"><strong>adInheritBoth</strong></span><span class="sxs-lookup"><span data-stu-id="1d7da-108"><strong>adInheritBoth</strong></span></span></p></td>
<td><p><span data-ttu-id="1d7da-109">3</span><span class="sxs-lookup"><span data-stu-id="1d7da-109">3</span></span></p></td>
<td><p><span data-ttu-id="1d7da-110">Objekte und andere Container, die im primären Objekt enthalten sind, erben den Eintrag.</span><span class="sxs-lookup"><span data-stu-id="1d7da-110">Both objects and other containers contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d7da-111"><strong>adInheritContainers</strong></span><span class="sxs-lookup"><span data-stu-id="1d7da-111"><strong>adInheritContainers</strong></span></span></p></td>
<td><p><span data-ttu-id="1d7da-112">2</span><span class="sxs-lookup"><span data-stu-id="1d7da-112">2</span></span></p></td>
<td><p><span data-ttu-id="1d7da-113">Andere Container, die im primären Objekt enthalten sind, erben den Eintrag.</span><span class="sxs-lookup"><span data-stu-id="1d7da-113">Other containers that are contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d7da-114"><strong>adInheritNone</strong></span><span class="sxs-lookup"><span data-stu-id="1d7da-114"><strong>adInheritNone</strong></span></span></p></td>
<td><p><span data-ttu-id="1d7da-115">0</span><span class="sxs-lookup"><span data-stu-id="1d7da-115">0</span></span></p></td>
<td><p><span data-ttu-id="1d7da-p101">Standardeinstellung. Es tritt keine Vererbung auf.</span><span class="sxs-lookup"><span data-stu-id="1d7da-p101">Default. No inheritance occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d7da-118"><strong>adInheritNoPropagate</strong></span><span class="sxs-lookup"><span data-stu-id="1d7da-118"><strong>adInheritNoPropagate</strong></span></span></p></td>
<td><p><span data-ttu-id="1d7da-119">4</span><span class="sxs-lookup"><span data-stu-id="1d7da-119">4</span></span></p></td>
<td><p><span data-ttu-id="1d7da-120">Die Flags <strong>adInheritObjects</strong> und <strong>adInheritContainers</strong> werden nicht an einen vererbten Eintrag weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="1d7da-120">The <strong>adInheritObjects</strong> and <strong>adInheritContainers</strong> flags are not propagated to an inherited entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d7da-121"><strong>Flags adInheritObjects</strong></span><span class="sxs-lookup"><span data-stu-id="1d7da-121"><strong>adInheritObjects</strong></span></span></p></td>
<td><p><span data-ttu-id="1d7da-122">1</span><span class="sxs-lookup"><span data-stu-id="1d7da-122">1</span></span></p></td>
<td><p><span data-ttu-id="1d7da-123">Nicht-Container-Objekte innerhalb des Containers erben die Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="1d7da-123">Non-container objects in the container inherit the permissions.</span></span></p></td>
</tr>
</tbody>
</table>

