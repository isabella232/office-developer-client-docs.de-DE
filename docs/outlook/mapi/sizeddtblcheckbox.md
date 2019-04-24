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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6d23d56a27095497aedc64d7bbf5ffda266d0c97
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282754"
---
# <a name="sizeddtblcheckbox"></a><span data-ttu-id="96132-103">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="96132-103">SizedDtblCheckBox</span></span>
 
<span data-ttu-id="96132-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96132-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="96132-105">Erstellt eine benannte Struktur, die eine [DTBLCHECKBOX](dtblcheckbox.md) -Struktur zur Beschreibung eines Kontrollkästchen-Steuerelements und einer Beschriftung einer angegebenen Länge enthält.</span><span class="sxs-lookup"><span data-stu-id="96132-105">Creates a named structure that includes a [DTBLCHECKBOX](dtblcheckbox.md) structure for describing a check box control and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="96132-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="96132-106">Header file:</span></span>  <br/> |<span data-ttu-id="96132-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="96132-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="96132-108">Zugehörige Struktur:</span><span class="sxs-lookup"><span data-stu-id="96132-108">Related structure:</span></span>  <br/> |<span data-ttu-id="96132-109">**DTBLCHECKBOX**</span><span class="sxs-lookup"><span data-stu-id="96132-109">**DTBLCHECKBOX**</span></span> <br/> |
   
```cpp
SizedDtblCheckBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="96132-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="96132-110">Parameters</span></span>

<span data-ttu-id="96132-111">_n_</span><span class="sxs-lookup"><span data-stu-id="96132-111">_n_</span></span>
  
> <span data-ttu-id="96132-112">Die Länge der Bezeichnung, die in die neue Struktur eingeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="96132-112">Length of the label to be included in the new structure.</span></span>
    
<span data-ttu-id="96132-113">_u_</span><span class="sxs-lookup"><span data-stu-id="96132-113">_u_</span></span>
  
> <span data-ttu-id="96132-114">Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="96132-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="96132-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="96132-115">Remarks</span></span>

<span data-ttu-id="96132-116">Mit dem **SizedDtblCheckBox** -Makro können Sie ein Kontrollkästchen definieren, wenn die Anzahl der Bezeichnungs Zeichen bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="96132-116">The **SizedDtblCheckBox** macro lets you define a check box when the number of label characters is known.</span></span> <span data-ttu-id="96132-117">Die neue Struktur wird mit den folgenden Elementen erstellt:</span><span class="sxs-lookup"><span data-stu-id="96132-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLCHECKBOX dtblcheckbox;
TCHAR lpszLabel[n];
```

<span data-ttu-id="96132-118">Wenn Sie einen Zeiger auf die resultierende Struktur aus dem **SizedDtblCheckBox** -Makro als **DTBLCHECKBOX** -Struktur Zeiger verwenden möchten, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="96132-118">To use a pointer to the resulting structure from the **SizedDtblCheckBox** macro as a **DTBLCHECKBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblCheckBox = (LPDTBLCHECKBOX) &SizedDtblCheckBox;
```

## <a name="see-also"></a><span data-ttu-id="96132-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96132-119">See also</span></span>

- [<span data-ttu-id="96132-120">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="96132-120">DTBLCHECKBOX</span></span>](dtblcheckbox.md)
- [<span data-ttu-id="96132-121">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="96132-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

