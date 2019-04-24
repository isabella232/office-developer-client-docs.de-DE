---
title: IAddrBookGetSearchPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetSearchPath
api_type:
- COM
ms.assetid: 43b51a66-71fa-4e10-93e4-d533b48af4de
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f8c129e772870804ef464765b2035a3582317a09
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341391"
---
# <a name="iaddrbookgetsearchpath"></a><span data-ttu-id="dae2a-103">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="dae2a-103">IAddrBook::GetSearchPath</span></span>

  
  
<span data-ttu-id="dae2a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dae2a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dae2a-105">Gibt eine sortierte Liste von Eintrags Bezeichnern der Container zurück, die in den von der [IAddrBook::](iaddrbook-resolvename.md) ResolveName-Methode initiierten namens Auflösungsprozess eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dae2a-105">Returns an ordered list of entry identifiers of the containers to be included in the name resolution process initiated by the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> 
  
```cpp
HRESULT GetSearchPath(
  ULONG ulFlags,
  LPSRowSet FAR * lppSearchPath
);
```

## <a name="parameters"></a><span data-ttu-id="dae2a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dae2a-106">Parameters</span></span>

 <span data-ttu-id="dae2a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dae2a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="dae2a-108">in Eine Bitmaske von Flags, die den Typ der im Suchpfad zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="dae2a-108">[in] A bitmask of flags that controls the type of the strings returned in the search path.</span></span> <span data-ttu-id="dae2a-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="dae2a-109">The following flag can be set:</span></span>
    
<span data-ttu-id="dae2a-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="dae2a-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="dae2a-111">Die zurückgegebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="dae2a-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="dae2a-112">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="dae2a-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="dae2a-113">_lppSearchPath_</span><span class="sxs-lookup"><span data-stu-id="dae2a-113">_lppSearchPath_</span></span>
  
> <span data-ttu-id="dae2a-114">Out Ein Zeiger auf einen Zeiger auf eine sortierte Liste von Container Eintrags-IDs.</span><span class="sxs-lookup"><span data-stu-id="dae2a-114">[out] A pointer to a pointer to an ordered list of container entry identifiers.</span></span> <span data-ttu-id="dae2a-115">**GetSearchPath** speichert die sortierte Liste in einer [SRowSet](srowset.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="dae2a-115">**GetSearchPath** stores the ordered list in an [SRowSet](srowset.md) structure.</span></span> <span data-ttu-id="dae2a-116">Wenn es in der Adressbuchhierarchie keine Container gibt, wird in der **SRowSet** -Struktur NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dae2a-116">If there are no containers in the address book hierarchy, zero is returned in the **SRowSet** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dae2a-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dae2a-117">Return value</span></span>

<span data-ttu-id="dae2a-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="dae2a-118">S_OK</span></span> 
  
> <span data-ttu-id="dae2a-119">Der Suchpfad wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="dae2a-119">The search path was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dae2a-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dae2a-120">Remarks</span></span>

<span data-ttu-id="dae2a-121">Clients und Dienstanbieter rufen die **GetSearchPath** -Methode auf, um den Suchpfad abzurufen, der zum Auflösen \*\*\*\* von Namen mit der ResolveName-Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dae2a-121">Clients and service providers call the **GetSearchPath** method to get the search path that is used to resolve names with the **ResolveName** method.</span></span> <span data-ttu-id="dae2a-122">In der Regel rufen Clients die [IAddrBook:: SetSearchPath](iaddrbook-setsearchpath.md) -Methode auf, um einen Container Suchpfad im Profil einzurichten, bevor Sie **GetSearchPath** aufrufen, um Sie abzurufen.</span><span class="sxs-lookup"><span data-stu-id="dae2a-122">Typically, clients call the [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) method to establish a container search path in the profile before they call **GetSearchPath** to retrieve it.</span></span> <span data-ttu-id="dae2a-123">Das Aufrufen von **SetSearchPath** ist jedoch optional.</span><span class="sxs-lookup"><span data-stu-id="dae2a-123">However, calling **SetSearchPath** is optional.</span></span> 
  
<span data-ttu-id="dae2a-124">Wenn **SetSearchPath** nie aufgerufen wurde, erstellt **GetSearchPath** einen Pfad, indem Sie die Hierarchietabellen des Adressbuches durcharbeiten.</span><span class="sxs-lookup"><span data-stu-id="dae2a-124">If **SetSearchPath** has never been called, **GetSearchPath** builds a path by working through the address book's hierarchy tables.</span></span> <span data-ttu-id="dae2a-125">Der von **GetSearchPath** eingerichtete Standardsuchpfad besteht aus den folgenden Containern in der folgenden Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="dae2a-125">The default search path established by **GetSearchPath** consists of the following containers in the following order:</span></span> 
  
1. <span data-ttu-id="dae2a-126">Der erste Container mit Berechtigung zum Lesen/Schreiben, in der Regel das persönliche Adressbuch (PAB).</span><span class="sxs-lookup"><span data-stu-id="dae2a-126">The first container with read/write permission, usually the personal address book (PAB).</span></span>
    
2. <span data-ttu-id="dae2a-127">Jeder Container, dessen **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))-Eigenschaft auf DT_GLOBAL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="dae2a-127">Every container that has its **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) property set to DT_GLOBAL.</span></span> <span data-ttu-id="dae2a-128">Diese Einstellung gibt an, dass der Container Empfänger enthält.</span><span class="sxs-lookup"><span data-stu-id="dae2a-128">This setting indicates that the container holds recipients.</span></span> 
    
