---
title: Übersicht über die Transport-Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a51547e6-8f0e-45f4-a341-3cfa735112c2
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 22b9da0cfe70cf499cc6f3a699eabe4aaee25b0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795766"
---
# <a name="transport-provider-overview"></a>Übersicht über die Transport-Anbieter

  
  
**Betrifft**: Outlook 
  
Ein Transportanbieter ist eine Dynamic Link Library (DLL) fungiert als Mittler zwischen MAPI-Subsystems und einen oder mehrere zugrunde liegenden messaging-Systeme. Messaging-System ist einen bestimmten Mechanismus, mit dem Nachrichten gesendet und empfangen werden. Beispiele von Messagingsystemen sind:
  
- Eine Netzwerkfreigabe Dateisystem, die der Adressbuchhierarchie Nachrichten direkt schreibt.
    
- Eine TCP/IP-Netzwerkschnittstelle, die mit der Adressbuchhierarchie messaging-Server herstellt.
    
- Ein Onlinedienst, die Benutzer eine Verbindung herstellen.
    
- Ein Host-basierte messaging oder Office Automatisierungssystem.
    
- Eine Reihe von Remoteprozeduraufrufe an einen Messagingserver.
    
- Alle Werte, die zum Übertragen von Daten von einem Computer zu einem anderen verwendet werden kann.
    
Ein Transportdienstes DLL muss die MAPI angegebene Schnittstelle entsprechen. Als Entwickler Anbieter Transport implementieren Sie diese Schnittstelle im Hinblick auf die Funktionalität im Nachrichtensystem vorhanden.
  

