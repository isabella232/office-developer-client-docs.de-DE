---
title: Eigenschaftenbezeichnerbereiche
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c01e95bb-be25-490d-880b-60674f890258
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cdf1eae945cddf9eb76a2b7a2532d5dc6568beac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422705"
---
# <a name="property-identifier-ranges"></a>Eigenschaftenbezeichnerbereiche

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In der folgenden Tabelle sind die verschiedenen Bereiche für Eigenschaftenbezeichner zusammengefasst, in denen der Besitzer für die Eigenschaften in den einzelnen Bereichen beschrieben wird.
  
|**Bezeichnerbereich**|**Beschreibung**|
|:-----|:-----|
|0000  <br/> |Reserviert von MAPI für den Sonderwert **PR_NULL**.  <br/> |
|0001 - 0BFF  <br/> |Von MAPI definierte Nachrichtenumschlageigenschaften.  <br/> |
|0C00 – 0DFF  <br/> |Von MAPI definierte Empfängereigenschaften.  <br/> |
|0E00 - 0FFF  <br/> |Nicht durchlässige Nachrichteneigenschaften, die von MAPI definiert werden.  <br/> |
|1000 – 2FFF  <br/> |Von MAPI definierte Nachrichteninhaltseigenschaften.  <br/> |
|3000 – 3FFF  <br/> |Eigenschaften für andere Objekte als Nachrichten und Empfänger, die von MAPI definiert sind.  <br/> |
|4000 – 57FF  <br/> |Nachrichtenumschlageigenschaften, die von Transportanbietern definiert werden.  <br/> |
|5800 – 5FFF  <br/> |Von Transport- und Adressbuchanbietern definierte Empfängereigenschaften.  <br/> |
|6000 – 65FF  <br/> |Nicht durchsetzbare Nachrichteneigenschaften, die von Clients definiert werden.  <br/> |
|6600 - 67FF  <br/> |Nicht durchlässige Eigenschaften, die von einem Dienstanbieter definiert werden. Diese Eigenschaften können für Benutzer sichtbar oder unsichtbar sein.  <br/> |
|6800 – 7BFF  <br/> |Nachrichteninhaltseigenschaften für benutzerdefinierte Nachrichtenklassen, die von erstellern dieser Klassen definiert werden.  <br/> |
|7C00 - 7FFF  <br/> |Nicht durchlässige Eigenschaften für benutzerdefinierte Nachrichtenklassen, die von erstellern dieser Klassen definiert werden.  <br/> |
|8000 – FFFE  <br/> |Von Clients und gelegentlich Dienstanbietern definierte Eigenschaften, die über die [Methoden IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) und [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) anhand des Namens identifiziert werden.  <br/> |
|FFFF  <br/> |Reserviert von MAPI für den speziellen Fehlerwert PROP_ID_INVALID.  <br/> |
   
Der Bereich zwischen 3000 und 3FFF ist für Eigenschaften reserviert, die nicht mit Nachrichten oder Empfängern in Zusammenhang stehen. MAPI teilt diesen Bereich nach Objekttypen in Unterbereiche auf. Die folgende Tabelle zeigt diese weitere Aufschlüsselung. 
  
|**Bezeichnerbereich**|**Typ der Eigenschaft**|
|:-----|:-----|
|3000 – 33FF  <br/> |Allgemeine Eigenschaften, die für mehrere Objekte angezeigt werden, z. **B. PR_DISPLAY_NAME** und **PR_ENTRYID**.  <br/> |
|3400 – 35FF  <br/> |Eigenschaften des Nachrichtenspeichers  <br/> |
|3600 – 36FF  <br/> |Eigenschaften von Ordner- und Adressbuchcontainern  <br/> |
|3700 - 38FF  <br/> |Anlageneigenschaften  <br/> |
|3900 - 39FF  <br/> |Adressbucheigenschaften  <br/> |
|3A00 - 3BFF  <br/> |Eigenschaften von Messagingbenutzern  <br/> |
|3C00 – 3CFF  <br/> |Eigenschaften der Verteilerliste  <br/> |
|3D00 – 3DFF  <br/> |Profileigenschaften  <br/> |
|3E00 - 3FFF  <br/> |Eigenschaften des Statusobjekts  <br/> |
   

