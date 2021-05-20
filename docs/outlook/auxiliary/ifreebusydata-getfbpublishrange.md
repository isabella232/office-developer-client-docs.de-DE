---
title: IFreeBusyDataGetFBPublishRange
manager: soliver
ms.date: 09/23/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a8bbe0c-17d1-9349-4c63-f257faf4edda
description: Ruft einen vordefinierten Zeitbereich für eine Aufzählung von Frei/Gebucht-Datenblöcken für einen Benutzer ab.
ms.openlocfilehash: 26951ea6a885f8d0e5e6a2fb5bcf9a63069c7f44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430077"
---
# <a name="ifreebusydatagetfbpublishrange"></a><span data-ttu-id="26db7-103">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="26db7-103">IFreeBusyData::GetFBPublishRange</span></span>

<span data-ttu-id="26db7-104">Ruft einen vordefinierten Zeitbereich für eine Aufzählung von Frei/Gebucht-Datenblöcken für einen Benutzer ab.</span><span class="sxs-lookup"><span data-stu-id="26db7-104">Gets a preset time range for an enumeration of free/busy blocks of data for a user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="26db7-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="26db7-105">Quick info</span></span>

<span data-ttu-id="26db7-106">Weitere [Informationen finden Sie unter IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="26db7-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT GetFBPublishRange( 
     LONG *prtmStart,  
     LONG *prtmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="26db7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="26db7-107">Parameters</span></span>

<span data-ttu-id="26db7-108">_prtmStart_</span><span class="sxs-lookup"><span data-stu-id="26db7-108">_prtmStart_</span></span>
  
> <span data-ttu-id="26db7-109">[out] Ein relativer Zeitwert für den Anfang von Frei/Gebucht-Informationen.</span><span class="sxs-lookup"><span data-stu-id="26db7-109">[out] A relative time value for the start of free/busy information.</span></span> <span data-ttu-id="26db7-110">Dieser Wert ist die Anzahl der Minuten seit dem 1. Januar 1601.</span><span class="sxs-lookup"><span data-stu-id="26db7-110">This value is the number of minutes since January 1, 1601.</span></span>
    
<span data-ttu-id="26db7-111">_prtmEnd_</span><span class="sxs-lookup"><span data-stu-id="26db7-111">_prtmEnd_</span></span>
  
> <span data-ttu-id="26db7-112">[out] Ein relativer Zeitwert für das Ende von Frei/Gebucht-Informationen.</span><span class="sxs-lookup"><span data-stu-id="26db7-112">[out] A relative time value for the end of free/busy information.</span></span> <span data-ttu-id="26db7-113">Dieser Wert ist die Anzahl der Minuten seit dem 1. Januar 1601.</span><span class="sxs-lookup"><span data-stu-id="26db7-113">This value is the number of minutes since January 1, 1601.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="26db7-114">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="26db7-114">Return values</span></span>

<span data-ttu-id="26db7-115">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="26db7-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="26db7-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="26db7-116">Remarks</span></span>

<span data-ttu-id="26db7-117">Ein Frei/Gebucht-Anbieter ruft [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) oder [IFreeBusyData::SetFBRange auf,](ifreebusydata-setfbrange.md) um den Zeitbereich für eine Enumeration zu festlegen.</span><span class="sxs-lookup"><span data-stu-id="26db7-117">A free/busy provider calls [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) or [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) to set the time range for an enumeration.</span></span> <span data-ttu-id="26db7-118">Wenn [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) oder [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) nicht aufgerufen wurde, müssen die Standardwerte für **prtmStart** und **prtmEnd** zwischen dem 1. April 1601 00:00:00Z und dem 31. August 4500 11:59:59Z festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="26db7-118">If either [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) or [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) has not been called, the default values for **prtmStart** and **prtmEnd** must be set between April 1st, 1601 00:00:00Z and August 31, 4500 11:59:59Z respectively.</span></span> <span data-ttu-id="26db7-119">Darüber hinaus sollten Sie die Startzeit nicht auf größer als die Endzeit festlegen.</span><span class="sxs-lookup"><span data-stu-id="26db7-119">Additionally, you should not set the start time to be greater than the end time.</span></span> 
  
<span data-ttu-id="26db7-120">**IFreeBusyData::GetFBPublishRange** muss die zwischengespeicherten Werte für den Zeitraum zurückgeben, der durch den letzten Aufruf für **IFreeBusyData::EnumBlocks** oder **IFreeBusyData::SetFBRange** festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="26db7-120">**IFreeBusyData::GetFBPublishRange** must return the cached values for the time range set by the most recent call for **IFreeBusyData::EnumBlocks** or **IFreeBusyData::SetFBRange**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="26db7-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26db7-121">See also</span></span>

- [<span data-ttu-id="26db7-122">Verwenden von relativer Zeit zum Zugriff auf Frei/Gebucht-Daten</span><span class="sxs-lookup"><span data-stu-id="26db7-122">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)
- [<span data-ttu-id="26db7-123">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="26db7-123">IFreeBusyData::EnumBlocks</span></span>](ifreebusydata-enumblocks.md)
- [<span data-ttu-id="26db7-124">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="26db7-124">IFreeBusyData::SetFBRange</span></span>](ifreebusydata-setfbrange.md)

