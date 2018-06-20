---
title: ISTHEMED Function
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: Gibt einen Boolean-Wert zurück, der angibt, ob ein Shape ein Design angewendet wurde.
ms.openlocfilehash: 4311780d8686b5792e999c204ec182d23efb723c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797269"
---
# <a name="isthemed-function"></a>ISTHEMED Function

Gibt einen Boolean-Wert zurück, der angibt, ob ein Shape ein Design angewendet wurde. 
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2013 
  
## <a name="syntax"></a>Syntax

 **ISTHEMED** ()
  
## <a name="return-value"></a>R�ckgabewert

Boolean
  
## <a name="remarks"></a>Hinweise

> [!NOTE]
> Die Funktion **ISTHEMED** in Visio 2013 ersetzt die **CELLISTHEMED** -Funktion aus früheren Versionen von Visio. 
  
Der **ISTHEMED** -Funktion, den Sie entsprechende Teile der Formatierung eines Designs auf eine Form zuweisen können jedoch die Möglichkeit, andere Teile des Designs mit Formatierung manuell angewendete Formatierung überschreiben beibehalten. Wenn Sie das Design anschließend erneut anwenden, manuelle Formatierung überschrieben, und die Form übernimmt alle Formatierungen des Designs. 
  
 **ISTHEMED** ergibt True, wenn die Zelle [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) in der Form größer als 0 ist. Wenn diese Zelle gleich 0 ist, berechnet **ISTHEMED** auf false festgelegt. Das Design der DocumentSheet und PageSheet hat keine Auswirkung auf den Wert der **ISTHEMED** -Funktion, die in einem ShapeSheet verwendet. Nur, wenn die Funktion **ISTHEMED** in wird wird die PageSheet der Seite Design Frage. 
  
## <a name="example"></a>Beispiel

||||
|:-----|:-----|:-----|
|Zelle  <br/> |Formel  <br/> |Ergebnis  <br/> |
|Char.Font  <br/> |IF(ISTHEMED(), THEMEVAL(), FONT("Calibri"))  <br/> |Wenn die Form ein entsprechendes mit Design versehenes angewendet hat, akzeptiert der Shape-Text die Formatierung aus dem Design Schriftart an. Wenn das Shape kein entsprechendes mit Design versehenes ist, wird der Shape-Text mit der Schriftart "Calibri" formatiert.  <br/> |
|LineColor  <br/> |IF (ISTHEMED, RGB (255, 0, 0), RGB (0, 255, 0))  <br/> |Wenn die Form ein entsprechendes mit Design versehenes angewendet hat, ist das Shape die Farbe Rot. Wenn das Shape kein entsprechendes mit Design versehenes ist, ist das Shape die Farbe Grün.  <br/> |
   

