---
title: Chapter-Eigenschaft (ADO)
TOCTitle: Chapter property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b4f4efc2ffab9f7996b2d805658b985badbaf87e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296395"
---
# <a name="chapter-property-ado"></a><span data-ttu-id="e5ba9-102">Chapter-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="e5ba9-102">Chapter property (ADO)</span></span>

<span data-ttu-id="e5ba9-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e5ba9-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="e5ba9-104">Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object.</span><span class="sxs-lookup"><span data-stu-id="e5ba9-104">Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="e5ba9-105">Wenn Sie das **Chapter** -Objekt mithilfe von " **\_Chapter** " festlegen, wird eine Teilmenge von Zeilen in ein ADO- **Recordset** -Objekt umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="e5ba9-105">When you use **put\_Chapter** to set the **Chapter** object, a subset of rows is turned into an ADO **Recordset** object.</span></span> <span data-ttu-id="e5ba9-106">This sets the current chapter of the **Rowset** object.</span><span class="sxs-lookup"><span data-stu-id="e5ba9-106">This sets the current chapter of the **Rowset** object.</span></span> <span data-ttu-id="e5ba9-107">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e5ba9-107">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5ba9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5ba9-108">Syntax</span></span>

<span data-ttu-id="e5ba9-109">HRESULT get\_Chapter (\[Out, retval\] Long\* plChapter);</span><span class="sxs-lookup"><span data-stu-id="e5ba9-109">HRESULT get\_Chapter(\[out, retval\] long\* plChapter);</span></span>

<span data-ttu-id="e5ba9-110">HRESULT put\_Chapter (\[in\] Long lChapter);</span><span class="sxs-lookup"><span data-stu-id="e5ba9-110">HRESULT put\_Chapter(\[in\] long lChapter);</span></span>

## <a name="parameters"></a><span data-ttu-id="e5ba9-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5ba9-111">Parameters</span></span>

|<span data-ttu-id="e5ba9-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5ba9-112">Parameter</span></span>|<span data-ttu-id="e5ba9-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5ba9-113">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="e5ba9-114">*plChapter*</span><span class="sxs-lookup"><span data-stu-id="e5ba9-114">*plChapter*</span></span> |<span data-ttu-id="e5ba9-115">Zeiger auf das Handle eines Kapitels.</span><span class="sxs-lookup"><span data-stu-id="e5ba9-115">Pointer to the handle of a chapter.</span></span>|
|<span data-ttu-id="e5ba9-116">*LChapter*</span><span class="sxs-lookup"><span data-stu-id="e5ba9-116">*LChapter*</span></span> |<span data-ttu-id="e5ba9-117">Handle eines Kapitels.</span><span class="sxs-lookup"><span data-stu-id="e5ba9-117">Handle of a chapter.</span></span>|

## <a name="return-values"></a><span data-ttu-id="e5ba9-118">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="e5ba9-118">Return values</span></span>

<span data-ttu-id="e5ba9-119">Diese Property-Methode gibt die standardmäßigen HRESULT-\_Werte zurück,\_einschließlich S OK und e Fail.</span><span class="sxs-lookup"><span data-stu-id="e5ba9-119">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="e5ba9-120">Betrifft</span><span class="sxs-lookup"><span data-stu-id="e5ba9-120">Applies To</span></span>

[<span data-ttu-id="e5ba9-121">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="e5ba9-121">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

