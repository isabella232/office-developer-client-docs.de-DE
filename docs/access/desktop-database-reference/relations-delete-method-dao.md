---
title: Relations.Delete-Methode (DAO)
TOCTitle: Delete Method
ms:assetid: e95408d2-9dde-44e7-875e-8f2d4b837cf6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836064(v=office.15)
ms:contentKeyID: 48548438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 462581e5b1ab3f09b697ee7f4b763a889d8119fd
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925527"
---
# <a name="relationsdelete-method-dao"></a><span data-ttu-id="428ee-102">Relations.Delete-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="428ee-102">Relations.Delete method (DAO)</span></span>


<span data-ttu-id="428ee-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="428ee-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="428ee-104">Löscht das angegebene **Relation**-Objekt aus der **Relations**-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="428ee-104">Deletes the specified **Relation** from the **Relations** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="428ee-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="428ee-105">Syntax</span></span>

<span data-ttu-id="428ee-106">*Ausdruck* . Löschen Sie die (***Name***)</span><span class="sxs-lookup"><span data-stu-id="428ee-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="428ee-107">*Ausdruck* Eine Variable, die ein **Relations** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="428ee-107">*expression* A variable that represents a **Relations** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="428ee-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="428ee-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="428ee-109">Name</span><span class="sxs-lookup"><span data-stu-id="428ee-109">Name</span></span></p></th>
<th><p><span data-ttu-id="428ee-110">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="428ee-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="428ee-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="428ee-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="428ee-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="428ee-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="428ee-113">Name</span><span class="sxs-lookup"><span data-stu-id="428ee-113">Name</span></span></p></td>
<td><p><span data-ttu-id="428ee-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="428ee-114">Required</span></span></p></td>
<td><p><span data-ttu-id="428ee-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="428ee-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="428ee-116">Der Name der zu löschenden Beziehung.</span><span class="sxs-lookup"><span data-stu-id="428ee-116">The name of the relation to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="428ee-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="428ee-117">Remarks</span></span>

<span data-ttu-id="428ee-118">Die **Delete**-Methode wird nur unterstützt, wenn es sich bei dem **Relation**-Objekt um ein neues Objekt handelt, das noch nicht angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="428ee-118">The **Delete** method is supported only when the **Relation** object is a new, unappended object.</span></span>

