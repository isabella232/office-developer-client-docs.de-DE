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
description: Enthält die Informationen für ein einzelnes Shape-Datenelement, das einem Shape zugeordnet ist. Ein Shape enthält für jedes Shape-Datenelement eine Shape Data-Zeile.Shape Data-Zeilen tragen die Bezeichnung Prop.Name und enthalten die folgende Zellen. Weitere Informationen finden Sie in den Themen zu den einzelnen Zellen.
ms.openlocfilehash: 7bf7eafd1869aa3c3ee03efbde30560cdaaeb302
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797998"
---
# <a name="shape-data-row-shape-data-section"></a>Zeile "Shape Data" (Abschnitt "Shape Data")

Enthält die Informationen für ein einzelnes Shape-Datenelement, das einem Shape zugeordnet ist. Ein Shape enthält für jedes Shape-Datenelement eine Shape Data-Zeile.Shape Data-Zeilen tragen die Bezeichnung Prop.Name und enthalten die folgende Zellen. Weitere Informationen finden Sie in den Themen zu den einzelnen Zellen.
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[Label](label-cell-shape-data-section.md) <br/> |Gibt die Beschriftung an, die dem Benutzer im Dialogfeld bzw. Fenster **Shape-Daten** angezeigt wird.  <br/> |
|[Prompt](prompt-cell-shape-data-section.md) <br/> |Gibt den Text der Beschreibung oder Anweisung an, der Benutzern im Dialogfeld bzw. Fenster **Shape-Daten** oder beim Auswählen des Elements angezeigt wird.  <br/> |
|[Typ](type-cell-shape-data-section.md) <br/> |Gibt einen Datentyp für den Wert des Shape-Datenelements an: Zeichenfolge (0), eine feste Liste (1), eine Zahl (2), einen booleschen Wert (3), eine variable Liste (4), einen Datums- oder Uhrzeitwert (5), eine Zeitdauer (6) oder eine Währung (7).  <br/> |
|[Format](format-cell-shape-data-section.md) <br/> |Gibt die Formatierung eines Shape-Datenelements an.  <br/> |
|[Wert](value-cell-shape-data-section.md) <br/> |Enthält den Wert eines Elements, der im Dialogfeld oder Fenster **Shape-Daten** eingegeben wurde.  <br/> |
|[SortKey](sortkey-cell-shape-data-section.md) <br/> |Gibt einen Schlüssel an, nach dem die Elemente im Dialogfeld oder Fenster **Shape-Daten** aufgelistet werden.  <br/> |
|[Nicht sichtbare](invisible-cell-shape-data-section.md) <br/> |Gibt an, ob das Shape-Datenelement im Dialogfeld oder Fenster Shape-Daten sichtbar ist. TRUE = nicht sichtbar, FALSE = sichtbar.<br/> |
|[Bitten Sie](ask-cell-shape-data-section.md) <br/> |Bestimmt, ob der Benutzer beim Erstellen einer Instanz oder beim Duplizieren oder Kopieren eines Shapes aufgefordert wird, Informationen zu Shape-Daten einzugeben.  <br/> |
|[LangID](langid-cell-shape-data-section.md) <br/> |Gibt die Sprache an, in der der Wert des Shape-Datenelements angezeigt wird.  <br/> |
|[Kalender](calendar-cell-miscellaneous-section.md) <br/> |Gibt den Typ des Kalenders an, der verwendet wird, wenn ein Shape-Datenelement vom Typ Datum ist.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

 Sie können beliebig viele Eigenschaft hinzufügen.  *Namen* Zeilen wie Sie benötigen, den Zeilen aussagekräftige Namen zuweisen und Zellenwerte festlegen. Um eine vorhandene Shape-Datenabschnitt ein Shape-Datenelements hinzuzufügen, mit der rechten Maustaste in einer Zeile, und klicken Sie im Kontextmenü auf **Zeile einfügen** . 
  
Sie können diese Zellen anhand ihrer Zeilennamen verweisen, die in einem ShapeSheet-Fenster als roter Text angezeigt. Eigenschaft aussagekräftige Namen zuzuweisen. *Namen* Zeilen, klicken Sie auf die Zeile, und geben Sie einen Namen wie *Preis* , z. B., um die Zeile mit dem Namen Prop.Price zu erstellen. Sie können dann die Zelle Label verweisen, indem Sie Prop.Price.Label mit. 
  
Der eingegebene Zeilenname muss innerhalb des Abschnitts eindeutig sein.
  

