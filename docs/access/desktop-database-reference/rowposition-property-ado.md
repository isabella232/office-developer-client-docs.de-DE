---
title: RowPosition-Eigenschaft (ADO)
TOCTitle: RowPosition property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84d3ad7cc5b3d43b15ac1113f6fa00932678ebc3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720961"
---
# <a name="rowposition-property-ado"></a><span data-ttu-id="8d891-102">RowPosition-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="8d891-102">RowPosition property (ADO)</span></span>

<span data-ttu-id="8d891-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8d891-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8d891-104">Ruft ein OLE DB- **RowPosition** -Objekt aus einem **ADORecordsetConstruction** -Objekt ab oder legt es dafür fest.</span><span class="sxs-lookup"><span data-stu-id="8d891-104">Gets or sets an OLE DB **RowPosition** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="8d891-105">Bei Verwendung **platzieren\_RowPosition** zur **RowPosition** -Objekt das resultierende **Recordset** -Objekt verwendet das **RowPosition** -Objekt zum Bestimmen der aktuellen Zeile.</span><span class="sxs-lookup"><span data-stu-id="8d891-105">When you use **put\_RowPosition** to set the **RowPosition** object, the resulting **Recordset** object uses the **RowPosition** object to determine the current row.</span></span>

<span data-ttu-id="8d891-106">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="8d891-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d891-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d891-107">Syntax</span></span>

<span data-ttu-id="8d891-108">HRESULT Get\_RowPosition (\[out Retval\] IUnknown\* \* PpRowPos);</span><span class="sxs-lookup"><span data-stu-id="8d891-108">HRESULT get\_RowPosition(\[out, retval\] IUnknown\*\* ppRowPos);</span></span>

<span data-ttu-id="8d891-109">Platzieren Sie HRESULT\_RowPosition (\[in\] IUnknown\* pRowPos);</span><span class="sxs-lookup"><span data-stu-id="8d891-109">HRESULT put\_RowPosition(\[in\] IUnknown\* pRowPos);</span></span>

## <a name="parameters"></a><span data-ttu-id="8d891-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d891-110">Parameters</span></span>

|<span data-ttu-id="8d891-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d891-111">Parameter</span></span>|<span data-ttu-id="8d891-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d891-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="8d891-113">*ppRowPos*</span><span class="sxs-lookup"><span data-stu-id="8d891-113">*ppRowPos*</span></span> |<span data-ttu-id="8d891-114">Zeiger auf ein OLE DB- **RowPosition** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="8d891-114">Pointer to an OLE DB **RowPosition** object.</span></span>|
|<span data-ttu-id="8d891-115">*PRowPos*</span><span class="sxs-lookup"><span data-stu-id="8d891-115">*PRowPos*</span></span> |<span data-ttu-id="8d891-116">Ein OLE DB- **RowPosition** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="8d891-116">An OLE DB **RowPosition** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="8d891-117">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8d891-117">Return values</span></span>

<span data-ttu-id="8d891-118">Diese Eigenschaftsmethode gibt die HRESULT-Standardwerte, einschließlich S\_OK und E\_fehl.</span><span class="sxs-lookup"><span data-stu-id="8d891-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d891-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8d891-119">Remarks</span></span>

<span data-ttu-id="8d891-p102">Wenn diese Eigenschaft festgelegt ist und sich das **Rowset** -Objekt für das **RowPosition** -Objekt vom **Rowset** -Objekt für das **Recordset** -Objekt unterscheidet, wird letzteres überschrieben. Dasselbe Verhalten gilt auch für das aktuelle **Chapter** -Objekt des **RowPosition** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="8d891-p102">When this property is set, if the **Rowset** object on the **RowPosition** object is different from the **Rowset** object on the **Recordset** object, the former overrides the latter. The same behavior applies to the current **Chapter** of the **RowPosition** as well.</span></span>

## <a name="applies-to"></a><span data-ttu-id="8d891-122">Gilt für</span><span class="sxs-lookup"><span data-stu-id="8d891-122">Applies to</span></span>

[<span data-ttu-id="8d891-123">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="8d891-123">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

