---
title: SizedDtblGroupBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblGroupBox
api_type:
- COM
ms.assetid: 7ca01bf7-5185-41cc-907e-01f256345997
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a3d8a76905aa9abb0e5bf001688608e03446704a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795551"
---
# <a name="sizeddtblgroupbox"></a><span data-ttu-id="3d851-103">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="3d851-103">SizedDtblGroupBox</span></span>

<span data-ttu-id="3d851-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3d851-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3d851-105">Erstellt eine benannte Struktur, die eine [DTBLGROUPBOX](dtblgroupbox.md) -Struktur für die Beschreibung ein Gruppenfeld-Steuerelement und ein Label mit einer angegebenen Länge enthält.</span><span class="sxs-lookup"><span data-stu-id="3d851-105">Creates a named structure that includes a [DTBLGROUPBOX](dtblgroupbox.md) structure for describing a group box control and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3d851-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="3d851-106">Header file:</span></span>  <br/> |<span data-ttu-id="3d851-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3d851-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3d851-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="3d851-108">Related structure:</span></span>  <br/> |<span data-ttu-id="3d851-109">**DTBLGROUPBOX**</span><span class="sxs-lookup"><span data-stu-id="3d851-109">**DTBLGROUPBOX**</span></span> <br/> |
   
```cpp
SizedDtblGroupBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="3d851-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d851-110">Parameters</span></span>

<span data-ttu-id="3d851-111">_n_</span><span class="sxs-lookup"><span data-stu-id="3d851-111">_n_</span></span>
  
> <span data-ttu-id="3d851-112">Länge der im Gruppenfeld Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="3d851-112">Length of the group box's label.</span></span> 
    
<span data-ttu-id="3d851-113">_u_</span><span class="sxs-lookup"><span data-stu-id="3d851-113">_u_</span></span>
  
> <span data-ttu-id="3d851-114">Der Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="3d851-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3d851-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d851-115">Remarks</span></span>

<span data-ttu-id="3d851-116">Das Makro **SizedDtblGroupBox** können Sie ein Gruppenfeld definieren, wenn die Länge des Bezeichnungsfelds bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="3d851-116">The **SizedDtblGroupBox** macro lets you define a group box control when the length of the label is known.</span></span> <span data-ttu-id="3d851-117">Die neue Struktur wird mit der folgenden Elemente erstellt:</span><span class="sxs-lookup"><span data-stu-id="3d851-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLGROUPBOX dtblgroupbox;
TCHAR lpszLabel[n];

```

<span data-ttu-id="3d851-118">Führen Sie einen Zeiger auf die resultierende Struktur aus dem Makro **SizedDtblGroupBox** als Zeiger Struktur **DTBLGROUPBOX** die folgende Umwandlung:</span><span class="sxs-lookup"><span data-stu-id="3d851-118">To use a pointer to the resulting structure from the **SizedDtblGroupBox** macro as a **DTBLGROUPBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblGroupBox = (LPDTBLGROUPBOX) &SizedDtblGroupBox;

```

## <a name="see-also"></a><span data-ttu-id="3d851-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d851-119">See also</span></span>

- [<span data-ttu-id="3d851-120">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="3d851-120">DTBLGROUPBOX</span></span>](dtblgroupbox.md)
- [<span data-ttu-id="3d851-121">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="3d851-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

