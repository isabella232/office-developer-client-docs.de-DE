---
title: Informationen zu Zeichenfolgen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251826
ms.localizationpriority: medium
ms.assetid: e1174d8f-70cb-4595-7906-889da15367db
description: 'Formeln können Zeichenfolgen enthalten. Wenn Sie ausgegebene Zeichenfolgen (z. B. einen Wert in einer Eingabeaufforderungszelle), Werte für Shape-Datenelemente oder ein Textfeld formatieren möchten, geben Sie eine Formatierungsangabe an. Ausgegebene Werte können als Zahl-Einheit-Paar, Zeichenfolge, Datum-Uhrzeit, Zeitdauer oder Währung formatiert werden. Das Formatbild0 #/10 uuformatiert beispielsweise das Zahleneinheitspaar 10,9 cm als 10 9/10 Zentimeter.'
ms.openlocfilehash: edc9cf9f2eb6a6b32d88944e0443f449084b79bc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598878"
---
# <a name="about-strings"></a>Informationen zu Zeichenfolgen

Formeln können Zeichenfolgen enthalten. Wenn Sie ausgegebene Zeichenfolgen (z. B. einen Wert in einer Eingabeaufforderungszelle), Werte für Shape-Datenelemente oder ein Textfeld formatieren möchten, geben Sie eine Formatierungsangabe an. Ausgegebene Werte können als Zahl-Einheit-Paar, Zeichenfolge, Datum-Uhrzeit, Zeitdauer oder Währung formatiert werden. Mit der Formatierungsangabe "0 #/10 uu" wird beispielsweise das Zahl-Einheit-Paar 10,9 cm als "10 9/10 Zentimeter" formatiert.
  
Sie können Formatbilder in der Zelle **Format** des Abschnitts Shape Data und als Argument für die Funktion **FORMAT** oder **FORMATEX** verwenden. Wenn Sie ein Textfeld einfügen, werden Formatbilder in der Liste der Formate im Dialogfeld **Feld** (Registerkarte **"Einfügen")** angezeigt. 
  
## <a name="using-functions-to-format-strings"></a>Verwenden von Funktionen zum Formatieren von Zeichenfolgen

In jeder Formel, die in eine Zeichenfolge aufgelöst wird, einschließlich benutzerdefinierter Textfeldformeln, können Sie die **FORMAT-** oder **FORMATEX-Funktion** verwenden. Die Funktion FORMAT gibt eine Zeichenfolge der formatierten Ausgabe zurück. Die **FORMATEX-Funktion** konvertiert untypierte Eingaben in die Einheiten, die Sie für das formatierte Ergebnis auswählen. 
  
## <a name="displaying-formatted-shape-data"></a>Anzeigen formatierter Shape-Daten

Sie können den angezeigten Wert eines Shape-Datenelements formatieren, indem Sie eine Formatierungsangabe in die Zelle Format eingeben.
  
Ein Projektplan-Shape kann beispielsweise ein Shape-Datenelement enthalten, das die Kosten eines Prozesses misst. Standardmäßig ist der Wert eines Shape-Datenelements eine Zeichenfolge. Um die Zeichenfolge "1200" zu formatieren, können Sie "$###,###.00" in die Zelle "Format" eingeben, damit dem Benutzer eine Währung angezeigt wird.
  
Microsoft Visio bestimmt das anzuzeigende Währungssymbol und das 1000er-Trennzeichen anhand der Einstellungen auf der Registerkarte **Währung** im Dialogfeld **Format anpassen** unter **Region und Sprache** in der Systemsteuerung. (Klicken Sie in **der Systemsteuerung** auf **"Region und Sprache" und** dann auf **"Zusätzliche Einstellungen.)**
  
Verwenden Sie die CY-Funktion, wenn Sie eine Zeichenfolge in einen Währungswert konvertieren möchten, damit Sie Berechnungen mit diesem Wert durchführen können.
  
## <a name="using-functions-to-manipulate-text-strings"></a>Verwenden von Funktionen zum Bearbeiten von Textzeichenfolgen

Mit Funktionen können Sie Textzeichenfolgen bearbeiten, z. B. bestimmte Zeichen in einer Zeichenfolge suchen oder ersetzen. Sie können auch Informationen zur Position eines Zeichens in einer Zeichenfolge abrufen, oder Anfangs- und Endzeichen einer Zeichenfolge bestimmen. 
  

