---
title: ParentRow-Eigenschaft (ADO)
TOCTitle: ParentRow Property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 834dcaed7d1acdcf66410584436e2ccee8c91c56
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476126"
---
# <a name="parentrow-property-ado"></a><span data-ttu-id="1ddad-102">ParentRow-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="1ddad-102">ParentRow Property (ADO)</span></span>


<span data-ttu-id="1ddad-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1ddad-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="1ddad-104">Legt den Container eines OLE DB- **Row** -Objekts für ein **ADORecordConstruction** -Objekt fest, sodass das übergeordnete Objekt der Zeile in ein ADO- **Record** -Objekt umgewandelt wird.</span><span class="sxs-lookup"><span data-stu-id="1ddad-104">Sets the container of an OLE DB **Row** object on an **ADORecordConstruction** object, so that the parent of the row is turned into an ADO **Record** object.</span></span>

<span data-ttu-id="1ddad-105">Lesegeschützt.</span><span class="sxs-lookup"><span data-stu-id="1ddad-105">Write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ddad-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ddad-106">Syntax</span></span>

<span data-ttu-id="1ddad-107">Platzieren Sie HRESULT\_ParentRow (\[in\] IUnknown\* pParent);</span><span class="sxs-lookup"><span data-stu-id="1ddad-107">HRESULT put\_ParentRow(\[in\] IUnknown\* pParent);</span></span>

## <a name="parameters"></a><span data-ttu-id="1ddad-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ddad-108">Parameters</span></span>

  - <span data-ttu-id="1ddad-109">*pParent*</span><span class="sxs-lookup"><span data-stu-id="1ddad-109">*pParent*</span></span>

  - <span data-ttu-id="1ddad-110">Ein Container einer Zeile.</span><span class="sxs-lookup"><span data-stu-id="1ddad-110">A container of a row.</span></span>

## <a name="return-values"></a><span data-ttu-id="1ddad-111">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="1ddad-111">Return Values</span></span>

<span data-ttu-id="1ddad-112">Diese Eigenschaftsmethode gibt die HRESULT-Standardwerte, einschließlich S\_OK und E\_fehl.</span><span class="sxs-lookup"><span data-stu-id="1ddad-112">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="1ddad-113">Betrifft</span><span class="sxs-lookup"><span data-stu-id="1ddad-113">Applies To</span></span>

[<span data-ttu-id="1ddad-114">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="1ddad-114">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

