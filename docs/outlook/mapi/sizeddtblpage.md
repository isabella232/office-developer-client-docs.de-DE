---
title: SizedDtblPage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblPage
api_type:
- COM
ms.assetid: 47b2a69d-e902-429f-8b31-166b51aeaf7f
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a1530443600df7cb73ff27d5cfbeab46f81bc53c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795546"
---
# <a name="sizeddtblpage"></a><span data-ttu-id="480ce-103">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="480ce-103">SizedDtblPage</span></span>

<span data-ttu-id="480ce-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="480ce-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="480ce-105">Erstellt eine benannte Struktur, die eine [DTBLPAGE](dtblpage.md) -Struktur für die Beschreibung eines Steuerelements mit Registerkarten, ein Label mit einer angegebenen Länge und einen Eintrag Hilfe Datei mit einer angegebenen Länge enthält.</span><span class="sxs-lookup"><span data-stu-id="480ce-105">Creates a named structure that includes a [DTBLPAGE](dtblpage.md) structure for describing a tabbed page control, a label of a specified length, and a Help file entry of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="480ce-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="480ce-106">Header file:</span></span>  <br/> |<span data-ttu-id="480ce-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="480ce-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="480ce-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="480ce-108">Related structure:</span></span>  <br/> |<span data-ttu-id="480ce-109">**DTBLPAGE**</span><span class="sxs-lookup"><span data-stu-id="480ce-109">**DTBLPAGE**</span></span> <br/> |
   
```cpp
SizedDtblPage (n, n1, u)
```

## <a name="parameters"></a><span data-ttu-id="480ce-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="480ce-110">Parameters</span></span>

<span data-ttu-id="480ce-111">_n_</span><span class="sxs-lookup"><span data-stu-id="480ce-111">_n_</span></span>
  
> <span data-ttu-id="480ce-112">Länge der Beschriftung für die Registerkarte Seite.</span><span class="sxs-lookup"><span data-stu-id="480ce-112">Length of the label for the page tab.</span></span>
    
<span data-ttu-id="480ce-113">_N1_</span><span class="sxs-lookup"><span data-stu-id="480ce-113">_n1_</span></span>
  
> <span data-ttu-id="480ce-114">Die Länge des Eintrags angezeigt wird, in der Datei "Mapisvc.inf", identifiziert der Hilfedatei, die mit der mit Registerkarten-Seitensteuerelement verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="480ce-114">Length of the entry appearing in the Mapisvc.inf file identifying the Help file that will be used with the tabbed page control.</span></span>
    
<span data-ttu-id="480ce-115">_u_</span><span class="sxs-lookup"><span data-stu-id="480ce-115">_u_</span></span>
  
> <span data-ttu-id="480ce-116">Der Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="480ce-116">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="480ce-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="480ce-117">Remarks</span></span>

<span data-ttu-id="480ce-118">Das Makro **SizedDtblPage** können Sie eine mit Registerkarten-Seitensteuerelement zu definieren, wenn die Anzahl der Zeichen in der zugeordneten Label und Hilfe Protokolldateieintrag bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="480ce-118">The **SizedDtblPage** macro lets you define a tabbed page control when the number of characters in the associated label and Help file entry is known.</span></span> <span data-ttu-id="480ce-119">Die neue Struktur wird mit der folgenden Elemente erstellt:</span><span class="sxs-lookup"><span data-stu-id="480ce-119">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLPAGE dtblpage;
TCHAR lpszLabel[n];
TCHAR lpszComponent[n1];
```

<span data-ttu-id="480ce-120">Führen Sie einen Zeiger auf die resultierende Struktur aus dem Makro **SizedDtblPage** als Zeiger Struktur **DTBLPAGE** die folgende Umwandlung:</span><span class="sxs-lookup"><span data-stu-id="480ce-120">To use a pointer to the resulting structure from the **SizedDtblPage** macro as a **DTBLPAGE** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblPage = (LPDTBLPAGE) &SizedDtblPage;
```

## <a name="see-also"></a><span data-ttu-id="480ce-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="480ce-121">See also</span></span>

- [<span data-ttu-id="480ce-122">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="480ce-122">DTBLPAGE</span></span>](dtblpage.md)
- [<span data-ttu-id="480ce-123">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="480ce-123">Macros Related to Structures</span></span>](macros-related-to-structures.md)

