---
title: Zelle "ConFixedCode" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm175
ms.localizationpriority: medium
ms.assetid: 8e7c9080-7ef1-0696-a3d2-d8f57ea5ab9b
description: Bestimmt die Umleitung eines Verbinders.
ms.openlocfilehash: b7d72fd0de48f70290f7ed59d3861cdd06be9213
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560018"
---
# <a name="confixedcode-cell-shape-layout-section"></a>Zelle "ConFixedCode" (Abschnitt "Shape Layout")

Bestimmt die Umleitung eines Verbinders.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Frei umleiten  <br/> |**visSLOConFixedRerouteFreely** <br/> |
|1  <br/> |Nach Bedarf umleiten (manuelles Umleiten)  <br/> |**visSLOConFixedRerouteAsNeeded** <br/> |
|2  <br/> |Nie umleiten  <br/> |**visSLOConFixedRerouteNever** <br/> |
|3  <br/> |Bei Überkreuzung umleiten  <br/> |**visSLOConFixedRerouteOnCrossover** <br/> |
|4   <br/> |Nur für internen Gebrauch.  <br/> |**visSLOConFixedByAlgFrom** <br/> |
|5  <br/> |Nur für internen Gebrauch.  <br/> |**visSLOConFixedByAlgTo** <br/> |
|6   <br/> |Nur für internen Gebrauch.  <br/> |**visSLOConFixedByAlgFromTo** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Sie können den Wert dieser Zelle auch festlegen, indem Sie einen dynamischen Verbinder auswählen, in der Gruppe **"Shape-Design"** auf der Registerkarte ["Entwickler"](run-in-developer-mode-display-the-developer-tab.md) auf **"Verhalten"** klicken und dann auf die Registerkarte **"Connector"** klicken. 
  
Um einen Verweis auf die Zelle "ConFixedCode" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ConFixedCode  <br/> |
   
Um einen Verweis auf die Zelle "ConFixedCode" anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLOConFixedCode** <br/> |
   

