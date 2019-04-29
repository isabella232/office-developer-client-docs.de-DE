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
ms.openlocfilehash: 01b42c04244d35d72dd856222b4bab543b84db45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412695"
---
# <a name="smessageclassarray"></a><span data-ttu-id="5fb2e-103">SMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="5fb2e-103">SMessageClassArray</span></span>

  
  
<span data-ttu-id="5fb2e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5fb2e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5fb2e-105">Enthält ein Array von Zeigern für Nachrichtenklassen Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="5fb2e-105">Contains an array of pointers to message class strings.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5fb2e-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="5fb2e-106">Header file:</span></span>  <br/> |<span data-ttu-id="5fb2e-107">Mapiform. h</span><span class="sxs-lookup"><span data-stu-id="5fb2e-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="5fb2e-108">Zugehöriges Makro:</span><span class="sxs-lookup"><span data-stu-id="5fb2e-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="5fb2e-109">CbMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="5fb2e-109">CbMessageClassArray</span></span>](cbmessageclassarray.md) <br/> |
   
```cpp
typedef struct 
{
  ULONG cValues;
  LPCSTR aMessageClass[MAPI_DIM];
} SMessageClassArray, FAR * LPSMESSAGECLASSARRAY;

```

## <a name="members"></a><span data-ttu-id="5fb2e-110">Members</span><span class="sxs-lookup"><span data-stu-id="5fb2e-110">Members</span></span>

 <span data-ttu-id="5fb2e-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="5fb2e-111">**cValues**</span></span>
  
> <span data-ttu-id="5fb2e-112">Anzahl der Nachrichtenklassen-Zeichenfolgenzeiger im Array.</span><span class="sxs-lookup"><span data-stu-id="5fb2e-112">Count of message class string pointers in the array.</span></span>
    
 <span data-ttu-id="5fb2e-113">**aMessageClass**</span><span class="sxs-lookup"><span data-stu-id="5fb2e-113">**aMessageClass**</span></span>
  
> <span data-ttu-id="5fb2e-114">Array von Zeigern auf Nachrichtenklassen Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="5fb2e-114">Array of pointers to message class strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5fb2e-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5fb2e-115">Remarks</span></span>

<span data-ttu-id="5fb2e-116">Die **SMessageClassArray** -Struktur wird als Parameter in den folgenden Methoden übergeben:</span><span class="sxs-lookup"><span data-stu-id="5fb2e-116">The **SMessageClassArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="5fb2e-117">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="5fb2e-117">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="5fb2e-118">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="5fb2e-118">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="5fb2e-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5fb2e-119">See also</span></span>



[<span data-ttu-id="5fb2e-120">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="5fb2e-120">MAPI Structures</span></span>](mapi-structures.md)

