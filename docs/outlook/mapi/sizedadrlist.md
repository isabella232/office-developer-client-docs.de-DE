---
title: SizedADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedADRLIST
api_type:
- COM
ms.assetid: 5c64d74a-83a7-4122-b1d1-fcca0f4a6cdb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c35a1eb54b29c04bc8eed453272b59aae0ea737e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423461"
---
# <a name="sizedadrlist"></a><span data-ttu-id="39262-103">SizedADRLIST</span><span class="sxs-lookup"><span data-stu-id="39262-103">SizedADRLIST</span></span>

<span data-ttu-id="39262-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39262-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39262-105">Definiert eine [ADRLIST](adrlist.md) -Struktur mit dem angegebenen Namen, die eine bestimmte Anzahl von [Miet](adrentry.md) Strukturen enthält.</span><span class="sxs-lookup"><span data-stu-id="39262-105">Defines an [ADRLIST](adrlist.md) structure with the specified name that contains a specified number of [ADRENTRY](adrentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="39262-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="39262-106">Header file:</span></span>  <br/> |<span data-ttu-id="39262-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="39262-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="39262-108">Zugehörige Struktur:</span><span class="sxs-lookup"><span data-stu-id="39262-108">Related structure:</span></span>  <br/> |<span data-ttu-id="39262-109">**ADRLIST**</span><span class="sxs-lookup"><span data-stu-id="39262-109">**ADRLIST**</span></span> <br/> |
   
```cpp
SizedADRLIST (_centries,_name)
```

## <a name="parameters"></a><span data-ttu-id="39262-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="39262-110">Parameters</span></span>

<span data-ttu-id="39262-111">__Zentrierungen_</span><span class="sxs-lookup"><span data-stu-id="39262-111">__centries_</span></span>
  
> <span data-ttu-id="39262-112">Die Anzahl der **Miet** Strukturen, die in die neue **ADRLIST** -Struktur eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="39262-112">Count of **ADRENTRY** structures to be included in the new **ADRLIST** structure.</span></span> 
    
<span data-ttu-id="39262-113">__Name_</span><span class="sxs-lookup"><span data-stu-id="39262-113">__name_</span></span>
  
> <span data-ttu-id="39262-114">Name für die neue **ADRLIST** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="39262-114">Name for the new **ADRLIST** structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="39262-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39262-115">Remarks</span></span>

<span data-ttu-id="39262-116">Mit dem **SizedADRLIST** -Makro können Sie eine Empfängerliste mit expliziten Grenzen definieren, wenn die Anforderungen an die Arraylänge bekannt sind.</span><span class="sxs-lookup"><span data-stu-id="39262-116">The **SizedADRLIST** macro lets you define a recipient list that has explicit bounds when array length requirements are known.</span></span> <span data-ttu-id="39262-117">Der folgende Code zeigt, wie das Ergebnis des **SizedADRLIST** -Makros in einen **ADRLIST** -Struktur Zeiger umgewandelt wird:</span><span class="sxs-lookup"><span data-stu-id="39262-117">The following code shows how to cast the result of the **SizedADRLIST** macro to an **ADRLIST** structure pointer:</span></span> 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a><span data-ttu-id="39262-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39262-118">See also</span></span>

- [<span data-ttu-id="39262-119">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="39262-119">ADRLIST</span></span>](adrlist.md)
- [<span data-ttu-id="39262-120">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="39262-120">ADRENTRY</span></span>](adrentry.md)
- [<span data-ttu-id="39262-121">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="39262-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

