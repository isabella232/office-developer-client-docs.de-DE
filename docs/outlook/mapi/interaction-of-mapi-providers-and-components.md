---
title: Interaktion von MAPI-Anbietern und-Komponenten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c0e010b-0432-4ef7-a243-3a4b46f0a19d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b88eafcc1ca6be98c5c1e9418072a5cb35f43345
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332172"
---
# <a name="interaction-of-mapi-providers-and-components"></a>Interaktion von MAPI-Anbietern und-Komponenten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI-Dienstanbieter jeglicher Art müssen bestimmte Richtlinien befolgen, um mit anderen MAPI-Komponenten zu arbeiten. Jeder Dienstanbieter muss:
  
- Verwenden Sie die richtigen Anbieter-und Anmeldeobjekte für die Initialisierung.
    
- Zurückgeben einer Dispatch-Tabelle mit Anbieter Einstiegspunkten nach der Initialisierung an das Messagingsystem.
    
- Registrieren Sie eine MAPI-Statustabellen Zeile für jede Ressource, die im Besitz des Anbieters ist, und rufen Sie die [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) -Methode zu geeigneten Zeiten auf. 
    
- Verwenden Sie die [IMAPISupport:: NewUID](imapisupport-newuid.md) -Methode, um gültige eindeutige IDs zu erhalten. 
    
- Unterstützen der allgemeinen MAPI-Schnittstellen für Objekte, die zurückgegeben werden.
    
- Verwenden Sie die MAPI-Speicher Zuweisungsfunktionen, um an Clientanwendungen zurückgegebener Speicher zuzuweisen und den von anderen Teilen des MAPI-Subsystems reservierten Arbeitsspeicher freizugeben.
    
- Führen Sie bei Bedarf einen Profil Abschnitt aus, um die Anmeldeinformationen für das zugrunde liegende Messagingsystem zu speichern.
    
- Verwenden Sie die [IMAPISupport:: RegisterPreprocessor](imapisupport-registerpreprocessor.md) -Methode, um alle Funktionen der Nachrichten Vorverarbeitung zu registrieren. 
    
- Schließen Sie die richtigen Headerdateien (einschließlich mapispi. h) ein, die allgemeine Konstanten, Strukturen, Schnittstellen und Rückgabewerte definieren.
    
- BeFolgen Sie die Adressformat Konventionen für allgemeine Adresstypen.
    

