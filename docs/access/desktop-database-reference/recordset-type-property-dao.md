---
title: Recordset.Type-Eigenschaft (DAO)
TOCTitle: Type Property
ms:assetid: d841b088-50bf-16d9-33e0-2140050e1ac6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835080(v=office.15)
ms:contentKeyID: 48548030
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 85e518dc5d13a6e8e70c449fb35158395b7a13aa
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920725"
---
# <a name="recordsettype-property-dao"></a><span data-ttu-id="30545-102">Recordset.Type-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="30545-102">Recordset.Type property (DAO)</span></span>


<span data-ttu-id="30545-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="30545-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="30545-p101">Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt diesen Wert zurück. Schreibgeschützter **Integer**-Wert.</span><span class="sxs-lookup"><span data-stu-id="30545-p101">Sets or returns a value that indicates the operational type or data type of an object. Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="30545-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="30545-106">Syntax</span></span>

<span data-ttu-id="30545-107">*Ausdruck* . Typ</span><span class="sxs-lookup"><span data-stu-id="30545-107">*expression* .Type</span></span>

<span data-ttu-id="30545-108">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="30545-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="30545-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30545-109">Remarks</span></span>

<span data-ttu-id="30545-110">Ein **Recordset**-Objekt kann folgende Einstellungen und Rückgabewerte haben.</span><span class="sxs-lookup"><span data-stu-id="30545-110">For a **Recordset** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="30545-111">Konstante</span><span class="sxs-lookup"><span data-stu-id="30545-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="30545-112">Typ der Datensatzgruppe</span><span class="sxs-lookup"><span data-stu-id="30545-112">Recordset type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30545-113"><strong>Übergeben</strong></span><span class="sxs-lookup"><span data-stu-id="30545-113"><strong>dbOpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="30545-114">Tabelle (nur Microsoft Access-Arbeitsbereiche)</span><span class="sxs-lookup"><span data-stu-id="30545-114">Table (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30545-115"><strong>dbOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="30545-115"><strong>dbOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="30545-116">Dynamisch (nur ODBCDirect-Arbeitsbereiche)</span><span class="sxs-lookup"><span data-stu-id="30545-116">Dynamic (ODBCDirect workspaces only)</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="30545-p102">[!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="30545-p102">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30545-119"><strong>dbOpenDynaset</strong></span><span class="sxs-lookup"><span data-stu-id="30545-119"><strong>dbOpenDynaset</strong></span></span></p></td>
<td><p><span data-ttu-id="30545-120">Dynaset</span><span class="sxs-lookup"><span data-stu-id="30545-120">Dynaset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30545-121"><strong>dbOpenSnapshot</strong></span><span class="sxs-lookup"><span data-stu-id="30545-121"><strong>dbOpenSnapshot</strong></span></span></p></td>
<td><p><span data-ttu-id="30545-122">Snapshot</span><span class="sxs-lookup"><span data-stu-id="30545-122">Snapshot</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30545-123"><strong>dbOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="30545-123"><strong>dbOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="30545-124">Vorwärtsgerichtet</span><span class="sxs-lookup"><span data-stu-id="30545-124">Forward-only</span></span></p></td>
</tr>
</tbody>
</table>

