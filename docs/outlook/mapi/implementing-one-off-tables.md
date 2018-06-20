---
title: Implementieren der einmalige Tabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57933d44-d47a-4e7f-ba95-b49b4934d0a5
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b72b8658270a8e007123df3ead01168208b8d1b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792561"
---
# <a name="implementing-one-off-tables"></a>Implementieren der einmalige Tabellen

**Betrifft**: Outlook 
  
Vom Dienstanbieter kann eine oder mehrere einmalige Tabellen implementieren. Eine einmalige Tabelle wird eine Übersichtsliste einmal-Vorlagen zum Erstellen von Empfängern, direkt in einen Container oder in der Empfängerliste von ausgehenden Nachrichten verwendet. Eine einmalige Vorlage ist ein Formular Benutzer beschäftigen zum Eingeben von Daten für einen bestimmten Typ der Adresse von Bedeutung. Wenn der Benutzer ist abgeschlossen arbeiten mit der Vorlage, der Anbieter den neuen Empfänger erstellt und fügt es der Nachricht hinzu. Jede Vorlage wird in der Regel einen einzelnes Adresstyp behandelt. Es ist jedoch möglich, für eine Vorlage, die mehrere Typen oder für mehrere Vorlagen zum Behandeln von des gleichen Typs. 
  
Der Anbieter muss die **OpenEntry** -Methode für jede Vorlage unterstützen, die sie in der einmaligen Tabelle enthält. Die Implementierung der **OpenEntry** abrufen soll eine zeigt die Tabelle für die Vorlage. MAPI wird die Anzeige-Tabelle verwendet, um die Vorlage für den Benutzer sichtbar zu machen. 
  
Obwohl die meisten der Zeilen in einmaligen Tabellen Vorlagen darstellen, können einige der Zeilen kategorisieren oder zu gruppieren, Vorlagen verwendet werden. Unabhängig davon, ob eine Zeile in einer einmaligen Tabelle darstellt, wird eine Vorlage durch den Wert der Spalte **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) angezeigt. Zeilen, die Vorlagen darstellen haben die PR_SELECTABLE-Spalte auf TRUE festgelegt. Zeilen, die keine Vorlagen darstellen festgelegt auf FALSE festgelegt.
  
MAPI werden drei Arten von einmaligen Tabellen definiert:
  
- Eine einmalige Tabelle, die die Vorlagen widerspiegelt, die ein einzelner Container unterstützt
    
- Eine einmalige Tabelle, die alle Vorlagen widerspiegelt, die vom Anbieter unterstützt 
    
- Eine einmalige Tabelle, die alle Vorlagen widerspiegelt, dass alle Anbieter im Profil plus einige unterstützen, dass MAPI unterstützt
    
Die ersten beiden Typen werden von Anbietern implementiert, die auf eine Nachricht oder in einen Container der Erstellung Empfänger zu unterstützen. Vom Dienstanbieter kann der gleiche Satz oder eine andere Menge von Vorlagen in ihren einmaligen Tabellen enthalten. Der Hauptunterschied zwischen den beiden Typen ist, dass die Container-Tabelle enthalten Vorlagen zum Erstellen von Empfängern, die Container hinzugefügt werden soll und die Provider-Tabelle sollte enthalten Vorlagen zum Erstellen von Empfängern an, die für ausgehende Nachrichten verwendet werden können. Ein Container kann nur einen eingeschränkten Satz mit Vorlagen unterstützen, jedoch einen einmaligen Tabelle der Dienstanbieter jede Vorlage der Anbieter unterstützt.
  
Der dritte Typ der einmaligen Tabelle ist MAPI implementiert. Anbieter erlangen Zugriff darauf durch Aufrufen von [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md). Die einmalige MAPI-Tabelle ist die Vereinigung von allen Tabellen Anbieter. Sie enthält jede Vorlage, die von jedem Provider im Profil unterstützt wird. Darüber hinaus enthält Vorlagen, die von MAPI unterstützt. Der Anbieter kann in dieser Tabelle an der Stelle für einen Container angeforderte Tabelle verwenden. Die Vorlagen in dieser Tabelle können jedoch auch verwendet werden, für das Erstellen von Empfängern für ausgehende Nachrichten.
  

