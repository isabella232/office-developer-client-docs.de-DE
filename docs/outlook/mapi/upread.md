---
title: UPREAD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 568f2336-cb4d-3f2c-a304-d29cdb0bcbcc
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7338edc13227e303ec5fa47da4a5d9ee611c6749
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419884"
---
# <a name="upread"></a><span data-ttu-id="10a26-103">UPREAD</span><span class="sxs-lookup"><span data-stu-id="10a26-103">UPREAD</span></span>

  
  
<span data-ttu-id="10a26-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10a26-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10a26-105">Informationen zum Hochladen des Lesestatus von Elementen während des [Status des Upload-Lesestatus](upload-read-status-state.md).</span><span class="sxs-lookup"><span data-stu-id="10a26-105">Information for uploading the read state of items during the [upload read status state](upload-read-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="10a26-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="10a26-106">Quick info</span></span>

```cpp
struct UPREAD 
{ 
    PUPREADE pupre; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="10a26-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="10a26-107">Members</span></span>

 <span data-ttu-id="10a26-108">_pupre_</span><span class="sxs-lookup"><span data-stu-id="10a26-108">_pupre_</span></span>
  
>  <span data-ttu-id="10a26-109">[out] Vektor von **[UPREADE-Einträgen.](upreade.md)**</span><span class="sxs-lookup"><span data-stu-id="10a26-109">[out] Vector of **[UPREADE](upreade.md)** entries.</span></span> 
    
 <span data-ttu-id="10a26-110">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="10a26-110">_cEnt_</span></span>
  
>  <span data-ttu-id="10a26-111">[out] Anzahl **der UPREADE-Einträge.**</span><span class="sxs-lookup"><span data-stu-id="10a26-111">[out] Number of **UPREADE** entries.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="10a26-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10a26-112">See also</span></span>



[<span data-ttu-id="10a26-113">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="10a26-113">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="10a26-114">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="10a26-114">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="10a26-115">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="10a26-115">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="10a26-116">UPREADE</span><span class="sxs-lookup"><span data-stu-id="10a26-116">UPREADE</span></span>](upreade.md)

