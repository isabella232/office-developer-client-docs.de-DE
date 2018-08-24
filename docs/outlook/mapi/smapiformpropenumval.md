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
ms.openlocfilehash: 2c49a17389a9bfc998f892e0becf96dca4cd773f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578717"
---
# <a name="smapiformpropenumval"></a><span data-ttu-id="3e62e-103">SMAPIFormPropEnumVal</span><span class="sxs-lookup"><span data-stu-id="3e62e-103">SMAPIFormPropEnumVal</span></span>

  
  
<span data-ttu-id="3e62e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e62e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e62e-105">Ordnet einen enumerierten ganzzahligen Wert einen Anzeigenamen für diesen Wert.</span><span class="sxs-lookup"><span data-stu-id="3e62e-105">Maps an enumerated integer value to a display name for that value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3e62e-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="3e62e-106">Header file:</span></span>  <br/> |<span data-ttu-id="3e62e-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="3e62e-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct _SMAPIFormPropEnumVal
{
  LPSTR pszDisplayName;
  ULONG nVal;
} SMAPIFormPropEnumVal;

```

## <a name="members"></a><span data-ttu-id="3e62e-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="3e62e-108">Members</span></span>

 <span data-ttu-id="3e62e-109">**pszDisplayName**</span><span class="sxs-lookup"><span data-stu-id="3e62e-109">**pszDisplayName**</span></span>
  
> <span data-ttu-id="3e62e-110">Zeichenfolge, die den Anzeigenamen für die in das **nVal** -Element angegebenen Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="3e62e-110">String that contains the display name for the value specified in the **nVal** member.</span></span> 
    
 <span data-ttu-id="3e62e-111">**nVal**</span><span class="sxs-lookup"><span data-stu-id="3e62e-111">**nVal**</span></span>
  
> <span data-ttu-id="3e62e-112">Ein Enumerationswert für den Anzeigenamen auf den Member **PszDisplayName** zeigt.</span><span class="sxs-lookup"><span data-stu-id="3e62e-112">An enumeration value for the display name pointed to by the **pszDisplayName** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3e62e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e62e-113">Remarks</span></span>

<span data-ttu-id="3e62e-114">Wenn ein Benutzer einen Anzeigenamen aus einem Formular auswählt, wird den Namen des entsprechenden-Enumerationswert gespeichert, mithilfe der Implementierung der [IMAPIProp](imapipropiunknown.md) -Schnittstelle, die dem Formular zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3e62e-114">When a user selects a display name from a form, the name's corresponding enumeration value is stored by using the [IMAPIProp](imapipropiunknown.md) interface implementation that is associated with the form.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3e62e-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e62e-115">See also</span></span>



[<span data-ttu-id="3e62e-116">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="3e62e-116">SMAPIFormProp</span></span>](smapiformprop.md)
  
[<span data-ttu-id="3e62e-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="3e62e-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="3e62e-118">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="3e62e-118">MAPI Structures</span></span>](mapi-structures.md)

