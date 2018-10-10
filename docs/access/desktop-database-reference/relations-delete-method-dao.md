---
title: Relations.Delete Method (DAO)
TOCTitle: Delete Method
ms:assetid: e95408d2-9dde-44e7-875e-8f2d4b837cf6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836064(v=office.15)
ms:contentKeyID: 48548438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6b228c21931131023d58efc91d0087ad76ca3b61
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473593"
---
# <a name="relationsdelete-method-dao"></a><span data-ttu-id="7f612-102">Relations.Delete Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="7f612-102">Relations.Delete Method (DAO)</span></span>


<span data-ttu-id="7f612-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7f612-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7f612-104">Löscht das angegebene **Relation**-Objekt aus der **Relations**-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="7f612-104">Deletes the specified **Relation** from the **Relations** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f612-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f612-105">Syntax</span></span>

<span data-ttu-id="7f612-106">*Ausdruck* . Löschen Sie die (***Name***)</span><span class="sxs-lookup"><span data-stu-id="7f612-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="7f612-107">*Ausdruck* Eine Variable, die ein **Relations** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="7f612-107">*expression* A variable that represents a **Relations** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="7f612-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f612-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7f612-109">Name</span><span class="sxs-lookup"><span data-stu-id="7f612-109">Name</span></span></p></th>
<th><p><span data-ttu-id="7f612-110">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="7f612-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="7f612-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7f612-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="7f612-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f612-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f612-113">Name</span><span class="sxs-lookup"><span data-stu-id="7f612-113">Name</span></span></p></td>
<td><p><span data-ttu-id="7f612-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="7f612-114">Required</span></span></p></td>
<td><p><span data-ttu-id="7f612-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="7f612-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="7f612-116">Der Name der zu löschenden Beziehung.</span><span class="sxs-lookup"><span data-stu-id="7f612-116">The name of the relation to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7f612-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f612-117">Remarks</span></span>

<span data-ttu-id="7f612-118">Die **Delete**-Methode wird nur unterstützt, wenn es sich bei dem **Relation**-Objekt um ein neues Objekt handelt, das noch nicht angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="7f612-118">The **Delete** method is supported only when the **Relation** object is a new, unappended object.</span></span>

