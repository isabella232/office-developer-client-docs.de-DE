---
title: TableDefs.Delete Method (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e39a1390c9ea26baa83d8203967d603237a3ab1c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474343"
---
# <a name="tabledefsdelete-method-dao"></a><span data-ttu-id="32457-102">TableDefs.Delete Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="32457-102">TableDefs.Delete Method (DAO)</span></span>


<span data-ttu-id="32457-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="32457-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="32457-104">Löscht das angegebene **TableDef**-Objekt aus der **TableDefs**-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="32457-104">Deletes the specified **TableDef** object from the **TableDefs** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="32457-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="32457-105">Syntax</span></span>

<span data-ttu-id="32457-106">*Ausdruck* . Löschen Sie die (***Name***)</span><span class="sxs-lookup"><span data-stu-id="32457-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="32457-107">*Ausdruck* Eine Variable, die ein **TableDefs** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="32457-107">*expression* A variable that represents a **TableDefs** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="32457-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="32457-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="32457-109">Name</span><span class="sxs-lookup"><span data-stu-id="32457-109">Name</span></span></p></th>
<th><p><span data-ttu-id="32457-110">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="32457-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="32457-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="32457-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="32457-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="32457-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32457-113">Name</span><span class="sxs-lookup"><span data-stu-id="32457-113">Name</span></span></p></td>
<td><p><span data-ttu-id="32457-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="32457-114">Required</span></span></p></td>
<td><p><span data-ttu-id="32457-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="32457-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="32457-116">Der Name des zu löschenden TableDef-Objekts.</span><span class="sxs-lookup"><span data-stu-id="32457-116">The name of the TableDef to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="32457-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="32457-117">Remarks</span></span>

<span data-ttu-id="32457-118">Die Delete-Methode wird nur dann unterstützt, wenn das TableDef-Objekt neu ist und noch nicht an die Datenbank angefügt wurde, oder wenn die Updatable-Eigenschaft des TableDef-Objekts auf True festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="32457-118">The Delete method is supported only when the **TableDef** object is new and hasn’t been appended to the database, or when the **Updatable** property of the **TableDef** is set to **True**.</span></span>

