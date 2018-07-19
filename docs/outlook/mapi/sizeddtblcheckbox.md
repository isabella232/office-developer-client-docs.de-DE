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
ms.openlocfilehash: 9a30554253bc11c8905273079429e4b41c20583a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795538"
---
# <a name="sizeddtblcheckbox"></a><span data-ttu-id="a4ef6-103">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="a4ef6-103">SizedDtblCheckBox</span></span>
 
<span data-ttu-id="a4ef6-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a4ef6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a4ef6-105">Erstellt eine benannte Struktur, die eine [DTBLCHECKBOX](dtblcheckbox.md) -Struktur für die Beschreibung ein Kontrollkästchen-Steuerelement und ein Label mit einer angegebenen Länge enthält.</span><span class="sxs-lookup"><span data-stu-id="a4ef6-105">Creates a named structure that includes a [DTBLCHECKBOX](dtblcheckbox.md) structure for describing a check box control and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a4ef6-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="a4ef6-106">Header file:</span></span>  <br/> |<span data-ttu-id="a4ef6-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a4ef6-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a4ef6-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="a4ef6-108">Related structure:</span></span>  <br/> |<span data-ttu-id="a4ef6-109">**DTBLCHECKBOX**</span><span class="sxs-lookup"><span data-stu-id="a4ef6-109">**DTBLCHECKBOX**</span></span> <br/> |
   
```cpp
SizedDtblCheckBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="a4ef6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4ef6-110">Parameters</span></span>

<span data-ttu-id="a4ef6-111">_n_</span><span class="sxs-lookup"><span data-stu-id="a4ef6-111">_n_</span></span>
  
> <span data-ttu-id="a4ef6-112">Länge der Beschriftung, die in die neue Struktur eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="a4ef6-112">Length of the label to be included in the new structure.</span></span>
    
<span data-ttu-id="a4ef6-113">_u_</span><span class="sxs-lookup"><span data-stu-id="a4ef6-113">_u_</span></span>
  
> <span data-ttu-id="a4ef6-114">Der Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="a4ef6-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a4ef6-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a4ef6-115">Remarks</span></span>

<span data-ttu-id="a4ef6-116">Das Makro **SizedDtblCheckBox** können Sie ein Kontrollkästchen definieren, wenn die Anzahl der Zeichen Bezeichnung bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="a4ef6-116">The **SizedDtblCheckBox** macro lets you define a check box when the number of label characters is known.</span></span> <span data-ttu-id="a4ef6-117">Die neue Struktur wird mit der folgenden Elemente erstellt:</span><span class="sxs-lookup"><span data-stu-id="a4ef6-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLCHECKBOX dtblcheckbox;
TCHAR lpszLabel[n];
```

<span data-ttu-id="a4ef6-118">Führen Sie einen Zeiger auf die resultierende Struktur aus dem Makro **SizedDtblCheckBox** als Zeiger Struktur **DTBLCHECKBOX** die folgende Umwandlung:</span><span class="sxs-lookup"><span data-stu-id="a4ef6-118">To use a pointer to the resulting structure from the **SizedDtblCheckBox** macro as a **DTBLCHECKBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblCheckBox = (LPDTBLCHECKBOX) &SizedDtblCheckBox;
```

## <a name="see-also"></a><span data-ttu-id="a4ef6-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4ef6-119">See also</span></span>

- [<span data-ttu-id="a4ef6-120">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="a4ef6-120">DTBLCHECKBOX</span></span>](dtblcheckbox.md)
- [<span data-ttu-id="a4ef6-121">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="a4ef6-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

