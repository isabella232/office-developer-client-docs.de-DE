---
title: Abschnitt [Properties] in der Formularkonfigurationsdatei
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f31a08ce-3a56-4c90-9502-5bcb09d8d80f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f582322c8ba2ffa0369792e531adf1ec4ccb3e28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791738"
---
# <a name="form-configuration-file-properties-section"></a><span data-ttu-id="6e675-103">Abschnitt [Properties] in der Formularkonfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="6e675-103">Form Configuration File [Properties] Section</span></span>

  
  
<span data-ttu-id="6e675-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6e675-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6e675-105">Im Abschnitt **[Eigenschaften]** werden den vollständigen Satz von Eigenschaften, die das Formular verwendet und veröffentlicht. d. h., können die Eigenschaften in der benutzerdefinierten Nachrichten, MAPI-Client Applications erstellt verwenden Sie beim Anzeigen von Spalten, Filtern von Inhalt Tabellen, Einrichten von Suchergebnissen Ordner, und so weiter.</span><span class="sxs-lookup"><span data-stu-id="6e675-105">The **[Properties]** section lists the complete set of properties that the form uses and publishes; that is, the properties it creates in its custom messages that MAPI client applications can use when displaying columns, filtering contents tables, setting up search-results folders, and so on.</span></span> <span data-ttu-id="6e675-106">Jeder Eintrag in der Liste diese Eigenschaft verweist auf eine nachfolgende **[-Eigenschaft.**</span><span class="sxs-lookup"><span data-stu-id="6e675-106">Each entry in this property list references a subsequent **[Property.**</span></span> <span data-ttu-id="6e675-107">_Zeichenfolge_ **]** Abschnitt wie folgt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="6e675-107">_string_ **]** section as shown following.</span></span> 
  
 <span data-ttu-id="6e675-108">**[Eigenschaften]**</span><span class="sxs-lookup"><span data-stu-id="6e675-108">**[Properties]**</span></span>
  
 <span data-ttu-id="6e675-109">**-Eigenschaft.**</span><span class="sxs-lookup"><span data-stu-id="6e675-109">**Property.**</span></span> <span data-ttu-id="6e675-110">_Zeichenfolge_ =  _Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="6e675-110">_string_ =  _string_</span></span>
  
<span data-ttu-id="6e675-111">Das Format einer [ **-Eigenschaft.**</span><span class="sxs-lookup"><span data-stu-id="6e675-111">The format of a [ **Property.**</span></span> <span data-ttu-id="6e675-112">_Zeichenfolge_] Abschnitt ist:</span><span class="sxs-lookup"><span data-stu-id="6e675-112">_string_] section is:</span></span> 
  
 <span data-ttu-id="6e675-113">**[-Eigenschaft.**</span><span class="sxs-lookup"><span data-stu-id="6e675-113">**[Property.**</span></span> <span data-ttu-id="6e675-114">_Zeichenfolge_ **]**</span><span class="sxs-lookup"><span data-stu-id="6e675-114">_string_ **]**</span></span>
  
 <span data-ttu-id="6e675-115">**Typ** =  _ganze Zahl_</span><span class="sxs-lookup"><span data-stu-id="6e675-115">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="6e675-116">**NmidPropset** =  _Guid_</span><span class="sxs-lookup"><span data-stu-id="6e675-116">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="6e675-117">**NmidString** =  _Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="6e675-117">**NmidString** =  _string_</span></span>
  
 <span data-ttu-id="6e675-118">**NmidInteger** =  _ganze Zahl_</span><span class="sxs-lookup"><span data-stu-id="6e675-118">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="6e675-119">**DisplayName** =  _Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="6e675-119">**DisplayName** =  _string_</span></span>
  
 <span data-ttu-id="6e675-120">**Flags** =  _ganze Zahl_</span><span class="sxs-lookup"><span data-stu-id="6e675-120">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="6e675-121">**SpecialType** = 0 | 1</span><span class="sxs-lookup"><span data-stu-id="6e675-121">**SpecialType** = 0|1</span></span> 
  
 <span data-ttu-id="6e675-122">**Enum1** =  _Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="6e675-122">**Enum1** =  _string_</span></span>
  
