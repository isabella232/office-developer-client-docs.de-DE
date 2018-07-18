---
title: Eigenschaftenbezeichnerbereiche
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c01e95bb-be25-490d-880b-60674f890258
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: aee199cbbd05606d20378023f103fa122f1457f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795320"
---
# <a name="property-identifier-ranges"></a>Eigenschaftenbezeichnerbereiche

  
  
**Betrifft**: Outlook 
  
In der folgenden Tabelle sind die unterschiedlichen Bereiche für Eigenschaftenbezeichner, zur Beschreibung des Besitzers für die Eigenschaften im jeweiligen Bereich zusammengefasst.
  
|**ID-Bereich**|**Beschreibung**|
|:-----|:-----|
|0000  <br/> |MAPI vorbehalten für den speziellen Wert **PR_NULL**.  <br/> |
|0001 - 0BFF  <br/> |Briefumschlag Nachrichteneigenschaften MAPI definiert.  <br/> |
|0C 00 - 0DFF  <br/> |Empfängereigenschaften MAPI definiert.  <br/> |
|0E00 - 0FFF  <br/> |Nicht-Übertragungseinehit Nachrichteneigenschaften MAPI definiert.  <br/> |
|1000 - 2FFF  <br/> |Content Nachrichteneigenschaften MAPI definiert.  <br/> |
|3000 - 3FFF  <br/> |Eigenschaften für Objekte, die keine Nachrichten und Empfänger MAPI definiert.  <br/> |
|4000 - 57FF  <br/> |Briefumschlag Nachrichteneigenschaften von Anbietern Transport definiert.  <br/> |
|5800 - 5FFF  <br/> |Empfängereigenschaften von Anbietern für Transport- und Address Book definiert.  <br/> |
|6000 - 65FF  <br/> |Nicht-Übertragungseinehit Nachrichteneigenschaften durch Clients definiert.  <br/> |
|6600 - 67FF  <br/> |Nicht-Übertragungseinehit von einem Dienstanbieter definierten Eigenschaften. Diese Eigenschaften können für Benutzer sichtbar oder ausgeblendet werden.  <br/> |
|6800 - 7BFF  <br/> |Content Nachrichteneigenschaften für benutzerdefinierte Nachrichtenklassen vom Ersteller dieser Klassen definiert.  <br/> |
|7C 00 - 7FFF  <br/> |Nicht-Übertragungseinehit Eigenschaften für benutzerdefinierte Nachrichtenklassen vom Ersteller dieser Klassen definiert.  <br/> |
|8000 - FFFE  <br/> |Eigenschaften von Clients definiert und gelegentlich-Dienstanbieter, die über die Methoden [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) und [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) namentlich identifiziert werden.  <br/> |
|FFFF  <br/> |MAPI vorbehalten für den speziellen Fehlerwert PROP_ID_INVALID.  <br/> |
   
Der Bereich zwischen 3000 und 3FFF für Eigenschaften, die keine Nachrichten oder Empfänger im Zusammenhang mit reserviert ist. MAPI unterteilt dieses Bereichs in untergeordneten Bereiche von Objekttypen. Die folgende Tabelle zeigt diese weitere Aufschlüsselung. 
  
|**ID-Bereich**|**Typ der Eigenschaft**|
|:-----|:-----|
|3000 - 33FF.  <br/> |Allgemeine Eigenschaften, die bei mehreren Objekten wie **PR_DISPLAY_NAME** und **PR_ENTRYID**angezeigt werden.  <br/> |
|3400 - 35FF  <br/> |Eigenschaften des Nachrichtenspeichers  <br/> |
|3600 - 36FF  <br/> |Ordner und Adressbucheinträge Containereigenschaften  <br/> |
|3700 - 38FF.  <br/> |Eigenschaften für Dateianlage  <br/> |
|3900 - 39FF  <br/> |Adressbucheigenschaften  <br/> |
|3A00 - 3BFF  <br/> |Messaging-Benutzereigenschaften  <br/> |
|3 C 00 - 3CFF  <br/> |Eigenschaften von Verteilerlisten  <br/> |
|3D 00 - 3DFF  <br/> |Profileigenschaften  <br/> |
|3E00 - 3FFF  <br/> |Status-Objekteigenschaften  <br/> |
   

