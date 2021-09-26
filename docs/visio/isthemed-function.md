---
title: ISTHEMED Function
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: Gibt einen booleschen Wert zurück, der angibt, ob auf eine Form ein Design angewendet wurde.
ms.openlocfilehash: 56fdbe781f8178bc7a388ff2d0540b8d3f0c1dc2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612568"
---
# <a name="isthemed-function"></a>ISTHEMED Function

Gibt einen booleschen Wert zurück, der angibt, ob auf eine Form ein Design angewendet wurde. 
  
## <a name="version-information"></a>Informationen zur Version

Hinzugefügte Version: Visio 2013
 
  
## <a name="syntax"></a>Syntax

 **ISTHEMED**()
  
## <a name="return-value"></a>Rückgabewert

Boolesch
  
## <a name="remarks"></a>Bemerkungen

> [!NOTE]
> Die **ISTHEMED-Funktion** in Visio 2013 ersetzt die **CELLISTHEMED-Funktion** aus früheren Versionen von Visio. 
  
Mit der **ISTHEMED-Funktion** können Sie einer Form geeignete Teile der Formatierung eines Designs zuweisen, aber die Möglichkeit beibehalten, andere Teile der Designformatierung mit manuell angewendeter Formatierung außer Kraft zu setzen. Wenn Sie das Design anschließend erneut anwenden, werden alle manuellen Formatierungen überschrieben, und die Form übernimmt die gesamte Formatierung des Designs. 
  
 **ISTHEMED** wird zu TRUE ausgewertet, wenn die [Zelle ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) in der Form größer als 0 ist. Wenn diese Zelle gleich 0 ist, wird **ISTHEMED** als FALSE ausgewertet. Das Design von DocumentSheet und PageSheet wirkt sich nicht auf den Wert der in einem ShapeSheet **verwendeten ISTHEMED-Funktion** aus. Nur wenn die **ISTHEMED-Funktion** im PageSheet angezeigt wird, ist das Design der Seite wichtig. 
  
## <a name="example"></a>Beispiel

||||
|:-----|:-----|:-----|
|Cell  <br/> |Formel  <br/> |Result  <br/> |
|Char.Font  <br/> |IF(ISTHEMED(), THEMEVAL(), FONT("Calibri"))  <br/> |Wenn auf die Form ein Design angewendet wurde, akzeptiert der Formtext die Schriftformatierung aus dem Design. Wenn es sich bei der Form nicht um ein Design handelt, wird der Formtext mit der Schriftart "Calibri" formatiert.  <br/> |
|Linecolor  <br/> |IF(ISTHEMED, RGB(255, 0, 0), RGB(0, 255, 0))  <br/> |Wenn auf die Form ein Design angewendet wird, ist die Linienfarbe der Form rot. Wenn es sich bei der Form nicht um ein Design handelt, ist die Linienfarbe der Form grün.  <br/> |
   

