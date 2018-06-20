---
title: IFreeBusyDataEnumBlocks
manager: soliver
ms.date: 02/18/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cd5a5ae-118f-c7da-4eda-e97590fc39d4
description: Ruft eine Schnittstelle, die Datenblöcke Frei/Gebucht-Informationen für einen Benutzer in einen angegebenen Zeitraum auflistet.
ms.openlocfilehash: ab377b1029296b6b4bac68d7169dcf7b8dcd8b87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790965"
---
# <a name="ifreebusydataenumblocks"></a><span data-ttu-id="afd89-103">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="afd89-103">IFreeBusyData::EnumBlocks</span></span>

<span data-ttu-id="afd89-104">Ruft eine Schnittstelle, die Datenblöcke Frei/Gebucht-Informationen für einen Benutzer in einen angegebenen Zeitraum auflistet.</span><span class="sxs-lookup"><span data-stu-id="afd89-104">Gets an interface that enumerates free/busy blocks of data for a user within a specified time range.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="afd89-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="afd89-105">Quick info</span></span>

<span data-ttu-id="afd89-106">Finden Sie unter [IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="afd89-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT EnumBlocks( 
     IEnumFBBlock **ppenumfb,  
     FILETIME ftmStart, 
     FILETIME ftmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="afd89-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="afd89-107">Parameters</span></span>

<span data-ttu-id="afd89-108">_ppenumfb_</span><span class="sxs-lookup"><span data-stu-id="afd89-108">_ppenumfb_</span></span>
  
> <span data-ttu-id="afd89-109">[out] Eine Schnittstelle zum Aufzählen von Frei/Gebucht-Blöcke.</span><span class="sxs-lookup"><span data-stu-id="afd89-109">[out] An interface to enumerate free/busy blocks.</span></span>
    
<span data-ttu-id="afd89-110">_ftmStart_</span><span class="sxs-lookup"><span data-stu-id="afd89-110">_ftmStart_</span></span>
  
> <span data-ttu-id="afd89-111">[in] Die Startzeit für die Enumeration.</span><span class="sxs-lookup"><span data-stu-id="afd89-111">[in] The start time for the enumeration.</span></span> <span data-ttu-id="afd89-112">Es wird in [FILETIME](http://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx)ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="afd89-112">It is expressed in [FILETIME](http://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx).</span></span>
    
<span data-ttu-id="afd89-113">_ftmEnd_</span><span class="sxs-lookup"><span data-stu-id="afd89-113">_ftmEnd_</span></span>
  
> <span data-ttu-id="afd89-114">[in] Die Endzeit für die Enumeration.</span><span class="sxs-lookup"><span data-stu-id="afd89-114">[in] The end time for the enumeration.</span></span> <span data-ttu-id="afd89-115">Es wird in **FILETIME**ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="afd89-115">It is expressed in **FILETIME**.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="afd89-116">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="afd89-116">Return values</span></span>

<span data-ttu-id="afd89-117">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="afd89-117">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="afd89-118">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="afd89-118">Remarks</span></span>

<span data-ttu-id="afd89-119">Diese Methode wird verwendet, um den Zeitbereich des Kalenderelemente für das Abrufen von Details anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="afd89-119">This method is used to indicate the time range of calendar items for which to retrieve details.</span></span> <span data-ttu-id="afd89-120">Die Werte der *FtmStart* und *FtmEnd* werden zwischengespeichert und in einem nachfolgenden Aufruf der [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="afd89-120">The values of  *ftmStart* and *ftmEnd* are cached and returned in a subsequent call of [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span></span>
  
<span data-ttu-id="afd89-121">Ein Anbieter Frei/Gebucht-Informationen kann auch anschließend die zurückgegebene [IEnumFBBlock](ienumfbblock.md) -Schnittstelle verwenden, um Zugriff auf die-Aufzählung.</span><span class="sxs-lookup"><span data-stu-id="afd89-121">A free/busy provider can also subsequently use the returned [IEnumFBBlock](ienumfbblock.md) interface to access the enumeration.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="afd89-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="afd89-122">See also</span></span>

- [<span data-ttu-id="afd89-123">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="afd89-123">IEnumFBBlock</span></span>](ienumfbblock.md)
- [<span data-ttu-id="afd89-124">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="afd89-124">IFreeBusyData::GetFBPublishRange</span></span>](ifreebusydata-getfbpublishrange.md)
- [<span data-ttu-id="afd89-125">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="afd89-125">IFreeBusyData::SetFBRange</span></span>](ifreebusydata-setfbrange.md)
- [<span data-ttu-id="afd89-126">Verwenden Sie relative Zeit Zugriff auf Frei/Gebucht-Daten</span><span class="sxs-lookup"><span data-stu-id="afd89-126">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

