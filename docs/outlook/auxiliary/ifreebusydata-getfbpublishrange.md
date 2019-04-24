---
title: IFreeBusyDataGetFBPublishRange
manager: soliver
ms.date: 09/23/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a8bbe0c-17d1-9349-4c63-f257faf4edda
description: Ruft einen vordefinierten Zeitraum für eine Enumeration von Frei/Gebucht-Datenblöcken für einen Benutzer ab.
ms.openlocfilehash: 26951ea6a885f8d0e5e6a2fb5bcf9a63069c7f44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317528"
---
# <a name="ifreebusydatagetfbpublishrange"></a><span data-ttu-id="dde36-103">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="dde36-103">IFreeBusyData::GetFBPublishRange</span></span>

<span data-ttu-id="dde36-104">Ruft einen vordefinierten Zeitraum für eine Enumeration von Frei/Gebucht-Datenblöcken für einen Benutzer ab.</span><span class="sxs-lookup"><span data-stu-id="dde36-104">Gets a preset time range for an enumeration of free/busy blocks of data for a user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="dde36-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="dde36-105">Quick info</span></span>

<span data-ttu-id="dde36-106">Siehe [IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="dde36-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT GetFBPublishRange( 
     LONG *prtmStart,  
     LONG *prtmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="dde36-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="dde36-107">Parameters</span></span>

<span data-ttu-id="dde36-108">_prtmStart_</span><span class="sxs-lookup"><span data-stu-id="dde36-108">_prtmStart_</span></span>
  
> <span data-ttu-id="dde36-109">Out Ein relativer Zeitwert für den Beginn der Frei/Gebucht-Informationen.</span><span class="sxs-lookup"><span data-stu-id="dde36-109">[out] A relative time value for the start of free/busy information.</span></span> <span data-ttu-id="dde36-110">Dieser Wert ist die Anzahl der Minuten seit dem 1. Januar 1601.</span><span class="sxs-lookup"><span data-stu-id="dde36-110">This value is the number of minutes since January 1, 1601.</span></span>
    
<span data-ttu-id="dde36-111">_prtmEnd_</span><span class="sxs-lookup"><span data-stu-id="dde36-111">_prtmEnd_</span></span>
  
> <span data-ttu-id="dde36-112">Out Ein relativer Zeitwert für das Ende der Frei/Gebucht-Informationen.</span><span class="sxs-lookup"><span data-stu-id="dde36-112">[out] A relative time value for the end of free/busy information.</span></span> <span data-ttu-id="dde36-113">Dieser Wert ist die Anzahl der Minuten seit dem 1. Januar 1601.</span><span class="sxs-lookup"><span data-stu-id="dde36-113">This value is the number of minutes since January 1, 1601.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="dde36-114">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="dde36-114">Return values</span></span>

<span data-ttu-id="dde36-115">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="dde36-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dde36-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dde36-116">Remarks</span></span>

<span data-ttu-id="dde36-117">Ein frei/gebucht-Anbieter ruft [IFreeBusyData:: EnumBlocks](ifreebusydata-enumblocks.md) oder [IFreeBusyData:: SetFBRange](ifreebusydata-setfbrange.md) auf, um den Zeitintervall für eine Enumeration festzulegen.</span><span class="sxs-lookup"><span data-stu-id="dde36-117">A free/busy provider calls [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) or [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) to set the time range for an enumeration.</span></span> <span data-ttu-id="dde36-118">Wenn entweder [IFreeBusyData:: EnumBlocks](ifreebusydata-enumblocks.md) oder [IFreeBusyData:: SetFBRange](ifreebusydata-setfbrange.md) nicht aufgerufen wurde, müssen die Standardwerte für **prtmStart** und **prtmEnd** zwischen dem 1. April 1601 00:00:00Z und dem 31. August 4500:59Z jeweils.</span><span class="sxs-lookup"><span data-stu-id="dde36-118">If either [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) or [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) has not been called, the default values for **prtmStart** and **prtmEnd** must be set between April 1st, 1601 00:00:00Z and August 31, 4500 11:59:59Z respectively.</span></span> <span data-ttu-id="dde36-119">Darüber hinaus sollten Sie die Startzeit nicht größer als die Endzeit festlegen.</span><span class="sxs-lookup"><span data-stu-id="dde36-119">Additionally, you should not set the start time to be greater than the end time.</span></span> 
  
<span data-ttu-id="dde36-120">**IFreeBusyData:: GetFBPublishRange** muss die zwischengespeicherten Werte für den Zeitraum zurückgeben, der durch den letzten Aufruf für **IFreeBusyData:: EnumBlocks** oder **IFreeBusyData:: SetFBRange**festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="dde36-120">**IFreeBusyData::GetFBPublishRange** must return the cached values for the time range set by the most recent call for **IFreeBusyData::EnumBlocks** or **IFreeBusyData::SetFBRange**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dde36-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dde36-121">See also</span></span>

- [<span data-ttu-id="dde36-122">Verwenden von relativer Zeit zum Zugriff auf Frei/Gebucht-Daten</span><span class="sxs-lookup"><span data-stu-id="dde36-122">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)
- [<span data-ttu-id="dde36-123">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="dde36-123">IFreeBusyData::EnumBlocks</span></span>](ifreebusydata-enumblocks.md)
- [<span data-ttu-id="dde36-124">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="dde36-124">IFreeBusyData::SetFBRange</span></span>](ifreebusydata-setfbrange.md)

