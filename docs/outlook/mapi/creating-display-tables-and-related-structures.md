---
title: Erstellen von Anzeigetabellen und verwandten Strukturen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a8548040-13ed-4a9f-a7ca-de610f94d7df
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 853a8db028d0e902f785cc3198e7994404af3ef1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592676"
---
# <a name="creating-display-tables-and-related-structures"></a>Erstellen von Anzeigetabellen und verwandten Strukturen
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das Erstellen einer Anzeigetabelle ähnelt dem Schreiben eines Programms mit einer Skriptsprache. Sie können eine Anzeigetabelle entweder erstellen, indem [Sie BuildDisplayTable](builddisplaytable.md) aufrufen oder benutzerdefinierten Code zum Auffüllen der Zeilen und Spalten der Tabelle schreiben. Im Allgemeinen sollten Sie die **BuildDisplayTable-Technik** verwenden, da sie einfacher ist. 
  
Bevor Sie **BuildDisplayTable** aufrufen können, um die MAPI zum Erstellen einer Anzeigetabelle aufzufordern, gibt es eine Hierarchie von Strukturen, die Sie erstellen müssen. Die Struktur der obersten Ebene, [DTPAGE,](dtpage.md)beschreibt eine einzelne Registerkarteneigenschaftsseite. In jeder **DTPAGE-Struktur** ist eine [DTCTL-Struktur](dtctl.md) vorhanden, die ein einzelnes Steuerelement beschreibt, z. B. ein Bearbeitungsfeld oder eine Optionsschaltfläche. Jede **DTCTL-Struktur** enthält eine Struktur, die für den Typ des Steuerelements spezifisch ist. Wenn die **DTCTL-Struktur** beispielsweise ein Bearbeitungsfeld-Steuerelement beschreibt, enthält sie eine **DTBLEDIT-Struktur.** Die **DTCTL-Struktur** für eine Optionsschaltfläche enthält eine **DTBLRADIOBUTTON-Struktur.** 
  
Diese Strukturen beziehen sich direkt auf **BuildDisplayTable**; sie haben außerhalb des Kontexts dieser Funktion keine Bedeutung. Wenn Sie **BuildDisplayTable** aufrufen, übergeben Sie eine oder mehrere **DTPAGE-Strukturen** als Eingabeparameter. Die **DTPAGE-Strukturen** enthalten ein Array von **DTCTL-Strukturen** und eine Anzahl der **DTCTL-Strukturen** im Array. Es gibt eine Struktur für jedes Steuerelement, das im Dialogfeld angezeigt werden soll. **DTPAGE-Strukturen** verfügen auch über eine Zeichenfolge, die den Namen einer entsprechenden Hilfedatei und Dialogfeldressource darstellt. 
  
Jede **DTCTL-Struktur** in einer **DTPAGE-Struktur** enthält die folgenden Daten, die zum Festlegen von Eigenschaften für das Steuerelement verwendet werden: 
  
- Der Steuerelementtyp zum Festlegen **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)).
    
- Steuerelementflags zum Festlegen **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)).
    
- Benachrichtigungsdaten zum Festlegen **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)).
    
- Die Steuerelementstruktur zum Festlegen **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)).
    
**DTCTL-Strukturen** enthalten auch einen Ressourcenbezeichner und für Bearbeitungs- und Kombinationsfeld-Steuerelemente einen Zeichenfilter. 
  
Das Steuerelementstrukturelement einer **DTCTL-Struktur** beschreibt die Daten, die für den Steuerelementtyp eindeutig sind. MAPI definiert eine andere Struktur für jeden Steuerelementtyp. Beispielsweise werden die Daten eines Bearbeitungssteuerelements durch eine **DTBLEDIT-Struktur** dargestellt. Die Daten eines Listenfelds werden durch eine **DTBLLBX-Struktur** dargestellt. 
  
Die Beziehung zwischen den drei Arten von Anzeigetabellenstrukturen wird in der folgenden Abbildung dargestellt. Das von dieser Anzeigetabelle beschriebene Dialogfeld verfügt über zwei Steuerelemente: eine Beschriftung und ein Bearbeitungssteuerelement. Die **DTBLLBX-Struktur** verfügt über einen Beschriftungsversatzmember, wie einige der Steuerelementstrukturen, die beschreiben, wo die Zeichenzeichenfolge für die Beschriftung beginnt. Zeichenfolgen für Beschriftungszeichen werden in der Regel unmittelbar nach der Struktur im Speicher platziert. 
  
**Anzeigetabellenstrukturen**
  
![Anzeigetabellenstrukturen](media/dtstruct.gif "Anzeigetabellenstrukturen")
  
## <a name="see-also"></a>Siehe auch

- [Implementierung von Anzeigetabellen](display-table-implementation.md)

