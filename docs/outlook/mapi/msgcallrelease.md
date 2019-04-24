---
title: MSGCALLRELEASE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MSGCALLRELEASE
api_type:
- COM
ms.assetid: 23c08597-41f0-4f48-a63e-79962fa812bc
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9ffaab1e9cc381be2abfb389f4b72067dca2438b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338563"
---
# <a name="msgcallrelease"></a><span data-ttu-id="94736-103">MSGCALLRELEASE</span><span class="sxs-lookup"><span data-stu-id="94736-103">MSGCALLRELEASE</span></span>

  
  
<span data-ttu-id="94736-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94736-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94736-105">Definiert eine Rückruffunktion, die eine **IStorage** -Schnittstellenach der endgültigen Version eines auf Ihr basierenden **IMessage** -Objekts mit der [OpenIMsgOnIStg](openimsgonistg.md) -Funktion freigeben kann.</span><span class="sxs-lookup"><span data-stu-id="94736-105">Defines a callback function that can free an **IStorage** interface after the final release of an **IMessage** object built on top of it with the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="94736-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="94736-106">Header file:</span></span>  <br/> |<span data-ttu-id="94736-107">IMessage. h</span><span class="sxs-lookup"><span data-stu-id="94736-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="94736-108">Definierte Funktion, implementiert von:</span><span class="sxs-lookup"><span data-stu-id="94736-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="94736-109">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="94736-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="94736-110">Definierte Funktion, aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="94736-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="94736-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="94736-111">MAPI</span></span>  <br/> |
   
```cpp
typedef void (STDAPICALLTYPE MSGCALLRELEASE)(
  ULONG  ulCallerData,
  LPMESSAGE  lpMessage );
```

## <a name="parameters"></a><span data-ttu-id="94736-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="94736-112">Parameters</span></span>

 <span data-ttu-id="94736-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="94736-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="94736-114">in Enthält Anruf Anwendungsinformationen zur **IMessage** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="94736-114">[in] Contains calling application information about the **IMessage** interface.</span></span> 
    
 <span data-ttu-id="94736-115">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="94736-115">_lpMessage_</span></span>
  
> <span data-ttu-id="94736-116">in Zeiger auf die Nachricht und die Anlagen auf oberster Ebene, die freigegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="94736-116">[in] Pointer to the top-level message and attachments that have been released.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="94736-117">Return value</span><span class="sxs-lookup"><span data-stu-id="94736-117">Return value</span></span>

<span data-ttu-id="94736-118">None.</span><span class="sxs-lookup"><span data-stu-id="94736-118">None.</span></span>
  

