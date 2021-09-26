---
title: Zelle "Format" (Abschnitt "Text Fields")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm400
ms.localizationpriority: medium
ms.assetid: ab937a00-84c2-6c1c-9080-b7c95ead4f63
description: Legt die Formatierung eines Textfelds in Form einer Zeichenfolge, einer Zahl, eines Datums oder einer Uhrzeit, einer Zeitdauer oder einer Währung fest.
ms.openlocfilehash: 97e49692f33f7ecee44a744002f5a35a2368ece9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598612"
---
# <a name="format-cell-text-fields-section"></a>Zelle "Format" (Abschnitt "Text Fields")

Legt die Formatierung eines Textfelds in Form einer Zeichenfolge, einer Zahl, eines Datums oder einer Uhrzeit, einer Zeitdauer oder einer Währung fest.
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn der Wert der Zelle Type 0, 2, 5, 6 oder 7 ist (Zeichenfolge, Zahl, Datum oder Uhrzeit, Dauer oder Währung), geben Sie ein für den Datentyp geeignetes Formatbild an. Beispielsweise formatiert das Formatbild "# #/4 UU" die Zahl 12,43 Zoll. als 12 2/4 ZOLL. Weitere Informationen zum Festlegen von Formatierungsangaben finden Sie unter [Informationen zu Formatierungsangaben](about-format-pictures.md).
  
Eine Zahl (Typ = 2) kann einen Bemaßungs-, Skalar-, Winkel-, Datums-, Zeit- oder Währungswert darstellen. Wenn Sie sicherstellen möchten, dass eine eingegebene Zahl immer als Datum, Uhrzeit oder Währung gewertet wird, verwenden Sie anstelle einer Formatierungsangabe die Funktionen DATETIME oder CY in der Zelle Format.
  
Um einen Verweis auf die Zelle "Format" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Fields.Format[  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Format anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionTextField** <br/> |
| Zeilenindex:  <br/> |**visRowField**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visFieldFormat** <br/> |
   

