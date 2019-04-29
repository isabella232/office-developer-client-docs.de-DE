---
title: ISTHEMED Function
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: Gibt einen booleschen Wert zurück, der angibt, ob auf eine Form ein Design angewendet wurde.
ms.openlocfilehash: 49f53eaaacbdc86a633703d6ef847e38097f5122
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418120"
---
# <a name="isthemed-function"></a>ISTHEMED Function

Gibt einen booleschen Wert zurück, der angibt, ob auf eine Form ein Design angewendet wurde. 
  
## <a name="version-information"></a>Informationen zur Version

Hinzugefügte Version: Visio 2013
 
  
## <a name="syntax"></a>Syntax

 **** Isthemed ()
  
## <a name="return-value"></a>Rückgabewert

Boolesch
  
## <a name="remarks"></a>Bemerkungen

> [!NOTE]
> Die **** isdesigned-Funktion in Visio 2013 ersetzt die **CELLISTHEMED** -Funktion aus früheren Versionen von Visio. 
  
Mit **** der isthemed-Funktion können Sie die entsprechenden Teile der Formatierung eines Designs einem Shape zuweisen, aber die Möglichkeit, andere Bereiche der Designformatierung mit manuell angewendeten Formatierungen außer Kraft zu setzen. Wenn Sie das Design anschließend erneut anwenden, werden alle manuellen Formatierungen außer Kraft gesetzt, und die Form übernimmt alle Formatierungen des Designs. 
  
 **** Isdesigned ergibt true, wenn die [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) -Zelle in der Form größer als 0 ist. Wenn diese Zelle gleich 0 ist, wird isdesigned als FALSE ausgewertet. **** Das Design von DocumentSheet und PageSheet hat keinen Einfluss auf den Wert der **** isthemed-Funktion, die in einem ShapeSheet verwendet wird. Nur wenn die **** isthemed-Funktion in der PageSheet angezeigt wird, ist das Design der Seite wichtig. 
  
## <a name="example"></a>Beispiel

||||
|:-----|:-----|:-----|
|Cell  <br/> |Formel  <br/> |Ergebnis  <br/> |
|Char. Font  <br/> |IF (isdesigned (), THEMEVAL (), FONT ("Calibri")))  <br/> |Wenn auf die Form ein Design angewendet wird, akzeptiert der Shape-Text die Schriftartenformatierung des Designs. Wenn es sich nicht um ein Design handelt, wird der Shape-Text mit der Schriftart "Calibri" formatiert.  <br/> |
|Zelle LineColor  <br/> |IF (ISDESIGNED, RGB (255, 0, 0), RGB (0, 255, 0))  <br/> |Wenn auf die Form ein Design angewendet wird, ist die Linienfarbe des Shapes rot. Wenn es sich nicht um ein Design handelt, ist die Linienfarbe der Form grün.  <br/> |
   

