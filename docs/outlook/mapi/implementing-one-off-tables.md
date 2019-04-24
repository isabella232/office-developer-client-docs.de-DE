---
title: Implementieren von einmaligen Tabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57933d44-d47a-4e7f-ba95-b49b4934d0a5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c29feae84d81874988997409fd229b042a701640
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310129"
---
# <a name="implementing-one-off-tables"></a>Implementieren von einmaligen Tabellen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ihr Anbieter kann eine oder mehrere einmalige Tabellen implementieren. Eine einmalige Tabelle ist eine Zusammenfassungsliste mit einmaligen Vorlagen, die zum Erstellen von Empfängern verwendet werden, entweder direkt in einem Container oder in der Empfängerliste einer ausgehenden Nachricht. Eine einmalige Vorlage ist ein Formular, mit dem Benutzerdaten eingeben können, die für einen bestimmten Adresstyp relevant sind. Wenn der Benutzer die Arbeit mit der Vorlage abgeschlossen hat, erstellt der Anbieter den neuen Empfänger und fügt ihn der Nachricht hinzu. In der Regel verarbeitet jede Vorlage einen einzelnen Adresstyp. Es ist jedoch möglich, dass eine Vorlage mehrere Typen oder mehrere Vorlagen für den gleichen Typ verarbeitet. 
  
Ihr Anbieter muss die **OpenEntry** -Methode für jede Vorlage unterstützen, die in der einmaligen Tabelle enthalten ist. Die Implementierung von **OpenEntry** sollte eine Anzeigetabelle für die Vorlage abrufen. MAPI verwendet die Anzeigetabelle, um die Vorlage für den Benutzer sichtbar zu machen. 
  
Obwohl die meisten Zeilen in einmaligen Tabellenvorlagen darstellen, können einige der Zeilen zum Kategorisieren oder Gruppieren von Vorlagen verwendet werden. Ob eine Zeile in einer einmaligen Tabelle eine Vorlage darstellt, wird durch den Wert der **PR_SELECTABLE** ([pidtagselectable (](pidtagselectable-canonical-property.md))-Spalte angezeigt. Zeilen, die Vorlagen darstellen, haben die PR_SELECTABLE-Spalte auf TRUE festgelegt; Zeilen, die keine Vorlagen darstellen, sind auf FALSE festgelegt.
  
MAPI definiert drei Arten von einmaligen Tabellen:
  
- Eine einmalige Tabelle, die die von einem einzelnen Container unterstützten Vorlagen widerspiegelt
    
- Eine einmalige Tabelle, die alle vom Anbieter unterstützten Vorlagen widerspiegelt 
    
- Eine einmalige Tabelle, die alle Vorlagen widerspiegelt, die alle Anbieter im Profil unterstützen, sowie einige, die von MAPI unterstützt werden
    
Die ersten beiden Typen werden von Anbietern implementiert, die die Erstellungs Empfänger unterstützen, entweder in einer Nachricht oder in einem Container. Ihr Anbieter kann den gleichen Satz oder einen anderen Satz von Vorlagen in seine einmaligen Tabellen aufnehmen. Der Hauptunterschied zwischen den beiden Typen besteht darin, dass die Anbieter Tabelle Vorlagen zum Erstellen von Empfängern enthält, die für ausgehende Nachrichten verwendet werden können, und Ihre Container Tabelle sollte Vorlagen zum Erstellen von Empfängern sein, die Ihrem Container hinzugefügt werden sollen. Ein Container kann nur eine eingeschränkte Gruppe von Vorlagen unterstützen, aber die einmalige Tabelle des Anbieters sollte alle vom Anbieter unterstützten Vorlagen aufweisen.
  
Der dritte Typ der einmaligen Tabelle wird von MAPI implementiert; Anbieter erhalten Zugriff darauf durch Aufrufen von [IMAPISupport:: GetOneOffTable](imapisupport-getoneofftable.md). Die MAPI-einmalige Tabelle ist die Vereinigung aller Anbieter Tabellen; Sie enthält jede Vorlage, die von jedem Anbieter im Profil unterstützt wird. Sie enthält auch Vorlagen, die von MAPI unterstützt werden. Ihr Anbieter kann diese Tabelle anstelle der für einen Container angeforderten Tabelle verwenden. Die Vorlagen in dieser Tabelle können jedoch auch zum Erstellen von Empfängern für ausgehende Nachrichten verwendet werden.
  

