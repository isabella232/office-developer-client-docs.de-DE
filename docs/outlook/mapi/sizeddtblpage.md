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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f14b8d7a9a73997f797f9cfa26a2e574222e839e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407445"
---
# <a name="sizeddtblpage"></a><span data-ttu-id="9c1b2-103">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="9c1b2-103">SizedDtblPage</span></span>

<span data-ttu-id="9c1b2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c1b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c1b2-105">Erstellt eine benannte Struktur, die eine [DTBLPAGE-Struktur](dtblpage.md) zum Beschreiben eines Seitensteuerelements mit Registerkarten, eine Bezeichnung einer angegebenen Länge und einen Hilfedateieintrag mit einer angegebenen Länge enthält.</span><span class="sxs-lookup"><span data-stu-id="9c1b2-105">Creates a named structure that includes a [DTBLPAGE](dtblpage.md) structure for describing a tabbed page control, a label of a specified length, and a Help file entry of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9c1b2-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="9c1b2-106">Header file:</span></span>  <br/> |<span data-ttu-id="9c1b2-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9c1b2-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9c1b2-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="9c1b2-108">Related structure:</span></span>  <br/> |<span data-ttu-id="9c1b2-109">**DTBLPAGE**</span><span class="sxs-lookup"><span data-stu-id="9c1b2-109">**DTBLPAGE**</span></span> <br/> |
   
```cpp
SizedDtblPage (n, n1, u)
```

## <a name="parameters"></a><span data-ttu-id="9c1b2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c1b2-110">Parameters</span></span>

<span data-ttu-id="9c1b2-111">_n_</span><span class="sxs-lookup"><span data-stu-id="9c1b2-111">_n_</span></span>
  
> <span data-ttu-id="9c1b2-112">Länge der Beschriftung für die Seitenregisterkarte.</span><span class="sxs-lookup"><span data-stu-id="9c1b2-112">Length of the label for the page tab.</span></span>
    
<span data-ttu-id="9c1b2-113">_n1_</span><span class="sxs-lookup"><span data-stu-id="9c1b2-113">_n1_</span></span>
  
> <span data-ttu-id="9c1b2-114">Länge des Eintrags, der in der Datei Mapisvc.inf angezeigt wird und die Hilfedatei identifiziert, die mit dem Seitensteuerelement mit Registerkarten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9c1b2-114">Length of the entry appearing in the Mapisvc.inf file identifying the Help file that will be used with the tabbed page control.</span></span>
    
<span data-ttu-id="9c1b2-115">_u_</span><span class="sxs-lookup"><span data-stu-id="9c1b2-115">_u_</span></span>
  
> <span data-ttu-id="9c1b2-116">Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="9c1b2-116">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9c1b2-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9c1b2-117">Remarks</span></span>

<span data-ttu-id="9c1b2-118">Mit **dem Makro SizedDtblPage** können Sie ein Seitensteuerelement mit Registerkarten definieren, wenn die Anzahl der Zeichen in der zugeordneten Bezeichnung und dem Hilfedateieintrag bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="9c1b2-118">The **SizedDtblPage** macro lets you define a tabbed page control when the number of characters in the associated label and Help file entry is known.</span></span> <span data-ttu-id="9c1b2-119">Die neue Struktur wird mit den folgenden Mitgliedern erstellt:</span><span class="sxs-lookup"><span data-stu-id="9c1b2-119">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLPAGE dtblpage;
TCHAR lpszLabel[n];
TCHAR lpszComponent[n1];
```

<span data-ttu-id="9c1b2-120">Führen Sie die folgende Gliederung aus, um einen Zeiger auf die resultierende Struktur des **SizedDtblPage-Makros** als **DTBLPAGE-Strukturzeiger** zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="9c1b2-120">To use a pointer to the resulting structure from the **SizedDtblPage** macro as a **DTBLPAGE** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblPage = (LPDTBLPAGE) &SizedDtblPage;
```

## <a name="see-also"></a><span data-ttu-id="9c1b2-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c1b2-121">See also</span></span>

- [<span data-ttu-id="9c1b2-122">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="9c1b2-122">DTBLPAGE</span></span>](dtblpage.md)
- [<span data-ttu-id="9c1b2-123">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="9c1b2-123">Macros Related to Structures</span></span>](macros-related-to-structures.md)

