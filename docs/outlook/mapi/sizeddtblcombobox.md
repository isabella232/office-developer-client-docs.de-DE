---
title: SizedDtblComboBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblComboBox
api_type:
- COM
ms.assetid: 1e5ea9f2-1029-4584-845a-890d3e956036
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fea2b496a34d7aa7f9469158fae14daf6a770608
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795555"
---
# <a name="sizeddtblcombobox"></a><span data-ttu-id="aa7af-103">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="aa7af-103">SizedDtblComboBox</span></span>
 
<span data-ttu-id="aa7af-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aa7af-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aa7af-105">Erstellt eine benannte Struktur, die enthält eine [DTBLCOMBOBOX](dtblcombobox.md) -Struktur für die Beschreibung ein Kombinationsfeld-Steuerelement und die maximale Anzahl von Zeichen, die in der zugehörigen Bearbeitungssteuerelement eingegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="aa7af-105">Creates a named structure that includes a [DTBLCOMBOBOX](dtblcombobox.md) structure for describing a combo box control and the maximum number of characters that can be entered in the associated edit control.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="aa7af-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="aa7af-106">Header file:</span></span>  <br/> |<span data-ttu-id="aa7af-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aa7af-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="aa7af-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="aa7af-108">Related structure:</span></span>  <br/> |<span data-ttu-id="aa7af-109">**DTBLCOMBOBOX**</span><span class="sxs-lookup"><span data-stu-id="aa7af-109">**DTBLCOMBOBOX**</span></span> <br/> |
   
```cpp
SizedDtblComboBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="aa7af-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa7af-110">Parameters</span></span>

<span data-ttu-id="aa7af-111">_n_</span><span class="sxs-lookup"><span data-stu-id="aa7af-111">_n_</span></span>
  
> <span data-ttu-id="aa7af-112">Anzahl der Zeichen, die in des Kombinationsfelds eingegeben werden können edit-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="aa7af-112">Number of characters that can be entered in the combo box's edit control.</span></span> 
    
<span data-ttu-id="aa7af-113">_u_</span><span class="sxs-lookup"><span data-stu-id="aa7af-113">_u_</span></span>
  
> <span data-ttu-id="aa7af-114">Der Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="aa7af-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="aa7af-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="aa7af-115">Remarks</span></span>

<span data-ttu-id="aa7af-116">Das Makro **SizedDtblComboBox** können Sie einem Kombinationsfeld definieren, wenn die Länge der Zeichenfolge aktiviert bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="aa7af-116">The **SizedDtblComboBox** macro lets you define a combo box when the length of the enabled character string is known.</span></span> <span data-ttu-id="aa7af-117">Die neue Struktur wird mit der folgenden Elemente erstellt:</span><span class="sxs-lookup"><span data-stu-id="aa7af-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLCOMBOBOX dtblcombobox;
TCHAR lpszCharsAllowed[n];

```

<span data-ttu-id="aa7af-118">Führen Sie einen Zeiger auf die resultierende Struktur aus dem Makro **SizedDtblComboBox** als Zeiger Struktur **DTBLCOMBOBOX** die folgende Umwandlung:</span><span class="sxs-lookup"><span data-stu-id="aa7af-118">To use a pointer to the resulting structure from the **SizedDtblComboBox** macro as a **DTBLCOMBOBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblComboBox = (LPDTBLCOMBOBOX) &SizedDtblComboBox;

```

## <a name="see-also"></a><span data-ttu-id="aa7af-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa7af-119">See also</span></span>

- [<span data-ttu-id="aa7af-120">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="aa7af-120">DTBLCOMBOBOX</span></span>](dtblcombobox.md)
- [<span data-ttu-id="aa7af-121">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="aa7af-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)
