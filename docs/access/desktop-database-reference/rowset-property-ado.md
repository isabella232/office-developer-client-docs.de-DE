---
title: Rowset-Eigenschaft (ADO)
TOCTitle: Rowset property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0d5979cb42e2ed4a979dc07016a4bb02b8097994
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949789"
---
# <a name="rowset-property-ado"></a><span data-ttu-id="10256-102">Rowset-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="10256-102">Rowset property (ADO)</span></span>

<span data-ttu-id="10256-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="10256-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="10256-104">Ein **Rowset**-OLE DB-Objekt wird aus einem **ADORecordsetConstruction**-Objekt abgerufen oder für dieses festgelegt.</span><span class="sxs-lookup"><span data-stu-id="10256-104">Gets or sets an OLE DB **Rowset** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="10256-105">Bei Verwendung der Put\_Rowset, das Rowset in ein ADO- **Recordset** -Objekt aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="10256-105">When you use put\_Rowset, the rowset is turned into an ADO **Recordset** object.</span></span>

<span data-ttu-id="10256-106">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="10256-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="10256-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="10256-107">Syntax</span></span>

<span data-ttu-id="10256-108">HRESULT Get\_Rowset (\[out Retval\] IUnknown\* \* PpRowset);</span><span class="sxs-lookup"><span data-stu-id="10256-108">HRESULT get\_Rowset(\[out, retval\] IUnknown\*\* ppRowset);</span></span>

<span data-ttu-id="10256-109">Platzieren Sie HRESULT\_Rowset (\[in\] IUnknown\* pRowset);</span><span class="sxs-lookup"><span data-stu-id="10256-109">HRESULT put\_Rowset(\[in\] IUnknown\* pRowset);</span></span>

## <a name="parameters"></a><span data-ttu-id="10256-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="10256-110">Parameters</span></span>

|<span data-ttu-id="10256-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="10256-111">Parameter</span></span>|<span data-ttu-id="10256-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10256-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="10256-113">*ppRowset*</span><span class="sxs-lookup"><span data-stu-id="10256-113">*ppRowset*</span></span> |<span data-ttu-id="10256-114">Zeiger auf ein OLE DB- **Rowset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="10256-114">Pointer to an OLE DB **Rowset** object.</span></span>|
|<span data-ttu-id="10256-115">*PRowset*</span><span class="sxs-lookup"><span data-stu-id="10256-115">*PRowset*</span></span> |<span data-ttu-id="10256-116">Ein OLE DB- **Rowset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="10256-116">An OLE DB **Rowset** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="10256-117">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="10256-117">Return values</span></span>

<span data-ttu-id="10256-118">Diese Eigenschaftsmethode gibt die HRESULT-Standardwerte, einschließlich S\_OK und E\_fehl.</span><span class="sxs-lookup"><span data-stu-id="10256-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="10256-119">Gilt für</span><span class="sxs-lookup"><span data-stu-id="10256-119">Applies to</span></span>

[<span data-ttu-id="10256-120">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="10256-120">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