3. <span data-ttu-id="dae2a-129">Der als Standard bezeichnete Container, wenn keine Container vorhanden sind, für die das DT_GLOBAL-Flag in der **PR_DISPLAY_TYPE** -Eigenschaft festgelegt ist, und der Standardcontainer sich vom ersten Container mit Berechtigung zum Lesen/Schreiben unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="dae2a-129">The container designated as the default, if there are no containers that have the DT_GLOBAL flag set in their **PR_DISPLAY_TYPE** property and the default container differs from the first container with read/write permission.</span></span> 
    
<span data-ttu-id="dae2a-130">Wenn **SetSearchPath** aufgerufen wurde, erstellt **GetSearchPath** einen Pfad mithilfe der Adressbuchcontainer, die im Profil gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="dae2a-130">If **SetSearchPath** has been called, **GetSearchPath** builds a path by using the address book containers that have been stored in the profile.</span></span> <span data-ttu-id="dae2a-131">**GetSearchPath** überprüft diesen Pfad, bevor er an den Aufrufer zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="dae2a-131">**GetSearchPath** validates this path before it returns it to the caller.</span></span> 
  
<span data-ttu-id="dae2a-132">Nach dem ersten Aufruf von **SetSearchPath**müssen nachfolgende Aufrufe an **SetSearchPath** verwendet werden, um den von **GetSearchPath**zurückgegebenen Suchpfad zu ändern.</span><span class="sxs-lookup"><span data-stu-id="dae2a-132">After the first call to **SetSearchPath**, subsequent calls to **SetSearchPath** must be used to modify the search path returned by **GetSearchPath**.</span></span> <span data-ttu-id="dae2a-133">Anders ausgedrückt erhält der aufrufende Client oder Anbieter nach dem ersten Aufruf von **SetSearchPath**nicht den Standardsuchpfad.</span><span class="sxs-lookup"><span data-stu-id="dae2a-133">In other words, the calling client or provider does not receive the default search path after the first call to **SetSearchPath**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dae2a-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dae2a-134">See also</span></span>



[<span data-ttu-id="dae2a-135">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="dae2a-135">IAddrBook::SetSearchPath</span></span>](iaddrbook-setsearchpath.md)
  
[<span data-ttu-id="dae2a-136">SRowSet</span><span class="sxs-lookup"><span data-stu-id="dae2a-136">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="dae2a-137">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="dae2a-137">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

