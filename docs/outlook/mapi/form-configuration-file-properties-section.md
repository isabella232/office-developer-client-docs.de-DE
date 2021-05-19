---
title: Abschnitt "Formularkonfigurationsdatei [Eigenschaften]
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
# <a name="form-configuration-file-properties-section"></a><span data-ttu-id="baac7-103">Abschnitt "Formularkonfigurationsdatei [Eigenschaften]</span><span class="sxs-lookup"><span data-stu-id="baac7-103">Form Configuration File [Properties] Section</span></span>

  
  
<span data-ttu-id="baac7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="baac7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="baac7-105">Im **Abschnitt [Eigenschaften]** werden die vollständigen Eigenschaften aufgeführt, die das Formular verwendet und veröffentlicht. Das heißt, die Eigenschaften, die sie in ihren benutzerdefinierten Nachrichten erstellt, die MAPI-Clientanwendungen beim Anzeigen von Spalten, Filtern von Inhaltstabellen, Einrichten von Suchergebnissenordnern und so weiter verwenden können.</span><span class="sxs-lookup"><span data-stu-id="baac7-105">The **[Properties]** section lists the complete set of properties that the form uses and publishes; that is, the properties it creates in its custom messages that MAPI client applications can use when displaying columns, filtering contents tables, setting up search-results folders, and so on.</span></span> <span data-ttu-id="baac7-106">Jeder Eintrag in dieser Eigenschaftenliste verweist auf eine nachfolgende **[Property.**</span><span class="sxs-lookup"><span data-stu-id="baac7-106">Each entry in this property list references a subsequent **[Property.**</span></span> <span data-ttu-id="baac7-107">_string_ **]** -Abschnitt wie im Folgenden gezeigt.</span><span class="sxs-lookup"><span data-stu-id="baac7-107">_string_ **]** section as shown following.</span></span> 
  
 <span data-ttu-id="baac7-108">**[Eigenschaften]**</span><span class="sxs-lookup"><span data-stu-id="baac7-108">**[Properties]**</span></span>
  
 <span data-ttu-id="baac7-109">**Eigenschaft.**</span><span class="sxs-lookup"><span data-stu-id="baac7-109">**Property.**</span></span> <span data-ttu-id="baac7-110">_string_  =   _string_</span><span class="sxs-lookup"><span data-stu-id="baac7-110">_string_ =  _string_</span></span>
  
<span data-ttu-id="baac7-111">Das Format einer [ **-Eigenschaft.**</span><span class="sxs-lookup"><span data-stu-id="baac7-111">The format of a [ **Property.**</span></span> <span data-ttu-id="baac7-112">_string_] abschnitt ist:</span><span class="sxs-lookup"><span data-stu-id="baac7-112">_string_] section is:</span></span> 
  
 <span data-ttu-id="baac7-113">**[Eigenschaft.**</span><span class="sxs-lookup"><span data-stu-id="baac7-113">**[Property.**</span></span> <span data-ttu-id="baac7-114">_string_ **]**</span><span class="sxs-lookup"><span data-stu-id="baac7-114">_string_ **]**</span></span>
  
 <span data-ttu-id="baac7-115">**Type**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="baac7-115">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="baac7-116">**NmidPropset**  =   _guid_</span><span class="sxs-lookup"><span data-stu-id="baac7-116">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="baac7-117">**NmidString**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="baac7-117">**NmidString** =  _string_</span></span>
  
 <span data-ttu-id="baac7-118">**NmidInteger**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="baac7-118">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="baac7-119">**DisplayName**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="baac7-119">**DisplayName** =  _string_</span></span>
  
 <span data-ttu-id="baac7-120">**Flags**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="baac7-120">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="baac7-121">**SpecialType** = 0|1</span><span class="sxs-lookup"><span data-stu-id="baac7-121">**SpecialType** = 0|1</span></span> 
  
 <span data-ttu-id="baac7-122">**Enum1**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="baac7-122">**Enum1** =  _string_</span></span>
  
