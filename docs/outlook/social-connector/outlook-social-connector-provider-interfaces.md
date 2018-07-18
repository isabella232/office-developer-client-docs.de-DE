---
title: Outlook Connector für soziale Netzwerke Provider-Schnittstellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f92b2c7-9f47-4c84-874b-fec1a2a5b555
description: Outlook Social Connector (OSC) ist ein Office-Feature von Office-Clientanwendungen gemeinsam genutzt werden, die eine Verbindung mit sozialen herstellt und damit Benutzer die Personen in ihren Netzwerken mit ihr in Verbindung bleiben können, ohne Office Business-Netzwerke.
ms.openlocfilehash: bc393f32e563bbbef70538ea00cd92cf7f96729c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796079"
---
# <a name="outlook-social-connector-provider-interfaces"></a>Outlook Connector für soziale Netzwerke Provider-Schnittstellen

Outlook Social Connector (OSC) ist ein Office-Feature von Office-Clientanwendungen gemeinsam genutzt werden, die eine Verbindung mit sozialen herstellt und damit Benutzer die Personen in ihren Netzwerken mit ihr in Verbindung bleiben können, ohne Office Business-Netzwerke. 
  
Ein OSC-Provider ist eine DLL-Datei, mit der die OSC für soziale Netzwerke Zugriff auf Daten in eine Möglichkeit, die unabhängig von den einzelnen sozialen Netzwerk-APIs kann, Component Object Model (COM). Die folgende Tabelle enthält die Schnittstellen in die Erweiterbarkeit des OSC-Providers. Ein OSC-Anbieter muss vier der fünf Schnittstellen zur Kommunikation mit dem OSC implementieren: [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md)und [ISocialSession](isocialsessioniunknown.md). Wenn der OSC-Anbieter Synchronisieren von Aktivitäten auf Abruf unterstützt oder Hybrid Synchronisierung von Freunden, Anmeldeinformationen Zwischenspeichern von und Anmelden bei Verwendung zwischengespeichert Anmeldeinformationen oder die Möglichkeit, führen eine Person, sollte der Anbieter [ISocialSession2 implementieren. ](isocialsession2iunknown.md)rascher.
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[ISocialPerson](isocialpersoniunknown.md) <br/> |Stellt eine Person im sozialen Netzwerk.  <br/> |
|[ISocialProfile](isocialprofileisocialperson.md) <br/> |Stellt die angemeldeten Benutzers.  <br/> |
|[ISocialProvider](isocialprovideriunknown.md) <br/> |Stellt eine Instanz eines OSC-Anbieters.  <br/> |
|[ISocialSession](isocialsessioniunknown.md) <br/> |Stellt eine Verbindung mit einer Website für soziale Netzwerke.  <br/> |
|[ISocialSession2](isocialsession2iunknown.md) <br/> |Synchronisieren von Aktivitäten, Hinzufügen von Freunden unterstützt, zwischengespeicherten bei Bedarf oder Hybriden Synchronisierung von Freunde oder Anmelden bei der für soziale Netzwerke mithilfe von Anmeldeinformationen.  <br/> |
   

