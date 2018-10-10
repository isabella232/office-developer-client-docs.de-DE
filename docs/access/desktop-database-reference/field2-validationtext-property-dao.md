---
title: Field2.ValidationText Property (DAO)
TOCTitle: ValidationText Property
ms:assetid: 6128f66c-3891-ae4d-d12d-354a79a9c05e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194867(v=office.15)
ms:contentKeyID: 48545202
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d971b14093dd02204327e6f0ef30a81c6567c5bc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475880"
---
# <a name="field2validationtext-property-dao"></a><span data-ttu-id="0b981-102">Field2.ValidationText Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="0b981-102">Field2.ValidationText Property (DAO)</span></span>


<span data-ttu-id="0b981-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0b981-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0b981-p101">Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der den Text oder die Meldung angibt, mit der die Anwendung anzeigt, dass der Wert eines **Field2**-Objekts nicht der in der Einstellung der **ValidationRule**-Eigenschaft angegebenen Gütigkeitsregel entspricht (gilt nur für Microsoft Access-Arbeitsbereiche). **String**-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="0b981-p101">Sets or returns a value that specifies the text of the message that your application displays if the value of a **Field2** object doesn't satisfy the validation rule specified by the **ValidationRule** property setting (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b981-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b981-106">Syntax</span></span>

<span data-ttu-id="0b981-107">*Ausdruck* . ValidationText</span><span class="sxs-lookup"><span data-stu-id="0b981-107">*expression* .ValidationText</span></span>

<span data-ttu-id="0b981-108">*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="0b981-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b981-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b981-109">Remarks</span></span>

<span data-ttu-id="0b981-p102">Die Einstellung oder der Rückgabewert ist vom Datentyp **String** und gibt den Text an, der angezeigt wird, wenn ein Benutzer einen ungültigen Wert für ein Feld einzugeben versucht. Bei Objekten, die noch keiner Auflistung angefügt sind, besteht für diese Eigenschaft Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="0b981-p102">The setting or return value is a **String** that specifies the text displayed if a user tries to enter an invalid value for a field. For an object not yet appended to a collection, this property is read/write.</span></span>

<span data-ttu-id="0b981-112">Bei einem **Field2**-Objekt hängt die Verwendung der **ValidationText**-Eigenschaft vom Objekt ab, das die **[Fields](fields-collection-dao.md)** -Auflistung enthält, der das **Field2**-Objekt angefügt wird (siehe folgende Tabelle).</span><span class="sxs-lookup"><span data-stu-id="0b981-112">For a **Field2** object, use of the **ValidationText** property depends on the object that contains the **[Fields](fields-collection-dao.md)** collection to which the **Field2** object is appended, as the following table shows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0b981-113">Zugehörigkeit zu Objekt</span><span class="sxs-lookup"><span data-stu-id="0b981-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="0b981-114">Verwendung</span><span class="sxs-lookup"><span data-stu-id="0b981-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0b981-115"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="0b981-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="0b981-116">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0b981-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b981-117"><strong>QueryDef-Objekt</strong></span><span class="sxs-lookup"><span data-stu-id="0b981-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="0b981-118">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0b981-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b981-119"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="0b981-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="0b981-120">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0b981-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b981-121"><strong>Beziehung</strong></span><span class="sxs-lookup"><span data-stu-id="0b981-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="0b981-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0b981-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b981-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="0b981-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="0b981-124">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="0b981-124">Read/write</span></span></p></td>
</tr>
</tbody>
</table>

