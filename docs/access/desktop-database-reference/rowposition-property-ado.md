---
title: RowPosition-Eigenschaft (ADO)
TOCTitle: RowPosition property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6f83d1b113b29be06ffded5263791d3db3068f7f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869071"
---
# <a name="rowposition-property-ado"></a><span data-ttu-id="a633e-102">RowPosition-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="a633e-102">RowPosition property (ADO)</span></span>


<span data-ttu-id="a633e-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a633e-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="a633e-104">Ruft ein OLE DB- **RowPosition** -Objekt aus einem **ADORecordsetConstruction** -Objekt ab oder legt es dafür fest.</span><span class="sxs-lookup"><span data-stu-id="a633e-104">Gets or sets an OLE DB **RowPosition** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="a633e-105">Bei Verwendung **platzieren\_RowPosition** zur **RowPosition** -Objekt das resultierende **Recordset** -Objekt verwendet das **RowPosition** -Objekt zum Bestimmen der aktuellen Zeile.</span><span class="sxs-lookup"><span data-stu-id="a633e-105">When you use **put\_RowPosition** to set the **RowPosition** object, the resulting **Recordset** object uses the **RowPosition** object to determine the current row.</span></span>

<span data-ttu-id="a633e-106">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a633e-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a633e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a633e-107">Syntax</span></span>

<span data-ttu-id="a633e-108">HRESULT Get\_RowPosition (\[out Retval\] IUnknown\* \* PpRowPos);</span><span class="sxs-lookup"><span data-stu-id="a633e-108">HRESULT get\_RowPosition(\[out, retval\] IUnknown\*\* ppRowPos);</span></span>

<span data-ttu-id="a633e-109">Platzieren Sie HRESULT\_RowPosition (\[in\] IUnknown\* pRowPos);</span><span class="sxs-lookup"><span data-stu-id="a633e-109">HRESULT put\_RowPosition(\[in\] IUnknown\* pRowPos);</span></span>

## <a name="parameters"></a><span data-ttu-id="a633e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a633e-110">Parameters</span></span>

  - <span data-ttu-id="a633e-111">*ppRowPos*</span><span class="sxs-lookup"><span data-stu-id="a633e-111">*ppRowPos*</span></span>

  - <span data-ttu-id="a633e-112">Zeiger auf ein OLE DB- **RowPosition** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="a633e-112">Pointer to an OLE DB **RowPosition** object.</span></span>

  - <span data-ttu-id="a633e-113">*PRowPos*</span><span class="sxs-lookup"><span data-stu-id="a633e-113">*PRowPos*</span></span>

  - <span data-ttu-id="a633e-114">Ein OLE DB- **RowPosition** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="a633e-114">An OLE DB **RowPosition** object.</span></span>

## <a name="return-values"></a><span data-ttu-id="a633e-115">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="a633e-115">Return values</span></span>

<span data-ttu-id="a633e-116">Diese Eigenschaftsmethode gibt die HRESULT-Standardwerte, einschließlich S\_OK und E\_fehl.</span><span class="sxs-lookup"><span data-stu-id="a633e-116">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a633e-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a633e-117">Remarks</span></span>

<span data-ttu-id="a633e-p102">Wenn diese Eigenschaft festgelegt ist und sich das **Rowset** -Objekt für das **RowPosition** -Objekt vom **Rowset** -Objekt für das **Recordset** -Objekt unterscheidet, wird letzteres überschrieben. Dasselbe Verhalten gilt auch für das aktuelle **Chapter** -Objekt des **RowPosition** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="a633e-p102">When this property is set, if the **Rowset** object on the **RowPosition** object is different from the **Rowset** object on the **Recordset** object, the former overrides the latter. The same behavior applies to the current **Chapter** of the **RowPosition** as well.</span></span>

## <a name="applies-to"></a><span data-ttu-id="a633e-120">Betrifft</span><span class="sxs-lookup"><span data-stu-id="a633e-120">Applies To</span></span>

[<span data-ttu-id="a633e-121">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="a633e-121">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

