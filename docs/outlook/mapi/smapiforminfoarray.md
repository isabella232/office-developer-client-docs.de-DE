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
ms.openlocfilehash: e274e24d9aff30bb39b1865306477164d413d9a8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416972"
---
# <a name="smapiforminfoarray"></a><span data-ttu-id="ddcfd-103">SMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="ddcfd-103">SMAPIFormInfoArray</span></span>

  
  
<span data-ttu-id="ddcfd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ddcfd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ddcfd-105">Enthält ein Array von Zeigern für Formular Informationsobjekte.</span><span class="sxs-lookup"><span data-stu-id="ddcfd-105">Contains an array of pointers to form information objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ddcfd-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="ddcfd-106">Header file:</span></span>  <br/> |<span data-ttu-id="ddcfd-107">Mapiform. h</span><span class="sxs-lookup"><span data-stu-id="ddcfd-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="ddcfd-108">Zugehöriges Makro:</span><span class="sxs-lookup"><span data-stu-id="ddcfd-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="ddcfd-109">CbMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="ddcfd-109">CbMAPIFormInfoArray</span></span>](cbmapiforminfoarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cForms;
  LPMAPIFORMINFO aFormInfo[MAPI_DIM];
} SMAPIFormInfoArray, FAR * LPSMAPIFORMINFOARRAY;

```

## <a name="members"></a><span data-ttu-id="ddcfd-110">Members</span><span class="sxs-lookup"><span data-stu-id="ddcfd-110">Members</span></span>

 <span data-ttu-id="ddcfd-111">**cForms**</span><span class="sxs-lookup"><span data-stu-id="ddcfd-111">**cForms**</span></span>
  
> <span data-ttu-id="ddcfd-112">Die Anzahl der Zeiger im Array, auf die durch das **aFormInfo** -Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ddcfd-112">Count of pointers in the array pointed to by the **aFormInfo** member.</span></span> 
    
 <span data-ttu-id="ddcfd-113">**aFormInfo**</span><span class="sxs-lookup"><span data-stu-id="ddcfd-113">**aFormInfo**</span></span>
  
> <span data-ttu-id="ddcfd-114">Zeiger auf ein Array von Zeigern auf Formular Informationsobjekte.</span><span class="sxs-lookup"><span data-stu-id="ddcfd-114">Pointer to an array of pointers to form information objects.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ddcfd-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ddcfd-115">Remarks</span></span>

<span data-ttu-id="ddcfd-116">Die **SMAPIFormInfoArray** -Struktur wird als Parameter in den folgenden Methoden übergeben:</span><span class="sxs-lookup"><span data-stu-id="ddcfd-116">The **SMAPIFormInfoArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="ddcfd-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="ddcfd-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="ddcfd-118">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="ddcfd-118">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="ddcfd-119">IMAPIFormMgr::SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="ddcfd-119">IMAPIFormMgr::SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md)
    
- [<span data-ttu-id="ddcfd-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="ddcfd-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="ddcfd-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ddcfd-121">See also</span></span>



[<span data-ttu-id="ddcfd-122">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="ddcfd-122">MAPI Structures</span></span>](mapi-structures.md)

