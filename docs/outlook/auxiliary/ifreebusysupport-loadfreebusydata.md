---
title: IFreeBusySupportLoadFreeBusyData
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: Gibt für jeden angegebenen Benutzer, eine Schnittstelle zum Aufzählen Datenblöcke Frei/Gebucht-Informationen innerhalb eines Zeitraums.
ms.openlocfilehash: 9af5a40da9f0a831de7346b44cee9ca004c02300
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790963"
---
# <a name="ifreebusysupportloadfreebusydata"></a><span data-ttu-id="55cf9-103">IFreeBusySupport::LoadFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="55cf9-103">IFreeBusySupport::LoadFreeBusyData</span></span>

<span data-ttu-id="55cf9-104">Gibt für jeden angegebenen Benutzer, eine Schnittstelle zum Aufzählen Datenblöcke Frei/Gebucht-Informationen innerhalb eines Zeitraums.</span><span class="sxs-lookup"><span data-stu-id="55cf9-104">Returns, for each specified user, an interface for enumerating free/busy blocks of data within a time range.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="55cf9-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="55cf9-105">Quick info</span></span>

<span data-ttu-id="55cf9-106">Finden Sie unter [IFreeBusySupport](ifreebusysupport.md).</span><span class="sxs-lookup"><span data-stu-id="55cf9-106">See [IFreeBusySupport](ifreebusysupport.md).</span></span>
  
```cpp
HRESULT LoadFreeBusyData( 
    ULONG cMax,  
    FBUser *rgfbuser, 
    IFreeBusyData **prgfbdata,  
    HRESULT *phrStatus, 
    ULONG *pcRead 
);
```

## <a name="parameters"></a><span data-ttu-id="55cf9-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="55cf9-107">Parameters</span></span>

<span data-ttu-id="55cf9-108">_cMax_</span><span class="sxs-lookup"><span data-stu-id="55cf9-108">_cMax_</span></span>
  
> <span data-ttu-id="55cf9-109">[in] Die Anzahl der zurückzugebenden [IFreeBusyData](ifreebusydata.md) -Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="55cf9-109">[in] The number of [IFreeBusyData](ifreebusydata.md) interfaces to return.</span></span> 
    
<span data-ttu-id="55cf9-110">_rgfbuser_</span><span class="sxs-lookup"><span data-stu-id="55cf9-110">_rgfbuser_</span></span>
  
> <span data-ttu-id="55cf9-111">[in] Das Array von Frei/Gebucht-Informationen abrufen von Daten für Benutzer.</span><span class="sxs-lookup"><span data-stu-id="55cf9-111">[in] The array of free/busy users to retrieve data for.</span></span>
    
<span data-ttu-id="55cf9-112">_prgfbdata_</span><span class="sxs-lookup"><span data-stu-id="55cf9-112">_prgfbdata_</span></span>
  
> <span data-ttu-id="55cf9-113">[in] [out] Das Array von **IFreeBusyData** -Schnittstellen, die das _Rgfbuser_ Array von [FBUser](fbuser.md) Strukturen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="55cf9-113">[in][out] The array of **IFreeBusyData** interfaces that correspond to the  _rgfbuser_ array of [FBUser](fbuser.md) structures.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="55cf9-114">Dieses Array von Zeigern wird vom Anrufer belegt und vom Anrufer freigegeben.</span><span class="sxs-lookup"><span data-stu-id="55cf9-114">This array of pointers is allocated by the caller and freed by the caller.</span></span> <span data-ttu-id="55cf9-115">Die tatsächlichen Schnittstellen auf den verwiesen werden freigegeben, wenn der Aufrufer diese nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="55cf9-115">The actual interfaces pointed to are released when the caller is done with them.</span></span> 
  
<span data-ttu-id="55cf9-116">_phrStatus_</span><span class="sxs-lookup"><span data-stu-id="55cf9-116">_phrStatus_</span></span>
  
> <span data-ttu-id="55cf9-117">[out] Das Array von **HRESULT** -Ergebnisse für jede entsprechende **IFreeBusyData** -Schnittstelle abrufen.</span><span class="sxs-lookup"><span data-stu-id="55cf9-117">[out] The array of **HRESULT** results for retrieving each corresponding **IFreeBusyData** interface.</span></span> <span data-ttu-id="55cf9-118">Der Wert kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="55cf9-118">The value may be NULL.</span></span> <span data-ttu-id="55cf9-119">Ein Ergebnis wird auf S_OK festgelegt, wenn die entsprechenden _Prgfbdata_ gültig ist.</span><span class="sxs-lookup"><span data-stu-id="55cf9-119">A result is set to S_OK if corresponding  _prgfbdata_ is valid.</span></span> 
    
<span data-ttu-id="55cf9-120">_pcRead_</span><span class="sxs-lookup"><span data-stu-id="55cf9-120">_pcRead_</span></span>
  
>  <span data-ttu-id="55cf9-121">[out] Die tatsächliche Anzahl von Benutzern für die eine **IFreeBusyData** Schnittstelle gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="55cf9-121">[out] The actual number of users for which an **IFreeBusyData** interface has been found.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="55cf9-122">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="55cf9-122">Return values</span></span>

<span data-ttu-id="55cf9-123">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="55cf9-123">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="55cf9-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55cf9-124">See also</span></span>

- [<span data-ttu-id="55cf9-125">Konstanten (Frei/Gebucht-API)</span><span class="sxs-lookup"><span data-stu-id="55cf9-125">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)

