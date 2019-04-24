---
title: Zelle "PaperKind" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60067
localization_priority: Normal
ms.assetid: b2c9616f-a144-eb99-54b6-b53745c7b4d6
description: Gibt den Papiertyp für den Druck der Seite an.
ms.openlocfilehash: 694aa1fb8b52f5ae323c47e9aab8715b4a48dfb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327062"
---
# <a name="paperkind-cell-print-properties-section"></a>Zelle "PaperKind" (Abschnitt "Print Properties")

Gibt den Papiertyp für den Druck der Seite an.
  
## <a name="remarks"></a>Bemerkungen

Diese Einstellung entspricht der Einstellung **Papierformat** im Dialogfeld **Druckeinrichtung** (Klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil für die **Seite einrichten** , und klicken Sie dann auf der Registerkarte **Druckeinrichtung** auf die Schaltfläche **Setup** ). 
  
Die numerischen Werte in dieser Zelle werden Konstanten (mit DMPAPER) zugeordnet, die für Papierauswahl in der Datei Microsoft Windows WinGDI. h definiert sind. 
  
Wenn Sie einen Verweis auf die Zelle PaperKind aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |PaperKind  <br/> |
   
Wenn Sie einen Verweis auf die Zelle PaperKind aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPrintProperties** <br/> |
|Zellenindex:  <br/> |**visPrintPropertiesPaperKind** <br/> |
   

