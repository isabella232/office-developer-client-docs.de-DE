---
title: Zelle "Type" (Abschnitt "Shape Data")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1055
localization_priority: Normal
ms.assetid: 1e24a906-83ce-32d2-5d7b-ba6dd6eea2d3
description: Gibt einen Datentyp für den Shape-Datenwert an.
ms.openlocfilehash: c2d38b521a8597a4582a4145ad808b0c0e26ff0a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406248"
---
# <a name="type-cell-shape-data-section"></a>Zelle "Type" (Abschnitt "Shape Data")

Gibt einen Datentyp für den Shape-Datenwert an.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Zeichenfolge. Dies ist der Standard.  <br/> |**visPropTypeString** <br/> |
|1  <br/> |Feste Liste. Zeigt die Listenelemente in einem Dropdown-Kombinationsfeld im Dialogfeld **Shape-Daten definieren** an. Geben Sie die Listenelemente in der Zelle Format an. Benutzer können nur ein Element aus der Liste auswählen.  <br/> |**visPropTypeListFix** <br/> |
|2  <br/> |Number. Enthält Datum, Uhrzeit, Zeitdauer, Währungs- und Skalarwerte sowie Maß- und Winkelangaben. Geben Sie in der Zelle Format eine Formatierungsangabe an.  <br/> |**visPropTypeNumber** <br/> |
|3  <br/> |Boolean. Zeigt FALSE und TRUE als Elemente an, die Benutzer aus einem Dropdown-Listenfeld im Dialogfeld **Shape-Daten definieren** auswählen können.  <br/> |**visPropTypeBool** <br/> |
|4  <br/> |Variablenliste. Zeigt die Listenelemente in einem Dropdown-Kombinationsfeld im Dialogfeld **Shape-Daten definieren** an. Geben Sie die Listenelemente in der Zelle Format an. Benutzer können ein Listenelement auswählen oder ein neues Element eingeben, das der aktuellen Liste in der Zelle Format hinzugefügt wird.  <br/> |**visPropTypeListVar** <br/> |
|5  <br/> |Datums- oder Uhrzeitwert. Zeigt Tage, Monate und Jahre oder Sekunden, Minuten und Stunden bzw. einen gemischten Datums- und Uhrzeitwert an. Geben Sie in der Zelle Format eine Formatierungsangabe an.  <br/> |**visPropTypeDate** <br/> |
|6  <br/> |Zeitdauerwert. Zeigt die verstrichene Zeit an. Geben Sie in der Zelle Format eine Formatierungsangabe an.  <br/> |**visPropTypeDuration** <br/> |
|7  <br/> |Währungswert. Verwendet die aktuelle Landes-/Regionaleinstellungen des Systems. Geben Sie in der Zelle Format eine Formatierungsangabe an.  <br/> |**visPropTypeCurrency** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle "Type" aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Prop. *Name* . Geben Sie WHERE Prop ein.  *Name* ist der Name der Zeile  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Type nach Index aus einem Programm abrufen möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionProp** <br/> |
|Zeilenindex:  <br/> |**visRowProp** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visCustPropsType** <br/> |
   

