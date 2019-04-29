---
title: Formular Konfigurationsdatei [Properties] Abschnitt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f31a08ce-3a56-4c90-9502-5bcb09d8d80f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 86d2257b821622094ff8d5ad3a5d7b1bfc74942b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421291"
---
# <a name="form-configuration-file-properties-section"></a><span data-ttu-id="2d56f-103">Formular Konfigurationsdatei [Properties] Abschnitt</span><span class="sxs-lookup"><span data-stu-id="2d56f-103">Form Configuration File [Properties] Section</span></span>

  
  
<span data-ttu-id="2d56f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d56f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d56f-105">Der Abschnitt **[Properties]** enthält den vollständigen Satz von Eigenschaften, die vom Formular verwendet und veröffentlicht werden. Das heißt, die Eigenschaften, die es in seinen benutzerdefinierten Nachrichten erstellt, die MAPI-Clientanwendungen beim Anzeigen von Spalten, Filtern von Inhaltstabellen, Einrichten von Suchergebnis Ordnern usw. verwenden können.</span><span class="sxs-lookup"><span data-stu-id="2d56f-105">The **[Properties]** section lists the complete set of properties that the form uses and publishes; that is, the properties it creates in its custom messages that MAPI client applications can use when displaying columns, filtering contents tables, setting up search-results folders, and so on.</span></span> <span data-ttu-id="2d56f-106">Jeder Eintrag in dieser Eigenschaftenliste verweist auf eine nachfolgende **[Eigenschaft.**</span><span class="sxs-lookup"><span data-stu-id="2d56f-106">Each entry in this property list references a subsequent **[Property.**</span></span> <span data-ttu-id="2d56f-107">_Zeichenfolge_ **]** -Abschnitt wie folgt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2d56f-107">_string_ **]** section as shown following.</span></span> 
  
 <span data-ttu-id="2d56f-108">**Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="2d56f-108">**[Properties]**</span></span>
  
 <span data-ttu-id="2d56f-109">**Eigenschaft.**</span><span class="sxs-lookup"><span data-stu-id="2d56f-109">**Property.**</span></span> <span data-ttu-id="2d56f-110">_Zeichen_ =  __ Folge</span><span class="sxs-lookup"><span data-stu-id="2d56f-110">_string_ =  _string_</span></span>
  
<span data-ttu-id="2d56f-111">Das Format einer [ **-Eigenschaft.**</span><span class="sxs-lookup"><span data-stu-id="2d56f-111">The format of a [ **Property.**</span></span> <span data-ttu-id="2d56f-112">_Zeichenfolge_] Section ist:</span><span class="sxs-lookup"><span data-stu-id="2d56f-112">_string_] section is:</span></span> 
  
 <span data-ttu-id="2d56f-113">**Eigenschaft.**</span><span class="sxs-lookup"><span data-stu-id="2d56f-113">**[Property.**</span></span> <span data-ttu-id="2d56f-114">_Zeichenfolge_ **]**</span><span class="sxs-lookup"><span data-stu-id="2d56f-114">_string_ **]**</span></span>
  
 <span data-ttu-id="2d56f-115">**Typ** =  _Integer_</span><span class="sxs-lookup"><span data-stu-id="2d56f-115">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="2d56f-116">**NmidPropset** =  -_GUID_</span><span class="sxs-lookup"><span data-stu-id="2d56f-116">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="2d56f-117">**NmidString** =  -_Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="2d56f-117">**NmidString** =  _string_</span></span>
  
 <span data-ttu-id="2d56f-118">**NmidInteger** =  -_Ganzzahl_</span><span class="sxs-lookup"><span data-stu-id="2d56f-118">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="2d56f-119">**DisplayName** =  -_Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="2d56f-119">**DisplayName** =  _string_</span></span>
  
 <span data-ttu-id="2d56f-120">**Flags** =  -_Ganzzahl_</span><span class="sxs-lookup"><span data-stu-id="2d56f-120">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="2d56f-121">**Specialtype** = 0 | 1</span><span class="sxs-lookup"><span data-stu-id="2d56f-121">**SpecialType** = 0|1</span></span> 
  
 <span data-ttu-id="2d56f-122">**Enum1** =  -_Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="2d56f-122">**Enum1** =  _string_</span></span>
  
