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
ms.openlocfilehash: 73475c5ee4e715796e06642756c05746b271d128
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795569"
---
# <a name="smapiformprop"></a><span data-ttu-id="147bb-103">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="147bb-103">SMAPIFormProp</span></span>

  
  
<span data-ttu-id="147bb-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="147bb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="147bb-105">Beschreibt eine benannte Eigenschaft mit einem Formular verwendet.</span><span class="sxs-lookup"><span data-stu-id="147bb-105">Describes a named property used with a form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="147bb-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="147bb-106">Header file:</span></span>  <br/> |<span data-ttu-id="147bb-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="147bb-107">Mapiform.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="147bb-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="147bb-108">Members</span></span>

 <span data-ttu-id="147bb-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="147bb-109">**ulFlags**</span></span>
  
> <span data-ttu-id="147bb-110">Kennzeichen, die das Format der Zeichenfolgen in der Struktur **SMAPIFormProp** zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="147bb-110">Flags used to distinguish the format of the strings in the **SMAPIFormProp** structure.</span></span> <span data-ttu-id="147bb-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="147bb-111">The following flag can be set:</span></span> 
    
<span data-ttu-id="147bb-112">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="147bb-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="147bb-113">Die zurückgegebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="147bb-113">The strings returned are in Unicode format.</span></span> <span data-ttu-id="147bb-114">Wenn der Parameter MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="147bb-114">If MAPI_UNICODE is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="147bb-115">**nPropType**</span><span class="sxs-lookup"><span data-stu-id="147bb-115">**nPropType**</span></span>
  
> <span data-ttu-id="147bb-116">Typ der benannten Eigenschaft, mit dem wichtigste Wort auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="147bb-116">Type of the named property, with the most significant word set to zero.</span></span> 
    
 <span data-ttu-id="147bb-117">**nmid**</span><span class="sxs-lookup"><span data-stu-id="147bb-117">**nmid**</span></span>
  
> <span data-ttu-id="147bb-118">Der Name für die benannte Eigenschaft, die enthält eine **GUID** -Struktur, identifiziert der Eigenschaftswert festlegen und einem numerischen oder Zeichenfolge, die ein Schnittstellennamen-ID und das Formular darstellt.</span><span class="sxs-lookup"><span data-stu-id="147bb-118">Name for the named property, which includes a **GUID** structure identifying the property set and either a numeric or string value that represents an interface identifier and form name.</span></span> 
    
 <span data-ttu-id="147bb-119">**pszDisplayName**</span><span class="sxs-lookup"><span data-stu-id="147bb-119">**pszDisplayName**</span></span>
  
> <span data-ttu-id="147bb-120">Zeiger auf den Anzeigenamen der benannten Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="147bb-120">Pointer to the display name of the named property.</span></span>
    
 <span data-ttu-id="147bb-121">**nSpecialType**</span><span class="sxs-lookup"><span data-stu-id="147bb-121">**nSpecialType**</span></span>
  
> <span data-ttu-id="147bb-122">Wert, der den Typ der Daten enthalten im **u** -Member beschreibt.</span><span class="sxs-lookup"><span data-stu-id="147bb-122">Value describing the type of data included in the **u** member.</span></span> <span data-ttu-id="147bb-123">Mögliche Werte sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="147bb-123">Possible values are as follows:</span></span> 
    
<span data-ttu-id="147bb-124">FPST_VANILLA</span><span class="sxs-lookup"><span data-stu-id="147bb-124">FPST_VANILLA</span></span> 
  
> <span data-ttu-id="147bb-125">Das **u** -Element enthält eine Enumeration nicht.</span><span class="sxs-lookup"><span data-stu-id="147bb-125">The **u** member does not contain an enumeration.</span></span> 
    
<span data-ttu-id="147bb-126">FPST_ENUM_PROP</span><span class="sxs-lookup"><span data-stu-id="147bb-126">FPST_ENUM_PROP</span></span> 
  
