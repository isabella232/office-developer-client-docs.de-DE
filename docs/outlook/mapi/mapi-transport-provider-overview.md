---
title: Übersicht über MAPI-Transportanbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b193e819-749e-4642-8afc-dbc47b17b617
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 42c41bd3f09a62c940a9b8b598a7adcd7dfccf08
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556098"
---
# <a name="mapi-transport-provider-overview"></a>Übersicht über MAPI-Transportanbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Transportanbieter behandeln die Nachrichtenübermittlung und den Empfang und implementieren bei Bedarf Sicherheit. Sie übernehmen auch alle erforderlichen Vor- und Nachbearbeitungsaufgaben. Es gibt in der Regel einen Transportanbieter für jedes aktive Messagingsystem.
  
Clientanwendungen kommunizieren mit dem Transportanbieter über einen Nachrichtenspeicheranbieter. 
  
Transportanbieter registrieren sich bei der MAPI, um einen oder mehrere bestimmte Arten von Empfängereinträgen zu verarbeiten. Wenn eine Nachricht gesendet werden kann, muss mapi bestimmen, welcher Transportanbieter die Übertragung verarbeiten soll. Je nach Empfängertyp kann die MAPI sogar mehrere Transportanbieter aufrufen. Wenn nur ein nicht verfügbarer Transportanbieter den Empfänger verarbeiten kann, wird die Nachrichtenübertragung verschoben, bis eine Verbindung mit diesem Anbieter wiederhergestellt werden kann.
  
Einige Messagingsysteme sind sichere Systeme. Alle potenziellen Benutzer müssen eine Reihe gültiger Anmeldeinformationen eingeben, bevor der Zugriff zulässig ist. MapI verhindert unbefugten Zugriff auf solche sicheren Messaging-Systeme, indem der Transportanbieter anmeldeinformationen bei der Anmeldung überprüft. 
  

