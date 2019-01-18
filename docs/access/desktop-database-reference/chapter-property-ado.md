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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717937"
---
# <a name="chapter-property-ado"></a><span data-ttu-id="f3f44-102">Chapter-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="f3f44-102">Chapter property (ADO)</span></span>

<span data-ttu-id="f3f44-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f3f44-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="f3f44-104">Ein **Chapter**-OLE DB-Objekt wird aus einem **ADORecordsetConstruction**-Objekt abgerufen oder für dieses festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f3f44-104">Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="f3f44-105">Bei Verwendung **platzieren\_Kapitel** , um das **Kapitel** -Objekt festzulegen, eine Teilmenge von Zeilen in ein ADO- **Recordset** -Objekt aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f3f44-105">When you use **put\_Chapter** to set the **Chapter** object, a subset of rows is turned into an ADO **Recordset** object.</span></span> <span data-ttu-id="f3f44-106">Hierdurch wird das aktuelle Kapitel des **Rowset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="f3f44-106">This sets the current chapter of the **Rowset** object.</span></span> <span data-ttu-id="f3f44-107">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="f3f44-107">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3f44-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3f44-108">Syntax</span></span>

<span data-ttu-id="f3f44-109">HRESULT Get\_Kapitel (\[out Retval\] lang\* PlChapter);</span><span class="sxs-lookup"><span data-stu-id="f3f44-109">HRESULT get\_Chapter(\[out, retval\] long\* plChapter);</span></span>

<span data-ttu-id="f3f44-110">Platzieren Sie HRESULT\_Kapitel (\[in\] lang lChapter);</span><span class="sxs-lookup"><span data-stu-id="f3f44-110">HRESULT put\_Chapter(\[in\] long lChapter);</span></span>

## <a name="parameters"></a><span data-ttu-id="f3f44-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3f44-111">Parameters</span></span>

|<span data-ttu-id="f3f44-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3f44-112">Parameter</span></span>|<span data-ttu-id="f3f44-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3f44-113">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f3f44-114">*plChapter*</span><span class="sxs-lookup"><span data-stu-id="f3f44-114">*plChapter*</span></span> |<span data-ttu-id="f3f44-115">Zeiger auf das Handle eines Kapitels.</span><span class="sxs-lookup"><span data-stu-id="f3f44-115">Pointer to the handle of a chapter.</span></span>|
|<span data-ttu-id="f3f44-116">*LChapter*</span><span class="sxs-lookup"><span data-stu-id="f3f44-116">*LChapter*</span></span> |<span data-ttu-id="f3f44-117">Handle eines Kapitels.</span><span class="sxs-lookup"><span data-stu-id="f3f44-117">Handle of a chapter.</span></span>|

## <a name="return-values"></a><span data-ttu-id="f3f44-118">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f3f44-118">Return values</span></span>

<span data-ttu-id="f3f44-119">Diese Eigenschaftsmethode gibt die HRESULT-Standardwerte, einschließlich S\_OK und E\_fehl.</span><span class="sxs-lookup"><span data-stu-id="f3f44-119">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="f3f44-120">Betrifft</span><span class="sxs-lookup"><span data-stu-id="f3f44-120">Applies To</span></span>

[<span data-ttu-id="f3f44-121">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="f3f44-121">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

