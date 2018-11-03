---
title: UpdateTypeEnum (Aufzählung) (DAO)
TOCTitle: UpdateTypeEnum Enumeration
ms:assetid: 7ac38bae-27fc-f3d0-5b75-569bce547954
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196186(v=office.15)
ms:contentKeyID: 48545800
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d38cf4554837c9c6434b7607746f2c40836ac950
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944620"
---
# <a name="updatetypeenum-enumeration-dao"></a><span data-ttu-id="96c06-102">UpdateTypeEnum (Aufzählung) (DAO)</span><span class="sxs-lookup"><span data-stu-id="96c06-102">UpdateTypeEnum enumeration (DAO)</span></span>


<span data-ttu-id="96c06-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="96c06-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="96c06-104">Hiermit geben Sie zusammen mit der **Update**-Methode an, welche Aktualisierungen auf den Datenträger geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="96c06-104">Used with the **Update** method to specify which updates to write to disk.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="96c06-105">Name</span><span class="sxs-lookup"><span data-stu-id="96c06-105">Name</span></span></p></th>
<th><p><span data-ttu-id="96c06-106">Wert</span><span class="sxs-lookup"><span data-stu-id="96c06-106">Value</span></span></p></th>
<th><p><span data-ttu-id="96c06-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="96c06-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96c06-108">dbUpdateBatch</span><span class="sxs-lookup"><span data-stu-id="96c06-108">dbUpdateBatch</span></span></p></td>
<td><p><span data-ttu-id="96c06-109">4</span><span class="sxs-lookup"><span data-stu-id="96c06-109">4</span></span></p></td>
<td><p><span data-ttu-id="96c06-110">Alle ausstehenden Änderungen im Updatecache werden auf den Datenträger geschrieben.</span><span class="sxs-lookup"><span data-stu-id="96c06-110">All pending changes in the update cache are written to disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96c06-111">dbUpdateCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="96c06-111">dbUpdateCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="96c06-112">2</span><span class="sxs-lookup"><span data-stu-id="96c06-112">2</span></span></p></td>
<td><p><span data-ttu-id="96c06-113">Nur die ausstehenden Änderungen des aktuellen Datensatzes werden auf den Datenträger geschrieben.</span><span class="sxs-lookup"><span data-stu-id="96c06-113">Only the current record's pending changes are written to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96c06-114">dbUpdateRegular</span><span class="sxs-lookup"><span data-stu-id="96c06-114">dbUpdateRegular</span></span></p></td>
<td><p><span data-ttu-id="96c06-115">1</span><span class="sxs-lookup"><span data-stu-id="96c06-115">1</span></span></p></td>
<td><p><span data-ttu-id="96c06-116">(Standard) Ausstehende Änderungen werden nicht zwischengespeichert und werden sofort auf den Datenträger geschrieben.</span><span class="sxs-lookup"><span data-stu-id="96c06-116">(Default) Pending changes are not cached and are written to disk immediately.</span></span></p></td>
</tr>
</tbody>
</table>

