---
title: Workspace.Type-Eigenschaft (DAO)
TOCTitle: Type Property
ms:assetid: 89e59280-d2cd-b6a2-16c5-9f14f42fdd99
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197086(v=office.15)
ms:contentKeyID: 48546177
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6c715da6ec535d90397b49e47be6ca76a72e5685
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926773"
---
# <a name="workspacetype-property-dao"></a><span data-ttu-id="f9862-102">Workspace.Type-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="f9862-102">Workspace.Type property (DAO)</span></span>


<span data-ttu-id="f9862-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f9862-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f9862-p101">Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt diesen Wert zurück. Schreibgeschützter **Integer**-Wert.</span><span class="sxs-lookup"><span data-stu-id="f9862-p101">Sets or returns a value that indicates the operational type or data type of an object. Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9862-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9862-106">Syntax</span></span>

<span data-ttu-id="f9862-107">*Ausdruck* . Typ</span><span class="sxs-lookup"><span data-stu-id="f9862-107">*expression* .Type</span></span>

<span data-ttu-id="f9862-108">*Ausdruck* Eine Variable, die ein **Workspace** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="f9862-108">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9862-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9862-109">Remarks</span></span>

<span data-ttu-id="f9862-110">Ein **Workspace**-Objekt kann folgende Einstellungen und Rückgabewerte haben.</span><span class="sxs-lookup"><span data-stu-id="f9862-110">For a **Workspace** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f9862-111">Konstante</span><span class="sxs-lookup"><span data-stu-id="f9862-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="f9862-112">Arbeitsbereichtyp</span><span class="sxs-lookup"><span data-stu-id="f9862-112">Workspace type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9862-113"><strong>dbUseJet</strong></span><span class="sxs-lookup"><span data-stu-id="f9862-113"><strong>dbUseJet</strong></span></span></p></td>
<td><p><span data-ttu-id="f9862-114">Der <strong>Arbeitsbereich</strong> ist mit der Microsoft Access-Datenbank-Engine verbunden.</span><span class="sxs-lookup"><span data-stu-id="f9862-114">The <strong>Workspace</strong> is connected to the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9862-115"><strong>dbUseODBC</strong></span><span class="sxs-lookup"><span data-stu-id="f9862-115"><strong>dbUseODBC</strong></span></span></p></td>
<td><p><span data-ttu-id="f9862-116">Der <strong>Arbeitsbereich</strong> ist mit einer ODBC-Datenquelle verbunden.</span><span class="sxs-lookup"><span data-stu-id="f9862-116">The <strong>Workspace</strong> is connected to an ODBC data source.</span></span></p></td>
</tr>
</tbody>
</table>

