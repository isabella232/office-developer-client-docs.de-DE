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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706142"
---
# <a name="rowset-property-ado"></a><span data-ttu-id="f50dd-102">Rowset-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="f50dd-102">Rowset property (ADO)</span></span>

<span data-ttu-id="f50dd-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f50dd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f50dd-104">Ein **Rowset**-OLE DB-Objekt wird aus einem **ADORecordsetConstruction**-Objekt abgerufen oder für dieses festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f50dd-104">Gets or sets an OLE DB **Rowset** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="f50dd-105">Bei Verwendung der Put\_Rowset, das Rowset in ein ADO- **Recordset** -Objekt aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f50dd-105">When you use put\_Rowset, the rowset is turned into an ADO **Recordset** object.</span></span>

<span data-ttu-id="f50dd-106">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="f50dd-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f50dd-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f50dd-107">Syntax</span></span>

<span data-ttu-id="f50dd-108">HRESULT Get\_Rowset (\[out Retval\] IUnknown\* \* PpRowset);</span><span class="sxs-lookup"><span data-stu-id="f50dd-108">HRESULT get\_Rowset(\[out, retval\] IUnknown\*\* ppRowset);</span></span>

<span data-ttu-id="f50dd-109">Platzieren Sie HRESULT\_Rowset (\[in\] IUnknown\* pRowset);</span><span class="sxs-lookup"><span data-stu-id="f50dd-109">HRESULT put\_Rowset(\[in\] IUnknown\* pRowset);</span></span>

## <a name="parameters"></a><span data-ttu-id="f50dd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f50dd-110">Parameters</span></span>

|<span data-ttu-id="f50dd-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f50dd-111">Parameter</span></span>|<span data-ttu-id="f50dd-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f50dd-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f50dd-113">*ppRowset*</span><span class="sxs-lookup"><span data-stu-id="f50dd-113">*ppRowset*</span></span> |<span data-ttu-id="f50dd-114">Zeiger auf ein OLE DB- **Rowset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="f50dd-114">Pointer to an OLE DB **Rowset** object.</span></span>|
|<span data-ttu-id="f50dd-115">*PRowset*</span><span class="sxs-lookup"><span data-stu-id="f50dd-115">*PRowset*</span></span> |<span data-ttu-id="f50dd-116">Ein OLE DB- **Rowset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="f50dd-116">An OLE DB **Rowset** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="f50dd-117">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f50dd-117">Return values</span></span>

<span data-ttu-id="f50dd-118">Diese Eigenschaftsmethode gibt die HRESULT-Standardwerte, einschließlich S\_OK und E\_fehl.</span><span class="sxs-lookup"><span data-stu-id="f50dd-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="f50dd-119">Gilt für</span><span class="sxs-lookup"><span data-stu-id="f50dd-119">Applies to</span></span>

[<span data-ttu-id="f50dd-120">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="f50dd-120">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

