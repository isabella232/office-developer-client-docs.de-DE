---
title: Interaktion von MAPI-Anbietern und -Komponenten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 2c0e010b-0432-4ef7-a243-3a4b46f0a19d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d9cec36654328accadce77a3f67da58542774aa6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564084"
---
# <a name="interaction-of-mapi-providers-and-components"></a>Interaktion von MAPI-Anbietern und -Komponenten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI-Dienstanbieter jeder Art müssen bestimmte Richtlinien befolgen, um mit anderen MAPI-Komponenten zu arbeiten. Jeder Dienstanbieter muss:
  
- Verwenden Sie die richtigen Anbieter- und Anmeldeobjekte für die Initialisierung.
    
- Zurückgeben einer Verteilertabelle mit Anbieter-Einstiegspunkten an das Messagingsystem bei der Initialisierung.
    
- Registrieren Sie eine MAPI-Statustabellenzeile für jede Ressource im Besitz des Anbieters, und rufen Sie die [IMAPISupport::ModifyStatusRow-Methode](imapisupport-modifystatusrow.md) zu entsprechenden Zeiten auf. 
    
- Verwenden Sie die [IMAPISupport::NewUID-Methode,](imapisupport-newuid.md) um gültige eindeutige Bezeichner (UIDs) abzurufen. 
    
- Unterstützen Sie die allgemeinen MAPI-Schnittstellen für zurückgegebene Objekte.
    
- Verwenden Sie die MAPI-Speicherzuweisungsfunktionen zum Zuordnen von Arbeitsspeicher, der clientanwendungen zurückgegeben wird, und zum Freigeben von Arbeitsspeicher, der von anderen Teilen des MAPI-Subsystems zugewiesen wurde.
    
- Verwalten Sie ggf. einen Profilabschnitt, um Anmeldeinformationen für das zugrunde liegende Messagingsystem zu speichern.
    
- Verwenden Sie die [IMAPISupport::RegisterPreprocessor-Methode,](imapisupport-registerpreprocessor.md) um alle Funktionen für die Vorverarbeitung von Nachrichten zu registrieren. 
    
- Schließen Sie die richtigen Headerdateien (einschließlich mapispi.h) ein, die allgemeine Konstanten, Strukturen, Schnittstellen und Rückgabewerte definieren.
    
- Befolgen Sie die Konventionen für das Adressformat für allgemeine Adresstypen.
    

