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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8861c8f86eaab6defb270b673e0ee200446aedb3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416265"
---
# <a name="sizeddtblcombobox"></a><span data-ttu-id="37a77-103">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="37a77-103">SizedDtblComboBox</span></span>
 
<span data-ttu-id="37a77-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37a77-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37a77-105">Erstellt eine benannte Struktur, die eine [DTBLCOMBOBOX-Struktur](dtblcombobox.md) zum Beschreiben eines Kombinationsfeldsteuerelements und die maximale Anzahl von Zeichen enthält, die in das zugeordnete Bearbeitungssteuerelement eingegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="37a77-105">Creates a named structure that includes a [DTBLCOMBOBOX](dtblcombobox.md) structure for describing a combo box control and the maximum number of characters that can be entered in the associated edit control.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="37a77-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="37a77-106">Header file:</span></span>  <br/> |<span data-ttu-id="37a77-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="37a77-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="37a77-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="37a77-108">Related structure:</span></span>  <br/> |<span data-ttu-id="37a77-109">**DTBLCOMBOBOX**</span><span class="sxs-lookup"><span data-stu-id="37a77-109">**DTBLCOMBOBOX**</span></span> <br/> |
   
```cpp
SizedDtblComboBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="37a77-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="37a77-110">Parameters</span></span>

<span data-ttu-id="37a77-111">_n_</span><span class="sxs-lookup"><span data-stu-id="37a77-111">_n_</span></span>
  
> <span data-ttu-id="37a77-112">Die Anzahl der Zeichen, die im Bearbeitungssteuerelement des Kombinationsfelds eingegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="37a77-112">Number of characters that can be entered in the combo box's edit control.</span></span> 
    
<span data-ttu-id="37a77-113">_u_</span><span class="sxs-lookup"><span data-stu-id="37a77-113">_u_</span></span>
  
> <span data-ttu-id="37a77-114">Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="37a77-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="37a77-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="37a77-115">Remarks</span></span>

<span data-ttu-id="37a77-116">Mit **dem Makro SizedDtblComboBox** können Sie ein Kombinationsfeld definieren, wenn die Länge der aktivierten Zeichenzeichenfolge bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="37a77-116">The **SizedDtblComboBox** macro lets you define a combo box when the length of the enabled character string is known.</span></span> <span data-ttu-id="37a77-117">Die neue Struktur wird mit den folgenden Mitgliedern erstellt:</span><span class="sxs-lookup"><span data-stu-id="37a77-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLCOMBOBOX dtblcombobox;
TCHAR lpszCharsAllowed[n];

```

<span data-ttu-id="37a77-118">Führen Sie die folgende Gliederung aus, um einen Zeiger auf die resultierende Struktur des **SizedDtblComboBox-Makros** als **DTBLCOMBOBOX-Strukturzeiger** zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="37a77-118">To use a pointer to the resulting structure from the **SizedDtblComboBox** macro as a **DTBLCOMBOBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblComboBox = (LPDTBLCOMBOBOX) &SizedDtblComboBox;

```

## <a name="see-also"></a><span data-ttu-id="37a77-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37a77-119">See also</span></span>

- [<span data-ttu-id="37a77-120">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="37a77-120">DTBLCOMBOBOX</span></span>](dtblcombobox.md)
- [<span data-ttu-id="37a77-121">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="37a77-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

