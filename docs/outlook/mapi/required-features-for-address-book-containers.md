---
title: Erforderliche Features für Adressbuchcontainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 3e221944-5dc9-4cce-8b47-73af84427aea
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 71a8a6ae48bd9da08eb9cf0cb6dad7b6fde7c129
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609663"
---
# <a name="required-features-for-address-book-containers"></a>Erforderliche Features für Adressbuchcontainer

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die meisten Adressbuchanbieter unterstützen mindestens einen Container, von dem einige modifizierbar sind. Adressbuchcontainer können Inhalte und Hierarchietabellen, Suchfunktionen und Namensauflösung bereitstellen. Modifiierbare Container ermöglichen das Löschen von Einträgen wie Messagingbenutzern, Verteilerlisten oder anderen Containern sowie das Hinzufügen von Einträgen aus Einträgen in anderen Containern oder aus einmaligen Vorlagen.
  
In der folgenden Tabelle werden features beschrieben, die von Adressbuchanbietern mit Containern benötigt werden, die modifizierbar oder schreibgeschützt sind, und wie Sie diese implementieren.
  
|**Feature**|**Implementierung**|
|:-----|:-----|
|Zugreifen auf Messaging-Benutzer  <br/> |Implementieren Sie die [IABLogon::OpenEntry-Methode.](iablogon-openentry.md) Weitere Informationen finden Sie unter Öffnen von [Adressbucheinträgen.](opening-address-book-entries.md)  <br/> |
|Vergleichen von Messagingbenutzern  <br/> |Implementieren Sie die [IABLogon::CompareEntryIDs-Methode.](iablogon-compareentryids.md) Weitere Informationen finden Sie unter [Vergleichen von Adressbucheinträgen.](comparing-address-book-entries.md)  <br/> |
|Erstellen von Messagingbenutzern  <br/> |1. Stellen Sie eine Liste der Erstellungsvorlagen in einer einmaligen Tabelle bereit, indem Sie die **Eigenschaft PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) unterstützen. Weitere Informationen finden Sie unter [Implementieren eines Containers One-Off Tabelle](implementing-a-container-one-off-table.md).  <br/> 2. Implementieren Sie die [IABContainer::CreateEntry-Methode.](iabcontainer-createentry.md) Weitere Informationen finden Sie unter [Hinzufügen von Adressbucheinträgen.](adding-address-book-entries.md)  <br/> |
|Kopieren von Messagingbenutzern  <br/> |Implementieren Sie die [IABContainer::CopyEntries-Methode.](iabcontainer-copyentries.md) Weitere Informationen finden Sie unter [Kopieren von Adressbucheinträgen.](copying-address-book-entries.md)  <br/> |
|Entfernen von Messagingbenutzern  <br/> |Implementieren Sie die [IABContainer::D eleteEntries-Methode.](iabcontainer-deleteentries.md) Weitere Informationen finden Sie unter [Entfernen von Adressbucheinträgen.](removing-address-book-entries.md)  <br/> |
|Bereitstellen von zusammenfassenden Informationen zu Messagingbenutzern  <br/> |Unterstützen der Containereigenschaft **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)). For more information, see [Inhalt von Tabellen](contents-tables.md).  <br/> |
|Bereitstellen detaillierter Informationen zu Messagingbenutzern  <br/> |Unterstützen Sie die **Eigenschaft PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) für Messagingbenutzer und Verteilerlisten. Weitere Informationen finden Sie unter [Anzeigen von Empfängerinformationen](displaying-recipient-information.md) und [Anzeigetabellen.](display-tables.md)  <br/> |
|Bereitstellen detaillierter Informationen zu einem Container  <br/> |Unterstützen Sie die **PR_DETAILS_TABLE-Eigenschaft** für den Container. Weitere Informationen finden Sie unter [Anzeigen von Empfängerinformationen](displaying-recipient-information.md) und [Anzeigetabellen.](display-tables.md)  <br/> |
|Bereitstellen einer hierarchischen Liste von Containern  <br/> |Unterstützen der Containereigenschaft **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)). Weitere Informationen finden Sie unter [Hierarchietabellen.](hierarchy-tables.md)  <br/> |
|Unterstützen von Messaging-Benutzereigenschaften  <br/> |Implementieren Sie die [IMailUser : IMAPIProp-Schnittstelle.](imailuserimapiprop.md)  <br/> |
|Auflösen nicht eindeutiger Namen  <br/> | Unterstützen Der **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) Eigenschaftseinschränkung.  <br/>  Optional implementieren Sie die [IABContainer::ResolveNames-Methode.](iabcontainer-resolvenames.md) For more information, see [Implementieren der Namensaufl�sung](implementing-name-resolution.md).  <br/> |
   

