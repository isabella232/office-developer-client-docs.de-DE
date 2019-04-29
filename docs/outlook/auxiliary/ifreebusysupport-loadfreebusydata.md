---
title: IFreeBusySupportLoadFreeBusyData
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: Gibt für jeden angegebenen Benutzer eine Schnittstelle zum Auflisten von Frei/Gebucht-Datenblöcken innerhalb eines Zeitintervalls zurück.
ms.openlocfilehash: e55f902117a20bfefaa5d9a2f3a067cb78ec86cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411232"
---
# <a name="ifreebusysupportloadfreebusydata"></a><span data-ttu-id="e7cd8-103">IFreeBusySupport::LoadFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="e7cd8-103">IFreeBusySupport::LoadFreeBusyData</span></span>

<span data-ttu-id="e7cd8-104">Gibt für jeden angegebenen Benutzer eine Schnittstelle zum Auflisten von Frei/Gebucht-Datenblöcken innerhalb eines Zeitintervalls zurück.</span><span class="sxs-lookup"><span data-stu-id="e7cd8-104">Returns, for each specified user, an interface for enumerating free/busy blocks of data within a time range.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="e7cd8-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="e7cd8-105">Quick info</span></span>

<span data-ttu-id="e7cd8-106">Siehe [IFreeBusySupport](ifreebusysupport.md).</span><span class="sxs-lookup"><span data-stu-id="e7cd8-106">See [IFreeBusySupport](ifreebusysupport.md).</span></span>
  
```cpp
HRESULT LoadFreeBusyData( 
    ULONG cMax,  
    FBUser *rgfbuser, 
    IFreeBusyData **prgfbdata,  
    HRESULT *phrStatus, 
    ULONG *pcRead 
);
```

## <a name="parameters"></a><span data-ttu-id="e7cd8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7cd8-107">Parameters</span></span>

<span data-ttu-id="e7cd8-108">_cMax_</span><span class="sxs-lookup"><span data-stu-id="e7cd8-108">_cMax_</span></span>
  
> <span data-ttu-id="e7cd8-109">in Die Anzahl der [IFreeBusyData](ifreebusydata.md) -Schnittstellen, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e7cd8-109">[in] The number of [IFreeBusyData](ifreebusydata.md) interfaces to return.</span></span> 
    
<span data-ttu-id="e7cd8-110">_rgfbuser_</span><span class="sxs-lookup"><span data-stu-id="e7cd8-110">_rgfbuser_</span></span>
  
> <span data-ttu-id="e7cd8-111">in Das Array der frei/gebucht-Benutzer, für das Daten abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e7cd8-111">[in] The array of free/busy users to retrieve data for.</span></span>
    
<span data-ttu-id="e7cd8-112">_prgfbdata_</span><span class="sxs-lookup"><span data-stu-id="e7cd8-112">_prgfbdata_</span></span>
  
> <span data-ttu-id="e7cd8-113">in Out Das Array der **IFreeBusyData** -Schnittstellen, die dem _rgfbuser_ -Array von [FBUser](fbuser.md) -Strukturen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e7cd8-113">[in][out] The array of **IFreeBusyData** interfaces that correspond to the  _rgfbuser_ array of [FBUser](fbuser.md) structures.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="e7cd8-114">Dieses Array von Zeigern wird vom Aufrufer zugewiesen und vom Aufrufer freigegeben.</span><span class="sxs-lookup"><span data-stu-id="e7cd8-114">This array of pointers is allocated by the caller and freed by the caller.</span></span> <span data-ttu-id="e7cd8-115">Die tatsächlichen Schnittstellen, auf die verwiesen wird, werden freigegeben, wenn der Aufrufer mit Ihnen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e7cd8-115">The actual interfaces pointed to are released when the caller is done with them.</span></span> 
  
<span data-ttu-id="e7cd8-116">_phrStatus_</span><span class="sxs-lookup"><span data-stu-id="e7cd8-116">_phrStatus_</span></span>
  
> <span data-ttu-id="e7cd8-117">Out Das Array der **HRESULT** -Ergebnisse zum Abrufen der jeweiligen **IFreeBusyData** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e7cd8-117">[out] The array of **HRESULT** results for retrieving each corresponding **IFreeBusyData** interface.</span></span> <span data-ttu-id="e7cd8-118">Der Wert kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="e7cd8-118">The value may be NULL.</span></span> <span data-ttu-id="e7cd8-119">Ein Ergebnis wird auf S_OK festgelegt, wenn die entsprechende _prgfbdata_ gültig ist.</span><span class="sxs-lookup"><span data-stu-id="e7cd8-119">A result is set to S_OK if corresponding  _prgfbdata_ is valid.</span></span> 
    
<span data-ttu-id="e7cd8-120">_pcRead_</span><span class="sxs-lookup"><span data-stu-id="e7cd8-120">_pcRead_</span></span>
  
>  <span data-ttu-id="e7cd8-121">Out Die tatsächliche Anzahl von Benutzern, für die eine **IFreeBusyData** -Schnittstelle gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="e7cd8-121">[out] The actual number of users for which an **IFreeBusyData** interface has been found.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="e7cd8-122">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="e7cd8-122">Return values</span></span>

<span data-ttu-id="e7cd8-123">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="e7cd8-123">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e7cd8-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7cd8-124">See also</span></span>

- [<span data-ttu-id="e7cd8-125">Konstanten (frei/gebucht-API)</span><span class="sxs-lookup"><span data-stu-id="e7cd8-125">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)

