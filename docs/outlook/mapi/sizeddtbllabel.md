---
title: SizedDtblLabel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblLabel
api_type:
- COM
ms.assetid: c7cb8cf9-7abd-4ee3-b88c-d61695f4ed31
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 1ae675d1d4adf841e18bbfc8990913136afe8b4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282705"
---
# <a name="sizeddtbllabel"></a><span data-ttu-id="f7baa-103">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="f7baa-103">SizedDtblLabel</span></span>

<span data-ttu-id="f7baa-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7baa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7baa-105">Erstellt eine benannte Struktur, die eine [DTBLLABEL](dtbllabel.md) -Struktur zur Beschreibung eines Label-Steuerelements und der zugeordneten Beschriftung einer angegebenen Länge enthält.</span><span class="sxs-lookup"><span data-stu-id="f7baa-105">Creates a named structure that includes a [DTBLLABEL](dtbllabel.md) structure for describing a label control and the associated label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f7baa-106">Angegeben in der Headerdatei:</span><span class="sxs-lookup"><span data-stu-id="f7baa-106">Specified in header file:</span></span>  <br/> |<span data-ttu-id="f7baa-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f7baa-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f7baa-108">Zugehörige Struktur</span><span class="sxs-lookup"><span data-stu-id="f7baa-108">Related structure</span></span>  <br/> |<span data-ttu-id="f7baa-109">**DTBLLABEL**</span><span class="sxs-lookup"><span data-stu-id="f7baa-109">**DTBLLABEL**</span></span> <br/> |
   
```cpp
SizedDtblLabel (n, u)
```

## <a name="parameters"></a><span data-ttu-id="f7baa-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7baa-110">Parameters</span></span>

<span data-ttu-id="f7baa-111">_n_</span><span class="sxs-lookup"><span data-stu-id="f7baa-111">_n_</span></span>
  
> <span data-ttu-id="f7baa-112">Länge der Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="f7baa-112">Length of the label.</span></span> <span data-ttu-id="f7baa-113">Dazu gehört das endGÜLTIGes NULL-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="f7baa-113">This includes the ending NULL character.</span></span> 
    
<span data-ttu-id="f7baa-114">_u_</span><span class="sxs-lookup"><span data-stu-id="f7baa-114">_u_</span></span>
  
> <span data-ttu-id="f7baa-115">Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="f7baa-115">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f7baa-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7baa-116">Remarks</span></span>

<span data-ttu-id="f7baa-117">Mit dem **SizedDtblLabel** -Makro können Sie eine Anzeige Tabellenbeschriftung definieren, wenn die Anzahl der Zeichen in der Bezeichnung bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="f7baa-117">The **SizedDtblLabel** macro lets you define a display table label when the number of characters in the label is known.</span></span> <span data-ttu-id="f7baa-118">Die neue Struktur wird mit den folgenden Elementen erstellt:</span><span class="sxs-lookup"><span data-stu-id="f7baa-118">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLLABEL dtbllabel;
TCHAR lpszLabelName[n];
```

<span data-ttu-id="f7baa-119">Wenn Sie einen Zeiger auf die resultierende Struktur aus dem **SizedDtblLabel** -Makro als **DTBLLABEL** -Struktur Zeiger verwenden möchten, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="f7baa-119">To use a pointer to the resulting structure from the **SizedDtblLabel** macro as a **DTBLLABEL** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblLabel = (LPDTBLLABEL) &SizedDtblLabel;
```

## <a name="see-also"></a><span data-ttu-id="f7baa-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7baa-120">See also</span></span>

- [<span data-ttu-id="f7baa-121">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="f7baa-121">DTBLLABEL</span></span>](dtbllabel.md)
- [<span data-ttu-id="f7baa-122">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="f7baa-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

