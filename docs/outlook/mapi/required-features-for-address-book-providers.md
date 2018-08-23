---
title: Erforderliche Funktionen für Adressbuchanbieter
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e2ccddd7-65e8-41f6-8e21-a4ae98190a96
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 919b21490bb3b4418ba291e8e06198028c995b00
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570871"
---
# <a name="required-features-for-address-book-providers"></a>Erforderliche Funktionen für Adressbuchanbieter

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Von adressbuchanbietern implementierte können mit Empfängerinformationen arbeiten, die temporäre oder permanente, lokale oder remote, eine oder mehrere Messagingsystemen verständlich und formatierte für eine Tabelle Datenträger, Datei oder Datenbank befinden. Es gibt eine Vielzahl von Features, die ein Adressbuchanbieter implementiert werden kann, wodurch Mehrwert und Verbessern der Interoperabilität mit Clients und andere Anbieter. Einige Features sind jedoch erforderlich.
  
In der folgenden Tabelle beschreibt die Features, die von allen adressbuchanbietern implementierte erforderlich sind, und die Schritte, die Sie durchführen, um diese zu implementieren müssen.
  
|**Funktion**|**Gewusst wie: Implementieren**|
|:-----|:-----|
|Sitzung anmelden  <br/> | Implementieren Sie eine Eintrag Point-Funktion. Weitere Informationen finden Sie unter [Implementieren einer Adresse Adressbuch Anbieter Eintrag Point-Funktion](implementing-an-address-book-provider-entry-point-function.md).  <br/>  Implementieren Sie die [IABProvider::Logon](iabprovider-logon.md) -Methode. Weitere Informationen finden Sie unter [implementieren Address Book Anbieter an- und Abmelden](implementing-address-book-provider-logon-and-logoff.md).  <br/> |
|Sitzung abmelden  <br/> |Implementieren Sie die [IABProvider::Shutdown](iabprovider-shutdown.md) -Methode. Weitere Informationen finden Sie unter [implementieren Address Book Anbieter an- und Abmelden](implementing-address-book-provider-logon-and-logoff.md).  <br/> |
|Erstellen von Eintragsbezeichner  <br/> |Bieten Sie Unterstützung für die Eigenschaft **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). Weitere Informationen finden Sie unter [MAPI-Eintragsbezeichner](mapi-entry-identifiers.md) und [Address Book-Bezeichner](address-book-identifiers.md).  <br/> |
|Beitrag zu der Tabelle "Status"  <br/> | Implementieren Sie die entsprechenden Methoden für die [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) Schnittstelle. Weitere Informationen finden Sie unter [Implementierung der Status-Objekts](status-object-implementation.md).  <br/>  Unterstützt die erforderlichen Status Tabelleneigenschaften. Weitere Informationen finden Sie unter [Statustabellen](status-tables.md).  <br/>  Rufen Sie [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md).  <br/> |
|Begrenzte Status Objekt unterstützen  <br/> | Implementieren Sie die [IMAPIStatus::ValidateState](imapistatus-validatestate.md) -Methode.  <br/>  MAPI_E_NO_SUPPORT aus anderen **IMAPIStatus** Methoden zurück.  <br/> |
|Interaktive und programmgesteuerte Unterstützung-Konfiguration  <br/> | Implementieren Sie eine Nachricht Service Entry Point-Funktion.  <br/>  Implementieren einer Tabelle anzeigen. Weitere Informationen finden Sie unter [Display Tables](display-tables.md) und [Implementierung der Anzeige-Tabelle](display-table-implementation.md).  <br/>  Implementieren eines Eigenschaftenblatts oder die [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) -Methode aufrufen. Weitere Informationen finden Sie unter [Implementierung von Eigenschaften Blatt](property-sheet-implementation.md).  <br/> |
   
Wenn der Anbieter Empfänger erstellen unterstützt, müssen Sie eine Liste der Erstellung Vorlagen angeben. Geben Sie dieser Liste durch die Implementierung der [GetOneOffTable](iablogon-getoneofftable.md) Methode, um alle Vorlagen, die von Ihrem Anbieter und die [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode des jeden Container zum Öffnen der **PR_CREATE_TEMPLATES** ([ unterstützt PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md))-Eigenschaft und enthalten alle Vorlagen, die vom Container unterstützt. Weitere Informationen finden Sie unter [Implementieren der einmaligen Tabellen](implementing-one-off-tables.md).
  

