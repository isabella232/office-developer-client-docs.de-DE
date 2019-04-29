---
title: Zelle "LineColorTrans" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50120
localization_priority: Normal
ms.assetid: b68054b5-7efd-1156-9dc1-5ec94e18d227
description: Definiert die Transparenzstufe der Linienfarbe eines Shapes.
ms.openlocfilehash: 555ea15de0279a37bcf67de7374d922b8692ce02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414438"
---
# <a name="linecolortrans-cell-line-format-section"></a>Zelle "LineColorTrans" (Abschnitt "Line Format")

Definiert die Transparenzstufe der Linienfarbe eines Shapes.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0 - 100  <br/> |Stellt die Transparenz in Prozent dar. Der Standardwert ist 0% (vollständig undurchsichtig).  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Werte werden auf ein halbes Prozent gerundet. Ein Wert von 100% bezeichnet völlige Transparenz. Ein Shape, dem eine völlig transparente Linienfarbe zugewiesen wurde, verhält sich auf dem Zeichenblatt zwar genauso wie ein Shape ohne Linien, die Interaktion mit anderen Objekten auf dem Zeichenblatt verläuft aber genauso wie bei Festlegen der Transparenz auf 0%. 
  
Sie können diesen Wert auch festlegen, indem Sie das Schieberegler-Steuerelement im Dialogfeld **Linie** verwenden (klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Shape** auf **Linie**, zeigen Sie auf **Linienbreite**, und klicken Sie dann auf **Weitere Linien**).
  
Wenn Sie einen Verweis auf die Zelle Zelle linecolortrans aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Zelle linecolortrans  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle linecolortrans aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowLine** <br/> |
|Zellenindex:  <br/> |**visLineColorTrans** <br/> |
   

