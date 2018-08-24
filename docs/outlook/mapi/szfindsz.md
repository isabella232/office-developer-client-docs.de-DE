---
title: SzFindSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindSz
api_type:
- COM
ms.assetid: f4584569-1246-4ac9-a404-48284e4920d7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0075db0a515166c5185657daf3fc6b1e121d6672
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585122"
---
# <a name="szfindsz"></a><span data-ttu-id="41514-103">SzFindSz</span><span class="sxs-lookup"><span data-stu-id="41514-103">SzFindSz</span></span>

  
  
<span data-ttu-id="41514-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41514-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="41514-105">Sucht den ersten Vorkommens einer Teilzeichenfolge mit Null endende in eine mit Null endende Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="41514-105">Locates the first occurrence of a null-terminated substring in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="41514-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="41514-106">Header file:</span></span>  <br/> |<span data-ttu-id="41514-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="41514-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="41514-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="41514-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="41514-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="41514-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="41514-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="41514-110">Called by:</span></span>  <br/> |<span data-ttu-id="41514-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="41514-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  LPCSTR lpszKey
);
```

## <a name="parameters"></a><span data-ttu-id="41514-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="41514-112">Parameters</span></span>

 <span data-ttu-id="41514-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="41514-113">_lpsz_</span></span>
  
> <span data-ttu-id="41514-114">[in] Zeiger auf die Null endende Zeichenfolge, die durchsucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="41514-114">[in] Pointer to the null-terminated string to be searched.</span></span> <span data-ttu-id="41514-115">Der Parameter _Lpsz_ muss 65536 Zeichen nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="41514-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
 <span data-ttu-id="41514-116">_lpszKey_</span><span class="sxs-lookup"><span data-stu-id="41514-116">_lpszKey_</span></span>
  
> <span data-ttu-id="41514-117">[in] Zeiger auf Null endende Teilzeichenfolge gesucht werden.</span><span class="sxs-lookup"><span data-stu-id="41514-117">[in] Pointer to the null-terminated substring to be searched for.</span></span> <span data-ttu-id="41514-118">Der Parameter _LpszKey_ muss 65536 Zeichen nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="41514-118">The  _lpszKey_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="41514-119">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="41514-119">Return value</span></span>

 <span data-ttu-id="41514-120">**SzFindSz** gibt einen Zeiger auf das erste Zeichen des ersten Vorkommens der Teilzeichenfolge in der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="41514-120">**SzFindSz** returns a pointer to the first character of the first occurrence of the substring in the string.</span></span> <span data-ttu-id="41514-121">Wenn die Teilzeichenfolge nicht an einer beliebigen Stelle in der Zeichenfolge auftritt, wenn _LpszKey_ größer als _Lpsz_ist oder einer der Parameter NULL ist, wird der Wert NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="41514-121">If the substring does not occur anywhere in the string, if  _lpszKey_ is larger than  _lpsz_, or if either parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="41514-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41514-122">Remarks</span></span>

<span data-ttu-id="41514-123">Die Funktion **SzFindSz** sucht nach einer genauen Übereinstimmung nur; Es ist Beachtung von Groß-/Kleinschreibung und diakritische Unterschiede.</span><span class="sxs-lookup"><span data-stu-id="41514-123">The **SzFindSz** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="41514-124">Suchvorgänge in Unicode und DBCS-Formate werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="41514-124">Searches in Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="41514-125">Die maximale Länge beide Parameter ist in Zeichen, was nicht notwendigerweise Bytes.</span><span class="sxs-lookup"><span data-stu-id="41514-125">The length limit on both parameters is in characters, not necessarily bytes.</span></span> 
  

