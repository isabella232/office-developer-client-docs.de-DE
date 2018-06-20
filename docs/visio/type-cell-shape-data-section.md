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
ms.openlocfilehash: e5471dcc1ed487a5992779f1faa4763887bebb2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798327"
---
# <a name="type-cell-shape-data-section"></a>Type Cell (Shape Data Section)

Gibt einen Datentyp für den Shape-Datenwert an.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Zeichenfolge. Dies ist der Standard.  <br/> |**visPropTypeString** <br/> |
|1  <br/> |Feste Liste. Zeigt Feld Listenelemente in einem Dropdown Kombinationsfeld im Dialogfeld **Shape-Daten definieren** . Geben Sie die Listenelemente in der Zelle Format. Benutzer können nur jeweils ein Element aus der Liste auswählen.  <br/> |**visPropTypeListFix** <br/> |
|2  <br/> |Number. Enthält Datum, Uhrzeit, Zeitdauer, Währungs- und Skalarwerte sowie Maß- und Winkelangaben. Geben Sie in der Zelle Format eine Formatierungsangabe an.  <br/> |**visPropTypeNumber** <br/> |
|3  <br/> |Boolean-Wert. Zeigt FALSE oder TRUE als Elemente in einem Dropdown-Listenfeld im Dialogfeld **Shape-Daten definieren** ausgewählt werden können.  <br/> |**visPropTypeBool** <br/> |
|4  <br/> |Variable Liste. Zeigt Feld Listenelemente in einem Dropdown Kombinationsfeld im Dialogfeld **Shape-Daten definieren** . Geben Sie die Listenelemente in der Zelle Format. Benutzer können entweder ein Listenelement auswählen oder geben Sie ein neues Element, das der aktuellen Liste in die Zelle Format hinzugefügt wird.  <br/> |**visPropTypeListVar** <br/> |
|5  <br/> |Datums- oder Uhrzeitwert. Zeigt Tage, Monate und Jahre oder Sekunden, Minuten und Stunden bzw. einen gemischten Datums- und Uhrzeitwert an. Geben Sie in der Zelle Format eine Formatierungsangabe an.  <br/> |**visPropTypeDate** <br/> |
|6  <br/> |Zeitdauerwert. Zeigt die verstrichene Zeit an. Geben Sie in der Zelle Format eine Formatierungsangabe an.  <br/> |**visPropTypeDuration** <br/> |
|7  <br/> |Währungswert. Verwendet die aktuellen Landes-/Regionaleinstellungen des Systems. Geben Sie in der Zelle Format eine Formatierungsangabe an.  <br/> |**visPropTypeCurrency** <br/> |
   
## <a name="remarks"></a>Hinweise

Zum Abrufen eines Verweises auf die Zelle Type nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Eigenschaft. *Name* . Typ wobei Prop.  *Name* ist der Zeilenname  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Type aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionProp** <br/> |
|Zeilenindex:  <br/> |**VisRowProp** +  *i* wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visCustPropsType** <br/> |
   

