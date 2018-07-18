---
title: Informationen zu Zeichenfolgen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251826
localization_priority: Normal
ms.assetid: e1174d8f-70cb-4595-7906-889da15367db
description: 'Formeln können Zeichenfolgen enthalten. Zum Formatieren von Zeichenfolgenausgabe wie in einer Zelle "Prompt", ein Shape-Datenwert Element oder ein Textfeld, geben Sie eine Formatierungsangabe. Ausgabe formatiert werden kann, als Zahl-Einheit-Paar, Zeichenfolge, Datum-Uhrzeit, Dauer oder Währung. Beispielsweise Kopplung das Format picture0 #/ 10 Uuformats die Zahl-Einheit 10,9 cm as10 9/10 Zentimeter.'
ms.openlocfilehash: 1fd003ecd5c824042e97a40fa8374aeead254ddc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796358"
---
# <a name="about-strings"></a>Informationen zu Zeichenfolgen

Formeln können Zeichenfolgen enthalten. Wenn Sie ausgegebene Zeichenfolgen (z. B. einen Wert in einer Eingabeaufforderungszelle), Werte für Shape-Datenelemente oder ein Textfeld formatieren möchten, geben Sie eine Formatierungsangabe an. Ausgegebene Werte können als Zahl-Einheit-Paar, Zeichenfolge, Datum-Uhrzeit, Zeitdauer oder Währung formatiert werden. Mit der Formatierungsangabe "0 #/10 uu" wird beispielsweise das Zahl-Einheit-Paar 10,9 cm als "10 9/10 Zentimeter" formatiert.
  
Sie können Formatierungsangaben in der Zelle **Format** des Shape-Datenabschnitt und als Argument an die Funktion **FORMAT** oder **FORMATEX** verwenden. Wenn Sie ein Textfeld einfügen, werden Formatierungsangaben in der Liste der Formate im Dialogfeld **Feld** (Registerkarte**Einfügen** ) angezeigt. 
  
## <a name="using-functions-to-format-strings"></a>Verwenden von Funktionen zum Formatieren von Zeichenfolgen

In jeder Formel, die in eine Zeichenfolge mit einer benutzerdefinierten Feld Textformeln, aufgelöst wird, können Sie die Funktion **FORMAT** oder **FORMATEX** verwenden. Die FORMAT-Funktion gibt eine Zeichenfolge der formatierten Ausgabe zurück. **FORMATEX** -Funktion konvertiert nicht typisierte Informationen in die Einheiten, die Sie für das formatierte Ergebnis auswählen. 
  
## <a name="displaying-formatted-shape-data"></a>Anzeigen formatierter Shape-Daten

Sie können den angezeigten Wert eines Shape-Datenelements formatieren, indem Sie eine Formatierungsangabe in die Zelle Format eingeben.
  
Ein Projektplan-Shape kann beispielsweise ein Shape-Datenelement enthalten, das die Kosten eines Prozesses misst. Standardmäßig ist der Wert eines Shape-Datenelements eine Zeichenfolge. Um die Zeichenfolge "1200" zu formatieren, können Sie "$###,###.00" in die Zelle "Format" eingeben, damit dem Benutzer eine Währung angezeigt wird.
  
Microsoft Visio verwendet die Einstellungen auf der Registerkarte **Währung** im Dialogfeld **Format anpassen** im Element **Region und Sprache** in der Systemsteuerung bestimmt das Währungssymbol und Tausende Trennzeichen angezeigt. (Klicken Sie in **Der Systemsteuerung**klicken Sie auf **Region und Sprache**, und klicken Sie dann auf **Zusätzliche Einstellungen**.)
  
Verwenden Sie die CY-Funktion, wenn Sie eine Zeichenfolge in einen Währungswert konvertieren möchten, damit Sie Berechnungen mit diesem Wert durchführen können.
  
## <a name="using-functions-to-manipulate-text-strings"></a>Verwenden von Funktionen zum Bearbeiten von Textzeichenfolgen

Mit Funktionen können Sie Textzeichenfolgen bearbeiten, z. B. bestimmte Zeichen in einer Zeichenfolge suchen oder ersetzen. Sie können auch Informationen zur Position eines Zeichens in einer Zeichenfolge abrufen, oder Anfangs- und Endzeichen einer Zeichenfolge bestimmen. 
  

