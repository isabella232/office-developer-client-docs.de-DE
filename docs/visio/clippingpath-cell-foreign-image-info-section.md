---
title: Zelle "ClippingPath" (Abschnitt "Foreign Image Info")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 0ec70417-5b23-45af-95a0-1b26f6791699
description: Enthält einen Verweis auf die Geometrie des Pfads, an den ein Bild gebunden ist.
ms.openlocfilehash: 6f65317c014435dd90cb293766e59bd5f1818589
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577983"
---
# <a name="clippingpath-cell-foreign-image-info-section"></a>Zelle "ClippingPath" (Abschnitt "Foreign Image Info")

Enthält einen Verweis auf die Geometrie des Pfads, an den ein Bild gebunden ist. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn die Zelle **ClippingPath** auf einen gültigen Pfad zeigt, wird das Bild abgeschnitten, sodass das Bild innerhalb des Pfads gerendert wird. Wenn die Zelle **ClippingPath** leer ist oder einen ungültigen Eintrag enthält, wird das Bild mithilfe der Skalierungs- und Offsetwerte mit einem rechteckigen Clip gerendert. 
  
> [!NOTE]
> Nur durch einen [Geometry-Abschnitt](geometry-section.md) im ShapeSheet des Bilds definierte Pfade sind gültige Einträge für die **Zelle ClippingPath.** Blattübergreifende Verweise können nicht zum Definieren eines Bildbeschneidungspfads verwendet werden. 
  
Verwenden Sie Folgendes, um einen Verweis auf die **Zelle "ClippingPath"** anhand des Namens aus einer anderen Formel, anhand des Werts des **N-Attributs** eines **Cell-Elements** oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ClippingPath  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **Zelle ClippingPath** anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowForeign** <br/> |
| Zellenindex:  <br/> |**visFrgnImgClippingPath** <br/> |
   
## <a name="example"></a>Beispiel

Sie können die Begrenzungsform eines Bilds in ein Oval ändern, indem Sie folgendermaßen vorgehen:
  
- Fügen Sie das Bild in den Zeichenbereich ein.
    
- Klicken Sie mit der rechten Maustaste auf das Bild, und wählen Sie dann **ShapeSheet anzeigen** aus.
    
- Klicken Sie mit der rechten Maustaste auf eine beliebige Stelle im ShapeSheet, und wählen Sie **Abschnitt einfügen aus.**
    
- Wählen Sie im Dialogfeld Abschnitt **einfügen** die Option **Geometrie** aus, und klicken Sie dann auf **OK.**
    
- Löschen Sie im neuen Abschnitt Geometrie (z. B. "Geometry2") alle Zeilen außer einer Zeile.
    
- Klicken Sie mit der rechten Maustaste auf die verbleibende Zeile, und klicken Sie dann auf **Zeilentyp ändern.**
    
- Wählen Sie im Dialogfeld **Zeilentyp ändern** **die Option "Ellipse" aus,** und klicken Sie dann auf **"OK".**
    
- Legen Sie im Abschnitt **"Fremdbild"** die Formel für die Zelle **ClippingPath**  `="Geometry2.Path"` fest, und akzeptieren Sie dann die Formel. 
    

