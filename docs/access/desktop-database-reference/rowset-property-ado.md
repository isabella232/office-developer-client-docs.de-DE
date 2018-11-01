---
title: Rowset-Eigenschaft (ADO)
TOCTitle: Rowset property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7be8abbce6828dd202e0c64eec342de9198f7a9b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878535"
---
# <a name="rowset-property-ado"></a><span data-ttu-id="76d13-102">Rowset-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="76d13-102">Rowset property (ADO)</span></span>


<span data-ttu-id="76d13-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="76d13-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="76d13-104">Ein **Rowset**-OLE DB-Objekt wird aus einem **ADORecordsetConstruction**-Objekt abgerufen oder für dieses festgelegt.</span><span class="sxs-lookup"><span data-stu-id="76d13-104">Gets or sets an OLE DB **Rowset** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="76d13-105">Bei Verwendung der Put\_Rowset, das Rowset in ein ADO- **Recordset** -Objekt aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="76d13-105">When you use put\_Rowset, the rowset is turned into an ADO **Recordset** object.</span></span>

<span data-ttu-id="76d13-106">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="76d13-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="76d13-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="76d13-107">Syntax</span></span>

<span data-ttu-id="76d13-108">HRESULT Get\_Rowset (\[out Retval\] IUnknown\* \* PpRowset);</span><span class="sxs-lookup"><span data-stu-id="76d13-108">HRESULT get\_Rowset(\[out, retval\] IUnknown\*\* ppRowset);</span></span>

<span data-ttu-id="76d13-109">Platzieren Sie HRESULT\_Rowset (\[in\] IUnknown\* pRowset);</span><span class="sxs-lookup"><span data-stu-id="76d13-109">HRESULT put\_Rowset(\[in\] IUnknown\* pRowset);</span></span>

## <a name="parameters"></a><span data-ttu-id="76d13-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="76d13-110">Parameters</span></span>

  - <span data-ttu-id="76d13-111">*ppRowset*</span><span class="sxs-lookup"><span data-stu-id="76d13-111">*ppRowset*</span></span>

  - <span data-ttu-id="76d13-112">Zeiger auf ein OLE DB- **Rowset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="76d13-112">Pointer to an OLE DB **Rowset** object.</span></span>

  - <span data-ttu-id="76d13-113">*PRowset*</span><span class="sxs-lookup"><span data-stu-id="76d13-113">*PRowset*</span></span>

  - <span data-ttu-id="76d13-114">Ein OLE DB- **Rowset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="76d13-114">An OLE DB **Rowset** object.</span></span>

## <a name="return-values"></a><span data-ttu-id="76d13-115">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="76d13-115">Return values</span></span>

<span data-ttu-id="76d13-116">Diese Eigenschaftsmethode gibt die HRESULT-Standardwerte, einschließlich S\_OK und E\_fehl.</span><span class="sxs-lookup"><span data-stu-id="76d13-116">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="76d13-117">Betrifft</span><span class="sxs-lookup"><span data-stu-id="76d13-117">Applies To</span></span>

[<span data-ttu-id="76d13-118">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="76d13-118">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

