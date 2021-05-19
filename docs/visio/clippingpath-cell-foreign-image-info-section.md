---
title: Zelle "ClippingPath" (Abschnitt "Foreign Image Info")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ec70417-5b23-45af-95a0-1b26f6791699
description: Enthält einen Verweis auf die Geometrie des Pfads, an den ein Bild gebunden ist.
ms.openlocfilehash: cfbbb3ca7294f751f088df7c3284bf6461270af7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425512"
---
# <a name="clippingpath-cell-foreign-image-info-section"></a>Zelle "ClippingPath" (Abschnitt "Foreign Image Info")

Enthält einen Verweis auf die Geometrie des Pfads, an den ein Bild gebunden ist. 
  
## <a name="remarks"></a>Hinweise

Wenn die **Zelle ClippingPath** auf einen gültigen Pfad zeigt, wird das Bild abgeschnitten, sodass das Bild innerhalb des Pfads gerendert wird. Wenn die **Zelle ClippingPath** leer ist oder einen ungültigen Eintrag enthält, wird das Bild mithilfe der Skalierungs- und Offsetwerte mit einem rechteckigen Clip gerendert. 
  
> [!NOTE]
> Nur von einem [Geometry-Abschnitt](geometry-section.md) im ShapeSheet des Bilds definierte Pfade sind gültige Einträge für die **Zelle ClippingPath.** Querverweise können nicht zum Definieren eines Pfads für die Bildausschnitte verwendet werden. 
  
Verwenden Sie zum Erhalten eines Verweises auf die **Zelle ClippingPath** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ClippingPath  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **Zelle ClippingPath** nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowForeign** <br/> |
| Zellenindex:  <br/> |**visFrgnImgClippingPath** <br/> |
   
## <a name="example"></a>Beispiel

Sie können die begrenzungsförmige Form eines Bilds in ein Oval ändern, indem Sie die folgenden Schritte tun:
  
- Fügen Sie das Bild in den Zeichenbereich ein.
    
- Klicken Sie mit der rechten Maustaste auf das Bild, und wählen Sie **dann ShapeSheet anzeigen aus.**
    
- Klicken Sie mit der rechten Maustaste auf eine beliebige Stelle im ShapeSheet, und wählen **Sie Abschnitt einfügen aus.**
    
- Wählen Sie **im Dialogfeld Abschnitt** einfügen die Option **Geometrie** aus, und klicken Sie dann auf **OK**.
    
- Löschen Sie im neuen Abschnitt Geometry (z. B. "Geometry2") bis auf eine Zeile.
    
- Klicken Sie mit der rechten Maustaste auf die verbleibende Zeile, und klicken Sie dann **auf Zeilentyp ändern.**
    
- Wählen Sie im Dialogfeld **Zeilentyp** ändern die Option **Ellipse** aus, und klicken Sie dann auf **OK**.
    
- Legen Sie **im Abschnitt** Fremdes Bild die Formel für die **Zelle ClippingPath** auf und  `="Geometry2.Path"` akzeptieren Sie die Formel. 
    

