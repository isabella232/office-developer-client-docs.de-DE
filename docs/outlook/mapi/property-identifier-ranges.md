---
title: Eigenschaftenbezeichnerbereiche
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c01e95bb-be25-490d-880b-60674f890258
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a9e0509cfa0ab3bdeb6b7d285c6635b2a00f9c51
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629599"
---
# <a name="property-identifier-ranges"></a>Eigenschaftenbezeichnerbereiche

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In der folgenden Tabelle werden die verschiedenen Bereiche für Eigenschaftsbezeichner zusammengefasst, wobei der Besitzer für die Eigenschaften in jedem Bereich beschrieben wird.
  
|**Bezeichnerbereich**|**Beschreibung**|
|:-----|:-----|
|0000  <br/> |Reserviert von MAPI für den speziellen Wert **PR_NULL**.  <br/> |
|0001 - 0BFF  <br/> |Von MAPI definierte Nachrichtenumschlageigenschaften.  <br/> |
|0C00 - 0DFF  <br/> |Von MAPI definierte Empfängereigenschaften.  <br/> |
|0E00 - 0FFF  <br/> |Von MAPI definierte eigenschaften für nicht datenübertragungsfähige Nachrichten.  <br/> |
|1000 - 2FFF  <br/> |Von MAPI definierte Nachrichteninhaltseigenschaften.  <br/> |
|3000 - 3FFF  <br/> |Eigenschaften für andere Objekte als Nachrichten und Empfänger, die von MAPI definiert werden.  <br/> |
|4000 - 57FF  <br/> |Von Transportanbietern definierte Nachrichtenumschlageigenschaften.  <br/> |
|5800 - 5FFF  <br/> |Empfängereigenschaften, die von Transport- und Adressbuchanbietern definiert sind.  <br/> |
|6000 - 65FF  <br/> |Von Clients definierte eigenschaften für nicht datenübertragungsfähige Nachrichten.  <br/> |
|6600 - 67FF  <br/> |Von einem Dienstanbieter definierte nicht übertragbare Eigenschaften. Diese Eigenschaften können für Benutzer sichtbar oder unsichtbar sein.  <br/> |
|6800 - 7BFF  <br/> |Nachrichteninhaltseigenschaften für benutzerdefinierte Nachrichtenklassen, die von Erstellern dieser Klassen definiert werden.  <br/> |
|7C00 - 7FFF  <br/> |Nicht übertragbare Eigenschaften für benutzerdefinierte Nachrichtenklassen, die von Erstellern dieser Klassen definiert werden.  <br/> |
|8000 – FFFE  <br/> |Eigenschaften, die von Clients und gelegentlich Dienstanbietern definiert werden, die durch den Namen über die Methoden [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) und [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) identifiziert werden.  <br/> |
|FFFF  <br/> |Reserviert von MAPI für den speziellen Fehlerwert PROP_ID_INVALID.  <br/> |
   
Der Bereich zwischen 3000 und 3FFF ist für Eigenschaften reserviert, die sich nicht auf Nachrichten oder Empfänger beziehen. MAPI teilt diesen Bereich nach Objekttypen in Unterbereiche auf. Die folgende Tabelle zeigt diese weitere Aufschlüsselung. 
  
|**Bezeichnerbereich**|**Typ der Eigenschaft**|
|:-----|:-----|
|3000 - 33FF  <br/> |Allgemeine Eigenschaften, die in mehreren Objekten angezeigt werden, z. **B. PR_DISPLAY_NAME** und **PR_ENTRYID**.  <br/> |
|3400 - 35FF  <br/> |Nachrichtenspeichereigenschaften  <br/> |
|3600 - 36FF  <br/> |Ordner- und Adressbuchcontainereigenschaften  <br/> |
|3700 - 38FF  <br/> |Anlageneigenschaften  <br/> |
|3900 - 39FF  <br/> |Adressbucheigenschaften  <br/> |
|3A00 - 3BFF  <br/> |Messaging-Benutzereigenschaften  <br/> |
|3C00 - 3CFF  <br/> |Verteilerlisteneigenschaften  <br/> |
|3D00 - 3DFF  <br/> |Profileigenschaften  <br/> |
|3E00 - 3FFF  <br/> |Status-Objekteigenschaften  <br/> |
   

