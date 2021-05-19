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
ms.openlocfilehash: 0a9bda8831f4a38b62d71a54115c40bb3374d97d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419317"
---
# <a name="sizeddtblgroupbox"></a><span data-ttu-id="57692-103">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="57692-103">SizedDtblGroupBox</span></span>

<span data-ttu-id="57692-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57692-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57692-105">Erstellt eine benannte Struktur, die eine [DTBLGROUPBOX-Struktur](dtblgroupbox.md) zum Beschreiben eines Gruppenfeldsteuerelements und einer Bezeichnung mit einer angegebenen Länge enthält.</span><span class="sxs-lookup"><span data-stu-id="57692-105">Creates a named structure that includes a [DTBLGROUPBOX](dtblgroupbox.md) structure for describing a group box control and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="57692-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="57692-106">Header file:</span></span>  <br/> |<span data-ttu-id="57692-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="57692-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="57692-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="57692-108">Related structure:</span></span>  <br/> |<span data-ttu-id="57692-109">**DTBLGROUPBOX**</span><span class="sxs-lookup"><span data-stu-id="57692-109">**DTBLGROUPBOX**</span></span> <br/> |
   
```cpp
SizedDtblGroupBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="57692-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="57692-110">Parameters</span></span>

<span data-ttu-id="57692-111">_n_</span><span class="sxs-lookup"><span data-stu-id="57692-111">_n_</span></span>
  
> <span data-ttu-id="57692-112">Länge der Bezeichnung des Gruppenfelds.</span><span class="sxs-lookup"><span data-stu-id="57692-112">Length of the group box's label.</span></span> 
    
<span data-ttu-id="57692-113">_u_</span><span class="sxs-lookup"><span data-stu-id="57692-113">_u_</span></span>
  
> <span data-ttu-id="57692-114">Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="57692-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="57692-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="57692-115">Remarks</span></span>

<span data-ttu-id="57692-116">Mit **dem Makro SizedDtblGroupBox** können Sie ein Gruppenfeldsteuerelement definieren, wenn die Länge der Bezeichnung bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="57692-116">The **SizedDtblGroupBox** macro lets you define a group box control when the length of the label is known.</span></span> <span data-ttu-id="57692-117">Die neue Struktur wird mit den folgenden Mitgliedern erstellt:</span><span class="sxs-lookup"><span data-stu-id="57692-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLGROUPBOX dtblgroupbox;
TCHAR lpszLabel[n];

```

<span data-ttu-id="57692-118">Führen Sie die folgende Gliederung aus, um einen Zeiger auf die resultierende Struktur des **SizedDtblGroupBox-Makros** als **DTBLGROUPBOX-Strukturzeiger** zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="57692-118">To use a pointer to the resulting structure from the **SizedDtblGroupBox** macro as a **DTBLGROUPBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblGroupBox = (LPDTBLGROUPBOX) &SizedDtblGroupBox;

```

## <a name="see-also"></a><span data-ttu-id="57692-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57692-119">See also</span></span>

- [<span data-ttu-id="57692-120">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="57692-120">DTBLGROUPBOX</span></span>](dtblgroupbox.md)
- [<span data-ttu-id="57692-121">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="57692-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

