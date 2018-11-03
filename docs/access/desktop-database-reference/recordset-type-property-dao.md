---
title: Recordset.Type-Eigenschaft (DAO)
TOCTitle: Type Property
ms:assetid: d841b088-50bf-16d9-33e0-2140050e1ac6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835080(v=office.15)
ms:contentKeyID: 48548030
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 540e5b8226907dc580d34ab3215d3c0dca67e3f6
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936882"
---
# <a name="recordsettype-property-dao"></a><span data-ttu-id="52dec-102">Recordset.Type-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="52dec-102">Recordset.Type property (DAO)</span></span>


<span data-ttu-id="52dec-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="52dec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="52dec-p101">Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt diesen Wert zurück. Schreibgeschützter **Integer**-Wert.</span><span class="sxs-lookup"><span data-stu-id="52dec-p101">Sets or returns a value that indicates the operational type or data type of an object. Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="52dec-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="52dec-106">Syntax</span></span>

<span data-ttu-id="52dec-107">*Ausdruck* . Typ</span><span class="sxs-lookup"><span data-stu-id="52dec-107">*expression* .Type</span></span>

<span data-ttu-id="52dec-108">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="52dec-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="52dec-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52dec-109">Remarks</span></span>

<span data-ttu-id="52dec-110">Ein **Recordset**-Objekt kann folgende Einstellungen und Rückgabewerte haben.</span><span class="sxs-lookup"><span data-stu-id="52dec-110">For a **Recordset** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="52dec-111">Konstante</span><span class="sxs-lookup"><span data-stu-id="52dec-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="52dec-112">Typ der Datensatzgruppe</span><span class="sxs-lookup"><span data-stu-id="52dec-112">Recordset type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52dec-113"><strong>Übergeben</strong></span><span class="sxs-lookup"><span data-stu-id="52dec-113"><strong>dbOpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="52dec-114">Tabelle (nur Microsoft Access-Arbeitsbereiche)</span><span class="sxs-lookup"><span data-stu-id="52dec-114">Table (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52dec-115"><strong>dbOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="52dec-115"><strong>dbOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="52dec-116">Dynamisch (nur ODBCDirect-Arbeitsbereiche)</span><span class="sxs-lookup"><span data-stu-id="52dec-116">Dynamic (ODBCDirect workspaces only)</span></span></p>

> [!NOTE]
> <span data-ttu-id="52dec-p102">[!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="52dec-p102">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52dec-119"><strong>dbOpenDynaset</strong></span><span class="sxs-lookup"><span data-stu-id="52dec-119"><strong>dbOpenDynaset</strong></span></span></p></td>
<td><p><span data-ttu-id="52dec-120">Dynaset</span><span class="sxs-lookup"><span data-stu-id="52dec-120">Dynaset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52dec-121"><strong>dbOpenSnapshot</strong></span><span class="sxs-lookup"><span data-stu-id="52dec-121"><strong>dbOpenSnapshot</strong></span></span></p></td>
<td><p><span data-ttu-id="52dec-122">Snapshot</span><span class="sxs-lookup"><span data-stu-id="52dec-122">Snapshot</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52dec-123"><strong>dbOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="52dec-123"><strong>dbOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="52dec-124">Vorwärtsgerichtet</span><span class="sxs-lookup"><span data-stu-id="52dec-124">Forward-only</span></span></p></td>
</tr>
</tbody>
</table>

