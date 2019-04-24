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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0a9bda8831f4a38b62d71a54115c40bb3374d97d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282733"
---
# <a name="sizeddtblgroupbox"></a><span data-ttu-id="527d8-103">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="527d8-103">SizedDtblGroupBox</span></span>

<span data-ttu-id="527d8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="527d8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="527d8-105">Erstellt eine benannte Struktur, die eine [DTBLGROUPBOX](dtblgroupbox.md) -Struktur zur Beschreibung eines Gruppenfeld-Steuerelements und einer Beschriftung einer angegebenen Länge enthält.</span><span class="sxs-lookup"><span data-stu-id="527d8-105">Creates a named structure that includes a [DTBLGROUPBOX](dtblgroupbox.md) structure for describing a group box control and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="527d8-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="527d8-106">Header file:</span></span>  <br/> |<span data-ttu-id="527d8-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="527d8-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="527d8-108">Zugehörige Struktur:</span><span class="sxs-lookup"><span data-stu-id="527d8-108">Related structure:</span></span>  <br/> |<span data-ttu-id="527d8-109">**DTBLGROUPBOX**</span><span class="sxs-lookup"><span data-stu-id="527d8-109">**DTBLGROUPBOX**</span></span> <br/> |
   
```cpp
SizedDtblGroupBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="527d8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="527d8-110">Parameters</span></span>

<span data-ttu-id="527d8-111">_n_</span><span class="sxs-lookup"><span data-stu-id="527d8-111">_n_</span></span>
  
> <span data-ttu-id="527d8-112">Länge der Beschriftung des Gruppenfelds.</span><span class="sxs-lookup"><span data-stu-id="527d8-112">Length of the group box's label.</span></span> 
    
<span data-ttu-id="527d8-113">_u_</span><span class="sxs-lookup"><span data-stu-id="527d8-113">_u_</span></span>
  
> <span data-ttu-id="527d8-114">Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="527d8-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="527d8-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="527d8-115">Remarks</span></span>

<span data-ttu-id="527d8-116">Mit dem **SizedDtblGroupBox** -Makro können Sie ein Gruppenfeld-Steuerelement definieren, wenn die Länge der Bezeichnung bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="527d8-116">The **SizedDtblGroupBox** macro lets you define a group box control when the length of the label is known.</span></span> <span data-ttu-id="527d8-117">Die neue Struktur wird mit den folgenden Elementen erstellt:</span><span class="sxs-lookup"><span data-stu-id="527d8-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLGROUPBOX dtblgroupbox;
TCHAR lpszLabel[n];

```

<span data-ttu-id="527d8-118">Wenn Sie einen Zeiger auf die resultierende Struktur aus dem **SizedDtblGroupBox** -Makro als **DTBLGROUPBOX** -Struktur Zeiger verwenden möchten, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="527d8-118">To use a pointer to the resulting structure from the **SizedDtblGroupBox** macro as a **DTBLGROUPBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblGroupBox = (LPDTBLGROUPBOX) &SizedDtblGroupBox;

```

## <a name="see-also"></a><span data-ttu-id="527d8-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="527d8-119">See also</span></span>

- [<span data-ttu-id="527d8-120">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="527d8-120">DTBLGROUPBOX</span></span>](dtblgroupbox.md)
- [<span data-ttu-id="527d8-121">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="527d8-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

