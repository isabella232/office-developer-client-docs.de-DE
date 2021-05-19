---
title: Zeile "Shape Data" (Abschnitt "Shape Data")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251344
localization_priority: Normal
ms.assetid: f3a83496-fccc-9d6a-02b9-60ebaf4911ea
description: Enthält die Informationen für ein einzelnes Shape-Datenelement, das einem Shape zugeordnet ist. Ein Shape enthält eine Shape Data-Zeile für jedes Shape-Datenelement. Shape Data-Zeilen werden Prop.name benannt und enthalten die folgenden Zellen. Weitere Informationen finden Sie in den spezifischen Zellthemen.
ms.openlocfilehash: 058f8f180a2eca4736d06dfcc533d81f45150c86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415397"
---
# <a name="shape-data-row-shape-data-section"></a>Zeile "Shape Data" (Abschnitt "Shape Data")

Enthält die Informationen für ein einzelnes Shape-Datenelement, das einem Shape zugeordnet ist. Ein Shape enthält eine Shape Data-Zeile für jedes Shape-Datenelement. Shape Data-Zeilen werden Prop.name benannt und enthalten die folgenden Zellen. Weitere Informationen finden Sie in den spezifischen Zellthemen.
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[Label](label-cell-shape-data-section.md) <br/> |Gibt die Beschriftung an, die dem Benutzer im Dialogfeld bzw. Fenster **Shape-Daten** angezeigt wird.  <br/> |
|[Prompt](prompt-cell-shape-data-section.md) <br/> |Gibt den Text der Beschreibung oder Anweisung an, der Benutzern im Dialogfeld bzw. Fenster **Shape-Daten** oder beim Auswählen des Elements angezeigt wird.  <br/> |
|[Typ](type-cell-shape-data-section.md) <br/> |Gibt einen Datentyp für den Wert des Shape-Datenelements an: Zeichenfolge (0), eine feste Liste (1), eine Zahl (2), einen booleschen Wert (3), eine variable Liste (4), einen Datums- oder Uhrzeitwert (5), eine Zeitdauer (6) oder eine Währung (7).  <br/> |
|[Format](format-cell-shape-data-section.md) <br/> |Gibt die Formatierung eines Shape-Datenelements an.  <br/> |
|[Wert](value-cell-shape-data-section.md) <br/> |Enthält den Wert eines Elements, der im Dialogfeld oder Fenster **Shape-Daten** eingegeben wurde.  <br/> |
|[SortKey](sortkey-cell-shape-data-section.md) <br/> |Gibt einen Schlüssel an, nach dem die Elemente im Dialogfeld oder Fenster **Shape-Daten** aufgelistet werden.  <br/> |
|[Invisible](invisible-cell-shape-data-section.md) <br/> |Gibt an, ob das Shape-Datenelement im Dialogfeld oder Fenster **"Shape-Daten"** angezeigt wird. TRUE = nicht sichtbar; FALSE = sichtbar.  <br/> |
|[Fragen](ask-cell-shape-data-section.md) <br/> |Bestimmt, ob der Benutzer beim Erstellen einer Instanz oder beim Duplizieren oder Kopieren eines Shapes aufgefordert wird, Informationen zu Shape-Daten einzugeben.  <br/> |
|[LangID](langid-cell-shape-data-section.md) <br/> |Gibt die Sprache an, in der der Wert des Shape-Datenelements angezeigt wird.  <br/> |
|[Calendar](calendar-cell-miscellaneous-section.md) <br/> |Gibt den Typ des Kalenders an, der verwendet wird, wenn ein Shape-Datenelement vom Typ Datum ist.  <br/> |
   
## <a name="remarks"></a>Hinweise

 Sie können so viele Prop hinzufügen.  *name*  rows as you need, assign meaningful names to the rows, and set cell values. Klicken Sie zum Hinzufügen eines Shape-Datenelements zu einem vorhandenen Abschnitt Shape Data mit der rechten Maustaste auf eine Zeile, und klicken Sie im Kontextmenü **auf** Zeile einfügen. 
  
Sie können auf diese Zellen durch ihren Zeilennamen verweisen, der in einem ShapeSheet-Fenster in rotem Text angezeigt wird. Klicken Sie zum Zuweisen  aussagekräftiger Namen zu Prop.Name-Zeilen auf die Zeile, und geben Sie dann einen Namen wie *z.* B. Price ein, um den Zeilennamen Prop.Price zu erstellen. Anschließend können Sie mithilfe von Prop.Price.Label auf die Zelle Label verweisen. 
  
Der eingegebene Zeilenname muss innerhalb des Abschnitts eindeutig sein.
  

