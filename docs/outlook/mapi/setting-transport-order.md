---
title: Festlegen des Transport Auftrags
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
# <a name="setting-transport-order"></a>Festlegen des Transport Auftrags

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der MAPI-Spooler weist die Verantwortung für ausgehende Nachrichten auf Grundlage der Adresstypen und Bezeichner zu, die von den Transportanbietern deklariert werden können. Transport Anbieter veröffentlichen eine Liste unterstützter Adresstypen und Bezeichner, die in **MAPIUID** -Strukturen gespeichert sind, wenn MAPI Ihre [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) -Methode direkt nach der Anmeldung aufruft. Der Adresstyp eines Empfängers wird in seiner **PR_ADDRTYPE** ([pidtagaddresstype (](pidtagaddresstype-canonical-property.md))-Eigenschaft gespeichert.
  
Die Registrierung für einen Adresstyp gibt MAPI an, dass der Transportanbieter an Empfänger senden kann, deren **PR_ADDRTYPE** -Eigenschaft auf den registrierten Adresstyp festgelegt ist. Entsprechend gibt die Registrierung für eine **MAPIUID** an, dass der Transportanbieter an Empfänger senden kann, die durch Eintrags-IDs mit der registrierten **MAPIUID**dargestellt werden.
  
Die meisten Transportanbieter registrieren für einen oder mehrere Adresstypen; wenige Register von **MAPIUID**. Transport Anbieter, die eng mit einem Adressbuchanbieter verbunden sind und dessen Eintrags-ID-Format verstehen, können sich registrieren, um Nachrichten von **MAPIUID**zu verarbeiten und dadurch die Leistung zu verbessern. Diese eng gekoppelten Transportanbieter können die e-Mail-Adresse des Empfängers und andere erforderliche Informationen aus der Eintrags-ID extrahieren, ohne Sie mit einem **IMAPISupport:: OpenEntry** -Aufruf öffnen zu müssen. 
  
MAPI verwaltet eine Bestellung für Transportanbieter, die verwendet wird, wenn mehrere Transportanbieter für denselben Adresstyp oder **MAPIUID**registriert haben. Sie können diese Reihenfolge überschreiben, indem Sie [IMsgServiceAdmin:: MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) aufrufen und eine sortierte Liste der **MAPIUID**s aller aktiven Transportanbieter übergeben, auf die durch den _lpUIDList_ -Parameter verwiesen wird: 
  
Um eine Liste aller Adresstypen abzurufen, die von einem der aktiven Transportanbieter verarbeitet werden können, rufen Sie [IMAPISession:: EnumAdrTypes](imapisession-enumadrtypes.md)auf. **EnumAdrTypes** gibt ein Array von Zeichenfolgen zurück, in denen Adresstypen beschrieben werden, die von den Transportanbietern unterstützt werden, die in der aktuellen Sitzung aktiv sind. 
  

