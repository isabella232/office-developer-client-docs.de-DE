---
title: Übersicht über den MAPI-Transportanbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b193e819-749e-4642-8afc-dbc47b17b617
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 20b03f7c52ec86d1fb554bf69c53947c3dda4f36
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404575"
---
# <a name="mapi-transport-provider-overview"></a>Übersicht über den MAPI-Transportanbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Transportanbieter verarbeiten nachrichtenübermittlung und -empfang und implementieren bei Bedarf Sicherheit. Außerdem übernehmen sie alle erforderlichen Vor- und Nachverarbeitungsaufgaben. Es gibt in der Regel einen Transportanbieter für jedes aktive Messagingsystem.
  
Clientanwendungen kommunizieren mit dem Transportanbieter über einen Nachrichtenspeicheranbieter. 
  
Transportanbieter registrieren sich bei MAPI, um einen oder mehrere bestimmte Typen von Empfängereinträgen zu verarbeiten. Wenn eine Nachricht gesendet werden kann, muss MAPI bestimmen, welcher Transportanbieter die Übertragung verarbeiten soll. Je nach Empfängertyp kann MAPI sogar mehrere Transportanbieter aufrufen. Wenn ein nicht verfügbarer Transportanbieter der einzige ist, der den Empfänger verarbeiten kann, wird die Nachrichtenübertragung verschoben, bis eine Verbindung mit diesem Anbieter wiederhergestellt werden kann.
  
Einige Messagingsysteme sind sichere Systeme. Alle potenziellen Benutzer müssen einen Satz gültiger Anmeldeinformationen eingeben, bevor der Zugriff zulässig ist. MAPI verhindert nicht autorisierten Zugriff auf solche sicheren Messagingsysteme, indem der Transportanbieter anmeldeinformationen zum Zeitpunkt der Anmeldung überprüft. 
  

