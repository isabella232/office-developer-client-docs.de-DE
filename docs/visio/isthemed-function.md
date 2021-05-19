---
title: ISTHEMED Function
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: Gibt einen booleschen Wert zurück, der angibt, ob auf ein Shape ein Design angewendet wurde.
ms.openlocfilehash: 49f53eaaacbdc86a633703d6ef847e38097f5122
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418120"
---
# <a name="isthemed-function"></a>ISTHEMED Function

Gibt einen booleschen Wert zurück, der angibt, ob auf ein Shape ein Design angewendet wurde. 
  
## <a name="version-information"></a>Informationen zur Version

Hinzugefügte Version: Visio 2013
 
  
## <a name="syntax"></a>Syntax

 **ISTHEMED**()
  
## <a name="return-value"></a>Rückgabewert

Boolesch
  
## <a name="remarks"></a>Bemerkungen

> [!NOTE]
> Die **ISTHEMED-Funktion** in Visio 2013 ersetzt die **CELLISTHEMED-Funktion** aus früheren Versionen Visio. 
  
Mit **der ISTHEMED-Funktion** können Sie einem Shape entsprechende Teile der Formatierung eines Designs zuweisen, aber die Möglichkeit beibehalten, andere Teile der Designformatierung mit manuell angewendeter Formatierung zu überschreiben. Wenn Sie das Design anschließend erneut anwenden, werden alle manuellen Formatierungen überschrieben, und die Form übernimmt alle Formatierungen des Designs. 
  
 **ISTHEMED wird** auf TRUE ausgewertet, wenn die [Zelle ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) in der Form größer als 0 ist. Wenn diese Zelle gleich 0 ist, wird **ISTHEMED** als FALSE ausgewertet. Das Design von DocumentSheet und PageSheet hat keine Auswirkungen auf den Wert der **ISTHEMED-Funktion,** die in einem ShapeSheet verwendet wird. Nur wenn die **ISTHEMED-Funktion** im PageSheet angezeigt wird, spielt das Design der Seite eine Rolle. 
  
## <a name="example"></a>Beispiel

||||
|:-----|:-----|:-----|
|Cell  <br/> |Formel  <br/> |Ergebnis  <br/> |
|Char.Font  <br/> |IF(ISTHEMED(), THEMEVAL(), FONT("Calibri"))  <br/> |Wenn auf das Shape ein Designdesign angewendet wurde, akzeptiert der Formtext die Schriftartformatierung aus dem Design. Wenn die Form nicht mit einem Bestimmten formatiert ist, wird der Formtext mit der Schriftart "Calibri" formatiert.  <br/> |
|LineColor  <br/> |IF(ISTHEMED, RGB(255, 0, 0), RGB(0, 255, 0))  <br/> |Wenn auf das Shape ein Gestaltungsschema angewendet wurde, ist die Linienfarbe des Shapes rot. Wenn die Form nicht mit Einem -Shape-gefärbt ist, ist die Linienfarbe des Shapes grün.  <br/> |
   

