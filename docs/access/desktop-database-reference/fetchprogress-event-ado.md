---
title: FetchProgress-Ereignis (ADO)
TOCTitle: FetchProgress event (ADO)
ms:assetid: 09145d9a-ea5e-b41c-6c54-33ec83e642a9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248828(v=office.15)
ms:contentKeyID: 48543114
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d863f51e7836acdc577ecd720df77114ed66f067
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293182"
---
# <a name="fetchprogress-event-ado"></a><span data-ttu-id="cc206-102">FetchProgress-Ereignis (ADO)</span><span class="sxs-lookup"><span data-stu-id="cc206-102">FetchProgress event (ADO)</span></span>

<span data-ttu-id="cc206-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cc206-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cc206-104">Das **FetchProgress**-Ereignis wird regelmäßig während einer langen asynchronen Operation aufgerufen, um einen Bericht darüber zu erstellen, wie viele zusätzliche Zeilen derzeit in das [Recordset](recordset-object-ado.md) abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="cc206-104">The **FetchProgress** event is called periodically during a lengthy asynchronous operation to report how many more rows have currently been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cc206-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc206-105">Syntax</span></span>

<span data-ttu-id="cc206-106">FetchProgress*Progress*, *MaxProgress*, *Status*, precordset \*\*</span><span class="sxs-lookup"><span data-stu-id="cc206-106">FetchProgress*Progress*, *MaxProgress*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="cc206-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc206-107">Parameters</span></span>

|<span data-ttu-id="cc206-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc206-108">Parameter</span></span>|<span data-ttu-id="cc206-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cc206-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="cc206-110">*Progress*</span><span class="sxs-lookup"><span data-stu-id="cc206-110">*Progress*</span></span> |<span data-ttu-id="cc206-111">Ein **Long** -Wert, der die Anzahl von Datensätzen angibt, die derzeit mit der Fetch-Operation abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="cc206-111">A **Long** value indicating the number of records that have currently been retrieved by the fetch operation.</span></span>|
|<span data-ttu-id="cc206-112">*MaxProgress*</span><span class="sxs-lookup"><span data-stu-id="cc206-112">*MaxProgress*</span></span> |<span data-ttu-id="cc206-113">Ein **Long** -Wert, der die maximale Anzahl von Datensätzen angibt, die erwartungsgemäß abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="cc206-113">A **Long** value indicating the maximum number of records expected to be retrieved.</span></span>|
|<span data-ttu-id="cc206-114">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="cc206-114">*adStatus*</span></span> |<span data-ttu-id="cc206-115">Ein [EventStatusEnum](eventstatusenum.md)-Statuswert.</span><span class="sxs-lookup"><span data-stu-id="cc206-115">An [EventStatusEnum](eventstatusenum.md) status value.</span></span>|
|<span data-ttu-id="cc206-116">*precordset*</span><span class="sxs-lookup"><span data-stu-id="cc206-116">*pRecordset*</span></span> |<span data-ttu-id="cc206-117">Ein **Recordset** -Objekt, das das Objekt darstellt, für das die Datensätze abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="cc206-117">A **Recordset** object that is the object for which the records are being retrieved.</span></span>|

## <a name="remarks"></a><span data-ttu-id="cc206-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc206-118">Remarks</span></span>

<span data-ttu-id="cc206-p101">Wenn **FetchProgress** mit einem untergeordneten **Recordset**-Objekt verwendet wird, ist zu beachten, dass die *Progress*- und *MaxProgress*-Parameterwerte vom zugrunde liegenden [Microsoft Cursor Service für OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md)-Rowset abgeleitet werden. Die zurückgegebenen Werte stellen die Gesamtanzahl von Datensätzen im zugrunde liegenden Rowset dar, nicht nur die Anzahl von Datensätzen im aktuellen Kapitel.</span><span class="sxs-lookup"><span data-stu-id="cc206-p101">When using **FetchProgress** with a child **Recordset**, be aware that the *Progress* and *MaxProgress* parameter values are derived from the underlying [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md) rowset. The values returned represent the total number of records in the underlying rowset, not just the number of records in the current chapter.</span></span>

> [!NOTE]
> <span data-ttu-id="cc206-121">[!HINWEIS] Um **FetchProgress** mit Microsoft Visual Basic zu verwenden, ist Visual Basic 6.0 oder höher erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cc206-121">To use **FetchProgress** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>


