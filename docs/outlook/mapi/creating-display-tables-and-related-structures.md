---
title: Erstellen von Anzeigetabellen und verwandten Strukturen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a8548040-13ed-4a9f-a7ca-de610f94d7df
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 350272324c3827f4630f0cf35e3ade0ff213ac4d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335613"
---
# <a name="creating-display-tables-and-related-structures"></a>Erstellen von Anzeigetabellen und verwandten Strukturen
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das Erstellen einer Anzeigetabelle ähnelt dem Schreiben eines Programms mit einer Skriptsprache. Sie können eine Anzeigetabelle entweder durch Aufrufen von [BuildDisplayTable](builddisplaytable.md) oder durch Schreiben von benutzerdefiniertem Code erstellen, um die Zeilen und Spalten der Tabelle aufzufüllen. Im Allgemeinen sollten Sie die **BuildDisplayTable** -Technik verwenden, da Sie einfacher ist. 
  
Bevor Sie **BuildDisplayTable** aufrufen können, um MAPI aufzufordern, eine Anzeigetabelle zu erstellen, gibt es eine Hierarchie von Strukturen, die Sie erstellen müssen. Die Struktur der obersten Ebene, [DTPAGE](dtpage.md), beschreibt eine einzelne Eigenschaftenseite im Registerkartenformat. In jeder **DTPAGE** -Struktur handelt es sich um eine [DTCTL](dtctl.md) -Struktur, die ein einzelnes Steuerelement beschreibt, beispielsweise ein Bearbeitungsfeld oder eine Optionsschaltfläche. Jede **DTCTL** -Struktur enthält eine Struktur, die spezifisch für den Typ des Steuerelements ist. Wenn beispielsweise die **DTCTL** -Struktur ein Bearbeitungsfeld-Steuerelement beschreibt, enthält es eine **DTBLEDIT** -Struktur. Die **DTCTL** -Struktur für ein Optionsfeld enthält eine **DTBLRADIOBUTTON** -Struktur. 
  
Diese Strukturen beziehen sich direkt auf **BuildDisplayTable**; Sie haben keine Bedeutung außerhalb des Kontexts dieser Funktion. Wenn Sie **BuildDisplayTable**aufrufen, übergeben Sie eine oder mehrere **DTPAGE** -Strukturen als Eingabeparameter. Die **DTPAGE** -Strukturen enthalten ein Array von **DTCTL** -Strukturen und die Anzahl der **DTCTL** -Strukturen im Array. Es gibt eine Struktur für jedes Steuerelement, das im Dialogfeld angezeigt werden soll. **DTPAGE** -Strukturen besitzen auch eine Zeichenfolge, die den Namen einer entsprechenden Hilfedatei und Dialogfeldressource darstellt. 
  
Jede **DTCTL** -Struktur in einer **DTPAGE** -Struktur enthält die folgenden Daten, die zum Festlegen der Eigenschaften für das Steuerelement verwendet werden: 
  
- Der Steuerelementtyp für das Festlegen von **PR_CONTROL_TYPE** ([pidtagcontroltype (](pidtagcontroltype-canonical-property.md)).
    
- Steuerelemente für das Festlegen von **PR_CONTROL_FLAGS** ([pidtagcontrolflags (](pidtagcontrolflags-canonical-property.md)).
    
- Benachrichtigungsdaten zum Festlegen von **PR_CONTROL_ID** ([pidtagcontrolid (](pidtagcontrolid-canonical-property.md)).
    
- Die Steuerelementstruktur zum Festlegen von **PR_CONTROL_STRUCTURE** ([pidtagcontrolstructure (](pidtagcontrolstructure-canonical-property.md)).
    
**DTCTL** -Strukturen enthalten auch einen Ressourcenbezeichner und für Bearbeitungs-und Kombinationsfeld-Steuerelemente einen Zeichenfilter. 
  
Die Steuerelementstruktur Member einer **DTCTL** -Struktur beschreibt die Daten, die für den Typ des Steuerelements eindeutig ist. MAPI definiert eine andere Struktur für jeden Steuerelementtyp. Beispielsweise werden die Daten eines Edit-Steuerelements durch eine **DTBLEDIT** -Struktur dargestellt. die Daten eines Listenfelds werden durch eine **DTBLLBX** -Struktur dargestellt. 
  
Die Beziehung zwischen den drei Arten von Anzeige Tabellenstrukturen ist in der folgenden Abbildung dargestellt. Das von dieser Anzeigetabelle beschriebene Dialogfeld verfügt über zwei Steuerelemente: eine Bezeichnung und ein Bearbeitungssteuerelement. Die **DTBLLBX** -Struktur besitzt einen Bezeichnungs Offset-Member, ebenso wie mehrere der Steuerelementstrukturen, die beschreiben, wo die Zeichenfolge für die Bezeichnung beginnt. BeZeichnungs Zeichen Zeichenfolgen werden normalerweise unmittelbar nach der Struktur in den Arbeitsspeicher verschoben. 
  
**Anzeigetabellenstrukturen**
  
![Anzeigen von Tabellenstrukturen] (media/dtstruct.gif "Anzeigen von Tabellenstrukturen")
  
## <a name="see-also"></a>Siehe auch

- [Implementierung von Anzeigetabellen](display-table-implementation.md)

