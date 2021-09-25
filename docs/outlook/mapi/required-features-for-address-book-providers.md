---
title: Erforderliche Features für Adressbuchanbieter
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e2ccddd7-65e8-41f6-8e21-a4ae98190a96
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1ef6075ec05a7272d2657544d5ea89ca5a04d1e9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578788"
---
# <a name="required-features-for-address-book-providers"></a>Erforderliche Features für Adressbuchanbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Adressbuchanbieter können mit Empfängerinformationen arbeiten, die temporär oder dauerhaft, lokal oder remote sind, von einem oder mehreren Messagingsystemen verstanden und für eine Datenträgerdatei oder Datenbanktabelle formatiert sind. Es gibt eine Vielzahl von Features, die ein Adressbuchanbieter implementieren kann, wodurch mehrwertiger wird und die Interoperabilität mit Clients und anderen Anbietern verbessert wird. Es sind jedoch einige Features erforderlich.
  
In der folgenden Tabelle werden die Features beschrieben, die von allen Adressbuchanbietern benötigt werden, sowie die Schritte, die Sie zur Implementierung ausführen müssen.
  
|**Feature**|**Implementierung**|
|:-----|:-----|
|Sitzungsanmeldung  <br/> | Implementieren sie eine Einstiegspunktfunktion. Weitere Informationen finden Sie unter [Implementieren einer Adressbuchanbieter-Einstiegspunktfunktion.](implementing-an-address-book-provider-entry-point-function.md)  <br/>  Implementieren Sie die [IABProvider::Logon-Methode.](iabprovider-logon.md) Weitere Informationen finden Sie unter [Implementieren der Adressbuchanbieteranmeldung und -abmeldung.](implementing-address-book-provider-logon-and-logoff.md)  <br/> |
|Sitzungsanmeldung  <br/> |Implementieren Sie die [IABProvider::Shutdown-Methode.](iabprovider-shutdown.md) Weitere Informationen finden Sie unter [Implementieren der Adressbuchanbieteranmeldung und -abmeldung.](implementing-address-book-provider-logon-and-logoff.md)  <br/> |
|Erstellen von Eintragsbezeichnern  <br/> |Stellen Sie Unterstützung für die **eigenschaft PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) bereit. Weitere Informationen finden Sie unter [MAPI-Eintragsbezeichner](mapi-entry-identifiers.md) und [Adressbuchbezeichner.](address-book-identifiers.md)  <br/> |
|Zur Statustabelle beitragen  <br/> | Implementieren Sie die entsprechenden Methoden der [IMAPIStatus : IMAPIProp-Schnittstelle.](imapistatusimapiprop.md) Weitere Informationen finden Sie unter [Status Object Implementation](status-object-implementation.md).  <br/>  Unterstützen Sie die erforderlichen Statustabelleneigenschaften. Weitere Informationen finden Sie unter [Statustabellen.](status-tables.md)  <br/>  Rufen Sie [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md)auf.  <br/> |
|Bereitstellen der Unterstützung für eingeschränkte Statusobjekt  <br/> | Implementieren Sie die [IMAPIStatus::ValidateState-Methode.](imapistatus-validatestate.md)  <br/>  Gibt MAPI_E_NO_SUPPORT von den anderen **IMAPIStatus-Methoden** zurück.  <br/> |
|Unterstützen der interaktiven und programmgesteuerten Konfiguration  <br/> | Implementieren Sie eine Nachrichtendienst-Einstiegspunktfunktion.  <br/>  Implementieren sie eine Anzeigetabelle. Weitere Informationen finden Sie unter ["Anzeigetabellen"](display-tables.md) und ["Display Table"-Implementierung.](display-table-implementation.md)  <br/>  Implementieren Sie ein Eigenschaftenblatt, oder rufen Sie die [IMAPISupport::D oConfigPropsheet-Methode](imapisupport-doconfigpropsheet.md) auf. Weitere Informationen finden Sie unter [Property Sheet-Implementierung.](property-sheet-implementation.md)  <br/> |
   
Wenn Ihr Anbieter außerdem die Erstellung von Empfängern unterstützt, müssen Sie eine Liste der Erstellungsvorlagen angeben. Stellen Sie diese Liste bereit, indem Sie die [IABLogon::GetOneOffTable-Methode](iablogon-getoneofftable.md) implementieren, um alle vorlagen einzuschließen, die von Ihrem Anbieter unterstützt werden, und die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) jedes Containers, um die **eigenschaft PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) zu öffnen und alle vom Container unterstützten Vorlagen einzuschließen. Weitere Informationen finden Sie unter [Implementieren von One-Off Tabellen.](implementing-one-off-tables.md)
  

