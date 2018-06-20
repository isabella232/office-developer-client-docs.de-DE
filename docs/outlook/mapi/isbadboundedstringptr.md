---
title: IsBadBoundedStringPtr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 888c60e3-7376-4d66-8ee2-ce81abafb185
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0e4e5d5910a7ff3551057760f065e79155d65e49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792825"
---
# <a name="isbadboundedstringptr"></a><span data-ttu-id="ade7e-103">IsBadBoundedStringPtr</span><span class="sxs-lookup"><span data-stu-id="ade7e-103">IsBadBoundedStringPtr</span></span>

  
  
<span data-ttu-id="ade7e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ade7e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ade7e-105">Überprüft, ob der aufrufende Prozess Lesezugriff auf den angegebenen Bereich des Arbeitsspeichers verfügt.</span><span class="sxs-lookup"><span data-stu-id="ade7e-105">Verifies that the calling process has read access to the specified range of memory.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ade7e-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="ade7e-106">Header file:</span></span>  <br/> |<span data-ttu-id="ade7e-107">mapiwin.h</span><span class="sxs-lookup"><span data-stu-id="ade7e-107">mapiwin.h</span></span>  <br/> |
|<span data-ttu-id="ade7e-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="ade7e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ade7e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ade7e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ade7e-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="ade7e-110">Called by:</span></span>  <br/> |<span data-ttu-id="ade7e-111">Clientanwendungen und -Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="ade7e-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
BOOL IsBadBoundedStringPtr(
  const void FAR* lpsz,
  UINT cchMax
);
```

## <a name="parameters"></a><span data-ttu-id="ade7e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ade7e-112">Parameters</span></span>

 <span data-ttu-id="ade7e-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="ade7e-113">_lpsz_</span></span>
  
> <span data-ttu-id="ade7e-114">[in] Zeiger auf eine mit Null endende ASCII-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="ade7e-114">[in] Pointer to a null-terminated ASCII string.</span></span>
    
 <span data-ttu-id="ade7e-115">_cchMax_</span><span class="sxs-lookup"><span data-stu-id="ade7e-115">_cchMax_</span></span>
  
> <span data-ttu-id="ade7e-116">[in] Die maximale Größe der Zeichenfolge in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="ade7e-116">[in] The maximum size of the string, in CHARs.</span></span> <span data-ttu-id="ade7e-117">Die Funktion für Lesezugriff für alle Zeichen bis zu abschließendes Null-Zeichen der Zeichenfolge überprüft, oder bis zu die Anzahl der Zeichen, die von diesem Parameter angegebene, je nachdem, was kleiner ist.</span><span class="sxs-lookup"><span data-stu-id="ade7e-117">The function checks for read access in all characters up to the terminating null character of the string, or up to the number of characters specified by this parameter, whichever is smaller.</span></span> <span data-ttu-id="ade7e-118">Wenn dieser Parameter auf 0 (null) ist, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="ade7e-118">If this parameter is zero, the return value is zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ade7e-119">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="ade7e-119">Return value</span></span>

<span data-ttu-id="ade7e-120">Der Rückgabewert ist 0 (null), wenn der aufrufende Prozess Lesezugriff für alle Zeichen bis zu abschließendes Null-Zeichen der Zeichenfolge oder Lesezugriff bis zu der Anzahl von Zeichen durch _CchMax_angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="ade7e-120">The return value is zero when the calling process has read access to all characters up to the terminating null character of the string, or read access up to the number of characters specified by  _cchMax_.</span></span>
  
<span data-ttu-id="ade7e-121">Der Rückgabewert ist ungleich NULL, wenn der aufrufende Prozess nicht Lesezugriff für alle Zeichen bis zu abschließendes Null-Zeichen der Zeichenfolge oder Lesezugriff bis zu der Anzahl von Zeichen durch _CchMax_angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ade7e-121">The return value is non-zero when the calling process does not have read access to all characters up to the terminating null character of the string, or read access up to the number of characters specified by  _cchMax_.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ade7e-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ade7e-122">Remarks</span></span>

<span data-ttu-id="ade7e-123">Die Funktion **IsBadBoundedStringPtr** entspricht **IsBadStringPtr**verwenden.</span><span class="sxs-lookup"><span data-stu-id="ade7e-123">The **IsBadBoundedStringPtr** function is equivalent to using **IsBadStringPtr**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ade7e-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ade7e-124">See also</span></span>



[<span data-ttu-id="ade7e-125">IsBadStringPtr</span><span class="sxs-lookup"><span data-stu-id="ade7e-125">IsBadStringPtr</span></span>](http://msdn.microsoft.com/en-us/library/windows/desktop/aa366714%28v=vs.85%29.aspx)

