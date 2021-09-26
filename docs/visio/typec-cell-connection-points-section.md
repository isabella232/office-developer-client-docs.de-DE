---
title: Zelle "Type / C" (Abschnitt "Connection Points")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251723
ms.localizationpriority: medium
ms.assetid: 2264d026-2041-3855-2b23-553ce67ae69d
description: Legt den Verbindungspunkttyp fest.
ms.openlocfilehash: a770ac5dfce17e9334a09345de8698491536e0ad
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603242"
---
# <a name="type--c-cell-connection-points-section"></a>Zelle "Type / C" (Abschnitt "Connection Points")

Legt den Verbindungspunkttyp fest.
  
|**Wert**|**Typ**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Innere  <br/> |**visCnnctTypeInward** <br/> |
|1  <br/> |Äußere  <br/> |**visCnnctTypeOutward** <br/> |
|2  <br/> |Nach &amp; innen nach außen  <br/> |**visCnnctTypeInwardOutward** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Sie können den Verbindungspunkttyp auch festlegen, indem Sie das Tool **Automatischer Verbinder** sowie ein Shape auswählen und anschließend mit der rechten Maustaste auf einen Verbindungspunkt klicken. Dazu müssen Sie in den [Entwicklermodus](run-in-developer-mode-display-the-developer-tab.md) wechseln. 
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle Type/C anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Connections.Type[  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Type/C anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionConnectionPts** <br/> |
|Zeilenindex:  <br/> |**visRowConnectionPts**  +   *i* where *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visCnnctType** (nicht erweiterte Zeilen) **visCnnctC** (erweiterte Zeilen)  <br/> |
   
Informationen zu erweiterten und nicht erweiterten Zeilen finden Sie in der Zeile Connections Points.
  

