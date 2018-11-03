---
title: FetchProgress-Ereignis (ADO)
TOCTitle: FetchProgress event (ADO)
ms:assetid: 09145d9a-ea5e-b41c-6c54-33ec83e642a9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248828(v=office.15)
ms:contentKeyID: 48543114
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 44e41c3e9d46c9d26f5aed18755c158a5dc68ba7
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946391"
---
# <a name="fetchprogress-event-ado"></a><span data-ttu-id="f03fb-102">FetchProgress-Ereignis (ADO)</span><span class="sxs-lookup"><span data-stu-id="f03fb-102">FetchProgress event (ADO)</span></span>


<span data-ttu-id="f03fb-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f03fb-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="f03fb-104">Das **FetchProgress** -Ereignis wird regelmäßig während einer langen asynchronen Operation aufgerufen, um einen Bericht darüber zu erstellen, wie viele zusätzliche Zeilen derzeit in das [Recordset](recordset-object-ado.md) abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="f03fb-104">The **FetchProgress** event is called periodically during a lengthy asynchronous operation to report how many more rows have currently been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f03fb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f03fb-105">Syntax</span></span>

<span data-ttu-id="f03fb-106">FetchProgress*Fortschritt*, *MaxProgress*, *AdStatus*, *pCommand*</span><span class="sxs-lookup"><span data-stu-id="f03fb-106">FetchProgress*Progress*, *MaxProgress*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="f03fb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f03fb-107">Parameters</span></span>

- <span data-ttu-id="f03fb-108">*Progress*</span><span class="sxs-lookup"><span data-stu-id="f03fb-108">*Progress*</span></span>

  - <span data-ttu-id="f03fb-109">Ein **Long** -Wert, der die Anzahl von Datensätzen angibt, die derzeit mit der Fetch-Operation abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="f03fb-109">A **Long** value indicating the number of records that have currently been retrieved by the fetch operation.</span></span>

- <span data-ttu-id="f03fb-110">*MaxProgress*</span><span class="sxs-lookup"><span data-stu-id="f03fb-110">*MaxProgress*</span></span>

  - <span data-ttu-id="f03fb-111">Ein **Long** -Wert, der die maximale Anzahl von Datensätzen angibt, die erwartungsgemäß abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f03fb-111">A **Long** value indicating the maximum number of records expected to be retrieved.</span></span>

- <span data-ttu-id="f03fb-112">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="f03fb-112">*adStatus*</span></span>

  - <span data-ttu-id="f03fb-113">Ein [EventStatusEnum](eventstatusenum.md)-Statuswert.</span><span class="sxs-lookup"><span data-stu-id="f03fb-113">An [EventStatusEnum](eventstatusenum.md) status value.</span></span>

- <span data-ttu-id="f03fb-114">*pCommand*</span><span class="sxs-lookup"><span data-stu-id="f03fb-114">*pRecordset*</span></span>

  - <span data-ttu-id="f03fb-115">Ein **Recordset** -Objekt, das das Objekt darstellt, für das die Datensätze abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f03fb-115">A **Recordset** object that is the object for which the records are being retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="f03fb-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f03fb-116">Remarks</span></span>

<span data-ttu-id="f03fb-117">Wenn **FetchProgress** mit einem untergeordneten **Recordset-Objekt**verwendet, achten Sie darauf, dass die Parameterwerte *des Fortschritts* und der *MaxProgress* aus dem zugrunde liegenden [Cursordiensts](microsoft-cursor-service-for-ole-db-ado-service-component.md) Rowset abgeleitet sind.</span><span class="sxs-lookup"><span data-stu-id="f03fb-117">When using **FetchProgress** with a child **Recordset**, be aware that the *Progress* and *MaxProgress* parameter values are derived from the underlying [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md) rowset.</span></span> <span data-ttu-id="f03fb-118">Die zurückgegebenen Werte stellen die Gesamtanzahl von Datensätzen im zugrunde liegenden Rowset dar, nicht nur die Anzahl von Datensätzen im aktuellen Kapitel.</span><span class="sxs-lookup"><span data-stu-id="f03fb-118">The values returned represent the total number of records in the underlying rowset, not just the number of records in the current chapter.</span></span>


> [!NOTE]
> <span data-ttu-id="f03fb-119">[!HINWEIS] Um **FetchProgress** mit Microsoft Visual Basic zu verwenden, ist Visual Basic 6.0 oder höher erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f03fb-119">To use **FetchProgress** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>


