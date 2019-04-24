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
ms.openlocfilehash: 522c67b19656c00ea169def98a42ca2b3c1db840
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345241"
---
# <a name="szfindch"></a><span data-ttu-id="7c832-103">SzFindCh</span><span class="sxs-lookup"><span data-stu-id="7c832-103">SzFindCh</span></span>
 
<span data-ttu-id="7c832-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c832-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c832-105">Sucht nach dem ersten Vorkommen eines Zeichens in einer null-terminierten Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="7c832-105">Searches for the first occurrence of a character in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7c832-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="7c832-106">Header file:</span></span>  <br/> |<span data-ttu-id="7c832-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7c832-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="7c832-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="7c832-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7c832-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7c832-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7c832-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="7c832-110">Called by:</span></span>  <br/> |<span data-ttu-id="7c832-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="7c832-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a><span data-ttu-id="7c832-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c832-112">Parameters</span></span>

<span data-ttu-id="7c832-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="7c832-113">_lpsz_</span></span>
  
> <span data-ttu-id="7c832-114">in Zeiger auf die zu durchsuchende NULL-terminierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="7c832-114">[in] Pointer to the null-terminated string to be searched.</span></span> 
    
<span data-ttu-id="7c832-115">_ch_</span><span class="sxs-lookup"><span data-stu-id="7c832-115">_ch_</span></span>
  
> <span data-ttu-id="7c832-116">in Das Zeichen, nach dem gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="7c832-116">[in] The character to be searched for.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7c832-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7c832-117">Return value</span></span>

<span data-ttu-id="7c832-118">**SzFindCh** gibt einen Zeiger auf das erste Vorkommen des Zeichens in der Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="7c832-118">**SzFindCh** returns a pointer to the first occurrence of the character in the string.</span></span> <span data-ttu-id="7c832-119">Wenn das Zeichen nicht an einer beliebigen Stelle in der Zeichenfolge auftritt oder wenn der _lpsz_ -Parameter NULL ist, wird der Wert NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7c832-119">If the character does not occur anywhere in the string, or if the  _lpsz_ parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7c832-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c832-120">Remarks</span></span>

<span data-ttu-id="7c832-121">Die **SzFindCh** -Funktion sucht nur nach einer genauen Übereinstimmung. Sie ist anfällig für Groß-/Kleinschreibung und diakritische Unterschiede.</span><span class="sxs-lookup"><span data-stu-id="7c832-121">The **SzFindCh** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="7c832-122">Die Suche im Unicode-und im DBCS-Format wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7c832-122">Searches in the Unicode and DBCS formats are supported.</span></span> 
  

