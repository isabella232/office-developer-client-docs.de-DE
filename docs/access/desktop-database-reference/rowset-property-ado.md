---
title: Rowset-Eigenschaft (ADO)
TOCTitle: Rowset property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: be2a4855b3411a11ddd5a76225acaa52344877a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306741"
---
# <a name="rowset-property-ado"></a><span data-ttu-id="7d295-102">Rowset-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="7d295-102">Rowset property (ADO)</span></span>

<span data-ttu-id="7d295-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7d295-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7d295-104">Gets or sets an OLE DB **Rowset** object from/on an **ADORecordsetConstruction** object.</span><span class="sxs-lookup"><span data-stu-id="7d295-104">Gets or sets an OLE DB **Rowset** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="7d295-105">Wenn Sie put\_-Rowset verwenden, wird das Rowset in ein ADO- **Recordset** -Objekt umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="7d295-105">When you use put\_Rowset, the rowset is turned into an ADO **Recordset** object.</span></span>

<span data-ttu-id="7d295-106">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="7d295-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d295-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d295-107">Syntax</span></span>

<span data-ttu-id="7d295-108">HRESULT get\_-Rowset\[(Out,\] retval\* \* IUnknown ppRowset);</span><span class="sxs-lookup"><span data-stu-id="7d295-108">HRESULT get\_Rowset(\[out, retval\] IUnknown\*\* ppRowset);</span></span>

<span data-ttu-id="7d295-109">HRESULT put\_-Rowset\[(\] in\* IUnknown pRowset);</span><span class="sxs-lookup"><span data-stu-id="7d295-109">HRESULT put\_Rowset(\[in\] IUnknown\* pRowset);</span></span>

## <a name="parameters"></a><span data-ttu-id="7d295-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d295-110">Parameters</span></span>

|<span data-ttu-id="7d295-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d295-111">Parameter</span></span>|<span data-ttu-id="7d295-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7d295-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="7d295-113">*ppRowset*</span><span class="sxs-lookup"><span data-stu-id="7d295-113">*ppRowset*</span></span> |<span data-ttu-id="7d295-114">Zeiger auf ein OLE DB- **Rowset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="7d295-114">Pointer to an OLE DB **Rowset** object.</span></span>|
|<span data-ttu-id="7d295-115">*PRowset*</span><span class="sxs-lookup"><span data-stu-id="7d295-115">*PRowset*</span></span> |<span data-ttu-id="7d295-116">Ein OLE DB- **Rowset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="7d295-116">An OLE DB **Rowset** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="7d295-117">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="7d295-117">Return values</span></span>

<span data-ttu-id="7d295-118">Diese Property-Methode gibt die standardmäßigen HRESULT-\_Werte zurück,\_einschließlich S OK und e Fail.</span><span class="sxs-lookup"><span data-stu-id="7d295-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="7d295-119">Gilt für</span><span class="sxs-lookup"><span data-stu-id="7d295-119">Applies to</span></span>

[<span data-ttu-id="7d295-120">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="7d295-120">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

