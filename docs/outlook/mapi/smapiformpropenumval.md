---
title: SMAPIFormPropEnumVal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormPropEnumVal
api_type:
- COM
ms.assetid: 694d40e9-cff2-435e-ad90-446044c306d2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 353bc574ca5987d71faf4841744de30a3d6c3f19
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435411"
---
# <a name="smapiformpropenumval"></a><span data-ttu-id="e8e23-103">SMAPIFormPropEnumVal</span><span class="sxs-lookup"><span data-stu-id="e8e23-103">SMAPIFormPropEnumVal</span></span>

  
  
<span data-ttu-id="e8e23-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8e23-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8e23-105">Karten einen aufgezählten ganzzahligen Wert in einen Anzeigenamen für den Wert.</span><span class="sxs-lookup"><span data-stu-id="e8e23-105">Maps an enumerated integer value to a display name for that value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e8e23-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="e8e23-106">Header file:</span></span>  <br/> |<span data-ttu-id="e8e23-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="e8e23-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct _SMAPIFormPropEnumVal
{
  LPSTR pszDisplayName;
  ULONG nVal;
} SMAPIFormPropEnumVal;

```

## <a name="members"></a><span data-ttu-id="e8e23-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="e8e23-108">Members</span></span>

 <span data-ttu-id="e8e23-109">**pszDisplayName**</span><span class="sxs-lookup"><span data-stu-id="e8e23-109">**pszDisplayName**</span></span>
  
> <span data-ttu-id="e8e23-110">Zeichenfolge, die den Anzeigenamen für den im **nVal-Element angegebenen Wert** enthält.</span><span class="sxs-lookup"><span data-stu-id="e8e23-110">String that contains the display name for the value specified in the **nVal** member.</span></span> 
    
 <span data-ttu-id="e8e23-111">**nVal**</span><span class="sxs-lookup"><span data-stu-id="e8e23-111">**nVal**</span></span>
  
> <span data-ttu-id="e8e23-112">Ein Enumerationswert für den Anzeigenamen, auf den das **pszDisplayName-Element** verweist.</span><span class="sxs-lookup"><span data-stu-id="e8e23-112">An enumeration value for the display name pointed to by the **pszDisplayName** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e8e23-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e8e23-113">Remarks</span></span>

<span data-ttu-id="e8e23-114">Wenn ein Benutzer einen Anzeigenamen aus einem Formular auswählt, wird der entsprechende Enumerationswert des Namens mithilfe der [IMAPIProp-Schnittstellenimplementierung](imapipropiunknown.md) gespeichert, die dem Formular zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e8e23-114">When a user selects a display name from a form, the name's corresponding enumeration value is stored by using the [IMAPIProp](imapipropiunknown.md) interface implementation that is associated with the form.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e8e23-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8e23-115">See also</span></span>



[<span data-ttu-id="e8e23-116">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="e8e23-116">SMAPIFormProp</span></span>](smapiformprop.md)
  
[<span data-ttu-id="e8e23-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="e8e23-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="e8e23-118">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="e8e23-118">MAPI Structures</span></span>](mapi-structures.md)

