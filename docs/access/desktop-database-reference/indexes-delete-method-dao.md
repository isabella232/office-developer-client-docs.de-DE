---
title: Indexes.Delete-Methode (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6ab52f353b7a3e636f64ff2ad6ad5354d62bed48
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703545"
---
# <a name="indexesdelete-method-dao"></a><span data-ttu-id="f3d9a-102">Indexes.Delete-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="f3d9a-102">Indexes.Delete method (DAO)</span></span>

<span data-ttu-id="f3d9a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f3d9a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f3d9a-104">Löscht das angegebene **Index**-Objekt aus der **Indexes**-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="f3d9a-104">Deletes the specified **Index** from the **Indexes** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3d9a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3d9a-105">Syntax</span></span>

<span data-ttu-id="f3d9a-106">*Ausdruck* . Löschen Sie die (***Name***)</span><span class="sxs-lookup"><span data-stu-id="f3d9a-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="f3d9a-107">*Ausdruck* Eine Variable, die ein **Indexes** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="f3d9a-107">*expression* A variable that represents an **Indexes** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="f3d9a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3d9a-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f3d9a-109">Name</span><span class="sxs-lookup"><span data-stu-id="f3d9a-109">Name</span></span></p></th>
<th><p><span data-ttu-id="f3d9a-110">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="f3d9a-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="f3d9a-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f3d9a-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="f3d9a-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3d9a-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3d9a-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="f3d9a-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="f3d9a-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f3d9a-114">Required</span></span></p></td>
<td><p><span data-ttu-id="f3d9a-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="f3d9a-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="f3d9a-116">Der Name des zu löschenden Index.</span><span class="sxs-lookup"><span data-stu-id="f3d9a-116">The name of the index to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f3d9a-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3d9a-117">Remarks</span></span>

<span data-ttu-id="f3d9a-118">Die **Delete** -Methode wird nur unterstützt, wenn das **Index** -Objekt neu ist und noch nicht an die Datenbank angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="f3d9a-118">The **Delete** method is supported only when the **Index** object is new and hasn’t been appended to the database.</span></span>

