---
title: Festlegen der Transportreihenfolge
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4a140ec3-9520-4119-a975-0fb6c1049967
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6e4c318678fdce7976140ff8f480ae638fd3ca4c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593025"
---
# <a name="setting-transport-order"></a>Festlegen der Transportreihenfolge

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Die MAPI-Warteschlange weist die Verantwortung für ausgehende Nachrichten basierend auf der Adresstypen und Bezeichner, die Transportanbieter deklarieren, dass sie verarbeiten können. Transportanbieter veröffentlichen Sie eine Liste der unterstützten Adresstypen und Bezeichner – gespeichert in **MAPIUID** Strukturen – Wenn MAPI ihre [IXPLogon::AddressTypes](ixplogon-addresstypes.md) -Methode aufruft, direkt nach der Anmeldung. Typ der Adresse des Empfängers wird in seiner **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))-Eigenschaft gespeichert.
  
Registrieren Sie sich für einen Adresstyp gibt an, MAPI, dass der Adressbuchhierarchie mit ihrer **PR_ADDRTYPE** -Eigenschaft, um den registrierten Adresstyp an Empfänger senden kann. Registrieren für eine **MAPIUID** gibt entsprechend an, dass der Adressbuchhierarchie an Empfänger übermitteln kann, die von Eintragsbezeichner mit der registrierten **MAPIUID**dargestellt werden.
  
Die meisten Transportanbieter registrieren Sie sich für eine oder mehrere Adresstypen; wenige registrieren, indem Sie **MAPIUID**. Transport-Anbietern, die sind eng mit einer Adressbuchanbieter gekoppelt und Grundlegendes zu seinem Eintrags-ID-Format, können zur Verarbeitung von Nachrichten durch **MAPIUID**, wodurch die Leistung gesteigert registrieren. Diese Transportanbieter eng gekoppelten können die e-Mail-Adresse des Empfängers und andere erforderliche Informationen aus der Eintrags-ID ohne es mit einem Anruf **IMAPISupport::OpenEntry** öffnen extrahieren. 
  
MAPI verwaltet einen Auftrag für Transportanbieter verwendet, wenn mehrere Transportanbieter für den gleichen Adresstyp oder **MAPIUID**registriert haben. Sie können diesen Auftrag außer Kraft setzen, durch Aufrufen von [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) und übergeben eine geordnete Liste von die s **MAPIUID**, der alle aktiven Transportanbieter auf den durch den Parameter _LpUIDList_ verwiesen.: 
  
Rufen Sie zum Abrufen einer Liste aller von einem Anbieter für die aktiven Transport behandelt werden können Adresstypen [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md). **EnumAdrTypes** gibt ein Array von Zeichenfolgen, die beschreibt Adresstypen unterstützt der Transport-Anbieter, die in der aktuellen Sitzung aktiv sind. 
  

