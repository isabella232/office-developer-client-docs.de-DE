---
title: IFreeBusyDataSetFBRange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e7147ea-0eb0-324a-80d8-4f0eef654c32
description: Legt die Zeitspanne für eine Enumeration der Datenblöcke Frei/Gebucht-Informationen für einen Benutzer fest.
ms.openlocfilehash: 84a25a2dd43f594caa075d90e4f183086452184a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790978"
---
# <a name="ifreebusydatasetfbrange"></a><span data-ttu-id="47828-103">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="47828-103">IFreeBusyData::SetFBRange</span></span>

<span data-ttu-id="47828-104">Legt die Zeitspanne für eine Enumeration der Datenblöcke Frei/Gebucht-Informationen für einen Benutzer fest.</span><span class="sxs-lookup"><span data-stu-id="47828-104">Sets the range of time for an enumeration of free/busy blocks of data for a user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="47828-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="47828-105">Quick info</span></span>

<span data-ttu-id="47828-106">Finden Sie unter [IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="47828-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT SetFBRange(
     LONG rtmStart,
     LONG rtmEnd
);
```

## <a name="parameters"></a><span data-ttu-id="47828-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="47828-107">Parameters</span></span>

<span data-ttu-id="47828-108">_rtmStart_</span><span class="sxs-lookup"><span data-stu-id="47828-108">_rtmStart_</span></span>
  
> <span data-ttu-id="47828-109">[in] Ein relative Zeitwert für den Anfang des Frei/Gebucht-Informationen.</span><span class="sxs-lookup"><span data-stu-id="47828-109">[in] A relative time value for the start of free/busy information.</span></span> <span data-ttu-id="47828-110">Dieser Wert ist die Anzahl der Minuten seit dem 1. Januar 1601.</span><span class="sxs-lookup"><span data-stu-id="47828-110">This value is the number of minutes since January 1, 1601.</span></span>
    
<span data-ttu-id="47828-111">_rtmEnd_</span><span class="sxs-lookup"><span data-stu-id="47828-111">_rtmEnd_</span></span>
  
> <span data-ttu-id="47828-112">[in] Ein relative Zeitwert für das Ende des Frei/Gebucht-Informationen.</span><span class="sxs-lookup"><span data-stu-id="47828-112">[in] A relative time value for the end of free/busy information.</span></span> <span data-ttu-id="47828-113">Dieser Wert ist die Anzahl der Minuten seit dem 1. Januar 1601.</span><span class="sxs-lookup"><span data-stu-id="47828-113">This value is the number of minutes since January 1, 1601.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="47828-114">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="47828-114">Return values</span></span>

<span data-ttu-id="47828-115">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="47828-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="47828-116">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="47828-116">Remarks</span></span>

<span data-ttu-id="47828-117">Diese Methode wird verwendet, um den Zeitbereich des Kalenderelemente für das Abrufen von Details anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="47828-117">This method is used to indicate the time range of calendar items for which to retrieve details.</span></span> <span data-ttu-id="47828-118">Die Werte der *FtmStart* und *FtmEnd* werden zwischengespeichert und in einem nachfolgenden Aufruf der [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="47828-118">The values of  *ftmStart*  and  *ftmEnd*  are cached and returned in a subsequent call of [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="47828-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47828-119">See also</span></span>

- [<span data-ttu-id="47828-120">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="47828-120">IFreeBusyData::EnumBlocks</span></span>](ifreebusydata-enumblocks.md)
- [<span data-ttu-id="47828-121">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="47828-121">IFreeBusyData::GetFBPublishRange</span></span>](ifreebusydata-getfbpublishrange.md)
- [<span data-ttu-id="47828-122">Verwenden von relativer Zeit zum Zugriff auf Frei/Gebucht-Daten</span><span class="sxs-lookup"><span data-stu-id="47828-122">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