<span data-ttu-id="baac7-123">Jede **[-Eigenschaft.**</span><span class="sxs-lookup"><span data-stu-id="baac7-123">Each **[Property.**</span></span> <span data-ttu-id="baac7-124">_im Abschnitt string_ **]** wird eine einzelne Eigenschaft beschrieben.</span><span class="sxs-lookup"><span data-stu-id="baac7-124">_string_ **]** section describes a single property.</span></span> <span data-ttu-id="baac7-125">Der **Type-Eintrag** gibt den MAPI-Eigenschaftstyp an, z. B. 3 (PT_I4) der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="baac7-125">The **Type** entry specifies the MAPI property type, for example 3 (PT_I4), of the property.</span></span> <span data-ttu-id="baac7-126">Der **Eintrag NmidPropset** ist optional. Zusammen mit dem **Eintrag NmidString** oder **dem Eintrag NmidInteger** gibt der **Eintrag NmidPropset** den Namen der Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="baac7-126">The **NmidPropset** entry is optional; together with either the **NmidString** entry or the **NmidInteger** entry, the **NmidPropset** entry gives the name of the property.</span></span> <span data-ttu-id="baac7-127">**NmidString** gibt den Namen der Eigenschaft an, **während NmidInteger** den Bezeichner der Eigenschaft angibt.</span><span class="sxs-lookup"><span data-stu-id="baac7-127">**NmidString** gives the name of the property, while **NmidInteger** gives the identifier of the property.</span></span> <span data-ttu-id="baac7-128">**NmidString** und **NmidInteger schließen** sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="baac7-128">**NmidString** and **NmidInteger** are mutually exclusive.</span></span> 
  
<span data-ttu-id="baac7-129">Wenn festgelegt, **sollte NmidPropset** den Namen des Eigenschaftensatz enthalten. Wenn **NmidPropset** nicht vorhanden ist, wird basierend auf der folgenden Regel ein Standardwert festgelegt: Wenn **NmidInteger** vorhanden ist und der Wert kleiner als 0x8000 ist, wird **NmidPropset** auf PS_MAPI.</span><span class="sxs-lookup"><span data-stu-id="baac7-129">If set, **NmidPropset** should contain the name of the property set; if absent, **NmidPropset** is set to a default based on the following rule: If **NmidInteger** is present and its value is less than 0x8000, **NmidPropset** is set to PS_MAPI.</span></span> <span data-ttu-id="baac7-130">Wenn der Wert **von NmidInteger** auf eine ganze Zahl festgelegt ist, die größer als 0x8000 ist, oder wenn er nicht vorhanden ist, wird **NmidPropset** auf PS_PUBLIC_STRINGS.</span><span class="sxs-lookup"><span data-stu-id="baac7-130">If the value of **NmidInteger** is set to an integer greater than 0x8000, or if it is absent, **NmidPropset** is set to PS_PUBLIC_STRINGS.</span></span> 
  
<span data-ttu-id="baac7-131">Der **Eintrag DisplayName** enthält die Bezeichnung für die Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="baac7-131">The **DisplayName** entry contains the label for the property.</span></span> <span data-ttu-id="baac7-132">Der **Eintrag SpecialType** gibt an, dass es sich bei dieser Eigenschaft um eine spezielle Eigenschaft handelt, sofern vorhanden und ungleich Null.</span><span class="sxs-lookup"><span data-stu-id="baac7-132">The **SpecialType** entry, if present and nonzero indicates that this property is a special property.</span></span> <span data-ttu-id="baac7-133">Derzeit ist **specialType** = 1 der einzige spezielle Eigenschaftstyp, der zeichenfolgenenumerierte Eigenschaften angibt.</span><span class="sxs-lookup"><span data-stu-id="baac7-133">At present, the only special property type defined is **SpecialType** = 1, which indicates string enumerated properties.</span></span> <span data-ttu-id="baac7-134">Wenn **SpecialType** auf 1 festgelegt ist, verweist **der Eintrag Enum1** auf **[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="baac7-134">If **SpecialType** is set to 1, the **Enum1** entry references the **[Enum1.**</span></span> <span data-ttu-id="baac7-135">_string_ **]** section.</span><span class="sxs-lookup"><span data-stu-id="baac7-135">_string_ **]** section.</span></span> 
  
<span data-ttu-id="baac7-136">Im Folgenden finden Sie ein Beispiel für **einen Abschnitt [Properties]** und ein **[Properties.**</span><span class="sxs-lookup"><span data-stu-id="baac7-136">Following is an example of a **[Properties]** section and a **[Properties.**</span></span> <span data-ttu-id="baac7-137">_string_ **]** section.</span><span class="sxs-lookup"><span data-stu-id="baac7-137">_string_ **]** section.</span></span> 
  
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

