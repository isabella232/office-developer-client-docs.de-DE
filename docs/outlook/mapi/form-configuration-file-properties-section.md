---
title: Abschnitt "Form Configuration File [Properties]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f31a08ce-3a56-4c90-9502-5bcb09d8d80f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fa32c4145292769951500b43f2684b6602552a1c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576254"
---
# <a name="form-configuration-file-properties-section"></a>Abschnitt "Form Configuration File [Properties]

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Im Abschnitt **[Eigenschaften]** werden die vollständigen Eigenschaften aufgelistet, die vom Formular verwendet und veröffentlicht werden. d. h. die Eigenschaften, die in benutzerdefinierten Nachrichten erstellt werden, die MAPI-Clientanwendungen beim Anzeigen von Spalten, Filtern von Inhaltstabellen, Einrichten von Suchergebnisordnern usw. verwenden können. Jeder Eintrag in dieser Eigenschaftenliste verweist auf eine nachfolgende **[Eigenschaft.** _string_ **]** section as shown following. 
  
 **[Eigenschaften]**
  
 **Eigenschaft.** _zeichenfolge_  =   _zeichenfolge_
  
Das Format einer [ **-Eigenschaft.** _string_] abschnitt lautet: 
  
 **[Eigenschaft.** _string_ **]**
  
 **Typ**  =   _ganze Zahl_
  
 **NmidPropset**  =   _GUID_
  
 **NmidString**  =   _zeichenfolge_
  
 **NmidInteger**  =   _ganze Zahl_
  
 **DisplayName**  =   _zeichenfolge_
  
 **Flags**  =   _ganze Zahl_
  
 **SpecialType** = 0|1 
  
 **Enumeration1**  =   _zeichenfolge_
  
Jede **[Eigenschaft.** im Abschnitt _string_ ] wird eine einzelne Eigenschaft beschrieben.  Der **Type-Eintrag** gibt den MAPI-Eigenschaftstyp an, z. B. 3 (PT_I4) der Eigenschaft. Der **NmidPropset-Eintrag** ist optional. Zusammen mit dem **NmidString-Eintrag** oder dem **NmidInteger-Eintrag** gibt der **NmidPropset-Eintrag** den Namen der Eigenschaft an. **NmidString** gibt den Namen der Eigenschaft an, **während NmidInteger** den Bezeichner der Eigenschaft angibt. **NmidString** und **NmidInteger** schließen sich gegenseitig aus. 
  
Wenn festgelegt, sollte **NmidPropset** den Namen des Eigenschaftensatzes enthalten. Wenn **NmidPropset** nicht vorhanden ist, wird basierend auf der folgenden Regel ein Standardwert festgelegt: Wenn **NmidInteger** vorhanden ist und der Wert kleiner als 0x8000 ist, wird **NmidPropset** auf PS_MAPI festgelegt. Wenn der Wert von **NmidInteger** auf eine ganze Zahl festgelegt ist, die größer als 0x8000 ist, oder wenn er nicht vorhanden ist, wird **NmidPropset** auf PS_PUBLIC_STRINGS festgelegt. 
  
Der **DisplayName-Eintrag** enthält die Beschriftung für die Eigenschaft. Wenn der **SpecialType-Eintrag** vorhanden und ungleich Null ist, wird angegeben, dass es sich bei dieser Eigenschaft um eine spezielle Eigenschaft handelt. Derzeit ist der einzige definierte spezielle Eigenschaftstyp **SpecialType** = 1, der zeichenfolgenaufgezählte Eigenschaften angibt. Wenn **SpecialType** auf 1 festgelegt ist, verweist der **Enum1-Eintrag** auf **[Enum1.** _string_ **]** section. 
  
Es folgt ein Beispiel für einen **[Properties]-Abschnitt** und ein **[Properties.)** _string_ **]** section. 
  
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

Der **Eintrag "Enum1"** im vorangehenden Beispiel verweist auf eine nachfolgende **[Enum1.** _Abschnitt_ string], der eine Enumeration eines bestimmten Typs beschreibt.  Eine solche Enumeration ordnet die erste Eigenschaft in der **[Eigenschaft.** _string_ **]** section with an integer property, called the index. Eine solche Enumeration enthält auch eine Liste der möglichen Werte, die das Anzeigeindexpaar annehmen kann. Das Angeben eines Eigenschaftstyps für die Enumeration ist nicht erforderlich, da ein **Enum1-Eintrag** definitionsgemäß immer den PT_I4 Typ aufweist. Das Format für **die [Enumeration1.** _string_ **]** section is: 
  
 **[Enumeration1.** _string_ **]**
  
 **NmidPropset**  =   _GUID_
  
 **NmidString**  =   _zeichenfolge_
  
 **NmidInteger**  =   _ganze Zahl_
  
 **EnumCount**  =   _ganze Zahl_
  
 **Val.** _ganze Zahl_ **.**  =   _Anzeigezeichenfolge_
  
 **Val.** _ganze Zahl_ **.**  =   _Index ganze Zahl_
  
Es folgt eine Beispieleigenschaftsdefinition für eine aufgezählte Eigenschaft namens "Fire Hazard" mit den möglichen Werten "Niedrig", "Mittel" und "Hoch".
  
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

 **[Enumeration1.** _Zeichenfolge_ **]-Abschnitte** können von Anwendungen für zwei Zwecke verwendet werden: zum Beschleunigen der Filterung von Eigenschaften mithilfe des Indexes anstelle der Zeichenfolge und zum Sortieren nach einer anderen Reihenfolge als die alphanumerische Reihenfolge der Zeichenfolgenwerte. Die Sortierung kann beispielsweise auf der Grundlage der Reihenfolge "Niedrig-Mittel-Hoch" anstelle von "Hoch-Mittel-Niedrig" erfolgen. 
  

