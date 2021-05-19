---
title: SMAPIFormProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormProp
api_type:
- COM
ms.assetid: 80f1c2e0-3567-4b16-86cb-d5e6ac95c2ee
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 968f9e1dad3a233b31f0ce29d3ce935b1257948c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416699"
---
# <a name="smapiformprop"></a><span data-ttu-id="a262f-103">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="a262f-103">SMAPIFormProp</span></span>

  
  
<span data-ttu-id="a262f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a262f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a262f-105">Beschreibt eine benannte Eigenschaft, die mit einem Formular verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a262f-105">Describes a named property used with a form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a262f-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="a262f-106">Header file:</span></span>  <br/> |<span data-ttu-id="a262f-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="a262f-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct _SMAPIFormProp
{
  ULONG ulFlags;
  ULONG nPropType;
  MAPINAMEID nmid;
  LPSTR pszDisplayName;
  FORMPROPSPECIALTYPE nSpecialType;
  union
  {
    struct
    {
      MAPINAMEID nmidIdx;
      ULONG cfpevAvailable;
      LPMAPIFORMPROPENUMVAL pfpevAvailable;
    } s1;
  } u;
} SMAPIFormProp, FAR * LPMAPIFORMPROP;

```

## <a name="members"></a><span data-ttu-id="a262f-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="a262f-108">Members</span></span>

 <span data-ttu-id="a262f-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="a262f-109">**ulFlags**</span></span>
  
> <span data-ttu-id="a262f-110">Flags, die zum Unterscheiden des Formats der Zeichenfolgen in der **SMAPIFormProp-Struktur verwendet** werden.</span><span class="sxs-lookup"><span data-stu-id="a262f-110">Flags used to distinguish the format of the strings in the **SMAPIFormProp** structure.</span></span> <span data-ttu-id="a262f-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="a262f-111">The following flag can be set:</span></span> 
    
<span data-ttu-id="a262f-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a262f-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a262f-113">Die zurückgegebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="a262f-113">The strings returned are in Unicode format.</span></span> <span data-ttu-id="a262f-114">Wenn MAPI_UNICODE nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a262f-114">If MAPI_UNICODE is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="a262f-115">**nPropType**</span><span class="sxs-lookup"><span data-stu-id="a262f-115">**nPropType**</span></span>
  
> <span data-ttu-id="a262f-116">Typ der benannten Eigenschaft, bei der das wichtigste Wort auf Null festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a262f-116">Type of the named property, with the most significant word set to zero.</span></span> 
    
 <span data-ttu-id="a262f-117">**nmid**</span><span class="sxs-lookup"><span data-stu-id="a262f-117">**nmid**</span></span>
  
> <span data-ttu-id="a262f-118">Name für die benannte Eigenschaft, die eine **GUID-Struktur** enthält, die den Eigenschaftensatz identifiziert, sowie einen numerischen wert oder einen Zeichenfolgenwert, der eine Schnittstellen-ID und einen Formularnamen darstellt.</span><span class="sxs-lookup"><span data-stu-id="a262f-118">Name for the named property, which includes a **GUID** structure identifying the property set and either a numeric or string value that represents an interface identifier and form name.</span></span> 
    
 <span data-ttu-id="a262f-119">**pszDisplayName**</span><span class="sxs-lookup"><span data-stu-id="a262f-119">**pszDisplayName**</span></span>
  
> <span data-ttu-id="a262f-120">Zeiger auf den Anzeigenamen der benannten Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a262f-120">Pointer to the display name of the named property.</span></span>
    
 <span data-ttu-id="a262f-121">**nSpecialType**</span><span class="sxs-lookup"><span data-stu-id="a262f-121">**nSpecialType**</span></span>
  
> <span data-ttu-id="a262f-122">Wert, der den Typ der im u-Element enthaltenen **Daten** beschreibt.</span><span class="sxs-lookup"><span data-stu-id="a262f-122">Value describing the type of data included in the **u** member.</span></span> <span data-ttu-id="a262f-123">Mögliche Werte sind:</span><span class="sxs-lookup"><span data-stu-id="a262f-123">Possible values are as follows:</span></span> 
    
<span data-ttu-id="a262f-124">FPST_VANILLA</span><span class="sxs-lookup"><span data-stu-id="a262f-124">FPST_VANILLA</span></span> 
  
> <span data-ttu-id="a262f-125">Das **u-Element** enthält keine Enumeration.</span><span class="sxs-lookup"><span data-stu-id="a262f-125">The **u** member does not contain an enumeration.</span></span> 
    
<span data-ttu-id="a262f-126">FPST_ENUM_PROP</span><span class="sxs-lookup"><span data-stu-id="a262f-126">FPST_ENUM_PROP</span></span> 
  
> <span data-ttu-id="a262f-127">Das **u-Element** enthält eine Struktur, die eine Enumeration beschreibt.</span><span class="sxs-lookup"><span data-stu-id="a262f-127">The **u** member contains a structure that describes an enumeration.</span></span> 
    
 <span data-ttu-id="a262f-128">**u**</span><span class="sxs-lookup"><span data-stu-id="a262f-128">**u**</span></span>
  
> <span data-ttu-id="a262f-129">Union, die die Zuordnung zwischen dem Namen und der Nummer der benannten Eigenschaft beschreibt.</span><span class="sxs-lookup"><span data-stu-id="a262f-129">Union describing the association between the name and number of the named property.</span></span> <span data-ttu-id="a262f-130">Mithilfe einiger Eigenschaften ist das **u-Element** leer.</span><span class="sxs-lookup"><span data-stu-id="a262f-130">By using some properties, the **u** member is empty.</span></span> <span data-ttu-id="a262f-131">Bei anderen Eigenschaften wird sie in einer Struktur dargestellt, die aus den folgenden Mitgliedern besteht:</span><span class="sxs-lookup"><span data-stu-id="a262f-131">With other properties, it is represented in a structure consisting of the following members:</span></span> 
    
 <span data-ttu-id="a262f-132">**nmidIdx**</span><span class="sxs-lookup"><span data-stu-id="a262f-132">**nmidIdx**</span></span>
  
> <span data-ttu-id="a262f-133">Die [MAPINAMEID-Struktur,](mapinameid.md) die den Eigenschaftensatz und den Bezeichner für die benannte Eigenschaft enthält.</span><span class="sxs-lookup"><span data-stu-id="a262f-133">The [MAPINAMEID](mapinameid.md) structure that contains the property set and identifier for the named property.</span></span> 
    
 <span data-ttu-id="a262f-134">**cfpevAvailable**</span><span class="sxs-lookup"><span data-stu-id="a262f-134">**cfpevAvailable**</span></span>
  
> <span data-ttu-id="a262f-135">Anzahl der [SMAPIFormPropEnumVal-Strukturen](smapiformpropenumval.md) im Array, auf die das **pfpevAvailable-Element verweist.**</span><span class="sxs-lookup"><span data-stu-id="a262f-135">Count of [SMAPIFormPropEnumVal](smapiformpropenumval.md) structures in the array pointed to by the **pfpevAvailable** member.</span></span> 
    
 <span data-ttu-id="a262f-136">**pfpevAvailable**</span><span class="sxs-lookup"><span data-stu-id="a262f-136">**pfpevAvailable**</span></span>
  
> <span data-ttu-id="a262f-137">Zeiger auf ein Array von **SMAPIFormPropEnumVal-Strukturen,** von denen jede einen Wert für die benannte Eigenschaft enthält.</span><span class="sxs-lookup"><span data-stu-id="a262f-137">Pointer to an array of **SMAPIFormPropEnumVal** structures, each of which holds a value for the named property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a262f-138">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a262f-138">Remarks</span></span>

<span data-ttu-id="a262f-139">Die **SMAPIFormProp-Struktur** enthält Informationen zu einer Formulareigenschaft, die als Teil der Definitionen der [IMAPIFormInfo-Schnittstelle verwendet](imapiforminfoimapiprop.md) wird. **nSpecialType** enthält ein Tag, das für die **u-Union** gilt, die Teil von **SMAPIFormProp ist.**</span><span class="sxs-lookup"><span data-stu-id="a262f-139">The **SMAPIFormProp** structure contains information about a form property used as part of the definitions of the [IMAPIFormInfo](imapiforminfoimapiprop.md) interface; **nSpecialType** contains a tag that applies to the **u** union that is part of **SMAPIFormProp**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a262f-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a262f-140">See also</span></span>



[<span data-ttu-id="a262f-141">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="a262f-141">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="a262f-142">SMAPIFormPropEnumVal</span><span class="sxs-lookup"><span data-stu-id="a262f-142">SMAPIFormPropEnumVal</span></span>](smapiformpropenumval.md)


[<span data-ttu-id="a262f-143">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="a262f-143">MAPI Structures</span></span>](mapi-structures.md)

