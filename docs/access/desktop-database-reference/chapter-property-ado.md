---
title: Chapter-Eigenschaft (ADO)
TOCTitle: Chapter property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5eeb3c6e2e8c7b7f1c0f6e733c1b86545a5e954f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887824"
---
# <a name="chapter-property-ado"></a><span data-ttu-id="bba98-102">Chapter-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="bba98-102">Chapter property (ADO)</span></span>


<span data-ttu-id="bba98-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bba98-103">**Applies to**: Access 2013, Office 2013</span></span>
 

<span data-ttu-id="bba98-104">Ein **Chapter**-OLE DB-Objekt wird aus einem **ADORecordsetConstruction**-Objekt abgerufen oder für dieses festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bba98-104">Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="bba98-105">Bei Verwendung **platzieren\_Kapitel** , um das **Kapitel** -Objekt festzulegen, eine Teilmenge von Zeilen in ein ADO- **Recordset** -Objekt aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="bba98-105">When you use **put\_Chapter** to set the **Chapter** object, a subset of rows is turned into an ADO **Recordset** object.</span></span> <span data-ttu-id="bba98-106">Hierdurch wird das aktuelle Kapitel des **Rowset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="bba98-106">This sets the current chapter of the **Rowset** object.</span></span> <span data-ttu-id="bba98-107">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="bba98-107">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bba98-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bba98-108">Syntax</span></span>

<span data-ttu-id="bba98-109">HRESULT Get\_Kapitel (\[out Retval\] lang\* PlChapter);</span><span class="sxs-lookup"><span data-stu-id="bba98-109">HRESULT get\_Chapter(\[out, retval\] long\* plChapter);</span></span>

<span data-ttu-id="bba98-110">Platzieren Sie HRESULT\_Kapitel (\[in\] lang lChapter);</span><span class="sxs-lookup"><span data-stu-id="bba98-110">HRESULT put\_Chapter(\[in\] long lChapter);</span></span>

## <a name="parameters"></a><span data-ttu-id="bba98-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="bba98-111">Parameters</span></span>

  - <span data-ttu-id="bba98-112">*plChapter*</span><span class="sxs-lookup"><span data-stu-id="bba98-112">*plChapter*</span></span>

  - <span data-ttu-id="bba98-113">Zeiger auf das Handle eines Kapitels.</span><span class="sxs-lookup"><span data-stu-id="bba98-113">Pointer to the handle of a chapter.</span></span>

  - <span data-ttu-id="bba98-114">*LChapter*</span><span class="sxs-lookup"><span data-stu-id="bba98-114">*LChapter*</span></span>

  - <span data-ttu-id="bba98-115">Handle eines Kapitels.</span><span class="sxs-lookup"><span data-stu-id="bba98-115">Handle of a chapter.</span></span>

## <a name="return-values"></a><span data-ttu-id="bba98-116">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="bba98-116">Return values</span></span>

<span data-ttu-id="bba98-117">Diese Eigenschaftsmethode gibt die HRESULT-Standardwerte, einschließlich S\_OK und E\_fehl.</span><span class="sxs-lookup"><span data-stu-id="bba98-117">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="bba98-118">Betrifft</span><span class="sxs-lookup"><span data-stu-id="bba98-118">Applies To</span></span>

[<span data-ttu-id="bba98-119">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="bba98-119">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

