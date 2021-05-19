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
# <a name="form-configuration-file-properties-section"></a>Abschnitt "Formularkonfigurationsdatei [Eigenschaften]

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Im **Abschnitt [Eigenschaften]** werden die vollständigen Eigenschaften aufgeführt, die das Formular verwendet und veröffentlicht. Das heißt, die Eigenschaften, die sie in ihren benutzerdefinierten Nachrichten erstellt, die MAPI-Clientanwendungen beim Anzeigen von Spalten, Filtern von Inhaltstabellen, Einrichten von Suchergebnissenordnern und so weiter verwenden können. Jeder Eintrag in dieser Eigenschaftenliste verweist auf eine nachfolgende **[Property.** _string_ **]** -Abschnitt wie im Folgenden gezeigt. 
  
 **[Eigenschaften]**
  
 **Eigenschaft.** _string_  =   _string_
  
Das Format einer [ **-Eigenschaft.** _string_] abschnitt ist: 
  
 **[Eigenschaft.** _string_ **]**
  
 **Type**  =   _integer_
  
 **NmidPropset**  =   _guid_
  
 **NmidString**  =   _string_
  
 **NmidInteger**  =   _integer_
  
 **DisplayName**  =   _string_
  
 **Flags**  =   _integer_
  
 **SpecialType** = 0|1 
  
 **Enum1**  =   _string_
  
Jede **[-Eigenschaft.** _im Abschnitt string_ **]** wird eine einzelne Eigenschaft beschrieben. Der **Type-Eintrag** gibt den MAPI-Eigenschaftstyp an, z. B. 3 (PT_I4) der Eigenschaft. Der **Eintrag NmidPropset** ist optional. Zusammen mit dem **Eintrag NmidString** oder **dem Eintrag NmidInteger** gibt der **Eintrag NmidPropset** den Namen der Eigenschaft an. **NmidString** gibt den Namen der Eigenschaft an, **während NmidInteger** den Bezeichner der Eigenschaft angibt. **NmidString** und **NmidInteger schließen** sich gegenseitig aus. 
  
Wenn festgelegt, **sollte NmidPropset** den Namen des Eigenschaftensatz enthalten. Wenn **NmidPropset** nicht vorhanden ist, wird basierend auf der folgenden Regel ein Standardwert festgelegt: Wenn **NmidInteger** vorhanden ist und der Wert kleiner als 0x8000 ist, wird **NmidPropset** auf PS_MAPI. Wenn der Wert **von NmidInteger** auf eine ganze Zahl festgelegt ist, die größer als 0x8000 ist, oder wenn er nicht vorhanden ist, wird **NmidPropset** auf PS_PUBLIC_STRINGS. 
  
Der **Eintrag DisplayName** enthält die Bezeichnung für die Eigenschaft. Der **Eintrag SpecialType** gibt an, dass es sich bei dieser Eigenschaft um eine spezielle Eigenschaft handelt, sofern vorhanden und ungleich Null. Derzeit ist **specialType** = 1 der einzige spezielle Eigenschaftstyp, der zeichenfolgenenumerierte Eigenschaften angibt. Wenn **SpecialType** auf 1 festgelegt ist, verweist **der Eintrag Enum1** auf **[Enum1.** _string_ **]** section. 
  
Im Folgenden finden Sie ein Beispiel für **einen Abschnitt [Properties]** und ein **[Properties.** _string_ **]** section. 
  
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

Der **Eintrag Enum1** im voranstellenden Beispiel verweist auf eine **nachfolgende [Enum1.** _string_ **]** -Abschnitt, der eine Aufzählung eines bestimmten Typs beschreibt. Eine solche Enumeration verknüpft die erste Eigenschaft in **der [Property.** _string_ **]** -Abschnitt mit einer integer-Eigenschaft, die als Index bezeichnet wird. Eine solche Enumeration enthält auch eine Liste der möglichen Werte, die das Anzeigeindexpaar annehmen kann. Das Angeben eines Eigenschaftstyps für die Enumeration ist nicht erforderlich, da ein **Enum1-Eintrag** definitionsgemäß immer den PT_I4 hat. Das Format für **[Enum1.** _string_ **]** section is: 
  
 **[Enum1.** _string_ **]**
  
 **NmidPropset**  =   _guid_
  
 **NmidString**  =   _string_
  
 **NmidInteger**  =   _integer_
  
 **EnumCount**  =   _integer_
  
 **Val.** _ganze Zahl_ **. Anzeigezeichenfolge**  =   
  
 **Val.** _ganze Zahl_ **. Index**  =   _ganzzahlig_
  
Im Folgenden finden Sie eine Beispieleigenschaftsdefinition für eine aufgezählte Eigenschaft mit dem Namen Fire Hazard mit den möglichen Werten Low, Medium und High.
  
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

 **[Enum1.** _string_ **]** -Abschnitte können von Anwendungen für zwei Zwecke verwendet werden: zum Beschleunigen der Filterung von Eigenschaften mithilfe des Indexes anstelle der Zeichenfolge und zum Sortieren nach einer anderen Reihenfolge als die alphanumerische Reihenfolge der Zeichenfolgenwerte. Die Sortierung kann beispielsweise auf der Basis der Reihenfolge "Low-Medium-High" statt "High-Medium-Low" durchgeführt werden. 
  

