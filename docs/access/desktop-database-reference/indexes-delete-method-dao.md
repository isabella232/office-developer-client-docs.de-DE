---
title: Indexes.Delete Method (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5b863780208e6ea59e7c518bcb09cb20f38d30a6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887131"
---
# <a name="indexesdelete-method-dao"></a><span data-ttu-id="fbc31-102">Indexes.Delete Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="fbc31-102">Indexes.Delete Method (DAO)</span></span>


<span data-ttu-id="fbc31-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fbc31-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fbc31-104">Löscht das angegebene **Index**-Objekt aus der **Indexes**-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="fbc31-104">Deletes the specified **Index** from the **Indexes** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbc31-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbc31-105">Syntax</span></span>

<span data-ttu-id="fbc31-106">*Ausdruck* . Löschen Sie die (***Name***)</span><span class="sxs-lookup"><span data-stu-id="fbc31-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="fbc31-107">*Ausdruck* Eine Variable, die ein **Indexes** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="fbc31-107">*expression* A variable that represents an **Indexes** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="fbc31-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbc31-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fbc31-109">Name</span><span class="sxs-lookup"><span data-stu-id="fbc31-109">Name</span></span></p></th>
<th><p><span data-ttu-id="fbc31-110">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="fbc31-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="fbc31-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="fbc31-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="fbc31-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fbc31-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fbc31-113">Name</span><span class="sxs-lookup"><span data-stu-id="fbc31-113">Name</span></span></p></td>
<td><p><span data-ttu-id="fbc31-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fbc31-114">Required</span></span></p></td>
<td><p><span data-ttu-id="fbc31-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="fbc31-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="fbc31-116">Der Name des zu löschenden Index.</span><span class="sxs-lookup"><span data-stu-id="fbc31-116">The name of the index to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="fbc31-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fbc31-117">Remarks</span></span>

<span data-ttu-id="fbc31-118">Die **Delete** -Methode wird nur unterstützt, wenn das **Index** -Objekt neu ist und noch nicht an die Datenbank angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="fbc31-118">The **Delete** method is supported only when the **Index** object is new and hasn’t been appended to the database.</span></span>

