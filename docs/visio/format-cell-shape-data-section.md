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
# <a name="format-cell-shape-data-section"></a>Format Cell (Shape Data Section)

Gibt die Formatierung eines Shape-Datenelements an, bei dem es sich um eine Zeichenfolge, eine feste Liste, eine Zahl, eine variable Liste, ein Datum oder eine Uhrzeit, eine Zeitdauer oder eine Währung handeln kann.
  
## <a name="remarks"></a>Hinweise

|**Shape-Datenelementtyp**|**Wert**|**Inhalt der Zelle "Format"**|
|:-----|:-----|:-----|
| Zeichenfolge  <br/> | 0  <br/> | Eine dem Datentyp entsprechende Formatierungsangabe.  <br/> |
| Feste Liste  <br/> | 1  <br/> | Die Elemente, die durch Semikolon getrennt in der Liste angezeigt werden sollen.  <br/> |
| Zahl  <br/> | 2  <br/> | Eine dem Datentyp entsprechende Formatierungsangabe.  <br/> |
| Variable Liste  <br/> | 4  <br/> | Die Elemente, die durch Semikolon getrennt in der Liste angezeigt werden sollen.  <br/> |
| Datum oder Uhrzeit  <br/> | 5  <br/> | Eine dem Datentyp entsprechende Formatierungsangabe.  <br/> |
| Dauer  <br/> | 6  <br/> | Eine dem Datentyp entsprechende Formatierungsangabe.  <br/> |
| Währung  <br/> | 7  <br/> | Eine dem Datentyp entsprechende Formatierungsangabe.  <br/> |
   
Als Beispiel für das Festlegen einer dem Datentyp entsprechenden Formatierungsangabe wird mit der Formatierungsangabe "# #/4 UU" die Zahl 12,43 in. als 12 2/4 ZOLL formatiert. Weitere Informationen zum Festlegen von Formatierungsangaben finden Sie unter [Informationen zu Formatierungsangaben](about-format-pictures.md).
  
Ein Beispiel für das Festlegen von Elementen für eine Liste wäre "Technik;Personal;Vertrieb;Marketing".
  
Datumswerte (Typ = 5) werden im kurzen Datumsformat angezeigt. Währungswerte (Typ = 7) werden mit den aktuellen Einstellungen des Benutzers für **Währung** auf der Registerkarte **Regionale Einstellungen** unter **Regions- und Sprachoptionen** in der **Systemsteuerung** angezeigt.
  
Eine Zahl (Typ = 2) kann einen Bemaßungs-, Skalar-, Winkel-, Datums-, Zeit- oder Währungswert darstellen. Wenn Sie sicherstellen möchten, dass eine eingegebene Zahl immer als Datum, Uhrzeit oder Währung ausgewertet wird, verwenden Sie anstelle einer Formatierungsangabe die Funktionen DATETIME oder CY in der Zelle Format.
  
Wenn Sie einen Verweis auf die Zelle Format aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Eigenschaft.  *Name* . Format, in dem Prop.  *Name* ist der Zeilenname  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Format aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionProp** <br/> |
| Zeilenindex:  <br/> |**VisRowProp** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCustPropsFormat** <br/> |
   

