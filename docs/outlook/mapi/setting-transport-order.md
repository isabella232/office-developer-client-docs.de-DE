---
title: Festlegen der Transportreihenfolge
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4a140ec3-9520-4119-a975-0fb6c1049967
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: dc1ead1b58ed92c67ffba888ee19b589eee6de3f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566689"
---
# <a name="setting-transport-order"></a>Festlegen der Transportreihenfolge

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der MAPI-Spooler weist die Verantwortung für ausgehende Nachrichten basierend auf den Adresstypen und Bezeichnern zu, die Transportanbieter deklarieren, dass sie sie verarbeiten können. Transportanbieter veröffentlichen eine Liste der unterstützten Adresstypen und Bezeichner , die in **MAPIUID-Strukturen** gespeichert sind, wenn MAPI ihre [IXPLogon::AddressTypes-Methode](ixplogon-addresstypes.md) direkt nach der Anmeldung aufruft. Der Adresstyp eines Empfängers wird in seiner **PR_ADDRTYPE** -[PidTagAddressType](pidtagaddresstype-canonical-property.md)) -Eigenschaft gespeichert.
  
Die Registrierung für einen Adresstyp gibt der MAPI an, dass der Transportanbieter Empfängern übermitteln kann, deren **PR_ADDRTYPE** Eigenschaft auf den registrierten Adresstyp festgelegt ist. Entsprechend bedeutet die Registrierung für eine **MAPIUID,** dass der Transportanbieter An Empfänger liefern kann, die durch Eintragsbezeichner mit der registrierten **MAPIUID** dargestellt werden.
  
Die meisten Transportanbieter registrieren sich für einen oder mehrere Adresstypen. einige Registrieren von **MAPIUID**. Transportanbieter, die eng mit einem Adressbuchanbieter gekoppelt sind und dessen Eintragsbezeichnerformat verstehen, können sich registrieren, um Nachrichten von **MAPIUID** zu verarbeiten, wodurch die Leistung verbessert wird. Diese eng gekoppelten Transportanbieter können die E-Mail-Adresse des Empfängers und andere erforderliche Informationen aus dem Eintragsbezeichner extrahieren, ohne sie mit einem **IMAPISupport::OpenEntry-Aufruf** öffnen zu müssen. 
  
MAPI verwaltet eine Bestellung für Transportanbieter, die verwendet wird, wenn sich mehrere Transportanbieter für denselben Adresstyp oder **MAPIUID** registriert haben. Sie können diese Reihenfolge überschreiben, indem Sie [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) aufrufen und eine sortierte Liste der **MAPIUID-Elemente** aller aktiven Transportanbieter übergeben, auf die durch den  _lpUIDList-Parameter_ verwiesen wird: 
  
Rufen Sie ZUM Abrufen einer Liste aller Adresstypen, die von einem der aktiven Transportanbieter verarbeitet werden können, [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md)auf. **EnumAdrTypes** gibt ein Array von Zeichenfolgen zurück, die Adresstypen beschreiben, die von den Transportanbietern unterstützt werden, die in der aktuellen Sitzung aktiv sind. 
  

