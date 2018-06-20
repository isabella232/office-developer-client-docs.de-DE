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
ms.openlocfilehash: c1a78889ea98133af46089fdc93b0c1c4bb24226
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793169"
---
# <a name="mapiuninitialize"></a><span data-ttu-id="555a1-103">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="555a1-103">MAPIUninitialize</span></span>

  
  
<span data-ttu-id="555a1-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="555a1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="555a1-105">Verringert der Referenzzähler bereinigt, und löscht pro Instanz globale Daten für die MAPI-DLL.</span><span class="sxs-lookup"><span data-stu-id="555a1-105">Decrements the reference count, cleans up, and deletes per-instance global data for the MAPI DLL.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="555a1-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="555a1-106">Header file:</span></span>  <br/> |<span data-ttu-id="555a1-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="555a1-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="555a1-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="555a1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="555a1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="555a1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="555a1-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="555a1-110">Called by:</span></span>  <br/> |<span data-ttu-id="555a1-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="555a1-111">Client applications</span></span>  <br/> |
   
```cpp
void MAPIUninitialize ( void );
```

## <a name="parameters"></a><span data-ttu-id="555a1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="555a1-112">Parameters</span></span>

<span data-ttu-id="555a1-113">Keine</span><span class="sxs-lookup"><span data-stu-id="555a1-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="555a1-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="555a1-114">Return value</span></span>

<span data-ttu-id="555a1-115">None.</span><span class="sxs-lookup"><span data-stu-id="555a1-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="555a1-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="555a1-116">Remarks</span></span>

<span data-ttu-id="555a1-117">Eine Clientanwendung ruft die **MAPIUninitialize** -Funktion, um die Interaktion mit MAPI, mit einem Aufruf der Funktion ["MAPIInitialize"](mapiinitialize.md) begonnen zu beenden.</span><span class="sxs-lookup"><span data-stu-id="555a1-117">A client application calls the **MAPIUninitialize** function to end its interaction with MAPI, begun with a call to the [MAPIInitialize](mapiinitialize.md) function.</span></span> <span data-ttu-id="555a1-118">Nachdem **MAPIUninitialize** aufgerufen wurde, können keine anderen MAPI-Aufrufe vom Client vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="555a1-118">After **MAPIUninitialize** is called, no other MAPI calls can be made by the client.</span></span> 
  
 <span data-ttu-id="555a1-119">**MAPIUninitialize** den Referenzzähler und die entsprechende **"MAPIInitialize"** Funktion erhöht den Referenzzähler.</span><span class="sxs-lookup"><span data-stu-id="555a1-119">**MAPIUninitialize** decrements the reference count, and the corresponding **MAPIInitialize** function increments the reference count.</span></span> <span data-ttu-id="555a1-120">Die Anzahl der Anrufe an eine Funktion muss daher die Anzahl der Aufrufe der anderen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="555a1-120">Thus, the number of calls to one function must equal the number of calls to the other.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="555a1-121">**"MAPIInitialize"** oder **MAPIUninitialize** aus kann nicht innerhalb einer Win32 **DllMain** -Funktion oder eine andere Funktion, die erstellt oder Threads beendet aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="555a1-121">You cannot call **MAPIInitialize** or **MAPIUninitialize** from within a Win32 **DllMain** function or any other function that creates or terminates threads.</span></span> <span data-ttu-id="555a1-122">Weitere Informationen finden Sie unter [Verwenden von threadsicheren Objekten](using-thread-safe-objects.md).</span><span class="sxs-lookup"><span data-stu-id="555a1-122">For more information, see [Using Thread-Safe Objects](using-thread-safe-objects.md).</span></span> 
  
