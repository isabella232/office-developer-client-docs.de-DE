---
title: Zeile - Eigenschaft, ActiveX Data Objects (ADO)
TOCTitle: Row property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b4beaa742bfc46ecd32fc04733c3e6ddaf12aa2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715004"
---
# <a name="row-property-ado"></a><span data-ttu-id="1877b-102">Row-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="1877b-102">Row property (ADO)</span></span>

<span data-ttu-id="1877b-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1877b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1877b-104">Ruft ein **Row** -Objekt von OLE DB aus einem **ADORecordConstruction** -Objekt ab oder legt es dafür fest.</span><span class="sxs-lookup"><span data-stu-id="1877b-104">Gets or sets an OLE DB **Row** object from/on an **ADORecordConstruction** object.</span></span> <span data-ttu-id="1877b-105">Bei Verwendung **platzieren\_Zeile** um ein **Row** -Objekt festgelegt, wird eine Zeile in ein ADO- **Record** -Objekt umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="1877b-105">When you use **put\_Row** to set a **Row** object, a row is turned into an ADO **Record** object.</span></span> <span data-ttu-id="1877b-106">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1877b-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1877b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1877b-107">Syntax</span></span>

<span data-ttu-id="1877b-108">HRESULT Get\_Zeile (\[out Retval\] IUnknown\* \* PpRow);</span><span class="sxs-lookup"><span data-stu-id="1877b-108">HRESULT get\_Row(\[out, retval\] IUnknown\*\* ppRow);</span></span>

<span data-ttu-id="1877b-109">Platzieren Sie HRESULT\_Zeile (\[in\] IUnknown\* pRow);</span><span class="sxs-lookup"><span data-stu-id="1877b-109">HRESULT put\_Row(\[in\] IUnknown\* pRow);</span></span>

## <a name="parameters"></a><span data-ttu-id="1877b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1877b-110">Parameters</span></span>

|<span data-ttu-id="1877b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="1877b-111">Parameter</span></span>|<span data-ttu-id="1877b-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1877b-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="1877b-113">*ppRow*</span><span class="sxs-lookup"><span data-stu-id="1877b-113">*ppRow*</span></span> |<span data-ttu-id="1877b-114">Zeiger auf ein OLE DB- **Row** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="1877b-114">Pointer to an OLE DB **Row** object.</span></span>|
|<span data-ttu-id="1877b-115">*PRow*</span><span class="sxs-lookup"><span data-stu-id="1877b-115">*PRow*</span></span> |<span data-ttu-id="1877b-116">Ein OLE DB- **Row** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="1877b-116">An OLE DB **Row** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="1877b-117">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="1877b-117">Return values</span></span>

<span data-ttu-id="1877b-118">Diese Eigenschaftsmethode gibt die HRESULT-Standardwerte, einschließlich S\_OK und E\_fehl.</span><span class="sxs-lookup"><span data-stu-id="1877b-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="1877b-119">Gilt für</span><span class="sxs-lookup"><span data-stu-id="1877b-119">Applies to</span></span>

[<span data-ttu-id="1877b-120">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="1877b-120">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

