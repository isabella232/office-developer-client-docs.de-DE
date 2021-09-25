---
title: Zeile "Shape Data" (Abschnitt "Shape Data")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251344
ms.localizationpriority: medium
ms.assetid: f3a83496-fccc-9d6a-02b9-60ebaf4911ea
description: Enthält die Informationen für ein einzelnes Shape-Datenelement, das einem Shape zugeordnet ist. Ein Shape enthält eine Shape-Datenzeile für jedes Shape-Datenelement. Shape-Datenzeilen werden Prop.name benannt und enthalten die folgenden Zellen. Weitere Informationen finden Sie in den spezifischen Zellthemen.
ms.openlocfilehash: d488c181912f924a49ed7a42bf0e25a66fa16b7d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559570"
---
# <a name="shape-data-row-shape-data-section"></a>Zeile "Shape Data" (Abschnitt "Shape Data")

Enthält die Informationen für ein einzelnes Shape-Datenelement, das einem Shape zugeordnet ist. Ein Shape enthält eine Shape-Datenzeile für jedes Shape-Datenelement. Shape-Datenzeilen werden Prop.name benannt und enthalten die folgenden Zellen. Weitere Informationen finden Sie in den spezifischen Zellthemen.
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[Label](label-cell-shape-data-section.md) <br/> |Gibt die Beschriftung an, die dem Benutzer im Dialogfeld bzw. Fenster **Shape-Daten** angezeigt wird.  <br/> |
|[Prompt](prompt-cell-shape-data-section.md) <br/> |Gibt den Text der Beschreibung oder Anweisung an, der Benutzern im Dialogfeld bzw. Fenster **Shape-Daten** oder beim Auswählen des Elements angezeigt wird.  <br/> |
|[Typ](type-cell-shape-data-section.md) <br/> |Gibt einen Datentyp für den Wert des Shape-Datenelements an: Zeichenfolge (0), eine feste Liste (1), eine Zahl (2), einen booleschen Wert (3), eine variable Liste (4), einen Datums- oder Uhrzeitwert (5), eine Zeitdauer (6) oder eine Währung (7).  <br/> |
|[Format](format-cell-shape-data-section.md) <br/> |Gibt die Formatierung eines Shape-Datenelements an.  <br/> |
|[Wert](value-cell-shape-data-section.md) <br/> |Enthält den Wert eines Elements, der im Dialogfeld oder Fenster **Shape-Daten** eingegeben wurde.  <br/> |
|[Sortkey](sortkey-cell-shape-data-section.md) <br/> |Gibt einen Schlüssel an, nach dem die Elemente im Dialogfeld oder Fenster **Shape-Daten** aufgelistet werden.  <br/> |
|[Unsichtbar](invisible-cell-shape-data-section.md) <br/> |Gibt an, ob das Shape-Datenelement im Dialogfeld oder Fenster Shape-Daten angezeigt wird.  TRUE = nicht sichtbar; FALSE = sichtbar.  <br/> |
|[Fragen](ask-cell-shape-data-section.md) <br/> |Bestimmt, ob der Benutzer beim Erstellen einer Instanz oder beim Duplizieren oder Kopieren eines Shapes aufgefordert wird, Informationen zu Shape-Daten einzugeben.  <br/> |
|[Langid](langid-cell-shape-data-section.md) <br/> |Gibt die Sprache an, in der der Wert des Shape-Datenelements angezeigt wird.  <br/> |
|[Calendar](calendar-cell-miscellaneous-section.md) <br/> |Gibt den Typ des Kalenders an, der verwendet wird, wenn ein Shape-Datenelement vom Typ Datum ist.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

 Sie können so viele Eigenschaften hinzufügen.  *Benennen*  Sie Zeilen nach Bedarf, weisen Sie den Zeilen aussagekräftige Namen zu, und legen Sie Zellwerte fest. Um einem vorhandenen Shape-Datenabschnitt ein Shape-Datenelement hinzuzufügen, klicken Sie mit der rechten Maustaste auf eine Zeile, und klicken Sie im Kontextmenü auf **"Zeile einfügen".** 
  
Sie können auf diese Zellen anhand ihres Zeilennamens verweisen, der in einem ShapeSheet-Fenster in rotem Text angezeigt wird. Klicken Sie auf die  Zeile, und geben Sie dann einen Namen wie *z. B. Price* ein, um den Zeilennamen Prop.Price zu erstellen, um zeilenweise aussagekräftige Namen zuzuweisen. Anschließend können Sie mithilfe von Prop.Price.Label auf die Zelle "Label" verweisen. 
  
Der eingegebene Zeilenname muss innerhalb des Abschnitts eindeutig sein.
  

