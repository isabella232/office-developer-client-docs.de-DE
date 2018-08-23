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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b2caa70600bd32234e38420f274bcd5c46ffb070
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578157"
---
# <a name="smessageclassarray"></a><span data-ttu-id="7fce0-103">SMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="7fce0-103">SMessageClassArray</span></span>

  
  
<span data-ttu-id="7fce0-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7fce0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7fce0-105">Enthält ein Array von Zeigern auf Nachricht Klasse Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="7fce0-105">Contains an array of pointers to message class strings.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7fce0-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="7fce0-106">Header file:</span></span>  <br/> |<span data-ttu-id="7fce0-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="7fce0-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="7fce0-108">Verwandte Makro:</span><span class="sxs-lookup"><span data-stu-id="7fce0-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="7fce0-109">CbMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="7fce0-109">CbMessageClassArray</span></span>](cbmessageclassarray.md) <br/> |
   
```cpp
typedef struct 
{
  ULONG cValues;
  LPCSTR aMessageClass[MAPI_DIM];
} SMessageClassArray, FAR * LPSMESSAGECLASSARRAY;

```

## <a name="members"></a><span data-ttu-id="7fce0-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="7fce0-110">Members</span></span>

 <span data-ttu-id="7fce0-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="7fce0-111">**cValues**</span></span>
  
> <span data-ttu-id="7fce0-112">Anzahl der Nachricht Klasse Zeichenfolgenzeiger im Array.</span><span class="sxs-lookup"><span data-stu-id="7fce0-112">Count of message class string pointers in the array.</span></span>
    
 <span data-ttu-id="7fce0-113">**aMessageClass**</span><span class="sxs-lookup"><span data-stu-id="7fce0-113">**aMessageClass**</span></span>
  
> <span data-ttu-id="7fce0-114">Array von Zeigern auf Nachricht Klasse Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="7fce0-114">Array of pointers to message class strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7fce0-115">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="7fce0-115">Remarks</span></span>

<span data-ttu-id="7fce0-116">Die Struktur **SMessageClassArray** wird als Parameter in der folgenden Methoden übergeben:</span><span class="sxs-lookup"><span data-stu-id="7fce0-116">The **SMessageClassArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="7fce0-117">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="7fce0-117">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="7fce0-118">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="7fce0-118">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="7fce0-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7fce0-119">See also</span></span>



[<span data-ttu-id="7fce0-120">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="7fce0-120">MAPI Structures</span></span>](mapi-structures.md)

