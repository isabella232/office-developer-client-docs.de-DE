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
ms.openlocfilehash: 6120439ea0d98ed6b64fe1542a4372265574723a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567531"
---
# <a name="sizeddtblcheckbox"></a><span data-ttu-id="6e069-103">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="6e069-103">SizedDtblCheckBox</span></span>
 
<span data-ttu-id="6e069-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e069-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e069-105">Erstellt eine benannte Struktur, die eine [DTBLCHECKBOX](dtblcheckbox.md) -Struktur für die Beschreibung ein Kontrollkästchen-Steuerelement und ein Label mit einer angegebenen Länge enthält.</span><span class="sxs-lookup"><span data-stu-id="6e069-105">Creates a named structure that includes a [DTBLCHECKBOX](dtblcheckbox.md) structure for describing a check box control and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6e069-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="6e069-106">Header file:</span></span>  <br/> |<span data-ttu-id="6e069-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6e069-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="6e069-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="6e069-108">Related structure:</span></span>  <br/> |<span data-ttu-id="6e069-109">**DTBLCHECKBOX**</span><span class="sxs-lookup"><span data-stu-id="6e069-109">**DTBLCHECKBOX**</span></span> <br/> |
   
```cpp
SizedDtblCheckBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="6e069-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e069-110">Parameters</span></span>

<span data-ttu-id="6e069-111">_n_</span><span class="sxs-lookup"><span data-stu-id="6e069-111">_n_</span></span>
  
> <span data-ttu-id="6e069-112">Länge der Beschriftung, die in die neue Struktur eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="6e069-112">Length of the label to be included in the new structure.</span></span>
    
<span data-ttu-id="6e069-113">_u_</span><span class="sxs-lookup"><span data-stu-id="6e069-113">_u_</span></span>
  
> <span data-ttu-id="6e069-114">Der Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="6e069-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6e069-115">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="6e069-115">Remarks</span></span>

<span data-ttu-id="6e069-116">Das Makro **SizedDtblCheckBox** können Sie ein Kontrollkästchen definieren, wenn die Anzahl der Zeichen Bezeichnung bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="6e069-116">The **SizedDtblCheckBox** macro lets you define a check box when the number of label characters is known.</span></span> <span data-ttu-id="6e069-117">Die neue Struktur wird mit der folgenden Elemente erstellt:</span><span class="sxs-lookup"><span data-stu-id="6e069-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLCHECKBOX dtblcheckbox;
TCHAR lpszLabel[n];
```

<span data-ttu-id="6e069-118">Führen Sie einen Zeiger auf die resultierende Struktur aus dem Makro **SizedDtblCheckBox** als Zeiger Struktur **DTBLCHECKBOX** die folgende Umwandlung:</span><span class="sxs-lookup"><span data-stu-id="6e069-118">To use a pointer to the resulting structure from the **SizedDtblCheckBox** macro as a **DTBLCHECKBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblCheckBox = (LPDTBLCHECKBOX) &SizedDtblCheckBox;
```

## <a name="see-also"></a><span data-ttu-id="6e069-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e069-119">See also</span></span>

- [<span data-ttu-id="6e069-120">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="6e069-120">DTBLCHECKBOX</span></span>](dtblcheckbox.md)
- [<span data-ttu-id="6e069-121">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="6e069-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

