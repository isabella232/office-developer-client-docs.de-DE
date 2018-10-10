---
title: Zeile - Eigenschaft, ActiveX Data Objects (ADO)
TOCTitle: Row Property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 05d97bb411c4199677f512d9412653ca5a4b4fe1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474077"
---
# <a name="row-property-ado"></a><span data-ttu-id="bc28b-102">Row-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="bc28b-102">Row Property (ADO)</span></span>


<span data-ttu-id="bc28b-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bc28b-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="bc28b-104">Ruft ein **Row** -Objekt von OLE DB aus einem **ADORecordConstruction** -Objekt ab oder legt es dafür fest.</span><span class="sxs-lookup"><span data-stu-id="bc28b-104">Gets or sets an OLE DB **Row** object from/on an **ADORecordConstruction** object.</span></span> <span data-ttu-id="bc28b-105">Bei Verwendung **platzieren\_Zeile** um ein **Row** -Objekt festgelegt, wird eine Zeile in ein ADO- **Record** -Objekt umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="bc28b-105">When you use **put\_Row** to set a **Row** object, a row is turned into an ADO **Record** object.</span></span> <span data-ttu-id="bc28b-106">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="bc28b-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc28b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc28b-107">Syntax</span></span>

<span data-ttu-id="bc28b-108">HRESULT Get\_Zeile (\[out Retval\] IUnknown\* \* PpRow);</span><span class="sxs-lookup"><span data-stu-id="bc28b-108">HRESULT get\_Row(\[out, retval\] IUnknown\*\* ppRow);</span></span>

<span data-ttu-id="bc28b-109">Platzieren Sie HRESULT\_Zeile (\[in\] IUnknown\* pRow);</span><span class="sxs-lookup"><span data-stu-id="bc28b-109">HRESULT put\_Row(\[in\] IUnknown\* pRow);</span></span>

## <a name="parameters"></a><span data-ttu-id="bc28b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc28b-110">Parameters</span></span>

  - <span data-ttu-id="bc28b-111">*ppRow*</span><span class="sxs-lookup"><span data-stu-id="bc28b-111">*ppRow*</span></span>

  - <span data-ttu-id="bc28b-112">Zeiger auf ein OLE DB- **Row** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="bc28b-112">Pointer to an OLE DB **Row** object.</span></span>

  - <span data-ttu-id="bc28b-113">*PRow*</span><span class="sxs-lookup"><span data-stu-id="bc28b-113">*PRow*</span></span>

  - <span data-ttu-id="bc28b-114">Ein OLE DB- **Row** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="bc28b-114">An OLE DB **Row** object.</span></span>

## <a name="return-values"></a><span data-ttu-id="bc28b-115">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="bc28b-115">Return Values</span></span>

<span data-ttu-id="bc28b-116">Diese Eigenschaftsmethode gibt die HRESULT-Standardwerte, einschließlich S\_OK und E\_fehl.</span><span class="sxs-lookup"><span data-stu-id="bc28b-116">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="bc28b-117">Betrifft</span><span class="sxs-lookup"><span data-stu-id="bc28b-117">Applies To</span></span>

[<span data-ttu-id="bc28b-118">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="bc28b-118">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

