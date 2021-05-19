---
title: Übersicht über den Transportanbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a51547e6-8f0e-45f4-a341-3cfa735112c2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 53bdba624ba759debba25bae78fb45b0f9d5247e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433157"
---
# <a name="transport-provider-overview"></a>Übersicht über den Transportanbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Transportanbieter ist eine DLL (Dynamic Link Library), die als Vermittler zwischen dem MAPI-Subsystem und einem oder mehreren zugrunde liegenden Messagingsystemen fungiert. Ein Messagingsystem ist ein bestimmter Mechanismus, mit dem Nachrichten gesendet und empfangen werden. Beispiele für Messagingsysteme sind:
  
- Ein freigegebenes Netzwerkdateisystem, in das der Transportanbieter Nachrichten direkt schreibt.
    
- Eine TCP/IP-Netzwerkschnittstelle, die der Transportanbieter zum Herstellen einer Verbindung mit einem Messagingserver verwendet.
    
- Ein Onlinedienst, mit dem Benutzer eine Verbindung herstellen.
    
- Ein hostbasiertes Messaging- oder Office-Automatisierungssystem.
    
- Eine Reihe von Remoteprozeduraufrufen an einen Messagingserver.
    
- Alles, was zum Übertragen von Daten von einem Computer auf einen anderen verwendet werden kann.
    
Eine Transportanbieter-DLL muss der von MAPI angegebenen Schnittstelle entsprechen. Als Entwickler eines Transportanbieters implementieren Sie diese Schnittstelle im Hinblick auf die Funktionalität, die im Messagingsystem vorhanden ist.
  

