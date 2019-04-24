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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319404"
---
# <a name="ifreebusysupportloadfreebusydata"></a><span data-ttu-id="3fd87-103">IFreeBusySupport::LoadFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="3fd87-103">IFreeBusySupport::LoadFreeBusyData</span></span>

<span data-ttu-id="3fd87-104">Gibt für jeden angegebenen Benutzer eine Schnittstelle zum Auflisten von Frei/Gebucht-Datenblöcken innerhalb eines Zeitintervalls zurück.</span><span class="sxs-lookup"><span data-stu-id="3fd87-104">Returns, for each specified user, an interface for enumerating free/busy blocks of data within a time range.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="3fd87-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="3fd87-105">Quick info</span></span>

<span data-ttu-id="3fd87-106">Siehe [IFreeBusySupport](ifreebusysupport.md).</span><span class="sxs-lookup"><span data-stu-id="3fd87-106">See [IFreeBusySupport](ifreebusysupport.md).</span></span>
  
```cpp
HRESULT LoadFreeBusyData( 
    ULONG cMax,  
    FBUser *rgfbuser, 
    IFreeBusyData **prgfbdata,  
    HRESULT *phrStatus, 
    ULONG *pcRead 
);
```

## <a name="parameters"></a><span data-ttu-id="3fd87-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3fd87-107">Parameters</span></span>

<span data-ttu-id="3fd87-108">_cMax_</span><span class="sxs-lookup"><span data-stu-id="3fd87-108">_cMax_</span></span>
  
> <span data-ttu-id="3fd87-109">in Die Anzahl der [IFreeBusyData](ifreebusydata.md) -Schnittstellen, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3fd87-109">[in] The number of [IFreeBusyData](ifreebusydata.md) interfaces to return.</span></span> 
    
<span data-ttu-id="3fd87-110">_rgfbuser_</span><span class="sxs-lookup"><span data-stu-id="3fd87-110">_rgfbuser_</span></span>
  
> <span data-ttu-id="3fd87-111">in Das Array der frei/gebucht-Benutzer, für das Daten abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3fd87-111">[in] The array of free/busy users to retrieve data for.</span></span>
    
<span data-ttu-id="3fd87-112">_prgfbdata_</span><span class="sxs-lookup"><span data-stu-id="3fd87-112">_prgfbdata_</span></span>
  
> <span data-ttu-id="3fd87-113">in Out Das Array der **IFreeBusyData** -Schnittstellen, die dem _rgfbuser_ -Array von [FBUser](fbuser.md) -Strukturen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3fd87-113">[in][out] The array of **IFreeBusyData** interfaces that correspond to the  _rgfbuser_ array of [FBUser](fbuser.md) structures.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="3fd87-114">Dieses Array von Zeigern wird vom Aufrufer zugewiesen und vom Aufrufer freigegeben.</span><span class="sxs-lookup"><span data-stu-id="3fd87-114">This array of pointers is allocated by the caller and freed by the caller.</span></span> <span data-ttu-id="3fd87-115">Die tatsächlichen Schnittstellen, auf die verwiesen wird, werden freigegeben, wenn der Aufrufer mit Ihnen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3fd87-115">The actual interfaces pointed to are released when the caller is done with them.</span></span> 
  
<span data-ttu-id="3fd87-116">_phrStatus_</span><span class="sxs-lookup"><span data-stu-id="3fd87-116">_phrStatus_</span></span>
  
> <span data-ttu-id="3fd87-117">Out Das Array der **HRESULT** -Ergebnisse zum Abrufen der jeweiligen **IFreeBusyData** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3fd87-117">[out] The array of **HRESULT** results for retrieving each corresponding **IFreeBusyData** interface.</span></span> <span data-ttu-id="3fd87-118">Der Wert kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="3fd87-118">The value may be NULL.</span></span> <span data-ttu-id="3fd87-119">Ein Ergebnis wird auf S_OK festgelegt, wenn die entsprechende _prgfbdata_ gültig ist.</span><span class="sxs-lookup"><span data-stu-id="3fd87-119">A result is set to S_OK if corresponding  _prgfbdata_ is valid.</span></span> 
    
<span data-ttu-id="3fd87-120">_pcRead_</span><span class="sxs-lookup"><span data-stu-id="3fd87-120">_pcRead_</span></span>
  
>  <span data-ttu-id="3fd87-121">Out Die tatsächliche Anzahl von Benutzern, für die eine **IFreeBusyData** -Schnittstelle gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="3fd87-121">[out] The actual number of users for which an **IFreeBusyData** interface has been found.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="3fd87-122">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="3fd87-122">Return values</span></span>

<span data-ttu-id="3fd87-123">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="3fd87-123">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3fd87-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3fd87-124">See also</span></span>

- [<span data-ttu-id="3fd87-125">Konstanten (frei/gebucht-API)</span><span class="sxs-lookup"><span data-stu-id="3fd87-125">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)

