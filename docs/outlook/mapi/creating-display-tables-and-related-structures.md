---
title: Erstellen von Tabellen anzeigen und verwandte Strukturen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a8548040-13ed-4a9f-a7ca-de610f94d7df
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 177fe21537e921a4b94a34ad531847701b16c344
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791481"
---
# <a name="creating-display-tables-and-related-structures"></a>Erstellen von Tabellen anzeigen und verwandte Strukturen
  
**Betrifft**: Outlook 
  
Erstellen einer Tabelle anzeigen ähnelt dem Schreiben eines Programms mit einer Skriptsprache. Sie können eine Tabelle anzeigen, entweder durch Aufrufen von [BuildDisplayTable](builddisplaytable.md) oder Schreiben von benutzerdefiniertem Code zum Auffüllen der Zeilen und Spalten der Tabelle auf erstellen. Im Allgemeinen verwenden Sie das Verfahren **BuildDisplayTable** , da es einfacher ist. 
  
Vor dem Aufruf der **BuildDisplayTable** um MAPI zum Erstellen einer Tabelle anzeigen auffordern ist eine Hierarchie von Strukturen, die Sie erstellen müssen. Die Hauptstruktur [DTPAGE](dtpage.md), wird eine einzelne Eigenschaftenseiten beschrieben. In jeder **DTPAGE** ist Struktur einer [DTCTL](dtctl.md) -Struktur, die ein einzelnes Steuerelement, wie ein Bearbeitungsfeld oder ein Optionsfeld beschreibt. Jede **DTCTL** -Datenstruktur enthält eine Struktur, die speziell für den Typ des Steuerelements ist. Beispielsweise wird ein **DTCTL** Struktur ein Bearbeitungsfeld-Steuerelement beschrieben, eine Struktur **DTBLEDIT** enthalten. Die **DTCTL** -Struktur für ein Optionsfeld enthält eine **DTBLRADIOBUTTON** -Struktur. 
  
Diese Strukturen beziehen sich direkt auf **BuildDisplayTable**; Sie haben keine Bedeutung außerhalb des Kontexts von dieser Funktion. Wenn Sie **BuildDisplayTable**aufrufen, übergeben Sie einen oder mehrere **DTPAGE** Strukturen als Eingabeparameter. Die Strukturen **DTPAGE** enthalten ein Array von **DTCTL** Strukturen und die Anzahl der **DTCTL** Strukturen im Array. Es ist eine Struktur für jedes Steuerelement im Dialogfeld angezeigt. **DTPAGE** Strukturen haben auch eine Zeichenfolge, die den Namen des eine entsprechende Hilfe-Datei und das Dialogfeld Feld Ressource darstellt. 
  
Jede **DTCTL** Struktur in einer **DTPAGE** Struktur enthält die folgenden Daten, die zum Festlegen von Eigenschaften für das Steuerelement verwendet werden: 
  
- Der Typ für **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) festlegen.
    
- Steuerelement-Flags für **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) festlegen.
    
- Benachrichtigungsdaten zum Festlegen von **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)).
    
- Die Steuerelement-Struktur für **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) festlegen.
    
**DTCTL** Strukturen enthalten außerdem einen Resource Identifier und für bearbeiten und Kombinationsfeld-Steuerelemente, ein Zeichen Filter. 
  
Das Steuerelement Struktur Mitglied einer **DTCTL** Struktur beschreibt die Daten, die für den Typ des Steuerelements eindeutig ist. MAPI definiert, eine andere Struktur für jeden Steuerelementtyp. Beispielsweise werden durch eine **DTBLEDIT** Struktur die Daten von einem Bearbeitungssteuerelement dargestellt. die Daten eines Listenfelds werden durch eine **DTBLLBX** Struktur dargestellt. 
  
In der folgenden Abbildung wird die Beziehung zwischen den drei Typen von Tabellenstrukturen anzeigen angezeigt. Das Dialogfeld durch diese zeigt die Tabelle beschriebenen hat zwei Steuerelemente: eine Bezeichnung und ein Edit-Steuerelement. Die Struktur **DTBLLBX** hat ein Label-Offset-Element, wie werden einige der Steuerelement-Strukturen, die beschreibt die Zeichenfolge für die Bezeichnung an, deren beginnt. Label-Zeichenfolgen werden in der Regel im Arbeitsspeicher, die unmittelbar auf der Struktur platziert. 
  
**Tabellenstrukturen anzeigen**
  
![Tabellenstrukturen anzeigen] (media/dtstruct.gif "Tabellenstrukturen anzeigen")
  
## <a name="see-also"></a>Siehe auch

- [Implementierung der Anzeige-Tabelle](display-table-implementation.md)

