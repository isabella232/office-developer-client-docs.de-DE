---
title: Erforderliche Features für Adressbuchcontainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3e221944-5dc9-4cce-8b47-73af84427aea
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: abdbd9030e0ea053d39b49ecc76a78821be9df82
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439681"
---
# <a name="required-features-for-address-book-containers"></a>Erforderliche Features für Adressbuchcontainer

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die meisten Adressbuchanbieter unterstützen mindestens einen Container, von dem einige änderbar sind. Adressbuchcontainer können Inhalts- und Hierarchietabellen, Suchfunktionen und Namensauflösung liefern. Modifizierbare Container ermöglichen das Löschen von Einträgen wie Messagingbenutzern, Verteilerlisten oder anderen Containern sowie das Hinzufügen von Einträgen aus Einträgen in anderen Containern oder aus einmal erstellten Vorlagen.
  
In der folgenden Tabelle werden features beschrieben, die für Adressbuchanbieter erforderlich sind, die Container, änderbar oder schreibgeschützt haben, und deren Implementierung.
  
|**Feature**|**Implementierung**|
|:-----|:-----|
|Zugreifen auf Messagingbenutzer  <br/> |Implementieren Sie [die IABLogon::OpenEntry-Methode.](iablogon-openentry.md) Weitere Informationen finden Sie unter [Opening Address Book Entries](opening-address-book-entries.md).  <br/> |
|Vergleichen von Messagingbenutzern  <br/> |Implementieren Sie [die IABLogon::CompareEntryIDs-Methode.](iablogon-compareentryids.md) Weitere Informationen finden Sie unter [Vergleichen von Adressbucheinträgen](comparing-address-book-entries.md).  <br/> |
|Erstellen von Messagingbenutzern  <br/> |1. Stellen Sie eine Liste der Erstellungsvorlagen in einer einmal erstellten Tabelle bereit, indem Sie die **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) -Eigenschaft unterstützen. Weitere Informationen finden Sie unter [Implementing a Container One-Off Table](implementing-a-container-one-off-table.md).  <br/> 2. Implementieren Sie die [IABContainer::CreateEntry-Methode.](iabcontainer-createentry.md) Weitere Informationen finden Sie unter [Hinzufügen von Adressbucheinträgen](adding-address-book-entries.md).  <br/> |
|Kopieren von Messagingbenutzern  <br/> |Implementieren Sie [die IABContainer::CopyEntries-Methode.](iabcontainer-copyentries.md) Weitere Informationen finden Sie unter [Kopieren von Adressbucheinträgen](copying-address-book-entries.md).  <br/> |
|Entfernen von Messagingbenutzern  <br/> |Implementieren Sie [die IABContainer::D eleteEntries-Methode.](iabcontainer-deleteentries.md) Weitere Informationen finden Sie unter [Entfernen von Adressbucheinträgen](removing-address-book-entries.md).  <br/> |
|Bereitstellen von Zusammenfassenden Informationen zu Messagingbenutzern  <br/> |Unterstützt die Containereigenschaft **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)). For more information, see [Inhalt von Tabellen](contents-tables.md).  <br/> |
|Bereitstellen detaillierter Informationen zu Messagingbenutzern  <br/> |Unterstützt die **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) -Eigenschaft für Messagingbenutzer und Verteilerlisten. Weitere Informationen finden Sie unter [Anzeigen von Empfängerinformationen und](displaying-recipient-information.md) [Anzeigetabellen](display-tables.md).  <br/> |
|Bereitstellen detaillierter Informationen zu einem Container  <br/> |Unterstützt die **PR_DETAILS_TABLE-Eigenschaft** für den Container. Weitere Informationen finden Sie unter [Anzeigen von Empfängerinformationen und](displaying-recipient-information.md) [Anzeigetabellen](display-tables.md).  <br/> |
|Bereitstellen einer hierarchischen Liste von Containern  <br/> |Unterstützt die Containereigenschaft **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)). Weitere Informationen finden Sie unter [Hierarchietabellen](hierarchy-tables.md).  <br/> |
|Unterstützen von Messagingbenutzereigenschaften  <br/> |Implementieren Sie [die IMailUser : IMAPIProp-Schnittstelle.](imailuserimapiprop.md)  <br/> |
|Auflösen nicht eindeutiger Namen  <br/> | Unterstützt die **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md))-Eigenschaftseinschränkung.  <br/>  Implementieren Sie optional die [IABContainer::ResolveNames-Methode.](iabcontainer-resolvenames.md) For more information, see [Implementieren der Namensaufl�sung](implementing-name-resolution.md).  <br/> |
   

