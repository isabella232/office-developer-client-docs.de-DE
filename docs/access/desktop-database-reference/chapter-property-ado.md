---
title: Chapter-Eigenschaft (ADO)
TOCTitle: Chapter property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d7523a930feed7431bf8be0bbb7222a4b305483
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949397"
---
# <a name="chapter-property-ado"></a><span data-ttu-id="9e194-102">Chapter-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="9e194-102">Chapter property (ADO)</span></span>

<span data-ttu-id="9e194-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9e194-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="9e194-104">Ein **Chapter**-OLE DB-Objekt wird aus einem **ADORecordsetConstruction**-Objekt abgerufen oder für dieses festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9e194-104">Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="9e194-105">Bei Verwendung **platzieren\_Kapitel** , um das **Kapitel** -Objekt festzulegen, eine Teilmenge von Zeilen in ein ADO- **Recordset** -Objekt aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9e194-105">When you use **put\_Chapter** to set the **Chapter** object, a subset of rows is turned into an ADO **Recordset** object.</span></span> <span data-ttu-id="9e194-106">Hierdurch wird das aktuelle Kapitel des **Rowset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="9e194-106">This sets the current chapter of the **Rowset** object.</span></span> <span data-ttu-id="9e194-107">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="9e194-107">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e194-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e194-108">Syntax</span></span>

<span data-ttu-id="9e194-109">HRESULT Get\_Kapitel (\[out Retval\] lang\* PlChapter);</span><span class="sxs-lookup"><span data-stu-id="9e194-109">HRESULT get\_Chapter(\[out, retval\] long\* plChapter);</span></span>

<span data-ttu-id="9e194-110">Platzieren Sie HRESULT\_Kapitel (\[in\] lang lChapter);</span><span class="sxs-lookup"><span data-stu-id="9e194-110">HRESULT put\_Chapter(\[in\] long lChapter);</span></span>

## <a name="parameters"></a><span data-ttu-id="9e194-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e194-111">Parameters</span></span>

|<span data-ttu-id="9e194-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e194-112">Parameter</span></span>|<span data-ttu-id="9e194-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e194-113">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="9e194-114">*plChapter*</span><span class="sxs-lookup"><span data-stu-id="9e194-114">*plChapter*</span></span> |<span data-ttu-id="9e194-115">Zeiger auf das Handle eines Kapitels.</span><span class="sxs-lookup"><span data-stu-id="9e194-115">Pointer to the handle of a chapter.</span></span>|
|<span data-ttu-id="9e194-116">*LChapter*</span><span class="sxs-lookup"><span data-stu-id="9e194-116">*LChapter*</span></span> |<span data-ttu-id="9e194-117">Handle eines Kapitels.</span><span class="sxs-lookup"><span data-stu-id="9e194-117">Handle of a chapter.</span></span>|

## <a name="return-values"></a><span data-ttu-id="9e194-118">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="9e194-118">Return values</span></span>

<span data-ttu-id="9e194-119">Diese Eigenschaftsmethode gibt die HRESULT-Standardwerte, einschließlich S\_OK und E\_fehl.</span><span class="sxs-lookup"><span data-stu-id="9e194-119">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="9e194-120">Betrifft</span><span class="sxs-lookup"><span data-stu-id="9e194-120">Applies To</span></span>

[<span data-ttu-id="9e194-121">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="9e194-121">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

