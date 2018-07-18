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
ms.openlocfilehash: bae750e7e940bc1417b3d225c9c81129e9da77b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795577"
---
# <a name="smapiformpropenumval"></a><span data-ttu-id="eb9bb-103">SMAPIFormPropEnumVal</span><span class="sxs-lookup"><span data-stu-id="eb9bb-103">SMAPIFormPropEnumVal</span></span>

  
  
<span data-ttu-id="eb9bb-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eb9bb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="eb9bb-105">Ordnet einen enumerierten ganzzahligen Wert einen Anzeigenamen für diesen Wert.</span><span class="sxs-lookup"><span data-stu-id="eb9bb-105">Maps an enumerated integer value to a display name for that value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eb9bb-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="eb9bb-106">Header file:</span></span>  <br/> |<span data-ttu-id="eb9bb-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="eb9bb-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct _SMAPIFormPropEnumVal
{
  LPSTR pszDisplayName;
  ULONG nVal;
} SMAPIFormPropEnumVal;

```

## <a name="members"></a><span data-ttu-id="eb9bb-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="eb9bb-108">Members</span></span>

 <span data-ttu-id="eb9bb-109">**pszDisplayName**</span><span class="sxs-lookup"><span data-stu-id="eb9bb-109">**pszDisplayName**</span></span>
  
> <span data-ttu-id="eb9bb-110">Zeichenfolge, die den Anzeigenamen für die in das **nVal** -Element angegebenen Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="eb9bb-110">String that contains the display name for the value specified in the **nVal** member.</span></span> 
    
 <span data-ttu-id="eb9bb-111">**nVal**</span><span class="sxs-lookup"><span data-stu-id="eb9bb-111">**nVal**</span></span>
  
> <span data-ttu-id="eb9bb-112">Ein Enumerationswert für den Anzeigenamen auf den Member **PszDisplayName** zeigt.</span><span class="sxs-lookup"><span data-stu-id="eb9bb-112">An enumeration value for the display name pointed to by the **pszDisplayName** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="eb9bb-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb9bb-113">Remarks</span></span>

<span data-ttu-id="eb9bb-114">Wenn ein Benutzer einen Anzeigenamen aus einem Formular auswählt, wird den Namen des entsprechenden-Enumerationswert gespeichert, mithilfe der Implementierung der [IMAPIProp](imapipropiunknown.md) -Schnittstelle, die dem Formular zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="eb9bb-114">When a user selects a display name from a form, the name's corresponding enumeration value is stored by using the [IMAPIProp](imapipropiunknown.md) interface implementation that is associated with the form.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="eb9bb-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb9bb-115">See also</span></span>



[<span data-ttu-id="eb9bb-116">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="eb9bb-116">SMAPIFormProp</span></span>](smapiformprop.md)
  
[<span data-ttu-id="eb9bb-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="eb9bb-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="eb9bb-118">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="eb9bb-118">MAPI Structures</span></span>](mapi-structures.md)

