---
title: IFreeBusySupportLoadFreeBusyData
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: Gibt für jeden angegebenen Benutzer eine Schnittstelle zum Aufzählen von Frei/Gebucht-Datenblöcken innerhalb eines Zeitbereichs zurück.
ms.openlocfilehash: e55f902117a20bfefaa5d9a2f3a067cb78ec86cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411232"
---
# <a name="ifreebusysupportloadfreebusydata"></a><span data-ttu-id="23d73-103">IFreeBusySupport::LoadFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="23d73-103">IFreeBusySupport::LoadFreeBusyData</span></span>

<span data-ttu-id="23d73-104">Gibt für jeden angegebenen Benutzer eine Schnittstelle zum Aufzählen von Frei/Gebucht-Datenblöcken innerhalb eines Zeitbereichs zurück.</span><span class="sxs-lookup"><span data-stu-id="23d73-104">Returns, for each specified user, an interface for enumerating free/busy blocks of data within a time range.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="23d73-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="23d73-105">Quick info</span></span>

<span data-ttu-id="23d73-106">Weitere [Informationen finden Sie unter IFreeBusySupport](ifreebusysupport.md).</span><span class="sxs-lookup"><span data-stu-id="23d73-106">See [IFreeBusySupport](ifreebusysupport.md).</span></span>
  
```cpp
HRESULT LoadFreeBusyData( 
    ULONG cMax,  
    FBUser *rgfbuser, 
    IFreeBusyData **prgfbdata,  
    HRESULT *phrStatus, 
    ULONG *pcRead 
);
```

## <a name="parameters"></a><span data-ttu-id="23d73-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="23d73-107">Parameters</span></span>

<span data-ttu-id="23d73-108">_cMax_</span><span class="sxs-lookup"><span data-stu-id="23d73-108">_cMax_</span></span>
  
> <span data-ttu-id="23d73-109">[in] Die Anzahl der [zurückzukehrende IFreeBusyData-Schnittstellen.](ifreebusydata.md)</span><span class="sxs-lookup"><span data-stu-id="23d73-109">[in] The number of [IFreeBusyData](ifreebusydata.md) interfaces to return.</span></span> 
    
<span data-ttu-id="23d73-110">_rgfbuser_</span><span class="sxs-lookup"><span data-stu-id="23d73-110">_rgfbuser_</span></span>
  
> <span data-ttu-id="23d73-111">[in] Das Array der Frei/Gebucht-Benutzer, für die Daten abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="23d73-111">[in] The array of free/busy users to retrieve data for.</span></span>
    
<span data-ttu-id="23d73-112">_prgfbdata_</span><span class="sxs-lookup"><span data-stu-id="23d73-112">_prgfbdata_</span></span>
  
> <span data-ttu-id="23d73-113">[in] [out] Das Array von **IFreeBusyData-Schnittstellen,** die dem  _rgfbuser-Array_ von [FBUser-Strukturen](fbuser.md) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="23d73-113">[in][out] The array of **IFreeBusyData** interfaces that correspond to the  _rgfbuser_ array of [FBUser](fbuser.md) structures.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="23d73-114">Dieses Array von Zeigern wird vom Anrufer zugewiesen und vom Anrufer frei.</span><span class="sxs-lookup"><span data-stu-id="23d73-114">This array of pointers is allocated by the caller and freed by the caller.</span></span> <span data-ttu-id="23d73-115">Die tatsächlichen Schnittstellen, auf die verwiesen wird, werden freigegeben, wenn der Aufrufer damit fertig ist.</span><span class="sxs-lookup"><span data-stu-id="23d73-115">The actual interfaces pointed to are released when the caller is done with them.</span></span> 
  
<span data-ttu-id="23d73-116">_phrStatus_</span><span class="sxs-lookup"><span data-stu-id="23d73-116">_phrStatus_</span></span>
  
> <span data-ttu-id="23d73-117">[out] Das Array von **HRESULT-Ergebnissen** zum Abrufen jeder entsprechenden **IFreeBusyData-Schnittstelle.**</span><span class="sxs-lookup"><span data-stu-id="23d73-117">[out] The array of **HRESULT** results for retrieving each corresponding **IFreeBusyData** interface.</span></span> <span data-ttu-id="23d73-118">Der Wert kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="23d73-118">The value may be NULL.</span></span> <span data-ttu-id="23d73-119">Ein Ergebnis wird auf S_OK festgelegt, wenn  _entsprechende prgfbdata_ gültig ist.</span><span class="sxs-lookup"><span data-stu-id="23d73-119">A result is set to S_OK if corresponding  _prgfbdata_ is valid.</span></span> 
    
<span data-ttu-id="23d73-120">_pcRead_</span><span class="sxs-lookup"><span data-stu-id="23d73-120">_pcRead_</span></span>
  
>  <span data-ttu-id="23d73-121">[out] Die tatsächliche Anzahl von Benutzern, für die eine **IFreeBusyData-Schnittstelle** gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="23d73-121">[out] The actual number of users for which an **IFreeBusyData** interface has been found.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="23d73-122">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="23d73-122">Return values</span></span>

<span data-ttu-id="23d73-123">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="23d73-123">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="23d73-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23d73-124">See also</span></span>

- [<span data-ttu-id="23d73-125">Konstanten (Frei/Gebucht-API)</span><span class="sxs-lookup"><span data-stu-id="23d73-125">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)

