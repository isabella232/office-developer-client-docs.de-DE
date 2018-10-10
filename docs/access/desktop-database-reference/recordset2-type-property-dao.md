---
title: Recordset2.Type Property (DAO)
TOCTitle: Type Property
ms:assetid: 9bec543e-7f59-ea59-dc79-41d0e08b5ab6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198080(v=office.15)
ms:contentKeyID: 48546583
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052880
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ee9afcd5367135da2d39fe889d17d089ae6f4c25
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472983"
---
# <a name="recordset2type-property-dao"></a><span data-ttu-id="fc06c-102">Recordset2.Type Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="fc06c-102">Recordset2.Type Property (DAO)</span></span>


<span data-ttu-id="fc06c-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fc06c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fc06c-p101">Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt diesen Wert zurück. Schreibgeschützter **Integer**-Wert.</span><span class="sxs-lookup"><span data-stu-id="fc06c-p101">Sets or returns a value that indicates the operational type or data type of an object. Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc06c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc06c-106">Syntax</span></span>

<span data-ttu-id="fc06c-107">*Ausdruck* . Typ</span><span class="sxs-lookup"><span data-stu-id="fc06c-107">*expression* .Type</span></span>

<span data-ttu-id="fc06c-108">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="fc06c-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc06c-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fc06c-109">Remarks</span></span>

<span data-ttu-id="fc06c-110">Ein **Recordset**-Objekt kann folgende Einstellungen und Rückgabewerte haben.</span><span class="sxs-lookup"><span data-stu-id="fc06c-110">For a **Recordset** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fc06c-111">Konstante</span><span class="sxs-lookup"><span data-stu-id="fc06c-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="fc06c-112">Typ der Datensatzgruppe</span><span class="sxs-lookup"><span data-stu-id="fc06c-112">Recordset type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc06c-113"><strong>Übergeben</strong></span><span class="sxs-lookup"><span data-stu-id="fc06c-113"><strong>dbOpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="fc06c-114">Tabelle (nur Microsoft Access-Arbeitsbereiche)</span><span class="sxs-lookup"><span data-stu-id="fc06c-114">Table (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc06c-115"><strong>dbOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="fc06c-115"><strong>dbOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="fc06c-116">Dynamisch (nur ODBCDirect-Arbeitsbereiche)</span><span class="sxs-lookup"><span data-stu-id="fc06c-116">Dynamic (ODBCDirect workspaces only)</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="fc06c-p102">[!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="fc06c-p102">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc06c-119"><strong>dbOpenDynaset</strong></span><span class="sxs-lookup"><span data-stu-id="fc06c-119"><strong>dbOpenDynaset</strong></span></span></p></td>
<td><p><span data-ttu-id="fc06c-120">Dynaset</span><span class="sxs-lookup"><span data-stu-id="fc06c-120">Dynaset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc06c-121"><strong>dbOpenSnapshot</strong></span><span class="sxs-lookup"><span data-stu-id="fc06c-121"><strong>dbOpenSnapshot</strong></span></span></p></td>
<td><p><span data-ttu-id="fc06c-122">Snapshot</span><span class="sxs-lookup"><span data-stu-id="fc06c-122">Snapshot</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc06c-123"><strong>dbOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="fc06c-123"><strong>dbOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="fc06c-124">Vorwärtsgerichtet</span><span class="sxs-lookup"><span data-stu-id="fc06c-124">Forward-only</span></span></p></td>
</tr>
</tbody>
</table>