<span data-ttu-id="6e675-123">Jede **[-Eigenschaft.**</span><span class="sxs-lookup"><span data-stu-id="6e675-123">Each **[Property.**</span></span> <span data-ttu-id="6e675-124">_Zeichenfolge_ **]** Abschnitt beschreibt eine einzelne Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6e675-124">_string_ **]** section describes a single property.</span></span> <span data-ttu-id="6e675-125">Der Eintrag vom **Typ** gibt den MAPI-Eigenschaft, zum Beispiel 3 (PT_I4), der-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6e675-125">The **Type** entry specifies the MAPI property type, for example 3 (PT_I4), of the property.</span></span> <span data-ttu-id="6e675-126">Der Eintrag **NmidPropset** ist optional. zusammen mit den Eintrag **NmidString** oder den Eintrag **NmidInteger** gibt der Eintrag **NmidPropset** den Namen der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6e675-126">The **NmidPropset** entry is optional; together with either the **NmidString** entry or the **NmidInteger** entry, the **NmidPropset** entry gives the name of the property.</span></span> <span data-ttu-id="6e675-127">**NmidString** gibt den Namen der Eigenschaft, während **NmidInteger** den Bezeichner der-Eigenschaft gibt.</span><span class="sxs-lookup"><span data-stu-id="6e675-127">**NmidString** gives the name of the property, while **NmidInteger** gives the identifier of the property.</span></span> <span data-ttu-id="6e675-128">**NmidString** und **NmidInteger** schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="6e675-128">**NmidString** and **NmidInteger** are mutually exclusive.</span></span> 
  
<span data-ttu-id="6e675-129">Wenn Set **NmidPropset** der Name des Eigenschaftensatzes enthalten sollte. Wenn nicht vorhanden ist, **NmidPropset** auf eine standardmäßige auf der Grundlage der folgenden Regel festgelegt ist: Wenn **NmidInteger** vorhanden ist und dessen Wert kleiner als 0 x 8000 ist, **NmidPropset** auf PS_MAPI festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6e675-129">If set, **NmidPropset** should contain the name of the property set; if absent, **NmidPropset** is set to a default based on the following rule: If **NmidInteger** is present and its value is less than 0x8000, **NmidPropset** is set to PS_MAPI.</span></span> <span data-ttu-id="6e675-130">Wenn der Wert der **NmidInteger** auf eine ganze Zahl größer als 0 x 8000 festgelegt ist oder wenn es nicht vorhanden ist, wird die **NmidPropset** auf PS_PUBLIC_STRINGS festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6e675-130">If the value of **NmidInteger** is set to an integer greater than 0x8000, or if it is absent, **NmidPropset** is set to PS_PUBLIC_STRINGS.</span></span> 
  
<span data-ttu-id="6e675-131">Der Eintrag **"DisplayName"** enthält die Beschriftung für die Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6e675-131">The **DisplayName** entry contains the label for the property.</span></span> <span data-ttu-id="6e675-132">Der Eintrag **SpecialType** , falls vorhanden und ungleich NULL bedeutet, dass diese Eigenschaft eine spezielle Eigenschaft ist.</span><span class="sxs-lookup"><span data-stu-id="6e675-132">The **SpecialType** entry, if present and nonzero indicates that this property is a special property.</span></span> <span data-ttu-id="6e675-133">Derzeit ist der einzige spezielle Eigenschaftentyp definiert **SpecialType** = 1, womit Zeichenfolgeneigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="6e675-133">At present, the only special property type defined is **SpecialType** = 1, which indicates string enumerated properties.</span></span> <span data-ttu-id="6e675-134">Wenn **SpecialType** auf 1 festgelegt ist, der Eintrag **Enum1** verweist auf die **[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="6e675-134">If **SpecialType** is set to 1, the **Enum1** entry references the **[Enum1.**</span></span> <span data-ttu-id="6e675-135">_Zeichenfolge_ **]** Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="6e675-135">_string_ **]** section.</span></span> 
  
<span data-ttu-id="6e675-136">Nachfolgend sehen Sie ein Beispiel für einen Abschnitt **[Eigenschaften]** und eine **[Eigenschaften.**</span><span class="sxs-lookup"><span data-stu-id="6e675-136">Following is an example of a **[Properties]** section and a **[Properties.**</span></span> <span data-ttu-id="6e675-137">_Zeichenfolge_ **]** Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="6e675-137">_string_ **]** section.</span></span> 
  
```cpp
[Properties]
Property.1 = Fire Hazard
Property.2 = Safe
[Property.Fire Hazard]
Type = 1
NmidPropSet = {E47F4480-8400-101B-934D-04021C007002]
NmidString = FireHazard
DisplayName = Fire Hazard
SpecialType = 1
Enum1 = HazardEnum

```

<span data-ttu-id="6e675-138">Der Eintrag **Enum1** in der vorherigen Beispiel Verweise auf einer nachfolgenden **[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="6e675-138">The **Enum1** entry in the preceeding example references to a subsequent **[Enum1.**</span></span> <span data-ttu-id="6e675-139">_Zeichenfolge_ **]** Abschnitt eine Enumeration eines bestimmten Typs beschreiben.</span><span class="sxs-lookup"><span data-stu-id="6e675-139">_string_ **]** section describing an enumeration of a particular type.</span></span> <span data-ttu-id="6e675-140">Eine-Enumeration ordnet die erste Eigenschaft in der **[-Eigenschaft.**</span><span class="sxs-lookup"><span data-stu-id="6e675-140">Such an enumeration associates the first property in the **[Property.**</span></span> <span data-ttu-id="6e675-141">_Zeichenfolge_ **]** Abschnitt mit einer ganzzahligen-Eigenschaft mit der Bezeichnung des Index.</span><span class="sxs-lookup"><span data-stu-id="6e675-141">_string_ **]** section with an integer property, called the index.</span></span> <span data-ttu-id="6e675-142">Eine-Enumeration enthält auch eine Liste der möglichen Werte, die das Display-Index-Paar übernehmen kann.</span><span class="sxs-lookup"><span data-stu-id="6e675-142">Such an enumeration also contains a list of the possible values that the display-index pair can assume.</span></span> <span data-ttu-id="6e675-143">Angeben einen Eigenschaftentyp für die Enumeration ist nicht erforderlich, da per Definition ein Eintrags **Enum1** immer der PT_I4-Typ hat.</span><span class="sxs-lookup"><span data-stu-id="6e675-143">Specifying a property type for the enumeration is unnecessary because by definition an **Enum1** entry always has the PT_I4 type.</span></span> <span data-ttu-id="6e675-144">Das Format für die **[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="6e675-144">The format for the **[Enum1.**</span></span> <span data-ttu-id="6e675-145">_Zeichenfolge_ **]** Abschnitt ist:</span><span class="sxs-lookup"><span data-stu-id="6e675-145">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="6e675-146">**[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="6e675-146">**[Enum1.**</span></span> <span data-ttu-id="6e675-147">_Zeichenfolge_ **]**</span><span class="sxs-lookup"><span data-stu-id="6e675-147">_string_ **]**</span></span>
  
 <span data-ttu-id="6e675-148">**NmidPropset** =  _Guid_</span><span class="sxs-lookup"><span data-stu-id="6e675-148">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="6e675-149">**NmidString** =  _Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="6e675-149">**NmidString** =  _string_</span></span>
  
 <span data-ttu-id="6e675-150">**NmidInteger** =  _ganze Zahl_</span><span class="sxs-lookup"><span data-stu-id="6e675-150">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="6e675-151">**EnumCount** =  _ganze Zahl_</span><span class="sxs-lookup"><span data-stu-id="6e675-151">**EnumCount** =  _integer_</span></span>
  
 <span data-ttu-id="6e675-152">**Val.**</span><span class="sxs-lookup"><span data-stu-id="6e675-152">**Val.**</span></span> <span data-ttu-id="6e675-153">_ganze Zahl_ **. Anzeige** =  _Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="6e675-153">_integer_ **.Display** =  _string_</span></span>
  
 <span data-ttu-id="6e675-154">**Val.**</span><span class="sxs-lookup"><span data-stu-id="6e675-154">**Val.**</span></span> <span data-ttu-id="6e675-155">_ganze Zahl_ **. Index** =  _ganze Zahl_</span><span class="sxs-lookup"><span data-stu-id="6e675-155">_integer_ **.Index** =  _integer_</span></span>
  
<span data-ttu-id="6e675-156">Es folgt eine Beispiel-Eigenschaftendefinition für eine enumerierten-Eigenschaft mit dem Namen Brandgefahr und mögliche Werte der niedrig, Mittel und hoch.</span><span class="sxs-lookup"><span data-stu-id="6e675-156">The following is an example property definition for an enumerated property named Fire Hazard with possible values of Low, Medium, and High.</span></span>
  
```cpp
[Properties]
Property1 = Fire Hazard
[Enum1.HazardEnum]
IdxNmidPropset={E47F4480-8400-101B-934D-04021C007002]
IdxNmidString=FireHazardEnum
EnumCount = 3
Val.1.Display = Low
Val.1.Index = 1
Val.2.Display = Medium
Val.2.Index = 2
Val.3.Display = High
Val.3.Index = 3

```

 <span data-ttu-id="6e675-157">**[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="6e675-157">**[Enum1.**</span></span> <span data-ttu-id="6e675-158">_Zeichenfolge_ **]** Abschnitte von Clientanwendungen für zwei Zwecke verwendet werden können: das Filtern von Eigenschaften mithilfe den Index anstelle der Zeichenfolge beschleunigt und von einer anderen Reihenfolge als die Zeichenfolgenwerte alphanumerischer Reihenfolge sortiert.</span><span class="sxs-lookup"><span data-stu-id="6e675-158">_string_ **]** sections can be used by applications for two purposes: to speed up the filtering of properties by using the index instead of the string and to sort by a different order than the alphanumeric order of the string values.</span></span> <span data-ttu-id="6e675-159">Beispielsweise könnte Sortierung basierend auf Niedrig, Mittel-hoher Reihenfolge statt besonders niedrig Reihenfolge erfolgen.</span><span class="sxs-lookup"><span data-stu-id="6e675-159">For example, sorting could be done based on Low-Medium-High order instead of High-Medium-Low order.</span></span> 
  

