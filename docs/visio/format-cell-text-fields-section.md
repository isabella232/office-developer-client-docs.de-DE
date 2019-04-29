---
title: Zelle "Format" (Abschnitt "Text Fields")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm400
localization_priority: Normal
ms.assetid: ab937a00-84c2-6c1c-9080-b7c95ead4f63
description: Legt die Formatierung eines Textfelds in Form einer Zeichenfolge, einer Zahl, eines Datums oder einer Uhrzeit, einer Zeitdauer oder einer Währung fest.
ms.openlocfilehash: c1c7fc7e9c699b7642369fbb979c005829b06cb8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431519"
---
# <a name="format-cell-text-fields-section"></a>Zelle "Format" (Abschnitt "Text Fields")

Legt die Formatierung eines Textfelds in Form einer Zeichenfolge, einer Zahl, eines Datums oder einer Uhrzeit, einer Zeitdauer oder einer Währung fest.
  
## <a name="remarks"></a>Bemerkungen

Wenn der Wert der Zelle Type 0, 2, 5, 6 oder 7 (Zeichenfolge, Zahl, Datum oder Uhrzeit, Dauer oder Währung) ist, geben Sie ein für den Datentyp geeignetes Format Bild an. Beispielsweise formatiert das Format Bild "# #/4 UU" die Zahl 12,43 in. als 12 2/4 Zoll. Weitere Informationen zum Festlegen von Formatierungsangaben finden Sie unter [Informationen zu Formatierungsangaben](about-format-pictures.md).
  
Eine Zahl (Typ = 2) kann einen Bemaßungs-, Skalar-, Winkel-, Datums-, Zeit- oder Währungswert darstellen. Wenn Sie sicherstellen möchten, dass eine eingegebene Zahl immer als Datum, Uhrzeit oder Währung gewertet wird, verwenden Sie anstelle einer Formatierungsangabe die Funktionen DATETIME oder CY in der Zelle Format.
  
Wenn Sie einen Verweis auf die Zelle Format aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Fields. Format [ *i* ] wobei *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Format aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionTextField** <br/> |
| Zeilenindex:  <br/> |**visRowField** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visFieldFormat** <br/> |
   

