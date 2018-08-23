---
title: Übersicht über die MAPI-Transport-Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b193e819-749e-4642-8afc-dbc47b17b617
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 244dae4d3413587b7a37e93328998b153fb8ece3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585332"
---
# <a name="mapi-transport-provider-overview"></a>Übersicht über die MAPI-Transport-Anbieter

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Transportanbieter die Nachrichtenübermittlung und Empfang verarbeiten und Implementieren von Sicherheit, falls dies erforderlich. Sie auch alle erforderlichen vorverarbeitung und übernehmen postprocessing Aufgaben. In der Regel eine Adressbuchhierarchie für jede active messaging-System ist vorhanden.
  
Clientanwendungen kommunizieren mit der Adressbuchhierarchie über einen Anbieter für die Nachricht anmelden. 
  
Transportanbieter registrieren MAPI, um eine oder mehrere bestimmte Arten von empfangenen Einträge zu behandeln. Wenn eine Nachricht gesendet werden kann, muss MAPI ermitteln, welche Adressbuchhierarchie die Übertragung behandelt werden sollen. MAPI kann für mehrere Adressbuchhierarchie je nach Typ des Empfängers sogar hinzuziehen. Ist eine nicht verfügbare Adressbuchhierarchie die einzige, die den Empfänger verarbeitet werden können, wird der Nachrichtenübermittlung verschoben werden, bis eine Verbindung mit diesem Anbieter wiederhergestellt werden kann.
  
Einige Messagingsysteme sind sichere Systeme. Alle potenzielle Benutzern sind erforderlich, um einen Satz von gültige Anmeldeinformationen eingeben, vor dem Zugriff zulässig ist. MAPI verhindert nicht autorisierten Zugriff auf solchen secure messaging-Systemen, dass der Adressbuchhierarchie Anmeldeinformationen bei der Anmeldung zu überprüfen. 
  

