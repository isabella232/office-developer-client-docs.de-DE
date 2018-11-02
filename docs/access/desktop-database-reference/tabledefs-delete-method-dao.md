---
title: TableDefs.Delete-Methode (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 122f30e5f6310bc180dd43582a6e1e05cc970d4b
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926493"
---
# <a name="tabledefsdelete-method-dao"></a><span data-ttu-id="5d72a-102">TableDefs.Delete-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="5d72a-102">TableDefs.Delete method (DAO)</span></span>


<span data-ttu-id="5d72a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5d72a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5d72a-104">Löscht das angegebene **TableDef**-Objekt aus der **TableDefs**-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="5d72a-104">Deletes the specified **TableDef** object from the **TableDefs** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d72a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d72a-105">Syntax</span></span>

<span data-ttu-id="5d72a-106">*Ausdruck* . Löschen Sie die (***Name***)</span><span class="sxs-lookup"><span data-stu-id="5d72a-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="5d72a-107">*Ausdruck* Eine Variable, die ein **TableDefs** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="5d72a-107">*expression* A variable that represents a **TableDefs** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="5d72a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d72a-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5d72a-109">Name</span><span class="sxs-lookup"><span data-stu-id="5d72a-109">Name</span></span></p></th>
<th><p><span data-ttu-id="5d72a-110">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="5d72a-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="5d72a-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5d72a-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="5d72a-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d72a-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d72a-113">Name</span><span class="sxs-lookup"><span data-stu-id="5d72a-113">Name</span></span></p></td>
<td><p><span data-ttu-id="5d72a-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="5d72a-114">Required</span></span></p></td>
<td><p><span data-ttu-id="5d72a-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="5d72a-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="5d72a-116">Der Name des zu löschenden TableDef-Objekts.</span><span class="sxs-lookup"><span data-stu-id="5d72a-116">The name of the TableDef to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5d72a-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d72a-117">Remarks</span></span>

<span data-ttu-id="5d72a-118">Die Delete-Methode wird nur dann unterstützt, wenn das TableDef-Objekt neu ist und noch nicht an die Datenbank angefügt wurde, oder wenn die Updatable-Eigenschaft des TableDef-Objekts auf True festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5d72a-118">The Delete method is supported only when the **TableDef** object is new and hasn’t been appended to the database, or when the **Updatable** property of the **TableDef** is set to **True**.</span></span>

