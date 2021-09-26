---
title: Zelle "Date" (Abschnitt "Annotation")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60036
ms.localizationpriority: medium
ms.assetid: f1f11803-614b-a40d-0a2d-131093e7609e
description: Enthält Datum und Uhrzeit der letzten Bearbeitung des Kommentars.
ms.openlocfilehash: e899fe5b74f45a41a38f48710d5da297a50d5915
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612883"
---
# <a name="date-cell-annotation-section"></a>Zelle "Date" (Abschnitt "Annotation")

Enthält Datum und Uhrzeit der letzten Bearbeitung des Kommentars. 
  
> [!NOTE]
> Diese Zelle wird nur zum Nachverfolgen von Kommentaren beim Öffnen einer VSD-Datei in Microsoft Visio 2013 oder beim Speichern einer VSDX-Datei im VSD-Dateiformat verwendet. Es wird nicht zum Nachverfolgen von Kommentaren in VSDX-Dokumenten in Visio 2013 verwendet. 
  
## <a name="remarks"></a>Bemerkungen

Auf der Benutzeroberfläche wird im Kommentarfeld nur das Datum angezeigt.
  
Um einen Verweis auf die Zelle Date anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Annotation.Date[  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Um einen Verweis auf die Zelle Date anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionAnnotation** <br/> |
| Zeilenindex:  <br/> |**visRowAnnotation**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visAnnotationDate** <br/> |
   

