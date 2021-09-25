---
title: Übersicht über Transportanbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a51547e6-8f0e-45f4-a341-3cfa735112c2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f189ed78d7feb1714fa2a04bf29403c6d33773af
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609320"
---
# <a name="transport-provider-overview"></a>Übersicht über Transportanbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Transportanbieter ist eine Dynamic Link Library (DLL), die als Vermittler zwischen dem MAPI-Subsystem und einem oder mehreren zugrunde liegenden Messagingsystemen fungiert. Ein Messagingsystem ist ein bestimmter Mechanismus, mit dem Nachrichten gesendet und empfangen werden. Einige Beispiele für Messagingsysteme sind:
  
- Ein freigegebenes Netzwerkdateisystem, in das der Transportanbieter Nachrichten direkt schreibt.
    
- Eine TCP/IP-Netzwerkschnittstelle, die der Transportanbieter zum Herstellen einer Verbindung mit einem Messagingserver verwendet.
    
- Ein Onlinedienst, mit dem Benutzer eine Verbindung herstellen.
    
- Ein hostbasiertes Messaging- oder Office-Automatisierungssystem.
    
- Eine Reihe von Remoteprozeduraufrufen an einen Messagingserver.
    
- Alles, was verwendet werden kann, um Daten von einem Computer auf einen anderen zu übertragen.
    
Eine Transportanbieter-DLL muss der von MAPI angegebenen Schnittstelle entsprechen. Als Entwickler von Transportanbietern implementieren Sie diese Schnittstelle hinsichtlich der Funktionen, die im Messagingsystem vorhanden sind.
  

