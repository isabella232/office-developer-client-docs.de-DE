---
title: SzFindLastCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindLastCh
api_type:
- COM
ms.assetid: 7c3e5a71-7b78-4328-b8ee-265cc4da4be5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c221f98d6551ea63971dd378d522c1f2bebb312b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795699"
---
# <a name="szfindlastch"></a><span data-ttu-id="a5d6e-103">SzFindLastCh</span><span class="sxs-lookup"><span data-stu-id="a5d6e-103">SzFindLastCh</span></span>

  
  
<span data-ttu-id="a5d6e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a5d6e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a5d6e-105">Sucht das letzte Vorkommen eines Zeichens in eine mit Null endende Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="a5d6e-105">Searches for the last occurrence of a character in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a5d6e-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="a5d6e-106">Header file:</span></span>  <br/> |<span data-ttu-id="a5d6e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a5d6e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a5d6e-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="a5d6e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a5d6e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a5d6e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a5d6e-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="a5d6e-110">Called by:</span></span>  <br/> |<span data-ttu-id="a5d6e-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="a5d6e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindLastCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a><span data-ttu-id="a5d6e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5d6e-112">Parameters</span></span>

 <span data-ttu-id="a5d6e-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="a5d6e-113">_lpsz_</span></span>
  
> <span data-ttu-id="a5d6e-114">[in] Zeiger auf die Null endende Zeichenfolge, die durchsucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="a5d6e-114">[in] Pointer to the null-terminated string to be searched.</span></span> 
    
 <span data-ttu-id="a5d6e-115">_Kapitel_</span><span class="sxs-lookup"><span data-stu-id="a5d6e-115">_ch_</span></span>
  
> <span data-ttu-id="a5d6e-116">[in] Das Zeichen an, nach dem gesucht wird.</span><span class="sxs-lookup"><span data-stu-id="a5d6e-116">[in] The character to be searched for.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a5d6e-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a5d6e-117">Return value</span></span>

 <span data-ttu-id="a5d6e-118">**SzFindLastCh** gibt einen Zeiger auf das letzte Vorkommen des Zeichens in der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="a5d6e-118">**SzFindLastCh** returns a pointer to the last occurrence of the character in the string.</span></span> <span data-ttu-id="a5d6e-119">Wenn das Zeichen nicht an einer beliebigen Stelle in der Zeichenfolge auftritt oder wenn der Parameter _Lpsz_ NULL ist, wird der Wert NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a5d6e-119">If the character does not occur anywhere in the string, or if the  _lpsz_ parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a5d6e-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5d6e-120">Remarks</span></span>

<span data-ttu-id="a5d6e-121">Die Funktion **SzFindLastCh** sucht nach einer genauen Übereinstimmung nur; Es ist Beachtung von Groß-/Kleinschreibung und diakritische Unterschiede.</span><span class="sxs-lookup"><span data-stu-id="a5d6e-121">The **SzFindLastCh** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="a5d6e-122">Sucht in den Formaten Unicode und DBCS werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a5d6e-122">Searches in the Unicode and DBCS formats are supported.</span></span> 
  

