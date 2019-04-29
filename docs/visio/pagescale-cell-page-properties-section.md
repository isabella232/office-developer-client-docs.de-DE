---
title: Zelle "PageScale" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm775
localization_priority: Normal
ms.assetid: e1da84b3-fd15-12b9-9342-0412e818b3b9
description: Bestimmt den Wert der Seiteneinheit im aktuellen Zeichnungsmaßstab. Der Zeichnungsmaßstab für die Seite ist das Verhältnis der in der Zelle PageScale angezeigten Seiteneinheit zur in der Zelle DrawingScale angezeigten Zeichnungseinheit.
ms.openlocfilehash: 0763fd6fad5f64bc741cbdd1e1227b0982323841
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405534"
---
# <a name="pagescale-cell-page-properties-section"></a>Zelle "PageScale" (Abschnitt "Page Properties")

Bestimmt den Wert der Seiteneinheit im aktuellen Zeichnungsmaßstab. Der Zeichnungsmaßstab für die Seite ist das Verhältnis der in der Zelle PageScale angezeigten Seiteneinheit zur in der Zelle DrawingScale angezeigten Zeichnungseinheit.
  
## <a name="remarks"></a>Bemerkungen

Sie können den Wert der Zelle PageScale auch auf der Registerkarte **Zeichnungs Skala** im Dialogfeld **Seite** einrichten festlegen (Klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil für die **Seite einrichten** ). Der Wert der Zelle ist die erste der beiden Zahlen im vordefinierten **** Feld Skalieren oder **Benutzerdefiniert** , je nachdem, welche Zeichnungs Skalierungseinstellung unter **Zeichnungsmaßstab**ausgewählt ist. Wenn Sie beispielsweise einen architektonischen Maßstab für Ihre Zeichnung auswählen, lautet der Zeichnungsmaßstab für die Seite 3/32 "= 1 ' 0". Der Wert in der Zelle PageScale ist 0,0938. (oder 3/32 ") und der Wert in der Zelle DrawingScale ist 1 ft.
  
Wenn Sie einen Verweis auf die Zelle PageScale aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |PageScale  <br/> |
   
Wenn Sie einen Verweis auf die Zelle PageScale aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPage** <br/> |
|Zellenindex:  <br/> |**visPageScale** <br/> |
   

