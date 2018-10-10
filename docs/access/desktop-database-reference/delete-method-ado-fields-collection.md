---
title: Delete-Methode (Fields-Auflistung in ADO)
TOCTitle: Delete Method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3dc4d3553113a35fba875c3eb23ec544ea3d6b7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474618"
---
# <a name="delete-method-ado-fields-collection"></a><span data-ttu-id="e4e95-102">Delete-Methode (Fields-Auflistung in ADO)</span><span class="sxs-lookup"><span data-stu-id="e4e95-102">Delete Method (ADO Fields Collection)</span></span>


<span data-ttu-id="e4e95-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e4e95-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="e4e95-104">Ein Objekt wird aus der [Fields](fields-collection-ado.md)-Auflistung gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e4e95-104">Deletes an object from the [Fields](fields-collection-ado.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4e95-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4e95-105">Syntax</span></span>

<span data-ttu-id="e4e95-106">*Felder*. *Feld* löschen</span><span class="sxs-lookup"><span data-stu-id="e4e95-106">*Fields*.Delete*Field*</span></span>

## <a name="parameters"></a><span data-ttu-id="e4e95-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4e95-107">Parameters</span></span>

  - <span data-ttu-id="e4e95-108">*Field*</span><span class="sxs-lookup"><span data-stu-id="e4e95-108">*Field*</span></span>

  - <span data-ttu-id="e4e95-p101">Ein **Variant** -Objekt, durch das das zu löschende [Field](field-object-ado.md)-Objekt festgelegt wird. Dieser Parameter kann der Name des **Field** -Objekts oder die Position des **Field** -Objekts selbst sein.</span><span class="sxs-lookup"><span data-stu-id="e4e95-p101">A **Variant** that designates the [Field](field-object-ado.md) object to delete. This parameter can be the name of the **Field** object or the ordinal position of the **Field** object itself.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4e95-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e4e95-111">Remarks</span></span>

<span data-ttu-id="e4e95-112">Durch Aufrufen der **Fields.Delete** -Methode für ein geöffnetes [Recordset](recordset-object-ado.md) wird ein Laufzeitfehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="e4e95-112">Calling the **Fields.Delete** method on an open [Recordset](recordset-object-ado.md) causes a run-time error.</span></span>

