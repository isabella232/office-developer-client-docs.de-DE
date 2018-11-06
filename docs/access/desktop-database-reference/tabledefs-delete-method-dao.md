---
title: TableDefs.Delete-Methode (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2d511155f7a5fe1e6b83092e2065302bab99765b
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999008"
---
# <a name="tabledefsdelete-method-dao"></a><span data-ttu-id="6c95d-102">TableDefs.Delete-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="6c95d-102">TableDefs.Delete method (DAO)</span></span>

<span data-ttu-id="6c95d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6c95d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6c95d-104">Löscht das angegebene **TableDef**-Objekt aus der **TableDefs**-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="6c95d-104">Deletes the specified **TableDef** object from the **TableDefs** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c95d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c95d-105">Syntax</span></span>

<span data-ttu-id="6c95d-106">*Ausdruck* . Löschen Sie die (***Name***)</span><span class="sxs-lookup"><span data-stu-id="6c95d-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="6c95d-107">*Ausdruck* Eine Variable, die ein **TableDefs** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="6c95d-107">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="6c95d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c95d-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6c95d-109">Name</span><span class="sxs-lookup"><span data-stu-id="6c95d-109">Name</span></span></p></th>
<th><p><span data-ttu-id="6c95d-110">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="6c95d-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="6c95d-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="6c95d-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="6c95d-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c95d-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c95d-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="6c95d-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="6c95d-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="6c95d-114">Required</span></span></p></td>
<td><p><span data-ttu-id="6c95d-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="6c95d-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="6c95d-116">Der Name des zu löschenden TableDef-Objekts.</span><span class="sxs-lookup"><span data-stu-id="6c95d-116">The name of the TableDef to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6c95d-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c95d-117">Remarks</span></span>

<span data-ttu-id="6c95d-118">Die Delete-Methode wird nur dann unterstützt, wenn das TableDef-Objekt neu ist und noch nicht an die Datenbank angefügt wurde, oder wenn die Updatable-Eigenschaft des TableDef-Objekts auf True festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6c95d-118">The Delete method is supported only when the **TableDef** object is new and hasn’t been appended to the database, or when the **Updatable** property of the **TableDef** is set to **True**.</span></span>

