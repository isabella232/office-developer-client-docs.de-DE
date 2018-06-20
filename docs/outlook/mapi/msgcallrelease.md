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
ms.openlocfilehash: aaa1adaa170349c3df3a2256802a502cb2512b20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793270"
---
# <a name="msgcallrelease"></a><span data-ttu-id="fea64-103">MSGCALLRELEASE</span><span class="sxs-lookup"><span data-stu-id="fea64-103">MSGCALLRELEASE</span></span>

  
  
<span data-ttu-id="fea64-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fea64-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fea64-105">Definiert eine Rückruffunktion, die eine Schnittstelle **IStorage** nach der endgültigen Version eines Objekts mit der Funktion [OpenIMsgOnIStg](openimsgonistg.md) aufbaut **IMessage** freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="fea64-105">Defines a callback function that can free an **IStorage** interface after the final release of an **IMessage** object built on top of it with the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fea64-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="fea64-106">Header file:</span></span>  <br/> |<span data-ttu-id="fea64-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="fea64-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="fea64-108">Definierte Funktion von implementiert:</span><span class="sxs-lookup"><span data-stu-id="fea64-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="fea64-109">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="fea64-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="fea64-110">Definierte Funktion aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="fea64-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="fea64-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="fea64-111">MAPI</span></span>  <br/> |
   
```cpp
typedef void (STDAPICALLTYPE MSGCALLRELEASE)(
  ULONG  ulCallerData,
  LPMESSAGE  lpMessage );
```

## <a name="parameters"></a><span data-ttu-id="fea64-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fea64-112">Parameters</span></span>

 <span data-ttu-id="fea64-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="fea64-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="fea64-114">[in] Enthält die aufrufende Anwendungsinformationen zur **IMessage** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="fea64-114">[in] Contains calling application information about the **IMessage** interface.</span></span> 
    
 <span data-ttu-id="fea64-115">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="fea64-115">_lpMessage_</span></span>
  
> <span data-ttu-id="fea64-116">[in] Zeiger auf der obersten Ebene Meldung und Anlagen, die veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="fea64-116">[in] Pointer to the top-level message and attachments that have been released.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fea64-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fea64-117">Return value</span></span>

<span data-ttu-id="fea64-118">None.</span><span class="sxs-lookup"><span data-stu-id="fea64-118">None.</span></span>
  

