---
title: IsBadBoundedStringPtr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 888c60e3-7376-4d66-8ee2-ce81abafb185
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9d5ebb0e16138c3cc65ff6fd7c635e5498c9c1ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278834"
---
# <a name="isbadboundedstringptr"></a><span data-ttu-id="ffdd0-103">IsBadBoundedStringPtr</span><span class="sxs-lookup"><span data-stu-id="ffdd0-103">IsBadBoundedStringPtr</span></span>

  
  
<span data-ttu-id="ffdd0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ffdd0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ffdd0-105">Überprüft, ob der aufrufende Prozess über Lesezugriff auf den angegebenen Speicherbereich verfügt.</span><span class="sxs-lookup"><span data-stu-id="ffdd0-105">Verifies that the calling process has read access to the specified range of memory.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ffdd0-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="ffdd0-106">Header file:</span></span>  <br/> |<span data-ttu-id="ffdd0-107">mapiwin. h</span><span class="sxs-lookup"><span data-stu-id="ffdd0-107">mapiwin.h</span></span>  <br/> |
|<span data-ttu-id="ffdd0-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="ffdd0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ffdd0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ffdd0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ffdd0-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="ffdd0-110">Called by:</span></span>  <br/> |<span data-ttu-id="ffdd0-111">Client Anwendungen und Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="ffdd0-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
BOOL IsBadBoundedStringPtr(
  const void FAR* lpsz,
  UINT cchMax
);
```

## <a name="parameters"></a><span data-ttu-id="ffdd0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ffdd0-112">Parameters</span></span>

 <span data-ttu-id="ffdd0-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="ffdd0-113">_lpsz_</span></span>
  
> <span data-ttu-id="ffdd0-114">in Zeiger auf eine NULL-terminierte ASCII-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="ffdd0-114">[in] Pointer to a null-terminated ASCII string.</span></span>
    
 <span data-ttu-id="ffdd0-115">_cchMax_</span><span class="sxs-lookup"><span data-stu-id="ffdd0-115">_cchMax_</span></span>
  
> <span data-ttu-id="ffdd0-116">in Die maximale Größe der Zeichenfolge in chars.</span><span class="sxs-lookup"><span data-stu-id="ffdd0-116">[in] The maximum size of the string, in CHARs.</span></span> <span data-ttu-id="ffdd0-117">Die Funktion überprüft den Lesezugriff in allen Zeichen bis zum abschließenden NULL-Zeichen der Zeichenfolge oder bis zur Anzahl der Zeichen, die durch diesen Parameter angegeben werden, je nachdem, welcher Wert kleiner ist.</span><span class="sxs-lookup"><span data-stu-id="ffdd0-117">The function checks for read access in all characters up to the terminating null character of the string, or up to the number of characters specified by this parameter, whichever is smaller.</span></span> <span data-ttu-id="ffdd0-118">Wenn dieser Parameter gleich NULL ist, ist der Rückgabewert NULL.</span><span class="sxs-lookup"><span data-stu-id="ffdd0-118">If this parameter is zero, the return value is zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ffdd0-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ffdd0-119">Return value</span></span>

<span data-ttu-id="ffdd0-120">Der Rückgabewert ist 0 (null), wenn der aufrufende Prozess Lesezugriff auf alle Zeichen bis zum beendenden Nullzeichen der Zeichenfolge hat, oder Lesezugriff bis zur Anzahl von Zeichen, die durch _cchMax_angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ffdd0-120">The return value is zero when the calling process has read access to all characters up to the terminating null character of the string, or read access up to the number of characters specified by  _cchMax_.</span></span>
  
<span data-ttu-id="ffdd0-121">Der Rückgabewert ist ungleich 0 (null), wenn der aufrufende Prozess keinen Lesezugriff auf alle Zeichen bis zum beendenden Nullzeichen der Zeichenfolge hat, oder Lesezugriff bis zur Anzahl von Zeichen, die durch _cchMax_angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ffdd0-121">The return value is non-zero when the calling process does not have read access to all characters up to the terminating null character of the string, or read access up to the number of characters specified by  _cchMax_.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ffdd0-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ffdd0-122">Remarks</span></span>

<span data-ttu-id="ffdd0-123">Die **IsBadBoundedStringPtr** -Funktion entspricht der Verwendung von **IsBadStringPtr**.</span><span class="sxs-lookup"><span data-stu-id="ffdd0-123">The **IsBadBoundedStringPtr** function is equivalent to using **IsBadStringPtr**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ffdd0-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ffdd0-124">See also</span></span>



[<span data-ttu-id="ffdd0-125">IsBadStringPtr</span><span class="sxs-lookup"><span data-stu-id="ffdd0-125">IsBadStringPtr</span></span>](https://msdn.microsoft.com/library/windows/desktop/aa366714%28v=vs.85%29.aspx)

