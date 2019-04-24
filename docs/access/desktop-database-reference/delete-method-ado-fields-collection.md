---
title: Delete-Methode (ADO Fields-Auflistung)
TOCTitle: Delete method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e5d97cec041d69ddbbfe61600ca6b03cb09bc466
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294106"
---
# <a name="delete-method-ado-fields-collection"></a><span data-ttu-id="2fb8d-102">Delete-Methode (ADO Fields-Auflistung)</span><span class="sxs-lookup"><span data-stu-id="2fb8d-102">Delete method (ADO Fields Collection)</span></span>

<span data-ttu-id="2fb8d-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2fb8d-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="2fb8d-104">Ein Objekt wird aus der [Fields](fields-collection-ado.md)-Auflistung gelöscht.</span><span class="sxs-lookup"><span data-stu-id="2fb8d-104">Deletes an object from the [Fields](fields-collection-ado.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fb8d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2fb8d-105">Syntax</span></span>

<span data-ttu-id="2fb8d-106">*Felder*. DELETE-*Feld*</span><span class="sxs-lookup"><span data-stu-id="2fb8d-106">*Fields*.Delete*Field*</span></span>

## <a name="parameters"></a><span data-ttu-id="2fb8d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2fb8d-107">Parameters</span></span>

|<span data-ttu-id="2fb8d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2fb8d-108">Parameter</span></span>|<span data-ttu-id="2fb8d-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2fb8d-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="2fb8d-110">*Feld*</span><span class="sxs-lookup"><span data-stu-id="2fb8d-110">*Field*</span></span> |<span data-ttu-id="2fb8d-p101">Ein **Variant** -Objekt, durch das das zu löschende [Field](field-object-ado.md)-Objekt festgelegt wird. Dieser Parameter kann der Name des **Field** -Objekts oder die Position des **Field** -Objekts selbst sein.</span><span class="sxs-lookup"><span data-stu-id="2fb8d-p101">A **Variant** that designates the [Field](field-object-ado.md) object to delete. This parameter can be the name of the **Field** object or the ordinal position of the **Field** object itself.</span></span>|

## <a name="remarks"></a><span data-ttu-id="2fb8d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2fb8d-113">Remarks</span></span>

<span data-ttu-id="2fb8d-114">Durch Aufrufen der **Fields.Delete**-Methode für ein geöffnetes [Recordset](recordset-object-ado.md) wird ein Laufzeitfehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="2fb8d-114">Calling the **Fields.Delete** method on an open [Recordset](recordset-object-ado.md) causes a run-time error.</span></span>

