---
title: TableDefs. Delete-Methode (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 63f543fd86e309372e0432c3e45513cd9d3942ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313993"
---
# <a name="tabledefsdelete-method-dao"></a><span data-ttu-id="acfdd-102">TableDefs. Delete-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="acfdd-102">TableDefs.Delete method (DAO)</span></span>

<span data-ttu-id="acfdd-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="acfdd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="acfdd-104">Löscht das angegebene **TableDef**-Objekt aus der **TableDefs**-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="acfdd-104">Deletes the specified **TableDef** object from the **TableDefs** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="acfdd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="acfdd-105">Syntax</span></span>

<span data-ttu-id="acfdd-106">*Ausdruck* . Delete (***Name***)</span><span class="sxs-lookup"><span data-stu-id="acfdd-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="acfdd-107">*Ausdruck* Eine Variable, die ein **Tabledefs** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="acfdd-107">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="acfdd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="acfdd-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="acfdd-109">Name</span><span class="sxs-lookup"><span data-stu-id="acfdd-109">Name</span></span></p></th>
<th><p><span data-ttu-id="acfdd-110">Erforderlich/optional</span><span class="sxs-lookup"><span data-stu-id="acfdd-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="acfdd-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="acfdd-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="acfdd-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="acfdd-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="acfdd-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="acfdd-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="acfdd-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="acfdd-114">Required</span></span></p></td>
<td><p><span data-ttu-id="acfdd-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="acfdd-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="acfdd-116">Der Name des zu löschenden TableDef-Objekts.</span><span class="sxs-lookup"><span data-stu-id="acfdd-116">The name of the TableDef to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="acfdd-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="acfdd-117">Remarks</span></span>

<span data-ttu-id="acfdd-118">Die Delete-Methode wird nur unterstützt, wenn das **TableDef** -Objekt neu ist und nicht an die Datenbank angefügt wurde oder wenn die **aktualisierbare** Eigenschaft des **TableDef** auf **true**festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="acfdd-118">The Delete method is supported only when the **TableDef** object is new and hasn’t been appended to the database, or when the **Updatable** property of the **TableDef** is set to **True**.</span></span>

