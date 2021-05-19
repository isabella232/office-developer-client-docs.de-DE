---
title: Interaktion von MAPI-Anbietern und -Komponenten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c0e010b-0432-4ef7-a243-3a4b46f0a19d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b88eafcc1ca6be98c5c1e9418072a5cb35f43345
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434662"
---
# <a name="interaction-of-mapi-providers-and-components"></a>Interaktion von MAPI-Anbietern und -Komponenten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI-Dienstanbieter jeder Art müssen bestimmte Richtlinien befolgen, um mit anderen MAPI-Komponenten zu arbeiten. Jeder Dienstanbieter muss:
  
- Verwenden Sie die richtigen Anbieter- und Anmeldeobjekte für die Initialisierung.
    
- Gibt bei der Initialisierung eine Verteilertabelle mit Anbietereintragspunkten an das Messagingsystem zurück.
    
- Registrieren Sie eine ZEILE der MAPI-Statustabelle für jede Ressource im Besitz des Anbieters, und rufen Sie die [IMAPISupport::ModifyStatusRow-Methode](imapisupport-modifystatusrow.md) zu entsprechenden Zeiten auf. 
    
- Verwenden Sie [die IMAPISupport::NewUID-Methode,](imapisupport-newuid.md) um gültige eindeutige Bezeichner (UIDs) zu erhalten. 
    
- Unterstützt die gängigen MAPI-Schnittstellen für zurückgegebene Objekte.
    
- Verwenden Sie die MAPI-Speicherzuweisungsfunktionen, um Clientanwendungen zurückgegebenen Arbeitsspeicher zuzuordnen und von anderen Teilen des MAPI-Subsystems zugewiesenen Arbeitsspeicher frei zu geben.
    
- Verwalten Sie bei Bedarf einen Profilabschnitt, um Anmeldeinformationen im zugrunde liegenden Messagingsystem zu speichern.
    
- Verwenden Sie [die IMAPISupport::RegisterPreprocessor-Methode,](imapisupport-registerpreprocessor.md) um alle Nachrichtenvorverarbeitungsfunktionen zu registrieren. 
    
- Fügen Sie die richtigen Headerdateien (einschließlich mapispi.h) ein, die allgemeine Konstanten, Strukturen, Schnittstellen und Rückgabewerte definieren.
    
- Befolgen Sie die Adressformatkonventionen für allgemeine Adresstypen.
    

