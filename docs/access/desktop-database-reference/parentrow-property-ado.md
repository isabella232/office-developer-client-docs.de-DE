---
title: ParentRow-Eigenschaft (ADO)
TOCTitle: ParentRow property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2844f7c93164c4b384a895cd32a13bd682154ce3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721724"
---
# <a name="parentrow-property-ado"></a><span data-ttu-id="3a3de-102">ParentRow-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="3a3de-102">ParentRow property (ADO)</span></span>

<span data-ttu-id="3a3de-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3a3de-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3a3de-104">Legt den Container eines OLE DB- **Row** -Objekts für ein **ADORecordConstruction** -Objekt fest, sodass das übergeordnete Objekt der Zeile in ein ADO- **Record** -Objekt umgewandelt wird.</span><span class="sxs-lookup"><span data-stu-id="3a3de-104">Sets the container of an OLE DB **Row** object on an **ADORecordConstruction** object, so that the parent of the row is turned into an ADO **Record** object.</span></span>

<span data-ttu-id="3a3de-105">Lesegeschützt.</span><span class="sxs-lookup"><span data-stu-id="3a3de-105">Write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a3de-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a3de-106">Syntax</span></span>

<span data-ttu-id="3a3de-107">Platzieren Sie HRESULT\_ParentRow (\[in\] IUnknown\* pParent);</span><span class="sxs-lookup"><span data-stu-id="3a3de-107">HRESULT put\_ParentRow(\[in\] IUnknown\* pParent);</span></span>

## <a name="parameters"></a><span data-ttu-id="3a3de-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a3de-108">Parameters</span></span>

|<span data-ttu-id="3a3de-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a3de-109">Parameter</span></span>|<span data-ttu-id="3a3de-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a3de-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="3a3de-111">*pParent*</span><span class="sxs-lookup"><span data-stu-id="3a3de-111">*pParent*</span></span> |<span data-ttu-id="3a3de-112">Ein Container einer Zeile.</span><span class="sxs-lookup"><span data-stu-id="3a3de-112">A container of a row.</span></span>|

## <a name="return-values"></a><span data-ttu-id="3a3de-113">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="3a3de-113">Return values</span></span>

<span data-ttu-id="3a3de-114">Diese Eigenschaftsmethode gibt die HRESULT-Standardwerte, einschließlich S\_OK und E\_fehl.</span><span class="sxs-lookup"><span data-stu-id="3a3de-114">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="3a3de-115">Gilt für</span><span class="sxs-lookup"><span data-stu-id="3a3de-115">Applies to</span></span>

[<span data-ttu-id="3a3de-116">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="3a3de-116">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

