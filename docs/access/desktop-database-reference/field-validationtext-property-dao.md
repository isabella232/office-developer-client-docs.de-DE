---
title: Field.ValidationText Property (DAO)
TOCTitle: ValidationText Property
ms:assetid: 6d9ec790-a9d2-84d7-ccba-57d738491e36
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195540(v=office.15)
ms:contentKeyID: 48545494
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c582795dc104171bd4c8435521e0da31718b1a38
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868889"
---
# <a name="fieldvalidationtext-property-dao"></a><span data-ttu-id="d8e36-102">Field.ValidationText Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="d8e36-102">Field.ValidationText Property (DAO)</span></span>


<span data-ttu-id="d8e36-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d8e36-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d8e36-p101">Legt einen Wert fest, der den Text der Nachricht angibt, die von der Anwendung angezeigt wird, wenn der Wert eines **Field**-Objekts die von der **ValidationRule**-Eigenschaft festgelegte Gültigkeitsregel nicht unterstützt, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche). **String**-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="d8e36-p101">Sets or returns a value that specifies the text of the message that your application displays if the value of a **Field** object doesn't satisfy the validation rule specified by the **ValidationRule** property setting (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8e36-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8e36-106">Syntax</span></span>

<span data-ttu-id="d8e36-107">*Ausdruck* . ValidationText</span><span class="sxs-lookup"><span data-stu-id="d8e36-107">*expression* .ValidationText</span></span>

<span data-ttu-id="d8e36-108">*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="d8e36-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8e36-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d8e36-109">Remarks</span></span>

<span data-ttu-id="d8e36-p102">Die Einstellung bzw. der Rückgabewert ist ein **String**-Wert des Texts, der angezeigt wird, wenn ein Benutzer versucht, einen ungültigen Wert für ein Feld einzugeben. Für ein Objekt, das noch nicht an eine Auflistung angehängt wurde, besteht Lese-/Schreibzugriff für diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d8e36-p102">The setting or return value is a **String** that specifies the text displayed if a user tries to enter an invalid value for a field. For an object not yet appended to a collection, this property is read/write.</span></span>

<span data-ttu-id="d8e36-112">Bei einem **Field**-Objekt hängt die Verwendung der **ValidationText**-Eigenschaft von dem Objekt ab, das die **[Fields](fields-collection-dao.md)** -Auflistung enthält, an die das **Field**-Objekt angehängt wird, wie in der folgenden Tabelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="d8e36-112">For a **Field** object, use of the **ValidationText** property depends on the object that contains the **[Fields](fields-collection-dao.md)** collection to which the **Field** object is appended, as the following table shows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d8e36-113">Zugehörigkeit zu Objekt</span><span class="sxs-lookup"><span data-stu-id="d8e36-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="d8e36-114">Verwendung</span><span class="sxs-lookup"><span data-stu-id="d8e36-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d8e36-115"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="d8e36-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="d8e36-116">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d8e36-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8e36-117"><strong>QueryDef-Objekt</strong></span><span class="sxs-lookup"><span data-stu-id="d8e36-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="d8e36-118">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d8e36-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8e36-119"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="d8e36-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="d8e36-120">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d8e36-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8e36-121"><strong>Beziehung</strong></span><span class="sxs-lookup"><span data-stu-id="d8e36-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="d8e36-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d8e36-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8e36-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="d8e36-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="d8e36-124">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="d8e36-124">Read/write</span></span></p></td>
</tr>
</tbody>
</table>

