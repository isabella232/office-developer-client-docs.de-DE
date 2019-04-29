---
title: Zelle "OnPage" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033793
localization_priority: Normal
ms.assetid: 4015506a-e24a-0276-c854-7791a7019067
description: Gibt an, ob die Zeichnung auf einer bestimmten Anzahl von Seiten gedruckt wird.
ms.openlocfilehash: 61d45a5bffdbb1afd5db9c608f80bc4f797f5191
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439604"
---
# <a name="onpage-cell-print-properties-section"></a>Zelle "OnPage" (Abschnitt "Print Properties")

Gibt an, ob die Zeichnung auf einer bestimmten Anzahl von Seiten gedruckt wird. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Das Zeichenblatt wird an eine bestimmte Anzahl von Drucker Seiten angepasst.  <br/> |
|FALSE  <br/> |Das Zeichenblatt wird nicht auf einer definierten Anzahl von Druckseiten ausgegeben (Standardwert).  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn die Zelle OnPage auf WAHR festgelegt ist, bestimmt Microsoft Visio anhand der Zellen PagesX und PagesY die Anzahl der Druckseiten, auf denen die Zeichnung ausgegeben werden soll. Die Werte in den Zellen ScaleX und ScaleY werden ignoriert. Diese Einstellung ist eine AutoSkalieren-Einstellung.
  
Dieser Wert entspricht der Option **an anpassen** auf der Register **Karte Druckeinrichtung** im Dialogfeld **Seite einrichten** (Klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil für die **Seite einrichten** ). 
  
Wenn Sie einen Verweis auf die Zelle onPage aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |OnPage  <br/> |
   
Wenn Sie einen Verweis auf die Zelle onPage aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPrintProperties** <br/> |
|Zellenindex:  <br/> |**visPrintPropertiesOnPage** <br/> |
   

