---
title: RowPosition-Eigenschaft (ADO)
TOCTitle: RowPosition property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0adb1cdf9ce7b096d7b80b86a89a819d5789b60b
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949383"
---
# <a name="rowposition-property-ado"></a><span data-ttu-id="ee56d-102">RowPosition-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="ee56d-102">RowPosition property (ADO)</span></span>

<span data-ttu-id="ee56d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee56d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ee56d-104">Ruft ein OLE DB- **RowPosition** -Objekt aus einem **ADORecordsetConstruction** -Objekt ab oder legt es dafür fest.</span><span class="sxs-lookup"><span data-stu-id="ee56d-104">Gets or sets an OLE DB **RowPosition** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="ee56d-105">Bei Verwendung **platzieren\_RowPosition** zur **RowPosition** -Objekt das resultierende **Recordset** -Objekt verwendet das **RowPosition** -Objekt zum Bestimmen der aktuellen Zeile.</span><span class="sxs-lookup"><span data-stu-id="ee56d-105">When you use **put\_RowPosition** to set the **RowPosition** object, the resulting **Recordset** object uses the **RowPosition** object to determine the current row.</span></span>

<span data-ttu-id="ee56d-106">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="ee56d-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee56d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee56d-107">Syntax</span></span>

<span data-ttu-id="ee56d-108">HRESULT Get\_RowPosition (\[out Retval\] IUnknown\* \* PpRowPos);</span><span class="sxs-lookup"><span data-stu-id="ee56d-108">HRESULT get\_RowPosition(\[out, retval\] IUnknown\*\* ppRowPos);</span></span>

<span data-ttu-id="ee56d-109">Platzieren Sie HRESULT\_RowPosition (\[in\] IUnknown\* pRowPos);</span><span class="sxs-lookup"><span data-stu-id="ee56d-109">HRESULT put\_RowPosition(\[in\] IUnknown\* pRowPos);</span></span>

## <a name="parameters"></a><span data-ttu-id="ee56d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee56d-110">Parameters</span></span>

|<span data-ttu-id="ee56d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee56d-111">Parameter</span></span>|<span data-ttu-id="ee56d-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee56d-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="ee56d-113">*ppRowPos*</span><span class="sxs-lookup"><span data-stu-id="ee56d-113">*ppRowPos*</span></span> |<span data-ttu-id="ee56d-114">Zeiger auf ein OLE DB- **RowPosition** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="ee56d-114">Pointer to an OLE DB **RowPosition** object.</span></span>|
|<span data-ttu-id="ee56d-115">*PRowPos*</span><span class="sxs-lookup"><span data-stu-id="ee56d-115">*PRowPos*</span></span> |<span data-ttu-id="ee56d-116">Ein OLE DB- **RowPosition** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="ee56d-116">An OLE DB **RowPosition** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="ee56d-117">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="ee56d-117">Return values</span></span>

<span data-ttu-id="ee56d-118">Diese Eigenschaftsmethode gibt die HRESULT-Standardwerte, einschließlich S\_OK und E\_fehl.</span><span class="sxs-lookup"><span data-stu-id="ee56d-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee56d-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ee56d-119">Remarks</span></span>

<span data-ttu-id="ee56d-p102">Wenn diese Eigenschaft festgelegt ist und sich das **Rowset** -Objekt für das **RowPosition** -Objekt vom **Rowset** -Objekt für das **Recordset** -Objekt unterscheidet, wird letzteres überschrieben. Dasselbe Verhalten gilt auch für das aktuelle **Chapter** -Objekt des **RowPosition** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="ee56d-p102">When this property is set, if the **Rowset** object on the **RowPosition** object is different from the **Rowset** object on the **Recordset** object, the former overrides the latter. The same behavior applies to the current **Chapter** of the **RowPosition** as well.</span></span>

## <a name="applies-to"></a><span data-ttu-id="ee56d-122">Gilt für</span><span class="sxs-lookup"><span data-stu-id="ee56d-122">Applies to</span></span>

[<span data-ttu-id="ee56d-123">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="ee56d-123">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

