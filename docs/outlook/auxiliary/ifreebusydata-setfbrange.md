---
title: IFreeBusyDataSetFBRange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e7147ea-0eb0-324a-80d8-4f0eef654c32
description: Legt den Zeitraum für eine Aufzählung von Frei/Gebucht-Datenblöcken für einen Benutzer fest.
ms.openlocfilehash: 4647453acb0e530521aa808f7f017e3e311644bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421662"
---
# <a name="ifreebusydatasetfbrange"></a><span data-ttu-id="fe624-103">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="fe624-103">IFreeBusyData::SetFBRange</span></span>

<span data-ttu-id="fe624-104">Legt den Zeitraum für eine Aufzählung von Frei/Gebucht-Datenblöcken für einen Benutzer fest.</span><span class="sxs-lookup"><span data-stu-id="fe624-104">Sets the range of time for an enumeration of free/busy blocks of data for a user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="fe624-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="fe624-105">Quick info</span></span>

<span data-ttu-id="fe624-106">Weitere [Informationen finden Sie unter IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="fe624-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT SetFBRange(
     LONG rtmStart,
     LONG rtmEnd
);
```

## <a name="parameters"></a><span data-ttu-id="fe624-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe624-107">Parameters</span></span>

<span data-ttu-id="fe624-108">_rtmStart_</span><span class="sxs-lookup"><span data-stu-id="fe624-108">_rtmStart_</span></span>
  
> <span data-ttu-id="fe624-109">[in] Ein relativer Zeitwert für den Anfang von Frei/Gebucht-Informationen.</span><span class="sxs-lookup"><span data-stu-id="fe624-109">[in] A relative time value for the start of free/busy information.</span></span> <span data-ttu-id="fe624-110">Dieser Wert ist die Anzahl der Minuten seit dem 1. Januar 1601.</span><span class="sxs-lookup"><span data-stu-id="fe624-110">This value is the number of minutes since January 1, 1601.</span></span>
    
<span data-ttu-id="fe624-111">_rtmEnd_</span><span class="sxs-lookup"><span data-stu-id="fe624-111">_rtmEnd_</span></span>
  
> <span data-ttu-id="fe624-112">[in] Ein relativer Zeitwert für das Ende von Frei/Gebucht-Informationen.</span><span class="sxs-lookup"><span data-stu-id="fe624-112">[in] A relative time value for the end of free/busy information.</span></span> <span data-ttu-id="fe624-113">Dieser Wert ist die Anzahl der Minuten seit dem 1. Januar 1601.</span><span class="sxs-lookup"><span data-stu-id="fe624-113">This value is the number of minutes since January 1, 1601.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="fe624-114">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="fe624-114">Return values</span></span>

<span data-ttu-id="fe624-115">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="fe624-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fe624-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fe624-116">Remarks</span></span>

<span data-ttu-id="fe624-117">Diese Methode wird verwendet, um den Zeitraum der Kalenderelemente anzugeben, für die Details abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="fe624-117">This method is used to indicate the time range of calendar items for which to retrieve details.</span></span> <span data-ttu-id="fe624-118">Die Werte *von ftmStart* und *ftmEnd* werden zwischengespeichert und in einem nachfolgenden Aufruf von [IFreeBusyData::GetFBPublishRange zurückgegeben.](ifreebusydata-getfbpublishrange.md)</span><span class="sxs-lookup"><span data-stu-id="fe624-118">The values of  *ftmStart*  and  *ftmEnd*  are cached and returned in a subsequent call of [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fe624-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe624-119">See also</span></span>

- [<span data-ttu-id="fe624-120">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="fe624-120">IFreeBusyData::EnumBlocks</span></span>](ifreebusydata-enumblocks.md)
- [<span data-ttu-id="fe624-121">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="fe624-121">IFreeBusyData::GetFBPublishRange</span></span>](ifreebusydata-getfbpublishrange.md)
- [<span data-ttu-id="fe624-122">Verwenden von relativer Zeit zum Zugriff auf Frei/Gebucht-Daten</span><span class="sxs-lookup"><span data-stu-id="fe624-122">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

