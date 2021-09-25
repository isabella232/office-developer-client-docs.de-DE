---
title: Zelle "Format" (Abschnitt "Shape Data")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251340
ms.localizationpriority: medium
ms.assetid: c36fc895-5577-59f6-0ff5-5892ca81a58f
description: Gibt die Formatierung eines Shape-Datenelements an, bei dem es sich um eine Zeichenfolge, eine feste Liste, eine Zahl, eine variable Liste, ein Datum oder eine Uhrzeit, eine Zeitdauer oder eine Währung handeln kann.
ms.openlocfilehash: e57e23525219ea1db515f303830464e7da363876
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574209"
---
# <a name="format-cell-shape-data-section"></a>Zelle "Format" (Abschnitt "Shape Data")

Gibt die Formatierung eines Shape-Datenelements an, bei dem es sich um eine Zeichenfolge, eine feste Liste, eine Zahl, eine variable Liste, ein Datum oder eine Uhrzeit, eine Zeitdauer oder eine Währung handeln kann.
  
## <a name="remarks"></a>HinwBemerkungeneise

|**Shape-Datenelementtyp**|**Wert**|**Inhalt der Zelle "Format"**|
|:-----|:-----|:-----|
| String  <br/> | 0  <br/> | Eine dem Datentyp entsprechende Formatierungsangabe.  <br/> |
| Feste Liste  <br/> | 1  <br/> | Die Elemente, die durch Semikolon getrennt in der Liste angezeigt werden sollen.  <br/> |
| Zahl  <br/> | 2  <br/> | Eine dem Datentyp entsprechende Formatierungsangabe.  <br/> |
| Variable Liste  <br/> | 4   <br/> | Die Elemente, die durch Semikolon getrennt in der Liste angezeigt werden sollen.  <br/> |
| Datum oder Uhrzeit  <br/> | 5  <br/> | Eine dem Datentyp entsprechende Formatierungsangabe.  <br/> |
| Dauer  <br/> | 6   <br/> | Eine dem Datentyp entsprechende Formatierungsangabe.  <br/> |
| Währung  <br/> | 7   <br/> | Eine dem Datentyp entsprechende Formatierungsangabe.  <br/> |
   
Als Beispiel für das Festlegen einer dem Datentyp entsprechenden Formatierungsangabe wird mit der Formatierungsangabe "# #/4 UU" die Zahl 12,43 in. als 12 2/4 ZOLL formatiert. Weitere Informationen zum Festlegen von Formatierungsangaben finden Sie unter [Informationen zu Formatierungsangaben](about-format-pictures.md).
  
Ein Beispiel für das Festlegen von Elementen für eine Liste wäre "Technik;Personal;Vertrieb;Marketing".
  
Datumswerte (Typ = 5) werden im kurzen Datumsformat angezeigt. Währungswerte (Typ = 7) werden mit den aktuellen Einstellungen des Benutzers für **Währung** auf der Registerkarte **Regionale Einstellungen** unter **Regions- und Sprachoptionen** in der **Systemsteuerung** angezeigt.
  
Eine Zahl (Typ = 2) kann einen Bemaßungs-, Skalar-, Winkel-, Datums-, Zeit- oder Währungswert darstellen. Wenn Sie sicherstellen möchten, dass eine eingegebene Zahl immer als Datum, Uhrzeit oder Währung ausgewertet wird, verwenden Sie anstelle einer Formatierungsangabe die Funktionen DATETIME oder CY in der Zelle Format.
  
Um einen Verweis auf die Zelle "Format" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Prop.  *Name*  . Format where Prop.  *Name*  ist der Zeilenname  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Format anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionProp** <br/> |
| Zeilenindex:  <br/> |**visRowProp**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visCustPropsFormat** <br/> |
   

