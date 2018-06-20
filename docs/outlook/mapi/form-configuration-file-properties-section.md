---
title: Formular Konfigurationsabschnitt Datei [Eigenschaften]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f31a08ce-3a56-4c90-9502-5bcb09d8d80f
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f582322c8ba2ffa0369792e531adf1ec4ccb3e28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791738"
---
# <a name="form-configuration-file-properties-section"></a>Formular Konfigurationsabschnitt Datei [Eigenschaften]

  
  
**Betrifft**: Outlook 
  
Im Abschnitt **[Eigenschaften]** werden den vollständigen Satz von Eigenschaften, die das Formular verwendet und veröffentlicht. d. h., können die Eigenschaften in der benutzerdefinierten Nachrichten, MAPI-Client Applications erstellt verwenden Sie beim Anzeigen von Spalten, Filtern von Inhalt Tabellen, Einrichten von Suchergebnissen Ordner, und so weiter. Jeder Eintrag in der Liste diese Eigenschaft verweist auf eine nachfolgende **[-Eigenschaft.** _Zeichenfolge_ **]** Abschnitt wie folgt dargestellt. 
  
 **[Eigenschaften]**
  
 **-Eigenschaft.** _Zeichenfolge_ =  _Zeichenfolge_
  
Das Format einer [ **-Eigenschaft.** _Zeichenfolge_] Abschnitt ist: 
  
 **[-Eigenschaft.** _Zeichenfolge_ **]**
  
 **Typ** =  _ganze Zahl_
  
 **NmidPropset** =  _Guid_
  
 **NmidString** =  _Zeichenfolge_
  
 **NmidInteger** =  _ganze Zahl_
  
 **DisplayName** =  _Zeichenfolge_
  
 **Flags** =  _ganze Zahl_
  
 **SpecialType** = 0 | 1 
  
 **Enum1** =  _Zeichenfolge_
  
Jede **[-Eigenschaft.** _Zeichenfolge_ **]** Abschnitt beschreibt eine einzelne Eigenschaft. Der Eintrag vom **Typ** gibt den MAPI-Eigenschaft, zum Beispiel 3 (PT_I4), der-Eigenschaft. Der Eintrag **NmidPropset** ist optional. zusammen mit den Eintrag **NmidString** oder den Eintrag **NmidInteger** gibt der Eintrag **NmidPropset** den Namen der Eigenschaft. **NmidString** gibt den Namen der Eigenschaft, während **NmidInteger** den Bezeichner der-Eigenschaft gibt. **NmidString** und **NmidInteger** schließen sich gegenseitig aus. 
  
Wenn Set **NmidPropset** der Name des Eigenschaftensatzes enthalten sollte. Wenn nicht vorhanden ist, **NmidPropset** auf eine standardmäßige auf der Grundlage der folgenden Regel festgelegt ist: Wenn **NmidInteger** vorhanden ist und dessen Wert kleiner als 0 x 8000 ist, **NmidPropset** auf PS_MAPI festgelegt ist. Wenn der Wert der **NmidInteger** auf eine ganze Zahl größer als 0 x 8000 festgelegt ist oder wenn es nicht vorhanden ist, wird die **NmidPropset** auf PS_PUBLIC_STRINGS festgelegt. 
  
Der Eintrag **"DisplayName"** enthält die Beschriftung für die Eigenschaft. Der Eintrag **SpecialType** , falls vorhanden und ungleich NULL bedeutet, dass diese Eigenschaft eine spezielle Eigenschaft ist. Derzeit ist der einzige spezielle Eigenschaftentyp definiert **SpecialType** = 1, womit Zeichenfolgeneigenschaften aufgelistet. Wenn **SpecialType** auf 1 festgelegt ist, der Eintrag **Enum1** verweist auf die **[Enum1.** _Zeichenfolge_ **]** Abschnitt. 
  
Nachfolgend sehen Sie ein Beispiel für einen Abschnitt **[Eigenschaften]** und eine **[Eigenschaften.** _Zeichenfolge_ **]** Abschnitt. 
  
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

Der Eintrag **Enum1** in der vorherigen Beispiel Verweise auf einer nachfolgenden **[Enum1.** _Zeichenfolge_ **]** Abschnitt eine Enumeration eines bestimmten Typs beschreiben. Eine-Enumeration ordnet die erste Eigenschaft in der **[-Eigenschaft.** _Zeichenfolge_ **]** Abschnitt mit einer ganzzahligen-Eigenschaft mit der Bezeichnung des Index. Eine-Enumeration enthält auch eine Liste der möglichen Werte, die das Display-Index-Paar übernehmen kann. Angeben einen Eigenschaftentyp für die Enumeration ist nicht erforderlich, da per Definition ein Eintrags **Enum1** immer der PT_I4-Typ hat. Das Format für die **[Enum1.** _Zeichenfolge_ **]** Abschnitt ist: 
  
 **[Enum1.** _Zeichenfolge_ **]**
  
 **NmidPropset** =  _Guid_
  
 **NmidString** =  _Zeichenfolge_
  
 **NmidInteger** =  _ganze Zahl_
  
 **EnumCount** =  _ganze Zahl_
  
 **Val.** _ganze Zahl_ **. Anzeige** =  _Zeichenfolge_
  
 **Val.** _ganze Zahl_ **. Index** =  _ganze Zahl_
  
Es folgt eine Beispiel-Eigenschaftendefinition für eine enumerierten-Eigenschaft mit dem Namen Brandgefahr und mögliche Werte der niedrig, Mittel und hoch.
  
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

 **[Enum1.** _Zeichenfolge_ **]** Abschnitte von Clientanwendungen für zwei Zwecke verwendet werden können: das Filtern von Eigenschaften mithilfe den Index anstelle der Zeichenfolge beschleunigt und von einer anderen Reihenfolge als die Zeichenfolgenwerte alphanumerischer Reihenfolge sortiert. Beispielsweise könnte Sortierung basierend auf Niedrig, Mittel-hoher Reihenfolge statt besonders niedrig Reihenfolge erfolgen. 
  

