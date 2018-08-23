---
title: SMAPIFormInfoArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormInfoArray
api_type:
- COM
ms.assetid: f5eeb75d-debb-4ac1-b239-e8e852460ce0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6c09c271fefcf31dcde01526d65091714c0b682d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576274"
---
# <a name="smapiforminfoarray"></a><span data-ttu-id="6eb5e-103">SMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="6eb5e-103">SMAPIFormInfoArray</span></span>

  
  
<span data-ttu-id="6eb5e-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6eb5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6eb5e-105">Enthält ein Array von Zeigern auf Formular Informationen Objekte.</span><span class="sxs-lookup"><span data-stu-id="6eb5e-105">Contains an array of pointers to form information objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6eb5e-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="6eb5e-106">Header file:</span></span>  <br/> |<span data-ttu-id="6eb5e-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="6eb5e-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="6eb5e-108">Verwandte Makro:</span><span class="sxs-lookup"><span data-stu-id="6eb5e-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="6eb5e-109">CbMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="6eb5e-109">CbMAPIFormInfoArray</span></span>](cbmapiforminfoarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cForms;
  LPMAPIFORMINFO aFormInfo[MAPI_DIM];
} SMAPIFormInfoArray, FAR * LPSMAPIFORMINFOARRAY;

```

## <a name="members"></a><span data-ttu-id="6eb5e-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="6eb5e-110">Members</span></span>

 <span data-ttu-id="6eb5e-111">**cForms**</span><span class="sxs-lookup"><span data-stu-id="6eb5e-111">**cForms**</span></span>
  
> <span data-ttu-id="6eb5e-112">Anzahl von Zeigern im Array, auf das Element **aFormInfo** zeigt.</span><span class="sxs-lookup"><span data-stu-id="6eb5e-112">Count of pointers in the array pointed to by the **aFormInfo** member.</span></span> 
    
 <span data-ttu-id="6eb5e-113">**aFormInfo**</span><span class="sxs-lookup"><span data-stu-id="6eb5e-113">**aFormInfo**</span></span>
  
> <span data-ttu-id="6eb5e-114">Zeiger auf ein Array von Zeigern auf Formular Informationen Objekte.</span><span class="sxs-lookup"><span data-stu-id="6eb5e-114">Pointer to an array of pointers to form information objects.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6eb5e-115">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="6eb5e-115">Remarks</span></span>

<span data-ttu-id="6eb5e-116">Die Struktur **SMAPIFormInfoArray** wird als Parameter in der folgenden Methoden übergeben:</span><span class="sxs-lookup"><span data-stu-id="6eb5e-116">The **SMAPIFormInfoArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="6eb5e-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="6eb5e-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="6eb5e-118">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="6eb5e-118">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="6eb5e-119">IMAPIFormMgr::SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="6eb5e-119">IMAPIFormMgr::SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md)
    
- [<span data-ttu-id="6eb5e-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="6eb5e-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="6eb5e-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6eb5e-121">See also</span></span>



[<span data-ttu-id="6eb5e-122">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="6eb5e-122">MAPI Structures</span></span>](mapi-structures.md)

