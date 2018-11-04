---
title: ParentRow-Eigenschaft (ADO)
TOCTitle: ParentRow property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 06bb1110dfa7e7a055fa6cd863dcd2cc17f3f585
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950149"
---
# <a name="parentrow-property-ado"></a><span data-ttu-id="08739-102">ParentRow-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="08739-102">ParentRow property (ADO)</span></span>

<span data-ttu-id="08739-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="08739-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="08739-104">Legt den Container eines OLE DB- **Row** -Objekts für ein **ADORecordConstruction** -Objekt fest, sodass das übergeordnete Objekt der Zeile in ein ADO- **Record** -Objekt umgewandelt wird.</span><span class="sxs-lookup"><span data-stu-id="08739-104">Sets the container of an OLE DB **Row** object on an **ADORecordConstruction** object, so that the parent of the row is turned into an ADO **Record** object.</span></span>

<span data-ttu-id="08739-105">Lesegeschützt.</span><span class="sxs-lookup"><span data-stu-id="08739-105">Write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="08739-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="08739-106">Syntax</span></span>

<span data-ttu-id="08739-107">Platzieren Sie HRESULT\_ParentRow (\[in\] IUnknown\* pParent);</span><span class="sxs-lookup"><span data-stu-id="08739-107">HRESULT put\_ParentRow(\[in\] IUnknown\* pParent);</span></span>

## <a name="parameters"></a><span data-ttu-id="08739-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="08739-108">Parameters</span></span>

|<span data-ttu-id="08739-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="08739-109">Parameter</span></span>|<span data-ttu-id="08739-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08739-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="08739-111">*pParent*</span><span class="sxs-lookup"><span data-stu-id="08739-111">*pParent*</span></span> |<span data-ttu-id="08739-112">Ein Container einer Zeile.</span><span class="sxs-lookup"><span data-stu-id="08739-112">A container of a row.</span></span>|

## <a name="return-values"></a><span data-ttu-id="08739-113">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="08739-113">Return values</span></span>

<span data-ttu-id="08739-114">Diese Eigenschaftsmethode gibt die HRESULT-Standardwerte, einschließlich S\_OK und E\_fehl.</span><span class="sxs-lookup"><span data-stu-id="08739-114">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="08739-115">Gilt für</span><span class="sxs-lookup"><span data-stu-id="08739-115">Applies to</span></span>

[<span data-ttu-id="08739-116">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="08739-116">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

