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
ms.openlocfilehash: 8861c8f86eaab6defb270b673e0ee200446aedb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282824"
---
# <a name="sizeddtblcombobox"></a><span data-ttu-id="3044b-103">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="3044b-103">SizedDtblComboBox</span></span>
 
<span data-ttu-id="3044b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3044b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3044b-105">Erstellt eine benannte Struktur, die eine [DTBLCOMBOBOX](dtblcombobox.md) -Struktur zur Beschreibung eines Kombinationsfeld-Steuerelements und die maximale Anzahl von Zeichen enthält, die im zugeordneten Bearbeitungssteuerelement eingegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="3044b-105">Creates a named structure that includes a [DTBLCOMBOBOX](dtblcombobox.md) structure for describing a combo box control and the maximum number of characters that can be entered in the associated edit control.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3044b-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="3044b-106">Header file:</span></span>  <br/> |<span data-ttu-id="3044b-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="3044b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3044b-108">Zugehörige Struktur:</span><span class="sxs-lookup"><span data-stu-id="3044b-108">Related structure:</span></span>  <br/> |<span data-ttu-id="3044b-109">**DTBLCOMBOBOX**</span><span class="sxs-lookup"><span data-stu-id="3044b-109">**DTBLCOMBOBOX**</span></span> <br/> |
   
```cpp
SizedDtblComboBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="3044b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3044b-110">Parameters</span></span>

<span data-ttu-id="3044b-111">_n_</span><span class="sxs-lookup"><span data-stu-id="3044b-111">_n_</span></span>
  
> <span data-ttu-id="3044b-112">Die Anzahl der Zeichen, die im Bearbeitungssteuerelement des Kombinationsfelds eingegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="3044b-112">Number of characters that can be entered in the combo box's edit control.</span></span> 
    
<span data-ttu-id="3044b-113">_u_</span><span class="sxs-lookup"><span data-stu-id="3044b-113">_u_</span></span>
  
> <span data-ttu-id="3044b-114">Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="3044b-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3044b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3044b-115">Remarks</span></span>

<span data-ttu-id="3044b-116">Mit dem **SizedDtblComboBox** -Makro können Sie ein Kombinationsfeld definieren, wenn die Länge der aktivierten Zeichenfolge bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="3044b-116">The **SizedDtblComboBox** macro lets you define a combo box when the length of the enabled character string is known.</span></span> <span data-ttu-id="3044b-117">Die neue Struktur wird mit den folgenden Elementen erstellt:</span><span class="sxs-lookup"><span data-stu-id="3044b-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLCOMBOBOX dtblcombobox;
TCHAR lpszCharsAllowed[n];

```

<span data-ttu-id="3044b-118">Wenn Sie einen Zeiger auf die resultierende Struktur aus dem **SizedDtblComboBox** -Makro als **DTBLCOMBOBOX** -Struktur Zeiger verwenden möchten, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="3044b-118">To use a pointer to the resulting structure from the **SizedDtblComboBox** macro as a **DTBLCOMBOBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblComboBox = (LPDTBLCOMBOBOX) &SizedDtblComboBox;

```

## <a name="see-also"></a><span data-ttu-id="3044b-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3044b-119">See also</span></span>

- [<span data-ttu-id="3044b-120">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="3044b-120">DTBLCOMBOBOX</span></span>](dtblcombobox.md)
- [<span data-ttu-id="3044b-121">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="3044b-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

