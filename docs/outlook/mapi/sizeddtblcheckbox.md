---
title: SizedDtblCheckBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblCheckBox
api_type:
- COM
ms.assetid: 9d04a124-54d4-43ac-967f-ea8e7a09b1d0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6d23d56a27095497aedc64d7bbf5ffda266d0c97
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420808"
---
# <a name="sizeddtblcheckbox"></a><span data-ttu-id="5116d-103">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="5116d-103">SizedDtblCheckBox</span></span>
 
<span data-ttu-id="5116d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5116d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5116d-105">Erstellt eine benannte Struktur, die eine [DTBLCHECKBOX-Struktur](dtblcheckbox.md) zum Beschreiben eines Kontrollkästchensteuerelements und einer Bezeichnung mit einer angegebenen Länge enthält.</span><span class="sxs-lookup"><span data-stu-id="5116d-105">Creates a named structure that includes a [DTBLCHECKBOX](dtblcheckbox.md) structure for describing a check box control and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5116d-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="5116d-106">Header file:</span></span>  <br/> |<span data-ttu-id="5116d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5116d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5116d-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="5116d-108">Related structure:</span></span>  <br/> |<span data-ttu-id="5116d-109">**DTBLCHECKBOX**</span><span class="sxs-lookup"><span data-stu-id="5116d-109">**DTBLCHECKBOX**</span></span> <br/> |
   
```cpp
SizedDtblCheckBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="5116d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5116d-110">Parameters</span></span>

<span data-ttu-id="5116d-111">_n_</span><span class="sxs-lookup"><span data-stu-id="5116d-111">_n_</span></span>
  
> <span data-ttu-id="5116d-112">Länge der Bezeichnung, die in die neue Struktur eingeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5116d-112">Length of the label to be included in the new structure.</span></span>
    
<span data-ttu-id="5116d-113">_u_</span><span class="sxs-lookup"><span data-stu-id="5116d-113">_u_</span></span>
  
> <span data-ttu-id="5116d-114">Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="5116d-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5116d-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5116d-115">Remarks</span></span>

<span data-ttu-id="5116d-116">Mit **dem Makro SizedDtblCheckBox** können Sie ein Kontrollkästchen definieren, wenn die Anzahl der Bezeichnungszeichen bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="5116d-116">The **SizedDtblCheckBox** macro lets you define a check box when the number of label characters is known.</span></span> <span data-ttu-id="5116d-117">Die neue Struktur wird mit den folgenden Mitgliedern erstellt:</span><span class="sxs-lookup"><span data-stu-id="5116d-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLCHECKBOX dtblcheckbox;
TCHAR lpszLabel[n];
```

<span data-ttu-id="5116d-118">Führen Sie die folgende Gliederung aus, um einen Zeiger auf die resultierende Struktur des **SizedDtblCheckBox-Makros** als **DTBLCHECKBOX-Strukturzeiger** zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="5116d-118">To use a pointer to the resulting structure from the **SizedDtblCheckBox** macro as a **DTBLCHECKBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblCheckBox = (LPDTBLCHECKBOX) &SizedDtblCheckBox;
```

## <a name="see-also"></a><span data-ttu-id="5116d-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5116d-119">See also</span></span>

- [<span data-ttu-id="5116d-120">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="5116d-120">DTBLCHECKBOX</span></span>](dtblcheckbox.md)
- [<span data-ttu-id="5116d-121">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="5116d-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

