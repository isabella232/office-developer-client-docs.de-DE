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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f7339588bcc6815545e7341eafffe9cf001c1d76
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270028"
---
# <a name="mapiuninitialize"></a><span data-ttu-id="36ddc-103">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="36ddc-103">MAPIUninitialize</span></span>

  
  
<span data-ttu-id="36ddc-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36ddc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36ddc-105">Dekrementiert den Verweiszähler, bereinigt und löscht einzelne globale Daten für die MAPI-DLL.</span><span class="sxs-lookup"><span data-stu-id="36ddc-105">Decrements the reference count, cleans up, and deletes per-instance global data for the MAPI DLL.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="36ddc-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="36ddc-106">Header file:</span></span>  <br/> |<span data-ttu-id="36ddc-107">Mapix. h</span><span class="sxs-lookup"><span data-stu-id="36ddc-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="36ddc-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="36ddc-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="36ddc-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="36ddc-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="36ddc-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="36ddc-110">Called by:</span></span>  <br/> |<span data-ttu-id="36ddc-111">Client Anwendungen</span><span class="sxs-lookup"><span data-stu-id="36ddc-111">Client applications</span></span>  <br/> |
   
```cpp
void MAPIUninitialize ( void );
```

## <a name="parameters"></a><span data-ttu-id="36ddc-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="36ddc-112">Parameters</span></span>

<span data-ttu-id="36ddc-113">Keine</span><span class="sxs-lookup"><span data-stu-id="36ddc-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="36ddc-114">Return value</span><span class="sxs-lookup"><span data-stu-id="36ddc-114">Return value</span></span>

<span data-ttu-id="36ddc-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="36ddc-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="36ddc-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="36ddc-116">Remarks</span></span>

<span data-ttu-id="36ddc-117">Eine Clientanwendung Ruft die **MAPIUninitialize** -Funktion auf, um die Interaktion mit MAPI zu beenden, angefangen mit einem Aufruf der [MAPIInitialize](mapiinitialize.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="36ddc-117">A client application calls the **MAPIUninitialize** function to end its interaction with MAPI, begun with a call to the [MAPIInitialize](mapiinitialize.md) function.</span></span> <span data-ttu-id="36ddc-118">Nachdem **MAPIUninitialize** aufgerufen wurde, können vom Client keine weiteren MAPI-Aufrufe durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="36ddc-118">After **MAPIUninitialize** is called, no other MAPI calls can be made by the client.</span></span> 
  
 <span data-ttu-id="36ddc-119">**MAPIUninitialize** dekrementiert den Verweiszähler, und die entsprechende **MAPIInitialize** -Funktion inkrementiert den Verweiszähler.</span><span class="sxs-lookup"><span data-stu-id="36ddc-119">**MAPIUninitialize** decrements the reference count, and the corresponding **MAPIInitialize** function increments the reference count.</span></span> <span data-ttu-id="36ddc-120">Daher muss die Anzahl der Aufrufe an eine Funktion der Anzahl der Aufrufe der anderen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="36ddc-120">Thus, the number of calls to one function must equal the number of calls to the other.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="36ddc-121">Sie können **MAPIInitialize** oder **MAPIUninitialize** nicht über eine Win32- **DllMain** -Funktion oder eine andere Funktion aufrufen, die Threads erstellt oder beendet.</span><span class="sxs-lookup"><span data-stu-id="36ddc-121">You cannot call **MAPIInitialize** or **MAPIUninitialize** from within a Win32 **DllMain** function or any other function that creates or terminates threads.</span></span> <span data-ttu-id="36ddc-122">Weitere Informationen finden Sie unter [Verwenden von Thread sicheren Objekten](using-thread-safe-objects.md).</span><span class="sxs-lookup"><span data-stu-id="36ddc-122">For more information, see [Using Thread-Safe Objects](using-thread-safe-objects.md).</span></span> 
  

