---
title: SzFindCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindCh
api_type:
- COM
ms.assetid: 3406d060-bfea-4cea-8253-2a9aeb9e8147
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b517eaffa56001d8c414888ee6cbc8ec4f49cf66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795697"
---
# <a name="szfindch"></a><span data-ttu-id="5a1fe-103">SzFindCh</span><span class="sxs-lookup"><span data-stu-id="5a1fe-103">SzFindCh</span></span>
 
<span data-ttu-id="5a1fe-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5a1fe-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5a1fe-105">Sucht nach dem ersten Vorkommen eines Zeichens in eine mit Null endende Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="5a1fe-105">Searches for the first occurrence of a character in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5a1fe-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="5a1fe-106">Header file:</span></span>  <br/> |<span data-ttu-id="5a1fe-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5a1fe-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5a1fe-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="5a1fe-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5a1fe-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5a1fe-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5a1fe-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="5a1fe-110">Called by:</span></span>  <br/> |<span data-ttu-id="5a1fe-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="5a1fe-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a><span data-ttu-id="5a1fe-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a1fe-112">Parameters</span></span>

<span data-ttu-id="5a1fe-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="5a1fe-113">_lpsz_</span></span>
  
> <span data-ttu-id="5a1fe-114">[in] Zeiger auf die Null endende Zeichenfolge, die durchsucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a1fe-114">[in] Pointer to the null-terminated string to be searched.</span></span> 
    
<span data-ttu-id="5a1fe-115">_Kapitel_</span><span class="sxs-lookup"><span data-stu-id="5a1fe-115">_ch_</span></span>
  
> <span data-ttu-id="5a1fe-116">[in] Das Zeichen an, nach dem gesucht wird.</span><span class="sxs-lookup"><span data-stu-id="5a1fe-116">[in] The character to be searched for.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5a1fe-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="5a1fe-117">Return value</span></span>

<span data-ttu-id="5a1fe-118">**SzFindCh** gibt einen Zeiger auf das erste Auftreten des Zeichens in der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="5a1fe-118">**SzFindCh** returns a pointer to the first occurrence of the character in the string.</span></span> <span data-ttu-id="5a1fe-119">Wenn das Zeichen nicht an einer beliebigen Stelle in der Zeichenfolge auftritt oder wenn der Parameter _Lpsz_ NULL ist, wird der Wert NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5a1fe-119">If the character does not occur anywhere in the string, or if the  _lpsz_ parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5a1fe-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5a1fe-120">Remarks</span></span>

<span data-ttu-id="5a1fe-121">Die Funktion **SzFindCh** sucht nach einer genauen Übereinstimmung nur; Es ist Beachtung von Groß-/Kleinschreibung und diakritische Unterschiede.</span><span class="sxs-lookup"><span data-stu-id="5a1fe-121">The **SzFindCh** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="5a1fe-122">Sucht in den Formaten Unicode und DBCS werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5a1fe-122">Searches in the Unicode and DBCS formats are supported.</span></span> 
  

