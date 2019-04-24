---
title: ClippingPath Cell (Foreign Image Info section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ec70417-5b23-45af-95a0-1b26f6791699
description: Enthält einen Verweis auf die Geometrie des Pfads, an den ein Bild gebunden ist.
ms.openlocfilehash: cfbbb3ca7294f751f088df7c3284bf6461270af7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341860"
---
# <a name="clippingpath-cell-foreign-image-info-section"></a>ClippingPath Cell (Foreign Image Info section)

Enthält einen Verweis auf die Geometrie des Pfads, an den ein Bild gebunden ist. 
  
## <a name="remarks"></a>Bemerkungen

Wenn die **ClippingPath** -Zelle auf einen gültigen Pfad zeigt, wird das Bild abgeschnitten, sodass das Bild innerhalb des Pfads gerendert wird. Wenn die Zelle **ClippingPath** leer ist oder einen ungültigen Eintrag enthält, wird das Bild mit einem rechteckigen Clip mit den Werten Scale und Offset gerendert. 
  
> [!NOTE]
> Nur Pfade, die durch einen [Geometry](geometry-section.md) -Abschnitt im ShapeSheet des Bilds definiert sind, sind gültige Einträge für die Zelle **ClippingPath** . Für die Definition eines Bild Beschneidungspfads können keine Kreuz Blatt Referenzen verwendet werden. 
  
Wenn Sie einen Verweis auf die Zelle **ClippingPath** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ClippingPath  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **ClippingPath** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowForeign** <br/> |
| Zellenindex:  <br/> |**visFrgnImgClippingPath** <br/> |
   
## <a name="example"></a>Beispiel

Sie können die Begrenzungsform eines Bilds in ein Oval ändern, indem Sie folgendermaßen vorgehen:
  
- Fügen Sie das Bild in den Zeichenbereich ein.
    
- Klicken Sie mit der rechten Maustaste auf das Bild, und klicken Sie dann auf **ShapeSheet anzeigen**.
    
- Klicken Sie mit der rechten Maustaste auf eine beliebige Stelle im ShapeSheet, und wählen Sie **Einfügen**aus.
    
- Wählen Sie im Dialogfeld **Abschnitt einfügen** die Option **Geometrie** aus, und klicken Sie dann auf **OK**.
    
- Löschen Sie im Abschnitt neue Geometrie (beispielsweise "Geometry2") nur eine Zeile.
    
- Klicken Sie mit der rechten Maustaste auf die verbleibende Zeile, und klicken Sie dann auf **zeilenTyp ändern**.
    
- Wählen Sie im Dialogfeld **zeilenTyp ändern** die Option **Ellipse** aus, und klicken Sie dann auf **OK**.
    
- Legen Sie im Abschnitt **fremdes Bild** die Formel für die Zelle **ClippingPath** auf `="Geometry2.Path"` fest, und akzeptieren Sie die Formel. 
    

