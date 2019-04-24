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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328105"
---
# <a name="form-configuration-file-properties-section"></a>Formular Konfigurationsdatei [Properties] Abschnitt

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Abschnitt **[Properties]** enthält den vollständigen Satz von Eigenschaften, die vom Formular verwendet und veröffentlicht werden. Das heißt, die Eigenschaften, die es in seinen benutzerdefinierten Nachrichten erstellt, die MAPI-Clientanwendungen beim Anzeigen von Spalten, Filtern von Inhaltstabellen, Einrichten von Suchergebnis Ordnern usw. verwenden können. Jeder Eintrag in dieser Eigenschaftenliste verweist auf eine nachfolgende **[Eigenschaft.** _Zeichenfolge_ **]** -Abschnitt wie folgt dargestellt. 
  
 **Eigenschaften**
  
 **Eigenschaft.** _Zeichen_ =  __ Folge
  
Das Format einer [ **-Eigenschaft.** _Zeichenfolge_] Section ist: 
  
 **Eigenschaft.** _Zeichenfolge_ **]**
  
 **Typ** =  _Integer_
  
 **NmidPropset** =  -_GUID_
  
 **NmidString** =  -_Zeichenfolge_
  
 **NmidInteger** =  -_Ganzzahl_
  
 **DisplayName** =  -_Zeichenfolge_
  
 **Flags** =  -_Ganzzahl_
  
 **Specialtype** = 0 | 1 
  
 **Enum1** =  -_Zeichenfolge_
  
Jede **[Eigenschaft.** _Zeichenfolge_ **]** section beschreibt eine einzelne Eigenschaft. Der **Type** -Eintrag gibt den MAPI-Eigenschaftentyp (beispielsweise 3 (PT_I4)) der Eigenschaft an. Der **NmidPropset** -Eintrag ist optional; zusammen mit dem **NmidString** -Eintrag oder dem **NmidInteger** -Eintrag gibt der **NmidPropset** -Eintrag den Namen der Eigenschaft an. **NmidString** gibt den Namen der Eigenschaft an, während **NmidInteger** den Bezeichner der Eigenschaft liefert. **NmidString** und **NmidInteger** schließen sich gegenseitig aus. 
  
Wenn festgelegt, sollte **NmidPropset** den Namen des Eigenschaftensatzes enthalten. Wenn nicht vorhanden, wird **NmidPropset** auf einen Standardwert basierend auf der folgenden Regel festgelegt: Wenn **NmidInteger** vorhanden ist und dessen Value kleiner als 0X8000 ist, wird **NmidPropset** auf PS_MAPI festgelegt. Wenn der Wert von **NmidInteger** auf eine ganze Zahl größer als 0X8000 festgelegt ist oder abwesend ist, wird **NmidPropset** auf PS_PUBLIC_STRINGS festgelegt. 
  
Der Eintrag **DisplayName** enthält die Bezeichnung für die Eigenschaft. Der **specialtype** -Eintrag, sofern vorhanden, und ungleich NULL gibt an, dass diese Eigenschaft eine spezielle Eigenschaft ist. Derzeit ist der einzige definierte Eigenschafts specialtype **** = 1, der Aufzählungs Eigenschaften für die Zeichenfolge angibt. Wenn **specialtype** auf 1 festgelegt ist, verweist der **Enum1** -Eintrag auf den **[Enum1.** _Zeichenfolge_ **]** -Abschnitt. 
  
Es folgt ein Beispiel für einen **[Properties]** -Abschnitt und eine **[Properties.** _Zeichenfolge_ **]** -Abschnitt. 
  
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

Der **Enum1** -Eintrag im vorherigen Beispiel verweist auf eine nachfolgende **[Enum1.** _Zeichenfolge_ **]** -Abschnitt, der eine Enumeration eines bestimmten Typs beschreibt. Eine solche Enumeration ordnet die erste Eigenschaft in der **[-Eigenschaft.** _Zeichenfolge_ **]** Section mit einer Integer-Eigenschaft, die als Index bezeichnet wird. Eine solche Enumeration enthält auch eine Liste der möglichen Werte, die das Paar vom Anzeigeindex annehmen kann. Das Angeben eines Eigenschaftentyps für die Enumeration ist nicht erforderlich, da ein **Enum1** -Eintrag per Definition immer den PT_I4-Typ aufweist. Das Format für **[Enum1.** _Zeichenfolge_ **]** section ist: 
  
 **[Enum1.** _Zeichenfolge_ **]**
  
 **NmidPropset** =  -_GUID_
  
 **NmidString** =  -_Zeichenfolge_
  
 **NmidInteger** =  -_Ganzzahl_
  
 **EnumCount** =  -_Ganzzahl_
  
 **Val.** _ganze Zahl_ **. ** =  _Zeichenfolge_
  
 **Val.** _ganze Zahl_ **. Index** =  _Ganzzahl_
  
Es folgt ein Beispiel für eine Eigenschaftendefinition für eine aufgezählte Eigenschaft mit dem Namen Fire Hazard mit möglichen Werten von niedrig, Mittel und hoch.
  
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

 **[Enum1.** _Zeichenfolge_ **]** Abschnitte können von Anwendungen aus zwei Gründen verwendet werden: um die Filterung von Eigenschaften zu beschleunigen, indem Sie den Index anstelle der Zeichenfolge verwenden und nach einer anderen Reihenfolge als die alphanumerische Reihenfolge der Zeichenfolgenwerte sortieren. Beispielsweise kann die Sortierung basierend auf der Reihenfolge von niedrig-bis mittel-groß statt der Reihenfolge von High-Medium-Low durchgeführt werden. 
  

