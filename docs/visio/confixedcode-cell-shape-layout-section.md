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
ms.openlocfilehash: b2b9cde309c720493f0e46962b2fe6c2e79545d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404183"
---
# <a name="confixedcode-cell-shape-layout-section"></a>Zelle "ConFixedCode" (Abschnitt "Shape Layout")

Bestimmt die Umleitung eines Verbinders.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Frei umleiten  <br/> |**visSLOConFixedRerouteFreely** <br/> |
|1  <br/> |Nach Bedarf umleiten (manuelles Umleiten)  <br/> |**visSLOConFixedRerouteAsNeeded** <br/> |
|2  <br/> |Nie umleiten  <br/> |**visSLOConFixedRerouteNever** <br/> |
|3  <br/> |Bei Überkreuzung umleiten  <br/> |**visSLOConFixedRerouteOnCrossover** <br/> |
|4  <br/> |Nur für internen Gebrauch.  <br/> |**visSLOConFixedByAlgFrom** <br/> |
|5  <br/> |Nur für internen Gebrauch.  <br/> |**visSLOConFixedByAlgTo** <br/> |
|6  <br/> |Nur für internen Gebrauch.  <br/> |**visSLOConFixedByAlgFromTo** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können den Wert dieser Zelle auch festlegen, indem Sie einen dynamischen Verbinder auswählen, auf der Registerkarte [Entwickler](run-in-developer-mode-display-the-developer-tab.md) in der Gruppe **Shape-Design** auf **Verhalten** klicken und dann auf die Registerkarte **Verbinder** klicken. 
  
Wenn Sie einen Verweis auf die Zelle Zelle ConFixedCode aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Zelle ConFixedCode  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle ConFixedCode aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLOConFixedCode** <br/> |
   

