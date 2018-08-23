---
title: Transportanbieterübersicht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a51547e6-8f0e-45f4-a341-3cfa735112c2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: dbc56b7334d3966696641a84f23a64ce3802e3e4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595272"
---
# <a name="transport-provider-overview"></a>Transportanbieterübersicht

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ein Transportanbieter ist eine Dynamic Link Library (DLL) fungiert als Mittler zwischen MAPI-Subsystems und einen oder mehrere zugrunde liegenden messaging-Systeme. Messaging-System ist einen bestimmten Mechanismus, mit dem Nachrichten gesendet und empfangen werden. Beispiele von Messagingsystemen sind:
  
- Eine Netzwerkfreigabe Dateisystem, die der Adressbuchhierarchie Nachrichten direkt schreibt.
    
- Eine TCP/IP-Netzwerkschnittstelle, die mit der Adressbuchhierarchie messaging-Server herstellt.
    
- Ein Onlinedienst, die Benutzer eine Verbindung herstellen.
    
- Ein Host-basierte messaging oder Office Automatisierungssystem.
    
- Eine Reihe von Remoteprozeduraufrufe an einen Messagingserver.
    
- Alle Werte, die zum Übertragen von Daten von einem Computer zu einem anderen verwendet werden kann.
    
Ein Transportdienstes DLL muss die MAPI angegebene Schnittstelle entsprechen. Als Entwickler Anbieter Transport implementieren Sie diese Schnittstelle im Hinblick auf die Funktionalität im Nachrichtensystem vorhanden.
  

