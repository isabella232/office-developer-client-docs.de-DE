---
title: Zelle "Type" (Abschnitt "Text Fields")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1060
ms.localizationpriority: medium
ms.assetid: 69d64520-9a47-07ca-09c7-d1e5da620348
description: Gibt einen Datentyp für den Textfeldwert an.
ms.openlocfilehash: 1b03caaa36b6c2fbc06a6295599853ef27d7629e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627237"
---
# <a name="type-cell-text-fields-section"></a>Zelle "Type" (Abschnitt "Text Fields")

Gibt einen Datentyp für den Textfeldwert an.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Zeichenfolge.  <br/> |
|2  <br/> |Number. Enthält Datum, Uhrzeit, Zeitdauer, Währungs- und Skalarwerte sowie Maß- und Winkelangaben. Geben Sie in der Zelle Format eine Formatierungsangabe an.  <br/> |
|5  <br/> |Datums- oder Uhrzeitwert. Zeigt Tage, Monate und Jahre oder Sekunden, Minuten und Stunden bzw. einen gemischten Datums- und Uhrzeitwert an. Geben Sie in der Zelle Format eine Formatierungsangabe an.  <br/> |
|6   <br/> |Zeitdauerwert. Zeigt die verstrichene Zeit an. Geben Sie in der Zelle Format eine Formatierungsangabe an.  <br/> |
|7   <br/> |Währungswert. Verwendet die aktuelle Landes-/Regionaleinstellungen des Systems. Geben Sie in der Zelle Format eine Formatierungsangabe an.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können den Wert dieser Zelle auch über das Dialogfeld **Feld** festlegen (bei ausgewählter Form klicken Sie auf der Registerkarte **"Einfügen"** in der **Textgruppe** auf **"Feld").** 
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle Type anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Fields.Type[ *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Type anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionTextField** <br/> |
|Zeilenindex:  <br/> |**visRowField**  +   *i* where *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visFieldType** <br/> |
   

