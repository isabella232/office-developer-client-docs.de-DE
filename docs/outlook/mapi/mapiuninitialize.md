---
title: MAPIUninitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIUninitialize
api_type:
- HeaderDef
ms.assetid: 0f4e54dc-80e5-49a7-9703-0225d8133492
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f7339588bcc6815545e7341eafffe9cf001c1d76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408523"
---
# <a name="mapiuninitialize"></a><span data-ttu-id="fc983-103">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="fc983-103">MAPIUninitialize</span></span>

  
  
<span data-ttu-id="fc983-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc983-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc983-105">Dekrementiert die Referenzanzahl, bereinigt und löscht die globalen Daten pro Instanz für die MAPI-DLL.</span><span class="sxs-lookup"><span data-stu-id="fc983-105">Decrements the reference count, cleans up, and deletes per-instance global data for the MAPI DLL.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fc983-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="fc983-106">Header file:</span></span>  <br/> |<span data-ttu-id="fc983-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="fc983-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="fc983-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="fc983-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fc983-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fc983-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fc983-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="fc983-110">Called by:</span></span>  <br/> |<span data-ttu-id="fc983-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="fc983-111">Client applications</span></span>  <br/> |
   
```cpp
void MAPIUninitialize ( void );
```

## <a name="parameters"></a><span data-ttu-id="fc983-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc983-112">Parameters</span></span>

<span data-ttu-id="fc983-113">Keine</span><span class="sxs-lookup"><span data-stu-id="fc983-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="fc983-114">Return value</span><span class="sxs-lookup"><span data-stu-id="fc983-114">Return value</span></span>

<span data-ttu-id="fc983-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="fc983-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fc983-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fc983-116">Remarks</span></span>

<span data-ttu-id="fc983-117">Eine Clientanwendung ruft die **MAPIUninitialize-Funktion** auf, um die Interaktion mit MAPI zu beenden, die mit einem Aufruf der [MAPIInitialize-Funktion begonnen](mapiinitialize.md) wurde.</span><span class="sxs-lookup"><span data-stu-id="fc983-117">A client application calls the **MAPIUninitialize** function to end its interaction with MAPI, begun with a call to the [MAPIInitialize](mapiinitialize.md) function.</span></span> <span data-ttu-id="fc983-118">Nach **dem Aufruf von MAPIUninitialize** können keine weiteren MAPI-Aufrufe vom Client ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fc983-118">After **MAPIUninitialize** is called, no other MAPI calls can be made by the client.</span></span> 
  
 <span data-ttu-id="fc983-119">**MAPIUninitialize** dekrementiert die Referenzanzahl, und die entsprechende **MAPIInitialize-Funktion** erhöht die Referenzanzahl.</span><span class="sxs-lookup"><span data-stu-id="fc983-119">**MAPIUninitialize** decrements the reference count, and the corresponding **MAPIInitialize** function increments the reference count.</span></span> <span data-ttu-id="fc983-120">Daher muss die Anzahl der Aufrufe einer Funktion der Anzahl der Aufrufe an die andere entspricht.</span><span class="sxs-lookup"><span data-stu-id="fc983-120">Thus, the number of calls to one function must equal the number of calls to the other.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="fc983-121">Sie können **MAPIInitialize** oder **MAPIUninitialize** nicht innerhalb einer Win32 **DllMain-Funktion** oder einer anderen Funktion aufrufen, die Threads erstellt oder beendet.</span><span class="sxs-lookup"><span data-stu-id="fc983-121">You cannot call **MAPIInitialize** or **MAPIUninitialize** from within a Win32 **DllMain** function or any other function that creates or terminates threads.</span></span> <span data-ttu-id="fc983-122">Weitere Informationen finden Sie unter [Using Thread-Safe Objects](using-thread-safe-objects.md).</span><span class="sxs-lookup"><span data-stu-id="fc983-122">For more information, see [Using Thread-Safe Objects](using-thread-safe-objects.md).</span></span> 
  

