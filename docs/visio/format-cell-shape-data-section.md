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
ms.openlocfilehash: bb02cfefd6dc93798ca5e2b0c657e4616515fd0e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415362"
---
# <a name="format-cell-shape-data-section"></a>Zelle "Format" (Abschnitt "Shape Data")

Gibt die Formatierung eines Shape-Datenelements an, bei dem es sich um eine Zeichenfolge, eine feste Liste, eine Zahl, eine variable Liste, ein Datum oder eine Uhrzeit, eine Zeitdauer oder eine Währung handeln kann.
  
## <a name="remarks"></a>Hinweise

|**Shape-Datenelementtyp**|**Wert**|**Inhalt der Zelle "Format"**|
|:-----|:-----|:-----|
| String  <br/> | 0  <br/> | Eine dem Datentyp entsprechende Formatierungsangabe.  <br/> |
| Feste Liste  <br/> | 1  <br/> | Die Elemente, die durch Semikolon getrennt in der Liste angezeigt werden sollen.  <br/> |
| Nummer  <br/> | 2  <br/> | Eine dem Datentyp entsprechende Formatierungsangabe.  <br/> |
| Variable Liste  <br/> | 4   <br/> | Die Elemente, die durch Semikolon getrennt in der Liste angezeigt werden sollen.  <br/> |
| Datum oder Uhrzeit  <br/> | 5   <br/> | Eine dem Datentyp entsprechende Formatierungsangabe.  <br/> |
| Dauer  <br/> | 6   <br/> | Eine dem Datentyp entsprechende Formatierungsangabe.  <br/> |
| Währung  <br/> | 7   <br/> | Eine dem Datentyp entsprechende Formatierungsangabe.  <br/> |
   
Als Beispiel für das Festlegen einer dem Datentyp entsprechenden Formatierungsangabe wird mit der Formatierungsangabe "# #/4 UU" die Zahl 12,43 in. als 12 2/4 ZOLL formatiert. Weitere Informationen zum Festlegen von Formatierungsangaben finden Sie unter [Informationen zu Formatierungsangaben](about-format-pictures.md).
  
Ein Beispiel für das Festlegen von Elementen für eine Liste wäre "Technik;Personal;Vertrieb;Marketing".
  
Datumswerte (Typ = 5) werden im kurzen Datumsformat angezeigt. Währungswerte (Typ = 7) werden mit den aktuellen Einstellungen des Benutzers für **Währung** auf der Registerkarte **Regionale Einstellungen** unter **Regions- und Sprachoptionen** in der **Systemsteuerung** angezeigt.
  
Eine Zahl (Typ = 2) kann einen Bemaßungs-, Skalar-, Winkel-, Datums-, Zeit- oder Währungswert darstellen. Wenn Sie sicherstellen möchten, dass eine eingegebene Zahl immer als Datum, Uhrzeit oder Währung ausgewertet wird, verwenden Sie anstelle einer Formatierungsangabe die Funktionen DATETIME oder CY in der Zelle Format.
  
Um einen Verweis auf die Zelle Format anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Prop.  *Name*  . Formatieren, in dem Prop.  *Name*  ist der Zeilenname  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Format nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionProp** <br/> |
| Zeilenindex:  <br/> |**visRowProp**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visCustPropsFormat** <br/> |
   

