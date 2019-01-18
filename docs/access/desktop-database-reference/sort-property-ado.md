---
title: Sort-Eigenschaft (ADO)
TOCTitle: Sort property (ADO)
ms:assetid: f2a39b7f-8b96-cd1a-8248-71f8b867454a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250230(v=office.15)
ms:contentKeyID: 48548652
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 62ac60b1c7575f0b0d3e003dc58a11fe4d86c131
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711413"
---
# <a name="sort-property-ado"></a><span data-ttu-id="4a200-102">Sort-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="4a200-102">Sort property (ADO)</span></span>


<span data-ttu-id="4a200-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4a200-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4a200-104">Gibt einen oder mehrere Feldnamen an, nach denen das [Recordset](recordset-object-ado.md) sortiert wird, und gibt an, ob die einzelnen Felder aufsteigend oder absteigend sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="4a200-104">Indicates one or more field names on which the [Recordset](recordset-object-ado.md) is sorted, and whether each field is sorted in ascending or descending order.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="4a200-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="4a200-105">Settings and return values</span></span>

<span data-ttu-id="4a200-p101">Legt einen **String** -Wert fest, der die Feldnamen im **Recordset** -Objekt angibt, nach denen sortiert wird, oder gibt den Wert zurück. Jeder Name wird durch ein Komma getrennt, ggf. gefolgt von einer Leerstelle und dem Schlüsselwort. **ASC** sortiert das Feld in aufsteigender, **DESC** in absteigender Reihenfolge. Wenn Sie kein Schlüsselwort angeben, wird das Feld standardmäßig in aufsteigender Reihenfolge sortiert.</span><span class="sxs-lookup"><span data-stu-id="4a200-p101">Sets or returns a **String** value that indicates the field names in the **Recordset** on which to sort. Each name is separated by a comma, and is optionally followed by a blank and the keyword, **ASC**, which sorts the field in ascending order, or **DESC**, which sorts the field in descending order. By default, if no keyword is specified, the field is sorted in ascending order.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a200-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4a200-109">Remarks</span></span>

<span data-ttu-id="4a200-p102">Für diese Eigenschaft muss die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt sein. Ein temporärer Index wird für jedes Feld erstellt, das in der **Sort** -Eigenschaft angegeben ist, sofern noch kein Index vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4a200-p102">This property requires the [CursorLocation](cursorlocation-property-ado.md) property to be set to **adUseClient**. A temporary index will be created for each field specified in the **Sort** property if an index does not already exist.</span></span>

<span data-ttu-id="4a200-112">Der Sortiervorgang ist effizient, da Daten nicht physisch neu angeordnet werden, sondern einfach nur in der im Index angegebenen Reihenfolge auf die Daten zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="4a200-112">The sort operation is efficient because data is not physically rearranged, but is simply accessed in the order specified by the index.</span></span>

<span data-ttu-id="4a200-p103">Wenn Sie für die **Sort** -Eigenschaft eine leere Zeichenfolge festlegen, werden die Zeilen in die ursprüngliche Reihenfolge zurückgesetzt und temporäre Indizes gelöscht. Vorhandene Indizes werden nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4a200-p103">Setting the **Sort** property to an empty string will reset the rows to their original order and delete temporary indexes. Existing indexes will not be deleted.</span></span>

<span data-ttu-id="4a200-115">Angenommen Sie, ein **Recordset-Objekt** namens *FirstName*, *LastName*und *MiddleInitial*drei Felder enthält.</span><span class="sxs-lookup"><span data-stu-id="4a200-115">Suppose a **Recordset** contains three fields named *firstName*, *middleInitial*, and *lastName*.</span></span> <span data-ttu-id="4a200-116">Legen Sie die **Sort** -Eigenschaft auf die Zeichenfolge "LastName DESC, FirstName ASC" die Reihenfolge der **Recordset-Objekt** nach dem Nachnamen in absteigender Reihenfolge und dann nach dem Vornamen in aufsteigender Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="4a200-116">Set the **Sort** property to the string, "lastName DESC, firstName ASC", which will order the **Recordset** by last name in descending order, then by first name in ascending order.</span></span> <span data-ttu-id="4a200-117">Der Mittelname wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="4a200-117">The middle initial is ignored.</span></span>

<span data-ttu-id="4a200-p105">Felder können nicht "ASC" oder "DESC" benannt werden, da sonst ein Konflikt mit den Schlüsselwörtern **ASC** und **DESC** auftritt. Geben Sie einem Feld mit einem Konflikte verursachenden Namen einen Alias. Verwenden Sie dazu das Schlüsselwort **AS** in der Abfrage, die das **Recordset** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4a200-p105">No field can be named "ASC" or "DESC" because those names conflict with the keywords **ASC** and **DESC**. Give a field with a conflicting name an alias by using the **AS** keyword in the query that returns the **Recordset**.</span></span>