<span data-ttu-id="baac7-138">Der **Eintrag Enum1** im voranstellenden Beispiel verweist auf eine **nachfolgende [Enum1.**</span><span class="sxs-lookup"><span data-stu-id="baac7-138">The **Enum1** entry in the preceeding example references to a subsequent **[Enum1.**</span></span> <span data-ttu-id="baac7-139">_string_ **]** -Abschnitt, der eine Aufzählung eines bestimmten Typs beschreibt.</span><span class="sxs-lookup"><span data-stu-id="baac7-139">_string_ **]** section describing an enumeration of a particular type.</span></span> <span data-ttu-id="baac7-140">Eine solche Enumeration verknüpft die erste Eigenschaft in **der [Property.**</span><span class="sxs-lookup"><span data-stu-id="baac7-140">Such an enumeration associates the first property in the **[Property.**</span></span> <span data-ttu-id="baac7-141">_string_ **]** -Abschnitt mit einer integer-Eigenschaft, die als Index bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="baac7-141">_string_ **]** section with an integer property, called the index.</span></span> <span data-ttu-id="baac7-142">Eine solche Enumeration enthält auch eine Liste der möglichen Werte, die das Anzeigeindexpaar annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="baac7-142">Such an enumeration also contains a list of the possible values that the display-index pair can assume.</span></span> <span data-ttu-id="baac7-143">Das Angeben eines Eigenschaftstyps für die Enumeration ist nicht erforderlich, da ein **Enum1-Eintrag** definitionsgemäß immer den PT_I4 hat.</span><span class="sxs-lookup"><span data-stu-id="baac7-143">Specifying a property type for the enumeration is unnecessary because by definition an **Enum1** entry always has the PT_I4 type.</span></span> <span data-ttu-id="baac7-144">Das Format für **[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="baac7-144">The format for the **[Enum1.**</span></span> <span data-ttu-id="baac7-145">_string_ **]** section is:</span><span class="sxs-lookup"><span data-stu-id="baac7-145">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="baac7-146">**[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="baac7-146">**[Enum1.**</span></span> <span data-ttu-id="baac7-147">_string_ **]**</span><span class="sxs-lookup"><span data-stu-id="baac7-147">_string_ **]**</span></span>
  
 <span data-ttu-id="baac7-148">**NmidPropset**  =   _guid_</span><span class="sxs-lookup"><span data-stu-id="baac7-148">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="baac7-149">**NmidString**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="baac7-149">**NmidString** =  _string_</span></span>
  
 <span data-ttu-id="baac7-150">**NmidInteger**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="baac7-150">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="baac7-151">**EnumCount**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="baac7-151">**EnumCount** =  _integer_</span></span>
  
 <span data-ttu-id="baac7-152">**Val.**</span><span class="sxs-lookup"><span data-stu-id="baac7-152">**Val.**</span></span> <span data-ttu-id="baac7-153">_ganze Zahl_ **. Anzeigezeichenfolge**  =   </span><span class="sxs-lookup"><span data-stu-id="baac7-153">_integer_ **.Display** =  _string_</span></span>
  
 <span data-ttu-id="baac7-154">**Val.**</span><span class="sxs-lookup"><span data-stu-id="baac7-154">**Val.**</span></span> <span data-ttu-id="baac7-155">_ganze Zahl_ **. Index**  =   _ganzzahlig_</span><span class="sxs-lookup"><span data-stu-id="baac7-155">_integer_ **.Index** =  _integer_</span></span>
  
<span data-ttu-id="baac7-156">Im Folgenden finden Sie eine Beispieleigenschaftsdefinition für eine aufgezählte Eigenschaft mit dem Namen Fire Hazard mit den möglichen Werten Low, Medium und High.</span><span class="sxs-lookup"><span data-stu-id="baac7-156">The following is an example property definition for an enumerated property named Fire Hazard with possible values of Low, Medium, and High.</span></span>
  
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

 <span data-ttu-id="baac7-157">**[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="baac7-157">**[Enum1.**</span></span> <span data-ttu-id="baac7-158">_string_ **]** -Abschnitte können von Anwendungen für zwei Zwecke verwendet werden: zum Beschleunigen der Filterung von Eigenschaften mithilfe des Indexes anstelle der Zeichenfolge und zum Sortieren nach einer anderen Reihenfolge als die alphanumerische Reihenfolge der Zeichenfolgenwerte.</span><span class="sxs-lookup"><span data-stu-id="baac7-158">_string_ **]** sections can be used by applications for two purposes: to speed up the filtering of properties by using the index instead of the string and to sort by a different order than the alphanumeric order of the string values.</span></span> <span data-ttu-id="baac7-159">Die Sortierung kann beispielsweise auf der Basis der Reihenfolge "Low-Medium-High" statt "High-Medium-Low" durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="baac7-159">For example, sorting could be done based on Low-Medium-High order instead of High-Medium-Low order.</span></span> 
  

