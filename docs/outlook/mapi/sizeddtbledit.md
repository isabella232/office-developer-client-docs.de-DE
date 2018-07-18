---
title: SizedDtblEdit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblEdit
api_type:
- COM
ms.assetid: a658d027-03a2-4cde-bf99-563e8521cb31
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4ea77023bdc9442325f4af46d23c107e7172ceaf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795543"
---
# <a name="sizeddtbledit"></a><span data-ttu-id="cf822-103">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="cf822-103">SizedDtblEdit</span></span>

<span data-ttu-id="cf822-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cf822-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cf822-105">Erstellt eine benannte Struktur, die enthält eine [DTBLEDIT](dtbledit.md) -Struktur für die Beschreibung ein Edit-Steuerelement und die maximale Anzahl von Zeichen, die im Steuerelement eingegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="cf822-105">Creates a named structure that includes a [DTBLEDIT](dtbledit.md) structure for describing an edit control and the maximum number of characters that can be entered in the control.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cf822-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="cf822-106">Header file:</span></span>  <br/> |<span data-ttu-id="cf822-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cf822-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="cf822-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="cf822-108">Related structure:</span></span>  <br/> |<span data-ttu-id="cf822-109">**DTBLEDIT**</span><span class="sxs-lookup"><span data-stu-id="cf822-109">**DTBLEDIT**</span></span> <br/> |
   
```cpp
SizedDtblEdit (n, u)
```

## <a name="parameters"></a><span data-ttu-id="cf822-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf822-110">Parameters</span></span>

<span data-ttu-id="cf822-111">_n_</span><span class="sxs-lookup"><span data-stu-id="cf822-111">_n_</span></span>
  
> <span data-ttu-id="cf822-112">Maximale Anzahl von Zeichen, die im Bearbeitungssteuerelement eingegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="cf822-112">Maximum number of characters that can be entered in the edit control.</span></span>
    
<span data-ttu-id="cf822-113">_u_</span><span class="sxs-lookup"><span data-stu-id="cf822-113">_u_</span></span>
  
> <span data-ttu-id="cf822-114">Der Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="cf822-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cf822-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf822-115">Remarks</span></span>

<span data-ttu-id="cf822-116">Das Makro **SizedDtblEdit** können Sie ein Edit-Steuerelement zu definieren, wenn die Anzahl der aktivierten Zeichen bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="cf822-116">The **SizedDtblEdit** macro lets you define an edit control when the number of enabled characters is known.</span></span> <span data-ttu-id="cf822-117">Die neue Struktur wird mit der folgenden Elemente erstellt:</span><span class="sxs-lookup"><span data-stu-id="cf822-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLEDIT dtbledit;
TCHAR lpszCharsAllowed[n];

```

<span data-ttu-id="cf822-118">Führen Sie einen Zeiger auf die resultierende Struktur aus dem Makro **SizedDtblEdit** als Zeiger Struktur **DTBLEDIT** die folgende Umwandlung:</span><span class="sxs-lookup"><span data-stu-id="cf822-118">To use a pointer to the resulting structure from the **SizedDtblEdit** macro as a **DTBLEDIT** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblEdit = (LPDTBLEDIT) &SizedDtblEdit;

```

## <a name="see-also"></a><span data-ttu-id="cf822-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf822-119">See also</span></span>

- [<span data-ttu-id="cf822-120">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="cf822-120">DTBLEDIT</span></span>](dtbledit.md)
- [<span data-ttu-id="cf822-121">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="cf822-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

