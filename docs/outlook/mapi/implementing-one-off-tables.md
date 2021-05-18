---
title: Implementieren One-Off Tabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57933d44-d47a-4e7f-ba95-b49b4934d0a5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c29feae84d81874988997409fd229b042a701640
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421641"
---
# <a name="implementing-one-off-tables"></a>Implementieren One-Off Tabellen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ihr Anbieter kann eine oder mehrere einmal enthaltene Tabellen implementieren. Eine einmal aufgeführte Tabelle ist eine Zusammenfassungsliste von einmal erstellten Vorlagen, die zum Erstellen von Empfängern verwendet werden, entweder direkt in einem Container oder in der Empfängerliste einer ausgehenden Nachricht. Eine einmalvorlage ist ein Formular, das Benutzer für die Eingabe von Daten verwenden, die für einen bestimmten Adresstyp relevant sind. Wenn der Benutzer mit der Vorlage fertig ist, erstellt ihr Anbieter den neuen Empfänger und fügt ihn der Nachricht hinzu. In der Regel verarbeitet jede Vorlage einen einzelnen Adresstyp. Es ist jedoch möglich, dass eine Vorlage mehrere Typen oder mehrere Vorlagen mit demselben Typ verarbeiten kann. 
  
Ihr Anbieter muss die **OpenEntry-Methode** für jede Vorlage unterstützen, die er in der einmal aufgeführten Tabelle enthält. Die Implementierung von **OpenEntry** sollte eine Anzeigetabelle für die Vorlage abrufen. MAPI verwendet die Anzeigetabelle, um die Vorlage für den Benutzer sichtbar zu machen. 
  
Obwohl die meisten Zeilen in einmal erstellten Tabellen Vorlagen darstellen, können einige der Zeilen zum Kategorisieren oder Gruppieren von Vorlagen verwendet werden. Ob eine Zeile in einer #A0 eine Vorlage darstellt, wird durch den Wert der Spalte **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) angegeben. Zeilen, die Vorlagen darstellen, PR_SELECTABLE auf TRUE festgelegt; Zeilen, die keine Vorlagen darstellen, haben sie auf FALSE festgelegt.
  
MAPI definiert drei Arten von einmal erstellten Tabellen:
  
- Eine einzelne Tabelle, die die Vorlagen widerspiegelt, die von einem einzelnen Container unterstützt werden
    
- Eine Einmaltabelle, die alle von Ihrem Anbieter unterstützten Vorlagen widerspiegelt 
    
- Eine einmalige Tabelle, die alle Vorlagen widerspiegelt, die alle Anbieter im Profil unterstützen, sowie einige, die VON MAPI unterstützt werden
    
Die ersten beiden Typen werden von Anbietern implementiert, die die Erstellungsempfänger unterstützen, entweder in einer Nachricht oder in einem Container. Ihr Anbieter kann denselben Satz oder einen anderen Satz von Vorlagen in seine einmal festgelegten Tabellen enthalten. Der Hauptunterschied zwischen den beiden Typen ist, dass Ihre Anbietertabelle Vorlagen zum Erstellen von Empfängern enthalten soll, die für ausgehende Nachrichten verwendet werden können, und ihre Containertabelle muss Vorlagen zum Erstellen von Empfängern enthalten, die Ihrem Container hinzugefügt werden sollen. Ein Container unterstützt möglicherweise nur einen eingeschränkten Satz von Vorlagen, aber die einzelne Tabelle des Anbieters sollte alle vom Anbieter unterstützten Vorlagen enthalten.
  
Der dritte Typ der einmal aufgeführten Tabelle wird von MAPI implementiert. Anbieter erhalten Zugriff darauf, indem [sie IMAPISupport::GetOneOffTable aufrufen.](imapisupport-getoneofftable.md) Die #A0 ist die Vereinigung aller Anbietertabellen. Sie enthält jede Vorlage, die von jedem Anbieter im Profil unterstützt wird. Es enthält auch Vorlagen, die von MAPI unterstützt werden. Ihr Anbieter kann diese Tabelle an stelle der für einen Container angeforderten Tabelle verwenden. Die Vorlagen in dieser Tabelle können jedoch auch zum Erstellen von Empfängern für ausgehende Nachrichten verwendet werden.
  

