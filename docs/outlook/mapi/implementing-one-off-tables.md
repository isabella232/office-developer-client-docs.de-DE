---
title: Implementieren von One-Off Tabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 57933d44-d47a-4e7f-ba95-b49b4934d0a5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 194180659b121a101eb20a3614093c7eaf57bc87
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610433"
---
# <a name="implementing-one-off-tables"></a>Implementieren von One-Off Tabellen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ihr Anbieter kann eine oder mehrere einmalige Tabellen implementieren. Eine einmalige Tabelle ist eine Zusammenfassungsliste mit einmaligen Vorlagen, die zum Erstellen von Empfängern verwendet werden, entweder direkt in einem Container oder in der Empfängerliste einer ausgehenden Nachricht. Eine einmalige Vorlage ist ein Formular, das Benutzer für die Eingabe von Daten verwenden, die für einen bestimmten Adresstyp relevant sind. Wenn der Benutzer die Arbeit mit der Vorlage abgeschlossen hat, erstellt ihr Anbieter den neuen Empfänger und fügt ihn der Nachricht hinzu. In der Regel verarbeitet jede Vorlage einen einzelnen Adresstyp. Es ist jedoch möglich, dass eine Vorlage mehrere Typen behandelt oder dass mehrere Vorlagen denselben Typ verarbeiten. 
  
Ihr Anbieter muss die **OpenEntry-Methode** für jede Vorlage unterstützen, die sie in die einmalige Tabelle einschließt. Die Implementierung von **OpenEntry** sollte eine Anzeigetabelle für die Vorlage abrufen. MAPI verwendet die Anzeigetabelle, um die Vorlage für den Benutzer sichtbar zu machen. 
  
Obwohl die meisten Zeilen in einmaligen Tabellen Vorlagen darstellen, können einige der Zeilen zum Kategorisieren oder Gruppieren von Vorlagen verwendet werden. Ob eine Zeile in einer einmaligen Tabelle eine Vorlage darstellt, wird durch den Wert der **spalte PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) angegeben. Für Zeilen, die Vorlagen darstellen, ist die PR_SELECTABLE Spalte auf TRUE festgelegt. Für Zeilen, die keine Vorlagen darstellen, ist sie auf FALSE festgelegt.
  
MAPI definiert drei Typen von einmaligen Tabellen:
  
- Eine einmalige Tabelle, die die Vorlagen wiedergibt, die ein einzelner Container unterstützt
    
- Eine einmalige Tabelle, die alle Vorlagen wiedergibt, die Ihr Anbieter unterstützt 
    
- Eine einmalige Tabelle, die alle Vorlagen wiedergibt, die alle Anbieter im Profil unterstützen, sowie einige, die mapi unterstützt
    
Die ersten beiden Typen werden von Anbietern implementiert, die die Erstellungsempfänger unterstützen, entweder in einer Nachricht oder in einem Container. Ihr Anbieter kann denselben Satz oder einen anderen Satz von Vorlagen in seine einmaligen Tabellen einschließen. Der Hauptunterschied zwischen den beiden Typen besteht darin, dass die Anbietertabelle Vorlagen zum Erstellen von Empfängern enthalten sollte, die für ausgehende Nachrichten verwendet werden können, und dass ihre Containertabelle Vorlagen zum Erstellen von Empfängern enthalten sollte, die Ihrem Container hinzugefügt werden sollen. Ein Container unterstützt möglicherweise nur einen eingeschränkten Satz von Vorlagen, aber die einmalige Tabelle des Anbieters sollte jede Vorlage enthalten, die der Anbieter unterstützt.
  
Der dritte Typ einer einmaligen Tabelle wird von mapi implementiert. Anbieter erhalten Zugriff darauf, indem [sie IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md)aufrufen. Die EINMALIGE MAPI-Tabelle ist die Vereinigung aller Anbietertabellen. Sie enthält jede Vorlage, die von jedem Anbieter im Profil unterstützt wird. Es enthält auch Vorlagen, die von MAPI unterstützt werden. Ihr Anbieter kann diese Tabelle anstelle der für einen Container angeforderten Tabelle verwenden. Die Vorlagen in dieser Tabelle können jedoch auch zum Erstellen von Empfängern für ausgehende Nachrichten verwendet werden.
  

