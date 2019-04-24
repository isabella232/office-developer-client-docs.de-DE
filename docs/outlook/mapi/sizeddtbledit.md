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
ms.openlocfilehash: b5b9c42d944ad9d3ce92e99d08d29964944c8028
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282803"
---
# <a name="sizeddtbledit"></a><span data-ttu-id="caa50-103">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="caa50-103">SizedDtblEdit</span></span>

<span data-ttu-id="caa50-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="caa50-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="caa50-105">Erstellt eine benannte Struktur, die eine [DTBLEDIT](dtbledit.md) -Struktur zur Beschreibung eines Bearbeitungssteuerelements und die maximale Anzahl von Zeichen enthält, die im Steuerelement eingegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="caa50-105">Creates a named structure that includes a [DTBLEDIT](dtbledit.md) structure for describing an edit control and the maximum number of characters that can be entered in the control.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="caa50-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="caa50-106">Header file:</span></span>  <br/> |<span data-ttu-id="caa50-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="caa50-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="caa50-108">Zugehörige Struktur:</span><span class="sxs-lookup"><span data-stu-id="caa50-108">Related structure:</span></span>  <br/> |<span data-ttu-id="caa50-109">**DTBLEDIT**</span><span class="sxs-lookup"><span data-stu-id="caa50-109">**DTBLEDIT**</span></span> <br/> |
   
```cpp
SizedDtblEdit (n, u)
```

## <a name="parameters"></a><span data-ttu-id="caa50-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="caa50-110">Parameters</span></span>

<span data-ttu-id="caa50-111">_n_</span><span class="sxs-lookup"><span data-stu-id="caa50-111">_n_</span></span>
  
> <span data-ttu-id="caa50-112">Maximale Anzahl von Zeichen, die im Bearbeitungssteuerelement eingegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="caa50-112">Maximum number of characters that can be entered in the edit control.</span></span>
    
<span data-ttu-id="caa50-113">_u_</span><span class="sxs-lookup"><span data-stu-id="caa50-113">_u_</span></span>
  
> <span data-ttu-id="caa50-114">Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="caa50-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="caa50-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="caa50-115">Remarks</span></span>

<span data-ttu-id="caa50-116">Mit dem **SizedDtblEdit** -Makro können Sie ein Bearbeitungssteuerelement definieren, wenn die Anzahl der aktivierten Zeichen bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="caa50-116">The **SizedDtblEdit** macro lets you define an edit control when the number of enabled characters is known.</span></span> <span data-ttu-id="caa50-117">Die neue Struktur wird mit den folgenden Elementen erstellt:</span><span class="sxs-lookup"><span data-stu-id="caa50-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLEDIT dtbledit;
TCHAR lpszCharsAllowed[n];

```

<span data-ttu-id="caa50-118">Wenn Sie einen Zeiger auf die resultierende Struktur aus dem **SizedDtblEdit** -Makro als **DTBLEDIT** -Struktur Zeiger verwenden möchten, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="caa50-118">To use a pointer to the resulting structure from the **SizedDtblEdit** macro as a **DTBLEDIT** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblEdit = (LPDTBLEDIT) &SizedDtblEdit;

```

## <a name="see-also"></a><span data-ttu-id="caa50-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="caa50-119">See also</span></span>

- [<span data-ttu-id="caa50-120">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="caa50-120">DTBLEDIT</span></span>](dtbledit.md)
- [<span data-ttu-id="caa50-121">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="caa50-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