> <span data-ttu-id="147bb-127">Das **u** -Element enthält eine Struktur, die eine Enumeration beschreibt.</span><span class="sxs-lookup"><span data-stu-id="147bb-127">The **u** member contains a structure that describes an enumeration.</span></span> 
    
 <span data-ttu-id="147bb-128">**u**</span><span class="sxs-lookup"><span data-stu-id="147bb-128">**u**</span></span>
  
> <span data-ttu-id="147bb-129">Union, die die Zuordnung zwischen den Namen und die Anzahl der benannten Eigenschaft beschreibt.</span><span class="sxs-lookup"><span data-stu-id="147bb-129">Union describing the association between the name and number of the named property.</span></span> <span data-ttu-id="147bb-130">Einige Eigenschaften verwenden, ist der Member **u** leer.</span><span class="sxs-lookup"><span data-stu-id="147bb-130">By using some properties, the **u** member is empty.</span></span> <span data-ttu-id="147bb-131">Mit anderen Eigenschaften wird in einer Struktur bestehend aus der folgenden Elemente dargestellt:</span><span class="sxs-lookup"><span data-stu-id="147bb-131">With other properties, it is represented in a structure consisting of the following members:</span></span> 
    
 <span data-ttu-id="147bb-132">**nmidIdx**</span><span class="sxs-lookup"><span data-stu-id="147bb-132">**nmidIdx**</span></span>
  
> <span data-ttu-id="147bb-133">Die [MAPINAMEID](mapinameid.md) -Struktur, die den Eigenschaftensatz und Bezeichner für die benannte Eigenschaft enthält.</span><span class="sxs-lookup"><span data-stu-id="147bb-133">The [MAPINAMEID](mapinameid.md) structure that contains the property set and identifier for the named property.</span></span> 
    
 <span data-ttu-id="147bb-134">**cfpevAvailable**</span><span class="sxs-lookup"><span data-stu-id="147bb-134">**cfpevAvailable**</span></span>
  
> <span data-ttu-id="147bb-135">Anzahl der [SMAPIFormPropEnumVal](smapiformpropenumval.md) Strukturen im Array auf der Member **PfpevAvailable** zeigt.</span><span class="sxs-lookup"><span data-stu-id="147bb-135">Count of [SMAPIFormPropEnumVal](smapiformpropenumval.md) structures in the array pointed to by the **pfpevAvailable** member.</span></span> 
    
 <span data-ttu-id="147bb-136">**pfpevAvailable**</span><span class="sxs-lookup"><span data-stu-id="147bb-136">**pfpevAvailable**</span></span>
  
> <span data-ttu-id="147bb-137">Zeiger auf ein Array von **SMAPIFormPropEnumVal** -Strukturen, von denen jeder einen Wert für die benannte Eigenschaft enthält.</span><span class="sxs-lookup"><span data-stu-id="147bb-137">Pointer to an array of **SMAPIFormPropEnumVal** structures, each of which holds a value for the named property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="147bb-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="147bb-138">Remarks</span></span>

<span data-ttu-id="147bb-139">Die **SMAPIFormProp** -Datenstruktur enthält Informationen zu einer Formulareigenschaft als Teil der Definitionen der [IMAPIFormInfo](imapiforminfoimapiprop.md) Schnittstelle verwendet; **nSpecialType** enthält einen Tag, der für die Vereinigung **u** gilt, die Teil der **SMAPIFormProp**ist.</span><span class="sxs-lookup"><span data-stu-id="147bb-139">The **SMAPIFormProp** structure contains information about a form property used as part of the definitions of the [IMAPIFormInfo](imapiforminfoimapiprop.md) interface; **nSpecialType** contains a tag that applies to the **u** union that is part of **SMAPIFormProp**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="147bb-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="147bb-140">See also</span></span>



[<span data-ttu-id="147bb-141">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="147bb-141">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="147bb-142">SMAPIFormPropEnumVal</span><span class="sxs-lookup"><span data-stu-id="147bb-142">SMAPIFormPropEnumVal</span></span>](smapiformpropenumval.md)


[<span data-ttu-id="147bb-143">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="147bb-143">MAPI Structures</span></span>](mapi-structures.md)

