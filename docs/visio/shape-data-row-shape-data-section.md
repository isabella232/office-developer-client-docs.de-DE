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
description: Enthält die Informationen für ein einzelnes Shape-Datenelement, das einem Shape zugeordnet ist. Ein Shape enthält eine Shape-Datenzeile für jedes Shape-Datenelement. Shape-Datenzeilen heißen Prop.name und enthalten die folgenden Zellen. Weitere Informationen finden Sie in den Themen zu bestimmten Zellen.
ms.openlocfilehash: 058f8f180a2eca4736d06dfcc533d81f45150c86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415397"
---
# <a name="shape-data-row-shape-data-section"></a>Zeile "Shape Data" (Abschnitt "Shape Data")

Enthält die Informationen für ein einzelnes Shape-Datenelement, das einem Shape zugeordnet ist. Ein Shape enthält eine Shape-Datenzeile für jedes Shape-Datenelement. Shape-Datenzeilen heißen Prop.name und enthalten die folgenden Zellen. Weitere Informationen finden Sie in den Themen zu bestimmten Zellen.
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[Label](label-cell-shape-data-section.md) <br/> |Gibt die Beschriftung an, die dem Benutzer im Dialogfeld bzw. Fenster **Shape-Daten** angezeigt wird.  <br/> |
|[Prompt](prompt-cell-shape-data-section.md) <br/> |Gibt den Text der Beschreibung oder Anweisung an, der Benutzern im Dialogfeld bzw. Fenster **Shape-Daten** oder beim Auswählen des Elements angezeigt wird.  <br/> |
|[Type](type-cell-shape-data-section.md) <br/> |Gibt einen Datentyp für den Wert des Shape-Datenelements an: Zeichenfolge (0), eine feste Liste (1), eine Zahl (2), einen booleschen Wert (3), eine variable Liste (4), einen Datums- oder Uhrzeitwert (5), eine Zeitdauer (6) oder eine Währung (7).  <br/> |
|[Format](format-cell-shape-data-section.md) <br/> |Gibt die Formatierung eines Shape-Datenelements an.  <br/> |
|[Wert](value-cell-shape-data-section.md) <br/> |Enthält den Wert eines Elements, der im Dialogfeld oder Fenster **Shape-Daten** eingegeben wurde.  <br/> |
|[SortKey](sortkey-cell-shape-data-section.md) <br/> |Gibt einen Schlüssel an, nach dem die Elemente im Dialogfeld oder Fenster **Shape-Daten** aufgelistet werden.  <br/> |
|[Unsichtbar](invisible-cell-shape-data-section.md) <br/> |Gibt an, ob das Shape-Datenelement im Dialogfeld oder Fenster **Shape-Daten** angezeigt wird. TRUE = nicht sichtbar; FALSE = sichtbar.  <br/> |
|[Bitten](ask-cell-shape-data-section.md) <br/> |Bestimmt, ob der Benutzer beim Erstellen einer Instanz oder beim Duplizieren oder Kopieren eines Shapes aufgefordert wird, Informationen zu Shape-Daten einzugeben.  <br/> |
|[LangID](langid-cell-shape-data-section.md) <br/> |Gibt die Sprache an, in der der Wert des Shape-Datenelements angezeigt wird.  <br/> |
|[Kalender](calendar-cell-miscellaneous-section.md) <br/> |Gibt den Typ des Kalenders an, der verwendet wird, wenn ein Shape-Datenelement vom Typ Datum ist.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

 Sie können beliebig viele Requisiten hinzufügen.  *benennen* Sie Zeilen, die Sie benötigen, und weisen Sie den Zeilen aussagekräftige Namen zu. Klicken Sie zum Hinzufügen eines Shape-Datenelements zu einem vorhandenen Shape-Datenabschnitt mit der rechten Maustaste auf eine Zeile, und klicken Sie dann im Kontextmenü auf **Zeile einfügen** . 
  
Sie können auf diese Zellen anhand ihres Zeilennamens verweisen, der in einem ShapeSheet-Fenster in rotem Text angezeigt wird. Zuweisen aussagekräftiger Namen zu Prop. *Name* rows, klicken Sie auf die Zeile, und geben Sie dann einen Namen wie *Price* ein, um beispielsweise den Zeilennamen Prop. Price zu erstellen. Sie können dann mithilfe von Prop. Price. Label auf die Zelle Label verweisen. 
  
Der eingegebene Zeilenname muss innerhalb des Abschnitts eindeutig sein.
  

