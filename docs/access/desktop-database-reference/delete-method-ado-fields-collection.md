---
title: Delete-Methode (ADO-Fields-Auflistung)
TOCTitle: Delete method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e5d97cec041d69ddbbfe61600ca6b03cb09bc466
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718259"
---
# <a name="delete-method-ado-fields-collection"></a><span data-ttu-id="99e3a-102">Delete-Methode (ADO-Fields-Auflistung)</span><span class="sxs-lookup"><span data-stu-id="99e3a-102">Delete method (ADO Fields Collection)</span></span>

<span data-ttu-id="99e3a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="99e3a-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="99e3a-104">Ein Objekt wird aus der [Fields](fields-collection-ado.md)-Auflistung gelöscht.</span><span class="sxs-lookup"><span data-stu-id="99e3a-104">Deletes an object from the [Fields](fields-collection-ado.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="99e3a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="99e3a-105">Syntax</span></span>

<span data-ttu-id="99e3a-106">*Felder*. *Feld* löschen</span><span class="sxs-lookup"><span data-stu-id="99e3a-106">*Fields*.Delete*Field*</span></span>

## <a name="parameters"></a><span data-ttu-id="99e3a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="99e3a-107">Parameters</span></span>

|<span data-ttu-id="99e3a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="99e3a-108">Parameter</span></span>|<span data-ttu-id="99e3a-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="99e3a-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="99e3a-110">*Field*</span><span class="sxs-lookup"><span data-stu-id="99e3a-110">*Field*</span></span> |<span data-ttu-id="99e3a-p101">Ein **Variant** -Objekt, durch das das zu löschende [Field](field-object-ado.md)-Objekt festgelegt wird. Dieser Parameter kann der Name des **Field** -Objekts oder die Position des **Field** -Objekts selbst sein.</span><span class="sxs-lookup"><span data-stu-id="99e3a-p101">A **Variant** that designates the [Field](field-object-ado.md) object to delete. This parameter can be the name of the **Field** object or the ordinal position of the **Field** object itself.</span></span>|

## <a name="remarks"></a><span data-ttu-id="99e3a-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="99e3a-113">Remarks</span></span>

<span data-ttu-id="99e3a-114">Durch Aufrufen der **Fields.Delete** -Methode für ein geöffnetes [Recordset](recordset-object-ado.md) wird ein Laufzeitfehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="99e3a-114">Calling the **Fields.Delete** method on an open [Recordset](recordset-object-ado.md) causes a run-time error.</span></span>

