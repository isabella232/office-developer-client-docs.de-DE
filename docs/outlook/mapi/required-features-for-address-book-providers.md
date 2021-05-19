---
title: Erforderliche Features für Adressbuchanbieter
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e2ccddd7-65e8-41f6-8e21-a4ae98190a96
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 56ca15440c8d323dbab1b6a92a01941106b86934
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421396"
---
# <a name="required-features-for-address-book-providers"></a>Erforderliche Features für Adressbuchanbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Adressbuchanbieter können mit temporären oder dauerhaften, lokalen oder remoten Empfängerinformationen arbeiten, die für ein oder mehrere Messagingsysteme verständlich und für eine Datenträgerdatei oder Datenbanktabelle formatiert sind. Es gibt eine Vielzahl von Features, die ein Adressbuchanbieter implementieren kann, wodurch ein Mehrwert und die Interoperabilität mit Clients und anderen Anbietern verbessert wird. Es sind jedoch einige Features erforderlich.
  
In der folgenden Tabelle werden die Features beschrieben, die von allen Adressbuchanbietern benötigt werden, sowie die Schritte, die Sie zur Implementierung der Adressbuchanbieter ausführen müssen.
  
|**Feature**|**Implementierung**|
|:-----|:-----|
|Sitzungsanmeldung  <br/> | Implementieren Sie eine Einstiegspunktfunktion. Weitere Informationen finden Sie unter [Implementing an Address Book Provider Entry Point Function](implementing-an-address-book-provider-entry-point-function.md).  <br/>  Implementieren Sie [die IABProvider::Logon-Methode.](iabprovider-logon.md) Weitere Informationen finden Sie unter [Implementing Address Book Provider Logon and Logoff](implementing-address-book-provider-logon-and-logoff.md).  <br/> |
|Sitzungsanmeldung  <br/> |Implementieren Sie [die IABProvider::Shutdown-Methode.](iabprovider-shutdown.md) Weitere Informationen finden Sie unter [Implementing Address Book Provider Logon and Logoff](implementing-address-book-provider-logon-and-logoff.md).  <br/> |
|Erstellen von Eintragsbezeichnern  <br/> |Stellen Sie Unterstützung für **die PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft zur Verfügung. Weitere Informationen finden Sie unter [MAPI Entry Identifiers](mapi-entry-identifiers.md) and [Address Book Identifiers](address-book-identifiers.md).  <br/> |
|Beitrag zur Statustabelle  <br/> | Implementieren Sie die entsprechenden Methoden der [IMAPIStatus : IMAPIProp-Schnittstelle.](imapistatusimapiprop.md) Weitere Informationen finden Sie unter [Status Object Implementation](status-object-implementation.md).  <br/>  Unterstützt die erforderlichen Statustabelle-Eigenschaften. Weitere Informationen finden Sie unter [Status Tables](status-tables.md).  <br/>  Rufen [Sie IMAPISupport::ModifyStatusRow auf.](imapisupport-modifystatusrow.md)  <br/> |
|Bereitstellen von eingeschränkter Statusobjektunterstützung  <br/> | Implementieren Sie die [IMAPIStatus::ValidateState-Methode.](imapistatus-validatestate.md)  <br/>  Gibt MAPI_E_NO_SUPPORT von den anderen **IMAPIStatus-Methoden** zurück.  <br/> |
|Unterstützung der interaktiven und programmgesteuerten Konfiguration  <br/> | Implementieren Einer Nachrichtendienst-Einstiegspunktfunktion.  <br/>  Implementieren sie eine Anzeigetabelle. Weitere Informationen finden Sie unter [Display Tables](display-tables.md) and Display [Table Implementation](display-table-implementation.md).  <br/>  Implementieren Sie ein Eigenschaftenblatt, oder rufen Sie die [IMAPISupport::D oConfigPropsheet-Methode](imapisupport-doconfigpropsheet.md) auf. Weitere Informationen finden Sie unter [Property Sheet Implementation](property-sheet-implementation.md).  <br/> |
   
Wenn Ihr Anbieter die Erstellung von Empfängern unterstützt, müssen Sie außerdem eine Liste der Erstellungsvorlagen hinzufügen. Geben Sie diese Liste an, indem Sie die [IABLogon::GetOneOffTable-Methode](iablogon-getoneofftable.md) implementieren, um alle von Ihrem Anbieter unterstützten Vorlagen und die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) jedes Containers zum Öffnen der **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md))-Eigenschaft und alle vom Container unterstützten Vorlagen hinzuzufügen. Weitere Informationen finden Sie unter [Implementing One-Off Tables](implementing-one-off-tables.md).
  

