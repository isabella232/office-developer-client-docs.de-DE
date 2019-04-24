---
title: IFreeBusyDataEnumBlocks
manager: soliver
ms.date: 02/18/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cd5a5ae-118f-c7da-4eda-e97590fc39d4
description: Ruft eine Schnittstelle ab, die Frei/Gebucht-Datenblöcke für einen Benutzer innerhalb eines angegebenen Zeitintervalls auflistet.
ms.openlocfilehash: 51a77b2f47166628db07259ef841e0d6173ee370
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317556"
---
# <a name="ifreebusydataenumblocks"></a><span data-ttu-id="d8c1d-103">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="d8c1d-103">IFreeBusyData::EnumBlocks</span></span>

<span data-ttu-id="d8c1d-104">Ruft eine Schnittstelle ab, die Frei/Gebucht-Datenblöcke für einen Benutzer innerhalb eines angegebenen Zeitintervalls auflistet.</span><span class="sxs-lookup"><span data-stu-id="d8c1d-104">Gets an interface that enumerates free/busy blocks of data for a user within a specified time range.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d8c1d-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="d8c1d-105">Quick info</span></span>

<span data-ttu-id="d8c1d-106">Siehe [IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="d8c1d-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT EnumBlocks( 
     IEnumFBBlock **ppenumfb,  
     FILETIME ftmStart, 
     FILETIME ftmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="d8c1d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8c1d-107">Parameters</span></span>

<span data-ttu-id="d8c1d-108">_ppenumfb_</span><span class="sxs-lookup"><span data-stu-id="d8c1d-108">_ppenumfb_</span></span>
  
> <span data-ttu-id="d8c1d-109">Out Eine Schnittstelle zum Auflisten von Frei/Gebucht-Blöcken.</span><span class="sxs-lookup"><span data-stu-id="d8c1d-109">[out] An interface to enumerate free/busy blocks.</span></span>
    
<span data-ttu-id="d8c1d-110">_ftmStart_</span><span class="sxs-lookup"><span data-stu-id="d8c1d-110">_ftmStart_</span></span>
  
> <span data-ttu-id="d8c1d-111">in Die Startzeit für die Enumeration.</span><span class="sxs-lookup"><span data-stu-id="d8c1d-111">[in] The start time for the enumeration.</span></span> <span data-ttu-id="d8c1d-112">Sie wird in [FILETIME](https://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx)ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="d8c1d-112">It is expressed in [FILETIME](https://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx).</span></span>
    
<span data-ttu-id="d8c1d-113">_ftmEnd_</span><span class="sxs-lookup"><span data-stu-id="d8c1d-113">_ftmEnd_</span></span>
  
> <span data-ttu-id="d8c1d-114">in Die Endzeit für die Enumeration.</span><span class="sxs-lookup"><span data-stu-id="d8c1d-114">[in] The end time for the enumeration.</span></span> <span data-ttu-id="d8c1d-115">Sie wird in **FILETIME**ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="d8c1d-115">It is expressed in **FILETIME**.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="d8c1d-116">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="d8c1d-116">Return values</span></span>

<span data-ttu-id="d8c1d-117">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="d8c1d-117">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d8c1d-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d8c1d-118">Remarks</span></span>

<span data-ttu-id="d8c1d-119">Diese Methode wird verwendet, um den Zeitintervall der Kalenderelemente anzugeben, für die Details abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d8c1d-119">This method is used to indicate the time range of calendar items for which to retrieve details.</span></span> <span data-ttu-id="d8c1d-120">Die Werte von *ftmStart* und *ftmEnd* werden zwischengespeichert und in einem nachfolgenden Aufruf von [IFreeBusyData:: GetFBPublishRange](ifreebusydata-getfbpublishrange.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d8c1d-120">The values of  *ftmStart* and *ftmEnd* are cached and returned in a subsequent call of [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span></span>
  
<span data-ttu-id="d8c1d-121">Ein frei/gebucht-Anbieter kann auch anschließend die zurückgegebene [IEnumFBBlock](ienumfbblock.md) -Schnittstelle verwenden, um auf die Enumeration zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="d8c1d-121">A free/busy provider can also subsequently use the returned [IEnumFBBlock](ienumfbblock.md) interface to access the enumeration.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d8c1d-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8c1d-122">See also</span></span>

- [<span data-ttu-id="d8c1d-123">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="d8c1d-123">IEnumFBBlock</span></span>](ienumfbblock.md)
- [<span data-ttu-id="d8c1d-124">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="d8c1d-124">IFreeBusyData::GetFBPublishRange</span></span>](ifreebusydata-getfbpublishrange.md)
- [<span data-ttu-id="d8c1d-125">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="d8c1d-125">IFreeBusyData::SetFBRange</span></span>](ifreebusydata-setfbrange.md)
- [<span data-ttu-id="d8c1d-126">Verwenden von relativer Zeit zum Zugriff auf Frei/Gebucht-Daten</span><span class="sxs-lookup"><span data-stu-id="d8c1d-126">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

