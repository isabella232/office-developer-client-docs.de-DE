---
title: Zelle "Type" (Abschnitt "Text Fields")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1060
localization_priority: Normal
ms.assetid: 69d64520-9a47-07ca-09c7-d1e5da620348
description: Gibt einen Datentyp für den Textfeldwert an.
ms.openlocfilehash: 68bfa8a84adb0d46d9621e6fc5383f4b6606f542
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798328"
---
# <a name="type-cell-text-fields-section"></a>Type Cell (Text Fields Section)

Gibt einen Datentyp für den Textfeldwert an.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Zeichenfolge.  <br/> |
|2  <br/> |Number. Enthält Datum, Uhrzeit, Zeitdauer, Währungs- und Skalarwerte sowie Maß- und Winkelangaben. Geben Sie in der Zelle Format eine Formatierungsangabe an.  <br/> |
|5  <br/> |Datums- oder Uhrzeitwert. Zeigt Tage, Monate und Jahre oder Sekunden, Minuten und Stunden bzw. einen gemischten Datums- und Uhrzeitwert an. Geben Sie in der Zelle Format eine Formatierungsangabe an.  <br/> |
|6  <br/> |Zeitdauerwert. Zeigt die verstrichene Zeit an. Geben Sie in der Zelle Format eine Formatierungsangabe an.  <br/> |
|7  <br/> |Währungswert. Verwendet die aktuellen Landes-/Regionaleinstellungen des Systems. Geben Sie in der Zelle Format eine Formatierungsangabe an.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können auch den Wert dieser Zelle im Dialogfeld **Feld** festlegen (klicken Sie mit einem Shape ausgewählt haben, klicken Sie auf der Registerkarte **Einfügen** in der Gruppe **Text** auf **Feld** ). 
  
Zum Abrufen eines Verweises auf die Zelle Type nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Fields.Type [ *i* ] wobei *i* = < 1 >, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Type aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionTextField** <br/> |
|Zeilenindex:  <br/> |**VisRowField** +  *i* wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visFieldType** <br/> |
   

