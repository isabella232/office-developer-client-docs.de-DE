---
title: Zelle "Format" (Abschnitt "Shape Data")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251340
localization_priority: Normal
ms.assetid: c36fc895-5577-59f6-0ff5-5892ca81a58f
description: Gibt die Formatierung eines Shape-Datenelements an, bei dem es sich um eine Zeichenfolge, eine feste Liste, eine Zahl, eine variable Liste, ein Datum oder eine Uhrzeit, eine Zeitdauer oder eine Währung handeln kann.
ms.openlocfilehash: 48342f21a107ff78fed2347fb679ed8199526056
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797081"
---
# <a name="format-cell-shape-data-section"></a>Zelle "Format" (Abschnitt "Shape Data")

Gibt die Formatierung eines Shape-Datenelements an, bei dem es sich um eine Zeichenfolge, eine feste Liste, eine Zahl, eine variable Liste, ein Datum oder eine Uhrzeit, eine Zeitdauer oder eine Währung handeln kann.
  
## <a name="remarks"></a>Hinweise

|**Shape-Datenelementtyp**|**Wert**|**Format Zelleninhalt**|
|:-----|:-----|:-----|
| Zeichenfolge  <br/> | 0  <br/> | Eine dem Datentyp entsprechende Formatierungsangabe.  <br/> |
| Feste Liste  <br/> | 1  <br/> | Die Elemente, die durch Semikolon getrennt in der Liste angezeigt werden sollen.  <br/> |
| Zahl  <br/> | 2  <br/> | Eine dem Datentyp entsprechende Formatierungsangabe.  <br/> |
| Variable Liste  <br/> | 4  <br/> | Die Elemente, die durch Semikolon getrennt in der Liste angezeigt werden sollen.  <br/> |
| Datum oder Uhrzeit  <br/> | 5  <br/> | Eine dem Datentyp entsprechende Formatierungsangabe.  <br/> |
| Dauer  <br/> | 6  <br/> | Eine dem Datentyp entsprechende Formatierungsangabe.  <br/> |
| Währung  <br/> | 7  <br/> | Eine dem Datentyp entsprechende Formatierungsangabe.  <br/> |
   
Als Beispiel für eine dem Datentyp entsprechende Formatierungsangabe angeben formatiert das Format Bild "# #/ 4 UU" das Zahl 12,43 In. als 12 2/4 Zoll. Weitere Informationen zum Festlegen einer Formatierungsangabe finden Sie unter [Informationen zu Formatierungsangaben](about-format-pictures.md).
  
Ein Beispiel für das Festlegen von Elementen für eine Liste wäre "Technik;Personal;Vertrieb;Marketing".
  
Datumswerte (Typ = 5) werden im kurzen Datumsformat angezeigt. Währungswerte (Type = 7) werden mithilfe des Benutzers die aktuelle Einstellung für die **Währung** auf der Registerkarte **Regionale Optionen** im Element **Regions- und Sprachoptionen** in **Der Systemsteuerung**angezeigt.
  
Eine Zahl (Typ = 2) kann einen Bemaßungs-, Skalar-, Winkel-, Datums-, Zeit- oder Währungswert darstellen. Wenn Sie sicherstellen möchten, dass eine eingegebene Zahl immer als Datum, Uhrzeit oder Währung ausgewertet wird, verwenden Sie anstelle einer Formatierungsangabe die Funktionen DATETIME oder CY in der Zelle Format.
  
Wenn Sie einen Verweis auf die Zelle Format nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Eigenschaft.  *Name* . Format, in dem Prop.  *Name* ist der Zeilenname  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Format aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionProp** <br/> |
| Zeilenindex:  <br/> |**VisRowProp** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCustPropsFormat** <br/> |
   

