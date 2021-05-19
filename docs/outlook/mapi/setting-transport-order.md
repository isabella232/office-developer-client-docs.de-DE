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
ms.openlocfilehash: efa2d6ab9edbd50634093b5185ef9036689f1379
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433598"
---
# <a name="setting-transport-order"></a>Festlegen der Transportreihenfolge

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der MAPI-Spooler weist ausgehende Nachrichten basierend auf den Adresstypen und Bezeichnern zu, die von Transportanbietern für die Verarbeitung deklariert werden können. Transportanbieter veröffentlichen eine Liste der unterstützten Adresstypen und Bezeichner , die in **MAPIUID-Strukturen** gespeichert sind, wenn MAPI die [IXPLogon::AddressTypes-Methode](ixplogon-addresstypes.md) direkt nach der Anmeldung aufruft. Der Adresstyp eines Empfängers wird in seiner **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) gespeichert.
  
Die Registrierung für einen Adresstyp gibt für MAPI an, dass der Transportanbieter Empfänger mit seiner **PR_ADDRTYPE** auf den registrierten Adresstyp festlegen kann. Auf ähnliche Weise bedeutet die Registrierung für eine **MAPIUID,** dass der Transportanbieter Empfängern, die durch Eintragsbezeichner mit der registrierten **MAPIUID** dargestellt werden, liefern kann.
  
Die meisten Transportanbieter registrieren sich für einen oder mehrere Adresstypen. nur wenige registrieren sich bei **MAPIUID**. Transportanbieter, die eng mit einem Adressbuchanbieter gekoppelt sind und dessen Eingabebezeichnerformat verstehen, können sich registrieren, um Nachrichten von **MAPIUID** zu verarbeiten, wodurch die Leistung verbessert wird. Diese eng gekoppelten Transportanbieter können die E-Mail-Adresse des Empfängers und andere erforderliche Informationen aus der Eintrags-ID extrahieren, ohne sie mit einem **IMAPISupport::OpenEntry-Aufruf** öffnen zu müssen. 
  
MAPI verwaltet eine Bestellung für Transportanbieter, die verwendet wird, wenn mehrere Transportanbieter sich für denselben Adresstyp oder **mapIUID registriert haben.** Sie können diese Reihenfolge überschreiben, indem Sie [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) aufrufen und eine sortierte Liste der **MAPIUID** s aller aktiven Transportanbieter übergeben, auf die der  _lpUIDList-Parameter_ verweist.: 
  
Rufen Sie [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md)auf, um eine Liste aller Adresstypen abzurufen, die von einem der aktiven Transportanbieter verarbeitet werden können. **EnumAdrTypes** gibt ein Array von Zeichenfolgen zurück, das Adresstypen beschreibt, die von den Transportanbietern unterstützt werden, die in der aktuellen Sitzung aktiv sind. 
  

