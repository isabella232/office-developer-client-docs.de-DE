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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306860"
---
# <a name="rowposition-property-ado"></a><span data-ttu-id="aa4c7-102">RowPosition-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="aa4c7-102">RowPosition property (ADO)</span></span>

<span data-ttu-id="aa4c7-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="aa4c7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="aa4c7-104">Ruft ein OLE DB- **RowPosition** -Objekt aus einem **ADORecordsetConstruction** -Objekt ab oder legt es dafür fest.</span><span class="sxs-lookup"><span data-stu-id="aa4c7-104">Gets or sets an OLE DB **RowPosition** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="aa4c7-105">Wenn Sie **\_RowPosition** verwenden, um das **RowPosition** -Objekt festZulegen, verwendet das resultierende **Recordset** -Objekt das **RowPosition** -Objekt, um die aktuelle Zeile zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="aa4c7-105">When you use **put\_RowPosition** to set the **RowPosition** object, the resulting **Recordset** object uses the **RowPosition** object to determine the current row.</span></span>

<span data-ttu-id="aa4c7-106">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="aa4c7-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa4c7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa4c7-107">Syntax</span></span>

<span data-ttu-id="aa4c7-108">HRESULT get\_RowPosition (\[Out, retval\] IUnknown\* \* ppRowPos);</span><span class="sxs-lookup"><span data-stu-id="aa4c7-108">HRESULT get\_RowPosition(\[out, retval\] IUnknown\*\* ppRowPos);</span></span>

<span data-ttu-id="aa4c7-109">HRESULT put\_RowPosition (\[in\] IUnknown\* pRowPos);</span><span class="sxs-lookup"><span data-stu-id="aa4c7-109">HRESULT put\_RowPosition(\[in\] IUnknown\* pRowPos);</span></span>

## <a name="parameters"></a><span data-ttu-id="aa4c7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa4c7-110">Parameters</span></span>

|<span data-ttu-id="aa4c7-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa4c7-111">Parameter</span></span>|<span data-ttu-id="aa4c7-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa4c7-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="aa4c7-113">*ppRowPos*</span><span class="sxs-lookup"><span data-stu-id="aa4c7-113">*ppRowPos*</span></span> |<span data-ttu-id="aa4c7-114">Zeiger auf ein OLE DB- **RowPosition** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="aa4c7-114">Pointer to an OLE DB **RowPosition** object.</span></span>|
|<span data-ttu-id="aa4c7-115">*PRowPos*</span><span class="sxs-lookup"><span data-stu-id="aa4c7-115">*PRowPos*</span></span> |<span data-ttu-id="aa4c7-116">Ein OLE DB- **RowPosition** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="aa4c7-116">An OLE DB **RowPosition** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="aa4c7-117">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="aa4c7-117">Return values</span></span>

<span data-ttu-id="aa4c7-118">Diese Property-Methode gibt die standardmäßigen HRESULT-\_Werte zurück,\_einschließlich S OK und e Fail.</span><span class="sxs-lookup"><span data-stu-id="aa4c7-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa4c7-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa4c7-119">Remarks</span></span>

<span data-ttu-id="aa4c7-p102">Wenn diese Eigenschaft festgelegt ist und sich das **Rowset**-Objekt für das **RowPosition**-Objekt vom **Rowset**-Objekt für das **Recordset**-Objekt unterscheidet, wird letzteres überschrieben. Dasselbe Verhalten gilt auch für das aktuelle **Chapter**-Objekt des **RowPosition**-Objekts.</span><span class="sxs-lookup"><span data-stu-id="aa4c7-p102">When this property is set, if the **Rowset** object on the **RowPosition** object is different from the **Rowset** object on the **Recordset** object, the former overrides the latter. The same behavior applies to the current **Chapter** of the **RowPosition** as well.</span></span>

## <a name="applies-to"></a><span data-ttu-id="aa4c7-122">Gilt für</span><span class="sxs-lookup"><span data-stu-id="aa4c7-122">Applies to</span></span>

[<span data-ttu-id="aa4c7-123">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="aa4c7-123">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

