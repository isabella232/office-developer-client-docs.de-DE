---
title: Recordset.Type-Eigenschaft (DAO)
TOCTitle: Type Property
ms:assetid: d841b088-50bf-16d9-33e0-2140050e1ac6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835080(v=office.15)
ms:contentKeyID: 48548030
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4a55af8aaa5cfb3d87e13125871a6ccbe1e7f2dd
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707423"
---
# <a name="recordsettype-property-dao"></a><span data-ttu-id="50c64-102">Recordset.Type-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="50c64-102">Recordset.Type property (DAO)</span></span>


<span data-ttu-id="50c64-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="50c64-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="50c64-p101">Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt diesen Wert zurück. Schreibgeschützter **Integer**-Wert.</span><span class="sxs-lookup"><span data-stu-id="50c64-p101">Sets or returns a value that indicates the operational type or data type of an object. Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="50c64-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="50c64-106">Syntax</span></span>

<span data-ttu-id="50c64-107">*Ausdruck* . Typ</span><span class="sxs-lookup"><span data-stu-id="50c64-107">*expression* .Type</span></span>

<span data-ttu-id="50c64-108">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="50c64-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="50c64-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50c64-109">Remarks</span></span>

<span data-ttu-id="50c64-110">Ein **Recordset**-Objekt kann folgende Einstellungen und Rückgabewerte haben.</span><span class="sxs-lookup"><span data-stu-id="50c64-110">For a **Recordset** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="50c64-111">Konstante</span><span class="sxs-lookup"><span data-stu-id="50c64-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="50c64-112">Typ der Datensatzgruppe</span><span class="sxs-lookup"><span data-stu-id="50c64-112">Recordset type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50c64-113"><strong>Übergeben</strong></span><span class="sxs-lookup"><span data-stu-id="50c64-113"><strong>dbOpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="50c64-114">Tabelle (nur Microsoft Access-Arbeitsbereiche)</span><span class="sxs-lookup"><span data-stu-id="50c64-114">Table (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50c64-115"><strong>dbOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="50c64-115"><strong>dbOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="50c64-116">Dynamisch (nur ODBCDirect-Arbeitsbereiche)</span><span class="sxs-lookup"><span data-stu-id="50c64-116">Dynamic (ODBCDirect workspaces only)</span></span></p>
<p><span data-ttu-id="50c64-117"><strong>Hinweis</strong>: für ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="50c64-117"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="50c64-118">Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="50c64-118">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50c64-119"><strong>dbOpenDynaset</strong></span><span class="sxs-lookup"><span data-stu-id="50c64-119"><strong>dbOpenDynaset</strong></span></span></p></td>
<td><p><span data-ttu-id="50c64-120">Dynaset</span><span class="sxs-lookup"><span data-stu-id="50c64-120">Dynaset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50c64-121"><strong>dbOpenSnapshot</strong></span><span class="sxs-lookup"><span data-stu-id="50c64-121"><strong>dbOpenSnapshot</strong></span></span></p></td>
<td><p><span data-ttu-id="50c64-122">Snapshot</span><span class="sxs-lookup"><span data-stu-id="50c64-122">Snapshot</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50c64-123"><strong>dbOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="50c64-123"><strong>dbOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="50c64-124">Vorwärtsgerichtet</span><span class="sxs-lookup"><span data-stu-id="50c64-124">Forward-only</span></span></p></td>
</tr>
</tbody>
</table>

