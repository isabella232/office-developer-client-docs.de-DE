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
ms.openlocfilehash: 0e1721ea667ad3bcd9f35880ab4e63bc90802c32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797624"
---
# <a name="pagescale-cell-page-properties-section"></a>PageScale Cell (Page Properties Section)

Bestimmt den Wert der Seiteneinheit im aktuellen Zeichnungsmaßstab. Der Zeichnungsmaßstab für die Seite ist das Verhältnis der in der Zelle PageScale angezeigten Seiteneinheit zur in der Zelle DrawingScale angezeigten Zeichnungseinheit.
  
## <a name="remarks"></a>Bemerkungen

Sie können den Wert der Zelle PageScale auch im Dialogfeld Seite einrichten auf der Registerkarte Zeichnungsmaßstab festlegen (klicken Sie dazu auf der Registerkarte Entwurf auf den Pfeil neben Seite einrichten). Der Wert der Zelle ist die erste der beiden Zahlen im Feld Vordefinierter Maßstab oder Benutzerdefinierter Maßstab, je nach dem Zeichnungsmaßstab, der unter Zeichnungsmaßstab ausgewählt wurde. Wenn Sie beispielsweise einen Architekturmaßstab für Ihre Zeichnung auswählen, ist der Zeichnungsmaßstab für die Seite 3/32" = 1'0". Der Wert in der Zelle PageScale lautet 0,0938 in. (oder 3/32") und der Wert in der Zelle DrawingScale 1 ft.
  
Wenn Sie einen Verweis auf die Zelle PageScale aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |PageScale  <br/> |
   
Wenn Sie einen Verweis auf die Zelle PageScale aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPage** <br/> |
|Zellenindex:  <br/> |**visPageScale** <br/> |
   

