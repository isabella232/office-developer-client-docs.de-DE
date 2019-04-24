---
title: Recordset. Type-Eigenschaft (DAO)
TOCTitle: Type Property
ms:assetid: d841b088-50bf-16d9-33e0-2140050e1ac6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835080(v=office.15)
ms:contentKeyID: 48548030
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4a55af8aaa5cfb3d87e13125871a6ccbe1e7f2dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307553"
---
# <a name="recordsettype-property-dao"></a><span data-ttu-id="632ae-102">Recordset. Type-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="632ae-102">Recordset.Type property (DAO)</span></span>


<span data-ttu-id="632ae-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="632ae-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="632ae-104">Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt diesen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="632ae-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="632ae-105">Schreibgeschützter **Integer**-Wert.</span><span class="sxs-lookup"><span data-stu-id="632ae-105">Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="632ae-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="632ae-106">Syntax</span></span>

<span data-ttu-id="632ae-107">*Ausdruck* . Typ</span><span class="sxs-lookup"><span data-stu-id="632ae-107">*expression* .Type</span></span>

<span data-ttu-id="632ae-108">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="632ae-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="632ae-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="632ae-109">Remarks</span></span>

<span data-ttu-id="632ae-110">Ein **Recordset**-Objekt kann folgende Einstellungen und Rückgabewerte haben.</span><span class="sxs-lookup"><span data-stu-id="632ae-110">For a **Recordset** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="632ae-111">Konstante</span><span class="sxs-lookup"><span data-stu-id="632ae-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="632ae-112">Typ der Datensatzgruppe</span><span class="sxs-lookup"><span data-stu-id="632ae-112">Recordset type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="632ae-113"><strong>dbOpenable</strong></span><span class="sxs-lookup"><span data-stu-id="632ae-113"><strong>dbOpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="632ae-114">Tabelle (nur Microsoft Access-Arbeitsbereiche)</span><span class="sxs-lookup"><span data-stu-id="632ae-114">Table (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="632ae-115"><strong>dbOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="632ae-115"><strong>dbOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="632ae-116">Dynamisch (nur ODBCDirect-Arbeitsbereiche)</span><span class="sxs-lookup"><span data-stu-id="632ae-116">Dynamic (ODBCDirect workspaces only)</span></span></p>
<p><span data-ttu-id="632ae-117"><strong>Hinweis</strong>: ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="632ae-117"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="632ae-118">Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="632ae-118">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="632ae-119"><strong>dbOpenDynaset</strong></span><span class="sxs-lookup"><span data-stu-id="632ae-119"><strong>dbOpenDynaset</strong></span></span></p></td>
<td><p><span data-ttu-id="632ae-120">Dynaset</span><span class="sxs-lookup"><span data-stu-id="632ae-120">Dynaset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="632ae-121"><strong>dbOpenSnapshot</strong></span><span class="sxs-lookup"><span data-stu-id="632ae-121"><strong>dbOpenSnapshot</strong></span></span></p></td>
<td><p><span data-ttu-id="632ae-122">Snapshot</span><span class="sxs-lookup"><span data-stu-id="632ae-122">Snapshot</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="632ae-123"><strong>dbOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="632ae-123"><strong>dbOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="632ae-124">Vorwärts</span><span class="sxs-lookup"><span data-stu-id="632ae-124">Forward-only</span></span></p></td>
</tr>
</tbody>
</table>

