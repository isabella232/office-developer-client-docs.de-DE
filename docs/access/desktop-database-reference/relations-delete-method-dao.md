---
title: Relations.Delete-Methode (DAO)
TOCTitle: Delete Method
ms:assetid: e95408d2-9dde-44e7-875e-8f2d4b837cf6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836064(v=office.15)
ms:contentKeyID: 48548438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7c7a42098bcc64a58f8a004c0f1d5a35fd4f34b7
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998924"
---
# <a name="relationsdelete-method-dao"></a><span data-ttu-id="95576-102">Relations.Delete-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="95576-102">Relations.Delete method (DAO)</span></span>

<span data-ttu-id="95576-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="95576-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="95576-104">Löscht das angegebene **Relation**-Objekt aus der **Relations**-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="95576-104">Deletes the specified **Relation** from the **Relations** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="95576-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="95576-105">Syntax</span></span>

<span data-ttu-id="95576-106">*Ausdruck* . Löschen Sie die (***Name***)</span><span class="sxs-lookup"><span data-stu-id="95576-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="95576-107">*Ausdruck* Eine Variable, die ein **Relations** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="95576-107">*expression* A variable that represents a **Relations** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="95576-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="95576-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="95576-109">Name</span><span class="sxs-lookup"><span data-stu-id="95576-109">Name</span></span></p></th>
<th><p><span data-ttu-id="95576-110">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="95576-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="95576-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="95576-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="95576-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="95576-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95576-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="95576-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="95576-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="95576-114">Required</span></span></p></td>
<td><p><span data-ttu-id="95576-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="95576-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="95576-116">Der Name der zu löschenden Beziehung.</span><span class="sxs-lookup"><span data-stu-id="95576-116">The name of the relation to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="95576-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95576-117">Remarks</span></span>

<span data-ttu-id="95576-118">Die **Delete**-Methode wird nur unterstützt, wenn es sich bei dem **Relation**-Objekt um ein neues Objekt handelt, das noch nicht angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="95576-118">The **Delete** method is supported only when the **Relation** object is a new, unappended object.</span></span>