<span data-ttu-id="2d56f-123">Jede **[Eigenschaft.**</span><span class="sxs-lookup"><span data-stu-id="2d56f-123">Each **[Property.**</span></span> <span data-ttu-id="2d56f-124">_Zeichenfolge_ **]** section beschreibt eine einzelne Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="2d56f-124">_string_ **]** section describes a single property.</span></span> <span data-ttu-id="2d56f-125">Der **Type** -Eintrag gibt den MAPI-Eigenschaftentyp (beispielsweise 3 (PT_I4)) der Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="2d56f-125">The **Type** entry specifies the MAPI property type, for example 3 (PT_I4), of the property.</span></span> <span data-ttu-id="2d56f-126">Der **NmidPropset** -Eintrag ist optional; zusammen mit dem **NmidString** -Eintrag oder dem **NmidInteger** -Eintrag gibt der **NmidPropset** -Eintrag den Namen der Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="2d56f-126">The **NmidPropset** entry is optional; together with either the **NmidString** entry or the **NmidInteger** entry, the **NmidPropset** entry gives the name of the property.</span></span> <span data-ttu-id="2d56f-127">**NmidString** gibt den Namen der Eigenschaft an, während **NmidInteger** den Bezeichner der Eigenschaft liefert.</span><span class="sxs-lookup"><span data-stu-id="2d56f-127">**NmidString** gives the name of the property, while **NmidInteger** gives the identifier of the property.</span></span> <span data-ttu-id="2d56f-128">**NmidString** und **NmidInteger** schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="2d56f-128">**NmidString** and **NmidInteger** are mutually exclusive.</span></span> 
  
<span data-ttu-id="2d56f-129">Wenn festgelegt, sollte **NmidPropset** den Namen des Eigenschaftensatzes enthalten. Wenn nicht vorhanden, wird **NmidPropset** auf einen Standardwert basierend auf der folgenden Regel festgelegt: Wenn **NmidInteger** vorhanden ist und dessen Value kleiner als 0X8000 ist, wird **NmidPropset** auf PS_MAPI festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2d56f-129">If set, **NmidPropset** should contain the name of the property set; if absent, **NmidPropset** is set to a default based on the following rule: If **NmidInteger** is present and its value is less than 0x8000, **NmidPropset** is set to PS_MAPI.</span></span> <span data-ttu-id="2d56f-130">Wenn der Wert von **NmidInteger** auf eine ganze Zahl größer als 0X8000 festgelegt ist oder abwesend ist, wird **NmidPropset** auf PS_PUBLIC_STRINGS festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2d56f-130">If the value of **NmidInteger** is set to an integer greater than 0x8000, or if it is absent, **NmidPropset** is set to PS_PUBLIC_STRINGS.</span></span> 
  
<span data-ttu-id="2d56f-131">Der Eintrag **DisplayName** enthält die Bezeichnung für die Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="2d56f-131">The **DisplayName** entry contains the label for the property.</span></span> <span data-ttu-id="2d56f-132">Der **specialtype** -Eintrag, sofern vorhanden, und ungleich NULL gibt an, dass diese Eigenschaft eine spezielle Eigenschaft ist.</span><span class="sxs-lookup"><span data-stu-id="2d56f-132">The **SpecialType** entry, if present and nonzero indicates that this property is a special property.</span></span> <span data-ttu-id="2d56f-133">Derzeit ist der einzige definierte Eigenschafts specialtype \*\*\*\* = 1, der Aufzählungs Eigenschaften für die Zeichenfolge angibt.</span><span class="sxs-lookup"><span data-stu-id="2d56f-133">At present, the only special property type defined is **SpecialType** = 1, which indicates string enumerated properties.</span></span> <span data-ttu-id="2d56f-134">Wenn **specialtype** auf 1 festgelegt ist, verweist der **Enum1** -Eintrag auf den **[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="2d56f-134">If **SpecialType** is set to 1, the **Enum1** entry references the **[Enum1.**</span></span> <span data-ttu-id="2d56f-135">_Zeichenfolge_ **]** -Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="2d56f-135">_string_ **]** section.</span></span> 
  
<span data-ttu-id="2d56f-136">Es folgt ein Beispiel für einen **[Properties]** -Abschnitt und eine **[Properties.**</span><span class="sxs-lookup"><span data-stu-id="2d56f-136">Following is an example of a **[Properties]** section and a **[Properties.**</span></span> <span data-ttu-id="2d56f-137">_Zeichenfolge_ **]** -Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="2d56f-137">_string_ **]** section.</span></span> 
  
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

