---
title: ClippingPath Cell (Foreign Image Info Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ec70417-5b23-45af-95a0-1b26f6791699
description: Enthält einen Verweis auf die Geometrie des Pfads, der ein Bild durch begrenzt wird.
ms.openlocfilehash: 9f1c159e303c1d7bc3467c36756a422a3f325c7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796631"
---
# <a name="clippingpath-cell-foreign-image-info-section"></a>ClippingPath Cell (Foreign Image Info Section)

Enthält einen Verweis auf die Geometrie des Pfads, der ein Bild durch begrenzt wird. 
  
## <a name="remarks"></a>Bemerkungen

Wenn die Zelle **ClippingPath** auf einen gültigen Pfad verweist, wird das Bild abgeschnitten, damit das Bild in den Pfad gerendert wird. Wenn die Zelle **ClippingPath** leer ist oder einen ungültigen Eintrag enthält, wird das Bild mit einem rechteckigen Clip unter Verwendung der Skalierung und Offset-Werte gerendert werden. 
  
> [!NOTE]
> Nur von einem Abschnitt [Geometry](geometry-section.md) des Bilds ShapeSheet definierten Pfade sind gültige Einträge für die Zelle **ClippingPath** . Cross-Tabellenbezüge können nicht verwendet werden, um ein Bild Clipping Pfad zu definieren. 
  
Wenn Sie einen Verweis auf die Zelle **ClippingPath** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
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

Sie können die umgebende Form eines Bilds in ein Oval ändern, die folgenden Schritte durch:
  
- Fügen Sie das Bild auf Zeichenbereich.
    
- Maustaste auf das Bild, und wählen Sie dann auf **ShapeSheet anzeigen**.
    
- Mit der rechten Sie Maustaste in das ShapeSheet, und wählen Sie **Im Abschnitt einfügen**.
    
- Klicken Sie im Dialogfeld **Abschnitt einfügen** wählen Sie **Geometrie aus** , und klicken Sie dann auf **OK**.
    
- Löschen Sie alle Zeilen in der neuen Geometrie-Abschnitt (z. B. "Geometry2").
    
- Mit der rechten Maustaste der verbleibenden Zeile, und klicken Sie dann auf **Zeilentyp ändern**.
    
- Klicken Sie im Dialogfeld **Zeilentyp ändern** wählen **Ellipse** aus, und klicken Sie dann auf **OK**.
    
- Legen Sie im Abschnitt **Foreign Image** , die Formel für die Zelle **ClippingPath** `="Geometry2.Path"` und akzeptieren Sie die Formel. 
    

