---
title: Interaktion von MAPI-Anbietern und Komponenten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c0e010b-0432-4ef7-a243-3a4b46f0a19d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c81da7673d6c0c59de6992bc46362069daf71b42
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592626"
---
# <a name="interaction-of-mapi-providers-and-components"></a>Interaktion von MAPI-Anbietern und Komponenten

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
MAPI-Dienstanbieter jeglicher Art müssen bestimmte Richtlinien andere MAPI-Komponenten entwickelt. Jeder Dienstanbieter muss:
  
- Verwenden Sie die entsprechenden Objekte Anbieter und die Anmeldeinformationen für die Initialisierung.
    
- Zurückgeben einer Tabelle Versendung der Anbieter Einstiegspunkte an die messaging-System bei der Initialisierung.
    
- Registrieren Sie eine MAPI-Status Tabellenzeile für jede Ressource, die vom Anbieter gehören, und rufen Sie die [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) -Methode zum entsprechenden Zeitpunkt. 
    
- Verwenden Sie die [IMAPISupport::NewUID](imapisupport-newuid.md) -Methode, um gültige eindeutige Bezeichner (UIDs) abzurufen. 
    
- Unterstützt die gemeinsamen MAPI-Schnittstellen für Objekte zurück.
    
- Verwenden Sie die MAPI-Speicherverwaltungsfunktionen Speicher Clientanwendungen zurückgegeben und durch andere Teile des MAPI-Subsystems Arbeitsspeicher freizugeben.
    
- Verwalten eines Abschnitts Profil; bei Bedarf zum Speichern von Anmeldeinformationen für den zugrunde liegenden messaging-System.
    
- Verwenden Sie die [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) -Methode, um eine beliebige Nachricht vorverarbeitung Funktionen registrieren. 
    
- Einfügen der richtigen Headerdateien (einschließlich mapispi.h), die definieren, häufige Konstanten, Strukturen, Schnittstellen und Rückgabewerte.
    
- Führen Sie die Adresse Format Konventionen für allgemeine Adresstypen.
    

