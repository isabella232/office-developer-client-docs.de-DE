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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b5b9c42d944ad9d3ce92e99d08d29964944c8028
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437644"
---
# <a name="sizeddtbledit"></a><span data-ttu-id="c6ec1-103">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="c6ec1-103">SizedDtblEdit</span></span>

<span data-ttu-id="c6ec1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6ec1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6ec1-105">Erstellt eine benannte Struktur, die eine [DTBLEDIT-Struktur](dtbledit.md) zum Beschreiben eines Bearbeitungssteuerelements und die maximale Anzahl von Zeichen enthält, die in das Steuerelement eingegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-105">Creates a named structure that includes a [DTBLEDIT](dtbledit.md) structure for describing an edit control and the maximum number of characters that can be entered in the control.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c6ec1-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c6ec1-106">Header file:</span></span>  <br/> |<span data-ttu-id="c6ec1-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c6ec1-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c6ec1-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="c6ec1-108">Related structure:</span></span>  <br/> |<span data-ttu-id="c6ec1-109">**DTBLEDIT**</span><span class="sxs-lookup"><span data-stu-id="c6ec1-109">**DTBLEDIT**</span></span> <br/> |
   
```cpp
SizedDtblEdit (n, u)
```

## <a name="parameters"></a><span data-ttu-id="c6ec1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6ec1-110">Parameters</span></span>

<span data-ttu-id="c6ec1-111">_n_</span><span class="sxs-lookup"><span data-stu-id="c6ec1-111">_n_</span></span>
  
> <span data-ttu-id="c6ec1-112">Maximale Anzahl von Zeichen, die im Bearbeitungssteuerelement eingegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-112">Maximum number of characters that can be entered in the edit control.</span></span>
    
<span data-ttu-id="c6ec1-113">_u_</span><span class="sxs-lookup"><span data-stu-id="c6ec1-113">_u_</span></span>
  
> <span data-ttu-id="c6ec1-114">Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c6ec1-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c6ec1-115">Remarks</span></span>

<span data-ttu-id="c6ec1-116">Mit **dem Makro SizedDtblEdit** können Sie ein Bearbeitungssteuerelement definieren, wenn die Anzahl der aktivierten Zeichen bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-116">The **SizedDtblEdit** macro lets you define an edit control when the number of enabled characters is known.</span></span> <span data-ttu-id="c6ec1-117">Die neue Struktur wird mit den folgenden Mitgliedern erstellt:</span><span class="sxs-lookup"><span data-stu-id="c6ec1-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLEDIT dtbledit;
TCHAR lpszCharsAllowed[n];

```

<span data-ttu-id="c6ec1-118">Führen Sie die folgende Gliederung aus, um einen Zeiger auf die resultierende Struktur des **SizeDtblEdit-Makros** als **DTBLEDIT-Strukturzeiger** zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="c6ec1-118">To use a pointer to the resulting structure from the **SizedDtblEdit** macro as a **DTBLEDIT** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblEdit = (LPDTBLEDIT) &SizedDtblEdit;

```

## <a name="see-also"></a><span data-ttu-id="c6ec1-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6ec1-119">See also</span></span>

- [<span data-ttu-id="c6ec1-120">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="c6ec1-120">DTBLEDIT</span></span>](dtbledit.md)
- [<span data-ttu-id="c6ec1-121">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="c6ec1-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

