---
title: Zelle "ConFixedCode" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm175
localization_priority: Normal
ms.assetid: 8e7c9080-7ef1-0696-a3d2-d8f57ea5ab9b
description: Bestimmt die Umleitung eines Verbinders.
ms.openlocfilehash: 448e721d8dd6e287c61488e28b875f76d0fa2977
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796706"
---
# <a name="confixedcode-cell-shape-layout-section"></a>ConFixedCode Cell (Shape Layout Section)

Bestimmt die Umleitung eines Verbinders.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |
          Frei umleiten
  <br/> |**visSLOConFixedRerouteFreely** <br/> |
|1  <br/> |
          Nach Bedarf umleiten (manuelles Umleiten)
  <br/> |**visSLOConFixedRerouteAsNeeded** <br/> |
|2  <br/> |
          Nie umleiten
  <br/> |**visSLOConFixedRerouteNever** <br/> |
|3  <br/> |
          Bei Überkreuzung umleiten
  <br/> |**visSLOConFixedRerouteOnCrossover** <br/> |
|4  <br/> |Nur zur internen Verwendung  <br/> |**visSLOConFixedByAlgFrom** <br/> |
|5  <br/> |Nur zur internen Verwendung  <br/> |**visSLOConFixedByAlgTo** <br/> |
|6  <br/> |Nur zur internen Verwendung  <br/> |**visSLOConFixedByAlgFromTo** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können auch den Wert für diese Zelle festlegen einen dynamischen Verbinder, indem Sie in der Gruppe **Shape-Design** auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) auf **Verhalten** klicken und dann auf die Registerkarte **Verbinder** . 
  
Wenn Sie einen Verweis auf die Zelle ConFixedCode aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ConFixedCode  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ConFixedCode aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLOConFixedCode** <br/> |
   

