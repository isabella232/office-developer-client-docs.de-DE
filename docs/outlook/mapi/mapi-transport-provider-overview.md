---
title: Übersicht über den MAPI-Transport Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b193e819-749e-4642-8afc-dbc47b17b617
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 20b03f7c52ec86d1fb554bf69c53947c3dda4f36
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357344"
---
# <a name="mapi-transport-provider-overview"></a>Übersicht über den MAPI-Transport Anbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Transport Anbieter verarbeiten Nachrichtenübertragung und-Empfang und implementieren ggf. Sicherheit. Sie kümmern sich auch um alle erforderlichen Vorverarbeitungs-und Nachbearbeitungsaufgaben. Es gibt in der Regel einen Transportanbieter für jedes aktive Messagingsystem.
  
Client Anwendungen kommunizieren mit dem Transportanbieter über einen Nachrichtenspeicher Anbieter. 
  
Transport Anbieter registrieren sich bei MAPI, um einen oder mehrere bestimmte Typen von Empfänger Einträgen zu behandeln. Wenn eine Nachricht gesendet werden kann, muss MAPI bestimmen, welcher Transportanbieter die Übertragung verarbeiten soll. Je nach Empfängertyp kann MAPI sogar mehrere Transportanbieter aufrufen. Wenn ein nicht verfügbarer Transportanbieter der einzige ist, der den Empfänger verarbeiten kann, wird die Nachrichtenübertragung verschoben, bis eine Verbindung mit diesem Anbieter hergestellt werden kann.
  
Einige Messagingsysteme sind sichere Systeme; alle potenziellen Benutzer müssen eine Reihe gültiger Anmeldeinformationen eingeben, bevor der Zugriff zulässig ist. MAPI verhindert den unbefugten Zugriff auf solche Secure Messaging-Systeme, indem der Transportanbieter Anmeldeinformationen zur Anmeldezeit überprüfen kann. 
  

