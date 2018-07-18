---
title: Erforderliche Funktionen für Adressbuchcontainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3e221944-5dc9-4cce-8b47-73af84427aea
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5eeaa9a8c1965954ad2eb0a6bfd2a174a355f10d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795390"
---
# <a name="required-features-for-address-book-containers"></a>Erforderliche Funktionen für Adressbuchcontainer

  
  
**Betrifft**: Outlook 
  
Die meisten adressbuchanbietern implementierte unterstützt mindestens einen Container, einige von ihnen geändert werden. Address Book Containern können Inhalt und Hierarchietabellen, Funktionen für die Suche und Auflösung angeben. Änderbare Container ermöglichen das Löschen der Einträge wie messaging-Benutzern, Verteilerlisten, oder andere Container und das Hinzufügen von Einträgen von Einträgen in andere Container oder von einmal-Vorlagen.
  
Die folgende Tabelle beschreibt die Features, die von adressbuchanbietern implementierte erforderlich sind, die Container geändert werden oder schreibgeschützt, und wie Sie sie implementieren.
  
|**Funktion**|**Gewusst wie: Implementieren**|
|:-----|:-----|
|Access-messaging-Benutzer  <br/> |Implementieren Sie die [IABLogon::OpenEntry](iablogon-openentry.md) -Methode. Weitere Informationen finden Sie unter [Öffnen von Adressbucheinträgen](opening-address-book-entries.md).  <br/> |
|Vergleichen von messaging-Benutzer  <br/> |Implementieren Sie die [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) -Methode. Weitere Informationen finden Sie unter [Vergleich von Adressbucheinträgen](comparing-address-book-entries.md).  <br/> |
|Erstellen von messaging-Benutzer  <br/> |1. Stellen Sie eine Liste der Erstellung von Vorlagen in einer einmaligen Tabelle durch die Unterstützung der **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md))-Eigenschaft. Weitere Informationen finden Sie unter [Implementieren einer einmaligen Container-Tabelle](implementing-a-container-one-off-table.md).  <br/> 2. implementieren Sie die [IABContainer::CreateEntry](iabcontainer-createentry.md) -Methode. Weitere Informationen finden Sie unter [Hinzufügen von Adressbucheinträgen](adding-address-book-entries.md).  <br/> |
|Kopieren von messaging-Benutzer  <br/> |Implementieren Sie die [IABContainer::CopyEntries](iabcontainer-copyentries.md) -Methode. Weitere Informationen finden Sie unter [Adressbucheinträge kopieren](copying-address-book-entries.md).  <br/> |
|Entfernen von messaging-Benutzer  <br/> |Implementieren Sie die [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) -Methode. Weitere Informationen finden Sie unter [Entfernen von Adressbucheinträgen](removing-address-book-entries.md).  <br/> |
|Bereitstellen Sie zusammenfassende Informationen zu Benutzern messaging  <br/> |Unterstützen Sie die Containereigenschaft **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)). For more information, see [Inhalt von Tabellen](contents-tables.md).  <br/> |
|Enthalten Sie detaillierte Informationen zu Benutzern messaging  <br/> |Unterstützen Sie die **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))-Eigenschaft auf messaging-Benutzer und Verteilerlisten. Weitere Informationen finden Sie unter [Anzeigen von Empfängerinformationen](displaying-recipient-information.md) und [Anzeige Tabellen](display-tables.md).  <br/> |
|Enthalten Sie detaillierte Informationen zu einem container  <br/> |Unterstützt die **PR_DETAILS_TABLE** -Eigenschaft für den Container an. Weitere Informationen finden Sie unter [Anzeigen von Empfängerinformationen](displaying-recipient-information.md) und [Anzeige Tabellen](display-tables.md).  <br/> |
|Stellen Sie eine hierarchische Liste der Container  <br/> |Unterstützen Sie die Containereigenschaft **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)). Weitere Informationen finden Sie unter [Hierarchietabellen](hierarchy-tables.md).  <br/> |
|Unterstützung von messaging-Benutzereigenschaften  <br/> |Implementieren der [IMailUser: IMAPIProp](imailuserimapiprop.md) Schnittstelle.  <br/> |
|Auflösen nicht eindeutiger Namen  <br/> | Unterstützung der eigenschaftseinschränkung **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)).  <br/>  Implementieren Sie optional die [IABContainer](iabcontainer-resolvenames.md) -Methode. For more information, see [Implementieren der Namensaufl�sung](implementing-name-resolution.md).  <br/> |
   

