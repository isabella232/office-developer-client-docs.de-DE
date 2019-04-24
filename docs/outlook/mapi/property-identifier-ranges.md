---
title: Eigenschaftenbezeichner Bereiche
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c01e95bb-be25-490d-880b-60674f890258
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: cdf1eae945cddf9eb76a2b7a2532d5dc6568beac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328532"
---
# <a name="property-identifier-ranges"></a>Eigenschaftenbezeichner Bereiche

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In der folgenden Tabelle sind die verschiedenen Bereiche für Eigenschaftsbezeichner zusammengefasst, die den Besitzer für die Eigenschaften in den einzelnen Bereichen beschreiben.
  
|**Bezeichnerbereich**|**Beschreibung**|
|:-----|:-----|
|0000  <br/> |Von MAPI für den speziellen Wert **PR_NULL**reserviert.  <br/> |
|0001-0BFF  <br/> |Von MAPI definierte Nachrichtenumschlag Eigenschaften.  <br/> |
|0C00-0DFF  <br/> |Von MAPI definierte Empfänger Eigenschaften.  <br/> |
|0E00-0FFF  <br/> |Nicht übertragbare Nachrichteneigenschaften, die von MAPI definiert werden.  <br/> |
|1000-2FFF  <br/> |Von MAPI definierte Nachrichteninhalts Eigenschaften.  <br/> |
|3000-3FFF  <br/> |Eigenschaften für andere Objekte als Nachrichten und Empfänger, die von MAPI definiert wurden.  <br/> |
|4000-57FF  <br/> |Nachrichtenumschlag Eigenschaften, die von Transportanbietern definiert werden.  <br/> |
|5800-5FFF  <br/> |Empfänger Eigenschaften, die von Transport-und Adressbuch Anbietern definiert werden.  <br/> |
|6000-65FF  <br/> |Nicht übertragbare Nachrichteneigenschaften, die von Clients definiert werden.  <br/> |
|6600-67FF  <br/> |Nicht übertragbare Eigenschaften, die von einem Dienstanbieter definiert werden. Diese Eigenschaften können für Benutzer sichtbar oder unsichtbar sein.  <br/> |
|6800-7BFF  <br/> |Nachrichteninhalts Eigenschaften für benutzerdefinierte Nachrichtenklassen, die von Erstellern dieser Klassen definiert werden.  <br/> |
|7C00-7FFF  <br/> |Nicht übertragbare Eigenschaften für benutzerdefinierte Nachrichtenklassen, die von Erstellern dieser Klassen definiert werden.  <br/> |
|8000-FFFE  <br/> |Von Clients und gelegentlichen Dienstanbietern definierte Eigenschaften, die über die [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) -und [IMAPIProp: GetIDsFromNames](imapiprop-getidsfromnames.md) -Methoden anhand des Namens identifiziert werden.  <br/> |
|FFFF  <br/> |Von MAPI für den speziellen Fehlerwert PROP_ID_INVALID reserviert.  <br/> |
   
Der Bereich zwischen 3000 und 3FFF ist für Eigenschaften reserviert, die sich nicht auf Nachrichten oder Empfänger beziehen. MAPI teilt diesen Bereich nach Objekttypen in Unterbereiche auf. die folgende Tabelle zeigt diese weitere Aufteilung. 
  
|**Bezeichnerbereich**|**Typ der Eigenschaft**|
|:-----|:-----|
|3000-33FF  <br/> |Allgemeine Eigenschaften, die für mehrere Objekte wie **PR_DISPLAY_NAME** und **PR_ENTRYID**angezeigt werden.  <br/> |
|3400-35FF  <br/> |Nachrichtenspeichereigenschaften  <br/> |
|3600-36FF  <br/> |Container Eigenschaften für Ordner und Adressbuch  <br/> |
|3700-38FF  <br/> |Attachment-Eigenschaften  <br/> |
|3900-39FF  <br/> |Adressbucheigenschaften  <br/> |
|3A00-3BFF  <br/> |Eigenschaften für Messaging-Benutzer  <br/> |
|3C00-3CFF  <br/> |Eigenschaften der Verteilerliste  <br/> |
|3D00-3DFF  <br/> |Profileigenschaften  <br/> |
|3E00-3FFF  <br/> |Eigenschaften des Status Objekts  <br/> |
   

