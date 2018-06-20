---
title: SMessageClassArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMessageClassArray
api_type:
- COM
ms.assetid: 05f8c191-db2b-4174-8b3c-a9fdabfe6ac8
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 01563e3655d42abc62ea88a12f2878e5d81129d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795598"
---
# <a name="smessageclassarray"></a><span data-ttu-id="40157-103">SMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="40157-103">SMessageClassArray</span></span>

  
  
<span data-ttu-id="40157-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="40157-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="40157-105">Enthält ein Array von Zeigern auf Nachricht Klasse Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="40157-105">Contains an array of pointers to message class strings.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="40157-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="40157-106">Header file:</span></span>  <br/> |<span data-ttu-id="40157-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="40157-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="40157-108">Verwandte Makro:</span><span class="sxs-lookup"><span data-stu-id="40157-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="40157-109">CbMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="40157-109">CbMessageClassArray</span></span>](cbmessageclassarray.md) <br/> |
   
```cpp
typedef struct 
{
  ULONG cValues;
  LPCSTR aMessageClass[MAPI_DIM];
} SMessageClassArray, FAR * LPSMESSAGECLASSARRAY;

```

## <a name="members"></a><span data-ttu-id="40157-110">Members</span><span class="sxs-lookup"><span data-stu-id="40157-110">Members</span></span>

 <span data-ttu-id="40157-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="40157-111">**cValues**</span></span>
  
> <span data-ttu-id="40157-112">Anzahl der Nachricht Klasse Zeichenfolgenzeiger im Array.</span><span class="sxs-lookup"><span data-stu-id="40157-112">Count of message class string pointers in the array.</span></span>
    
 <span data-ttu-id="40157-113">**aMessageClass**</span><span class="sxs-lookup"><span data-stu-id="40157-113">**aMessageClass**</span></span>
  
> <span data-ttu-id="40157-114">Array von Zeigern auf Nachricht Klasse Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="40157-114">Array of pointers to message class strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="40157-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="40157-115">Remarks</span></span>

<span data-ttu-id="40157-116">Die Struktur **SMessageClassArray** wird als Parameter in der folgenden Methoden übergeben:</span><span class="sxs-lookup"><span data-stu-id="40157-116">The **SMessageClassArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="40157-117">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="40157-117">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="40157-118">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="40157-118">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="40157-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40157-119">See also</span></span>



[<span data-ttu-id="40157-120">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="40157-120">MAPI Structures</span></span>](mapi-structures.md)

