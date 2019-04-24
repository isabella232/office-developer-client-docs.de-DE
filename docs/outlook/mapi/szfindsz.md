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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9fc21a27cb6c9041bdd8976ce5f030f0ab9eb57f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345745"
---
# <a name="szfindsz"></a><span data-ttu-id="9e76c-103">SzFindSz</span><span class="sxs-lookup"><span data-stu-id="9e76c-103">SzFindSz</span></span>

  
  
<span data-ttu-id="9e76c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e76c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e76c-105">Sucht das erste Vorkommen einer null-terminierten Teilzeichenfolge in einer null-terminierten Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9e76c-105">Locates the first occurrence of a null-terminated substring in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9e76c-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="9e76c-106">Header file:</span></span>  <br/> |<span data-ttu-id="9e76c-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="9e76c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="9e76c-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="9e76c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9e76c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9e76c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9e76c-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="9e76c-110">Called by:</span></span>  <br/> |<span data-ttu-id="9e76c-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="9e76c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  LPCSTR lpszKey
);
```

## <a name="parameters"></a><span data-ttu-id="9e76c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e76c-112">Parameters</span></span>

 <span data-ttu-id="9e76c-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="9e76c-113">_lpsz_</span></span>
  
> <span data-ttu-id="9e76c-114">in Zeiger auf die zu durchsuchende NULL-terminierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9e76c-114">[in] Pointer to the null-terminated string to be searched.</span></span> <span data-ttu-id="9e76c-115">Der _lpsz_ -parameter darf 65536 Zeichen nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="9e76c-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
 <span data-ttu-id="9e76c-116">_lpszKey_</span><span class="sxs-lookup"><span data-stu-id="9e76c-116">_lpszKey_</span></span>
  
> <span data-ttu-id="9e76c-117">in Zeiger auf die mit NULL endende Teilzeichenfolge, nach der gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="9e76c-117">[in] Pointer to the null-terminated substring to be searched for.</span></span> <span data-ttu-id="9e76c-118">Der _lpszKey_ -parameter darf 65536 Zeichen nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="9e76c-118">The  _lpszKey_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9e76c-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9e76c-119">Return value</span></span>

 <span data-ttu-id="9e76c-120">**SzFindSz** gibt einen Zeiger auf das erste Zeichen des ersten Vorkommens der Teilzeichenfolge in der Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="9e76c-120">**SzFindSz** returns a pointer to the first character of the first occurrence of the substring in the string.</span></span> <span data-ttu-id="9e76c-121">Wenn die Teilzeichenfolge an keiner beliebigen Stelle in der Zeichenfolge auftritt, wenn _lpszKey_ größer als _lpsz_ist oder wenn einer der Parameter NULL ist, wird der Wert NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9e76c-121">If the substring does not occur anywhere in the string, if  _lpszKey_ is larger than  _lpsz_, or if either parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9e76c-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e76c-122">Remarks</span></span>

<span data-ttu-id="9e76c-123">Die **SzFindSz** -Funktion sucht nur nach einer genauen Übereinstimmung. Sie ist anfällig für Groß-/Kleinschreibung und diakritische Unterschiede.</span><span class="sxs-lookup"><span data-stu-id="9e76c-123">The **SzFindSz** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="9e76c-124">Suchvorgänge in Unicode-und DBCS-Formaten werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9e76c-124">Searches in Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="9e76c-125">Die Längenbeschränkung für beide Parameter ist in Zeichen, nicht unbedingt in Bytes.</span><span class="sxs-lookup"><span data-stu-id="9e76c-125">The length limit on both parameters is in characters, not necessarily bytes.</span></span> 
  

