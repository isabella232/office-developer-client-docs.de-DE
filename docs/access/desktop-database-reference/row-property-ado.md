---
title: Row-Eigenschaft-ActiveX Data Objects (ADO)
TOCTitle: Row property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b4beaa742bfc46ecd32fc04733c3e6ddaf12aa2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306482"
---
# <a name="row-property-ado"></a><span data-ttu-id="67842-102">Row-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="67842-102">Row property (ADO)</span></span>

<span data-ttu-id="67842-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="67842-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="67842-104">Ruft ein **Row** -Objekt von OLE DB aus einem **ADORecordConstruction** -Objekt ab oder legt es dafür fest.</span><span class="sxs-lookup"><span data-stu-id="67842-104">Gets or sets an OLE DB **Row** object from/on an **ADORecordConstruction** object.</span></span> <span data-ttu-id="67842-105">Wenn Sie zum Festlegen eines **Row** -Objekts die **\_Put-Zeile** verwenden, wird eine Zeile in ein ADO- **Record** -Objekt umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="67842-105">When you use **put\_Row** to set a **Row** object, a row is turned into an ADO **Record** object.</span></span> <span data-ttu-id="67842-106">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="67842-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="67842-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="67842-107">Syntax</span></span>

<span data-ttu-id="67842-108">HRESULT get\_Row (\[Out, retval\] IUnknown\* \* ppRow);</span><span class="sxs-lookup"><span data-stu-id="67842-108">HRESULT get\_Row(\[out, retval\] IUnknown\*\* ppRow);</span></span>

<span data-ttu-id="67842-109">\_Zeile mit HRESULT (\[in\] IUnknown\* Bug);</span><span class="sxs-lookup"><span data-stu-id="67842-109">HRESULT put\_Row(\[in\] IUnknown\* pRow);</span></span>

## <a name="parameters"></a><span data-ttu-id="67842-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="67842-110">Parameters</span></span>

|<span data-ttu-id="67842-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="67842-111">Parameter</span></span>|<span data-ttu-id="67842-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="67842-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="67842-113">*ppRow*</span><span class="sxs-lookup"><span data-stu-id="67842-113">*ppRow*</span></span> |<span data-ttu-id="67842-114">Zeiger auf ein OLE DB- **Row** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="67842-114">Pointer to an OLE DB **Row** object.</span></span>|
|<span data-ttu-id="67842-115">*PRow*</span><span class="sxs-lookup"><span data-stu-id="67842-115">*PRow*</span></span> |<span data-ttu-id="67842-116">Ein OLE DB- **Row** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="67842-116">An OLE DB **Row** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="67842-117">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="67842-117">Return values</span></span>

<span data-ttu-id="67842-118">Diese Property-Methode gibt die standardmäßigen HRESULT-\_Werte zurück,\_einschließlich S OK und e Fail.</span><span class="sxs-lookup"><span data-stu-id="67842-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="67842-119">Gilt für</span><span class="sxs-lookup"><span data-stu-id="67842-119">Applies to</span></span>

[<span data-ttu-id="67842-120">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="67842-120">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

