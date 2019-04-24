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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 353bc574ca5987d71faf4841744de30a3d6c3f19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309492"
---
# <a name="smapiformpropenumval"></a><span data-ttu-id="0baed-103">SMAPIFormPropEnumVal</span><span class="sxs-lookup"><span data-stu-id="0baed-103">SMAPIFormPropEnumVal</span></span>

  
  
<span data-ttu-id="0baed-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0baed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0baed-105">Ordnet einen aufgezählten ganzzahligen Wert einem Anzeigenamen für diesen Wert zu.</span><span class="sxs-lookup"><span data-stu-id="0baed-105">Maps an enumerated integer value to a display name for that value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0baed-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="0baed-106">Header file:</span></span>  <br/> |<span data-ttu-id="0baed-107">Mapiform. h</span><span class="sxs-lookup"><span data-stu-id="0baed-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct _SMAPIFormPropEnumVal
{
  LPSTR pszDisplayName;
  ULONG nVal;
} SMAPIFormPropEnumVal;

```

## <a name="members"></a><span data-ttu-id="0baed-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="0baed-108">Members</span></span>

 <span data-ttu-id="0baed-109">**pszDisplayName**</span><span class="sxs-lookup"><span data-stu-id="0baed-109">**pszDisplayName**</span></span>
  
> <span data-ttu-id="0baed-110">Zeichenfolge, die den Anzeigenamen für den im **NVAL** -Element angegebenen Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="0baed-110">String that contains the display name for the value specified in the **nVal** member.</span></span> 
    
 <span data-ttu-id="0baed-111">**nVal**</span><span class="sxs-lookup"><span data-stu-id="0baed-111">**nVal**</span></span>
  
> <span data-ttu-id="0baed-112">Ein Enumerationswert für den Anzeigenamen, auf den vom **pszDisplayName** -Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="0baed-112">An enumeration value for the display name pointed to by the **pszDisplayName** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0baed-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0baed-113">Remarks</span></span>

<span data-ttu-id="0baed-114">Wenn ein Benutzer einen Anzeigenamen aus einem Formular auswählt, wird der entsprechende Enumerationswert des Namens mithilfe der [IMAPIProp](imapipropiunknown.md) -Schnittstellenimplementierung gespeichert, die dem Formular zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0baed-114">When a user selects a display name from a form, the name's corresponding enumeration value is stored by using the [IMAPIProp](imapipropiunknown.md) interface implementation that is associated with the form.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0baed-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0baed-115">See also</span></span>



[<span data-ttu-id="0baed-116">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="0baed-116">SMAPIFormProp</span></span>](smapiformprop.md)
  
[<span data-ttu-id="0baed-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="0baed-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="0baed-118">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="0baed-118">MAPI Structures</span></span>](mapi-structures.md)

