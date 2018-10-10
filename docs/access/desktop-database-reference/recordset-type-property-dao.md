---
title: Recordset.Type Property (DAO)
TOCTitle: Type Property
ms:assetid: d841b088-50bf-16d9-33e0-2140050e1ac6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835080(v=office.15)
ms:contentKeyID: 48548030
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f56af1af04ea2cbd603a2f4a0c71bc8e67e5be51
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472630"
---
# <a name="recordsettype-property-dao"></a><span data-ttu-id="94397-102">Recordset.Type Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="94397-102">Recordset.Type Property (DAO)</span></span>


<span data-ttu-id="94397-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="94397-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="94397-p101">Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt diesen Wert zurück. Schreibgeschützter **Integer**-Wert.</span><span class="sxs-lookup"><span data-stu-id="94397-p101">Sets or returns a value that indicates the operational type or data type of an object. Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="94397-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="94397-106">Syntax</span></span>

<span data-ttu-id="94397-107">*Ausdruck* . Typ</span><span class="sxs-lookup"><span data-stu-id="94397-107">*expression* .Type</span></span>

<span data-ttu-id="94397-108">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="94397-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="94397-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94397-109">Remarks</span></span>

<span data-ttu-id="94397-110">Ein **Recordset**-Objekt kann folgende Einstellungen und Rückgabewerte haben.</span><span class="sxs-lookup"><span data-stu-id="94397-110">For a **Recordset** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="94397-111">Konstante</span><span class="sxs-lookup"><span data-stu-id="94397-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="94397-112">Typ der Datensatzgruppe</span><span class="sxs-lookup"><span data-stu-id="94397-112">Recordset type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="94397-113"><strong>Übergeben</strong></span><span class="sxs-lookup"><span data-stu-id="94397-113"><strong>dbOpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="94397-114">Tabelle (nur Microsoft Access-Arbeitsbereiche)</span><span class="sxs-lookup"><span data-stu-id="94397-114">Table (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94397-115"><strong>dbOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="94397-115"><strong>dbOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="94397-116">Dynamisch (nur ODBCDirect-Arbeitsbereiche)</span><span class="sxs-lookup"><span data-stu-id="94397-116">Dynamic (ODBCDirect workspaces only)</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="94397-p102">[!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="94397-p102">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94397-119"><strong>dbOpenDynaset</strong></span><span class="sxs-lookup"><span data-stu-id="94397-119"><strong>dbOpenDynaset</strong></span></span></p></td>
<td><p><span data-ttu-id="94397-120">Dynaset</span><span class="sxs-lookup"><span data-stu-id="94397-120">Dynaset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94397-121"><strong>dbOpenSnapshot</strong></span><span class="sxs-lookup"><span data-stu-id="94397-121"><strong>dbOpenSnapshot</strong></span></span></p></td>
<td><p><span data-ttu-id="94397-122">Snapshot</span><span class="sxs-lookup"><span data-stu-id="94397-122">Snapshot</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94397-123"><strong>dbOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="94397-123"><strong>dbOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="94397-124">Vorwärtsgerichtet</span><span class="sxs-lookup"><span data-stu-id="94397-124">Forward-only</span></span></p></td>
</tr>
</tbody>
</table>

