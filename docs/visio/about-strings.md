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
description: 'Formeln können Zeichenfolgen enthalten. Wenn Sie ausgegebene Zeichenfolgen (z. B. einen Wert in einer Eingabeaufforderungszelle), Werte für Shape-Datenelemente oder ein Textfeld formatieren möchten, geben Sie eine Formatierungsangabe an. Ausgegebene Werte können als Zahl-Einheit-Paar, Zeichenfolge, Datum-Uhrzeit, Zeitdauer oder Währung formatiert werden. Beispiel: das Format picture0 #/10 uuformats das Nummern Einheiten paar 10,9 cm AS10 9/10 Zentimeter.'
ms.openlocfilehash: aa95e11db387913edbb40292f7da6a0f4b8a5cf7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345066"
---
# <a name="about-strings"></a><span data-ttu-id="6ca8b-106">Informationen zu Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="6ca8b-106">About Strings</span></span>

<span data-ttu-id="6ca8b-p102">Formeln können Zeichenfolgen enthalten. Wenn Sie ausgegebene Zeichenfolgen (z. B. einen Wert in einer Eingabeaufforderungszelle), Werte für Shape-Datenelemente oder ein Textfeld formatieren möchten, geben Sie eine Formatierungsangabe an. Ausgegebene Werte können als Zahl-Einheit-Paar, Zeichenfolge, Datum-Uhrzeit, Zeitdauer oder Währung formatiert werden. Mit der Formatierungsangabe "0 #/10 uu" wird beispielsweise das Zahl-Einheit-Paar 10,9 cm als "10 9/10 Zentimeter" formatiert.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-p102">Formulas can contain strings. To format string output, such as in a prompt cell, a shape data item value, or a text field, you specify a format picture. Output can be formatted as a number-unit pair, string, date-time, duration, or currency. For example, the format picture "0 #/10 uu" formats the number-unit pair 10.9cm as "10 9/10 centimeters".</span></span>
  
<span data-ttu-id="6ca8b-111">Sie können Format Bilder in der Zelle **Format** des Abschnitts Shape-Daten und als Argument für die **Format** -oder **FORMATEX** -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-111">You can use format pictures in the **Format** cell of the Shape Data section and as an argument to the **FORMAT** or **FORMATEX** function.</span></span> <span data-ttu-id="6ca8b-112">Wenn Sie ein Textfeld einfügen, werden Bilder in der Liste der Formate im Dialogfeld **Feld** (Registerkarte**Einfügen** ) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-112">When you insert a text field, format pictures appear in the list of formats in the **Field** dialog box (**Insert** tab).</span></span> 
  
## <a name="using-functions-to-format-strings"></a><span data-ttu-id="6ca8b-113">Verwenden von Funktionen zum Formatieren von Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="6ca8b-113">Using functions to format strings</span></span>

<span data-ttu-id="6ca8b-114">In einer beliebigen Formel, die in eine Zeichenfolge aufgelöst wird, einschließlich benutzerdefinierter Textfeldformeln, können Sie die **Format** -oder die **FORMATEX** -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-114">In any formula that resolves to a string, including custom text field formulas, you can use the **FORMAT** or **FORMATEX** function.</span></span> <span data-ttu-id="6ca8b-115">Die Funktion FORMAT gibt eine Zeichenfolge der formatierten Ausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-115">The FORMAT function returns a string of the formatted output.</span></span> <span data-ttu-id="6ca8b-116">Die **FORMATEX** -Funktion konvertiert nicht typisierte Eingabe in die Einheiten, die Sie für das formatierte Ergebnis auswählen.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-116">The **FORMATEX** function converts untyped input to the units you choose for the formatted result.</span></span> 
  
## <a name="displaying-formatted-shape-data"></a><span data-ttu-id="6ca8b-117">Anzeigen formatierter Shape-Daten</span><span class="sxs-lookup"><span data-stu-id="6ca8b-117">Displaying formatted shape data</span></span>

<span data-ttu-id="6ca8b-118">Sie können den angezeigten Wert eines Shape-Datenelements formatieren, indem Sie eine Formatierungsangabe in die Zelle Format eingeben.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-118">You can format the displayed value of a shape data item by entering a format picture in the Format cell.</span></span>
  
<span data-ttu-id="6ca8b-p105">Ein Projektplan-Shape kann beispielsweise ein Shape-Datenelement enthalten, das die Kosten eines Prozesses misst. Standardmäßig ist der Wert eines Shape-Datenelements eine Zeichenfolge. Um die Zeichenfolge "1200" zu formatieren, können Sie "$###,###.00" in die Zelle "Format" eingeben, damit dem Benutzer eine Währung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-p105">For example, a project timeline shape can have a shape data item that measures the cost of a process. By default, a shape data item value is a string. To format the string "1200", you can enter "$###,###.00" in the Format cell so that the user sees a currency.</span></span>
  
<span data-ttu-id="6ca8b-122">Microsoft Visio bestimmt das anzuzeigende Währungssymbol und das 1000er-Trennzeichen anhand der Einstellungen auf der Registerkarte **Währung** im Dialogfeld \*\*Format anpassen \*\* unter **Region und Sprache** in der Systemsteuerung.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-122">Microsoft Visio uses the settings on the **Currency** tab in the **Customize Format** dialog box in the **Region and Language** item in Control Panel to determine the currency symbol and thousands separator to display.</span></span> <span data-ttu-id="6ca8b-123">(Klicken Sie in der **System**Steuerung auf **Region und Sprache**, und klicken Sie dann auf **Weitere Einstellungen**.)</span><span class="sxs-lookup"><span data-stu-id="6ca8b-123">(In **Control Panel**, click **Region and Language**, and then click **Additional Settings**.)</span></span>
  
<span data-ttu-id="6ca8b-124">Verwenden Sie die CY-Funktion, wenn Sie eine Zeichenfolge in einen Währungswert konvertieren möchten, damit Sie Berechnungen mit diesem Wert durchführen können.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-124">To convert a string to a currency value so that you can perform calculations with the value, use the CY function.</span></span>
  
## <a name="using-functions-to-manipulate-text-strings"></a><span data-ttu-id="6ca8b-125">Verwenden von Funktionen zum Bearbeiten von Textzeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="6ca8b-125">Using functions to manipulate text strings</span></span>

<span data-ttu-id="6ca8b-p107">Mit Funktionen können Sie Textzeichenfolgen bearbeiten, z. B. bestimmte Zeichen in einer Zeichenfolge suchen oder ersetzen. Sie können auch Informationen zur Position eines Zeichens in einer Zeichenfolge abrufen, oder Anfangs- und Endzeichen einer Zeichenfolge bestimmen.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-p107">You can use functions to manipulate text strings, for example, to locate or replace certain characters in a text string. You can also get information about the position of a character in a string, or identify beginning and ending characters in a text string.</span></span> 
  

