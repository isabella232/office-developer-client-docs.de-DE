---
title: SizedDtblLabel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblLabel
api_type:
- COM
ms.assetid: c7cb8cf9-7abd-4ee3-b88c-d61695f4ed31
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1ae675d1d4adf841e18bbfc8990913136afe8b4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408614"
---
# <a name="sizeddtbllabel"></a><span data-ttu-id="321a7-103">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="321a7-103">SizedDtblLabel</span></span>

<span data-ttu-id="321a7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="321a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="321a7-105">Erstellt eine benannte Struktur, die eine [DTBLLABEL-Struktur](dtbllabel.md) zum Beschreiben eines Bezeichnungssteuerelements und der zugeordneten Bezeichnung einer angegebenen Länge enthält.</span><span class="sxs-lookup"><span data-stu-id="321a7-105">Creates a named structure that includes a [DTBLLABEL](dtbllabel.md) structure for describing a label control and the associated label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="321a7-106">In der Headerdatei angegeben:</span><span class="sxs-lookup"><span data-stu-id="321a7-106">Specified in header file:</span></span>  <br/> |<span data-ttu-id="321a7-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="321a7-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="321a7-108">Verwandte Struktur</span><span class="sxs-lookup"><span data-stu-id="321a7-108">Related structure</span></span>  <br/> |<span data-ttu-id="321a7-109">**DTBLLABEL**</span><span class="sxs-lookup"><span data-stu-id="321a7-109">**DTBLLABEL**</span></span> <br/> |
   
```cpp
SizedDtblLabel (n, u)
```

## <a name="parameters"></a><span data-ttu-id="321a7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="321a7-110">Parameters</span></span>

<span data-ttu-id="321a7-111">_n_</span><span class="sxs-lookup"><span data-stu-id="321a7-111">_n_</span></span>
  
> <span data-ttu-id="321a7-112">Länge der Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="321a7-112">Length of the label.</span></span> <span data-ttu-id="321a7-113">Dies schließt das endende NULL-Zeichen ein.</span><span class="sxs-lookup"><span data-stu-id="321a7-113">This includes the ending NULL character.</span></span> 
    
<span data-ttu-id="321a7-114">_u_</span><span class="sxs-lookup"><span data-stu-id="321a7-114">_u_</span></span>
  
> <span data-ttu-id="321a7-115">Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="321a7-115">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="321a7-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="321a7-116">Remarks</span></span>

<span data-ttu-id="321a7-117">Mit **dem Makro SizedDtblLabel** können Sie eine Anzeigetabelle definieren, wenn die Anzahl der Zeichen in der Bezeichnung bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="321a7-117">The **SizedDtblLabel** macro lets you define a display table label when the number of characters in the label is known.</span></span> <span data-ttu-id="321a7-118">Die neue Struktur wird mit den folgenden Mitgliedern erstellt:</span><span class="sxs-lookup"><span data-stu-id="321a7-118">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLLABEL dtbllabel;
TCHAR lpszLabelName[n];
```

<span data-ttu-id="321a7-119">Führen Sie die folgende Gliederung aus, um einen Zeiger auf die resultierende Struktur des **SizedDtblLabel-Makros** als **DTBLLABEL-Strukturzeiger** zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="321a7-119">To use a pointer to the resulting structure from the **SizedDtblLabel** macro as a **DTBLLABEL** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblLabel = (LPDTBLLABEL) &SizedDtblLabel;
```

## <a name="see-also"></a><span data-ttu-id="321a7-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="321a7-120">See also</span></span>

- [<span data-ttu-id="321a7-121">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="321a7-121">DTBLLABEL</span></span>](dtbllabel.md)
- [<span data-ttu-id="321a7-122">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="321a7-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