<span data-ttu-id="2d56f-138">Der **Enum1** -Eintrag im vorherigen Beispiel verweist auf eine nachfolgende **[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="2d56f-138">The **Enum1** entry in the preceeding example references to a subsequent **[Enum1.**</span></span> <span data-ttu-id="2d56f-139">_Zeichenfolge_ **]** -Abschnitt, der eine Enumeration eines bestimmten Typs beschreibt.</span><span class="sxs-lookup"><span data-stu-id="2d56f-139">_string_ **]** section describing an enumeration of a particular type.</span></span> <span data-ttu-id="2d56f-140">Eine solche Enumeration ordnet die erste Eigenschaft in der **[-Eigenschaft.**</span><span class="sxs-lookup"><span data-stu-id="2d56f-140">Such an enumeration associates the first property in the **[Property.**</span></span> <span data-ttu-id="2d56f-141">_Zeichenfolge_ **]** Section mit einer Integer-Eigenschaft, die als Index bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="2d56f-141">_string_ **]** section with an integer property, called the index.</span></span> <span data-ttu-id="2d56f-142">Eine solche Enumeration enthält auch eine Liste der möglichen Werte, die das Paar vom Anzeigeindex annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="2d56f-142">Such an enumeration also contains a list of the possible values that the display-index pair can assume.</span></span> <span data-ttu-id="2d56f-143">Das Angeben eines Eigenschaftentyps für die Enumeration ist nicht erforderlich, da ein **Enum1** -Eintrag per Definition immer den PT_I4-Typ aufweist.</span><span class="sxs-lookup"><span data-stu-id="2d56f-143">Specifying a property type for the enumeration is unnecessary because by definition an **Enum1** entry always has the PT_I4 type.</span></span> <span data-ttu-id="2d56f-144">Das Format für **[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="2d56f-144">The format for the **[Enum1.**</span></span> <span data-ttu-id="2d56f-145">_Zeichenfolge_ **]** section ist:</span><span class="sxs-lookup"><span data-stu-id="2d56f-145">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="2d56f-146">**[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="2d56f-146">**[Enum1.**</span></span> <span data-ttu-id="2d56f-147">_Zeichenfolge_ **]**</span><span class="sxs-lookup"><span data-stu-id="2d56f-147">_string_ **]**</span></span>
  
 <span data-ttu-id="2d56f-148">**NmidPropset** =  -_GUID_</span><span class="sxs-lookup"><span data-stu-id="2d56f-148">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="2d56f-149">**NmidString** =  -_Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="2d56f-149">**NmidString** =  _string_</span></span>
  
 <span data-ttu-id="2d56f-150">**NmidInteger** =  -_Ganzzahl_</span><span class="sxs-lookup"><span data-stu-id="2d56f-150">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="2d56f-151">**EnumCount** =  -_Ganzzahl_</span><span class="sxs-lookup"><span data-stu-id="2d56f-151">**EnumCount** =  _integer_</span></span>
  
 <span data-ttu-id="2d56f-152">**Val.**</span><span class="sxs-lookup"><span data-stu-id="2d56f-152">**Val.**</span></span> <span data-ttu-id="2d56f-153">_ganze Zahl_ \*\*. \*\* =  _Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="2d56f-153">_integer_ **.Display** =  _string_</span></span>
  
 <span data-ttu-id="2d56f-154">**Val.**</span><span class="sxs-lookup"><span data-stu-id="2d56f-154">**Val.**</span></span> <span data-ttu-id="2d56f-155">_ganze Zahl_ **. Index** =  _Ganzzahl_</span><span class="sxs-lookup"><span data-stu-id="2d56f-155">_integer_ **.Index** =  _integer_</span></span>
  
<span data-ttu-id="2d56f-156">Es folgt ein Beispiel für eine Eigenschaftendefinition für eine aufgezählte Eigenschaft mit dem Namen Fire Hazard mit möglichen Werten von niedrig, Mittel und hoch.</span><span class="sxs-lookup"><span data-stu-id="2d56f-156">The following is an example property definition for an enumerated property named Fire Hazard with possible values of Low, Medium, and High.</span></span>
  
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

 <span data-ttu-id="2d56f-157">**[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="2d56f-157">**[Enum1.**</span></span> <span data-ttu-id="2d56f-158">_Zeichenfolge_ **]** Abschnitte können von Anwendungen aus zwei Gründen verwendet werden: um die Filterung von Eigenschaften zu beschleunigen, indem Sie den Index anstelle der Zeichenfolge verwenden und nach einer anderen Reihenfolge als die alphanumerische Reihenfolge der Zeichenfolgenwerte sortieren.</span><span class="sxs-lookup"><span data-stu-id="2d56f-158">_string_ **]** sections can be used by applications for two purposes: to speed up the filtering of properties by using the index instead of the string and to sort by a different order than the alphanumeric order of the string values.</span></span> <span data-ttu-id="2d56f-159">Beispielsweise kann die Sortierung basierend auf der Reihenfolge von niedrig-bis mittel-groß statt der Reihenfolge von High-Medium-Low durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2d56f-159">For example, sorting could be done based on Low-Medium-High order instead of High-Medium-Low order.</span></span> 
  

