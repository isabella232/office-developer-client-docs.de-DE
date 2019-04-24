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
ms.openlocfilehash: abdbd9030e0ea053d39b49ecc76a78821be9df82
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328707"
---
# <a name="required-features-for-address-book-containers"></a>Erforderliche Funktionen für Adressbuchcontainer

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die meisten Adressbuchanbieter unterstützen mindestens einen Container, von denen einige geändert werden können. Adressbuchcontainer können Inhalts-und Hierarchietabellen, Suchfunktionen und Namensauflösung bereitstellen. Veränderbare Container ermöglichen das Löschen von Einträgen wie Messaging Benutzern, Verteilerlisten oder anderen Containern und das Hinzufügen von Einträgen aus Einträgen in anderen Containern oder aus einmaligen Vorlagen.
  
In der folgenden Tabelle werden die Features beschrieben, die von Adressbuch Anbietern benötigt werden, die über Container, veränderbare oder schreibgeschützte Objekte und ihre Implementierung verfügen.
  
|**Feature**|**VorGehensWeise**|
|:-----|:-----|
|Zugriff auf Messagingbenutzer  <br/> |Implementieren Sie die [IABLogon:: OpenEntry](iablogon-openentry.md) -Methode. Weitere Informationen finden Sie unter [Öffnen von Adressbucheinträgen](opening-address-book-entries.md).  <br/> |
|Vergleichen von Messaging Benutzern  <br/> |Implementieren Sie die [IABLogon:: CompareEntryIDs](iablogon-compareentryids.md) -Methode. Weitere Informationen finden Sie unter [Vergleichen von Adressbucheinträgen](comparing-address-book-entries.md).  <br/> |
|Erstellen von Messaging Benutzern  <br/> |1. Stellen Sie eine Liste der Erstellungsvorlagen in einer einmaligen Tabelle bereit, indem Sie die **PR_CREATE_TEMPLATES** ([pidtagcreatetemplates (](pidtagcreatetemplates-canonical-property.md))-Eigenschaft unterstützen. Weitere Informationen finden Sie unter [Implementieren einer Container-einmal Tabelle](implementing-a-container-one-off-table.md).  <br/> 2. implementieren Sie die [IABContainer:: CreateEntry](iabcontainer-createentry.md) -Methode. Weitere Informationen finden Sie unter [Hinzufügen von Adressbucheinträgen](adding-address-book-entries.md).  <br/> |
|Kopieren von Messaging Benutzern  <br/> |Implementieren Sie die [IABContainer:: CopyEntries](iabcontainer-copyentries.md) -Methode. Weitere Informationen finden Sie unter [Kopieren von Adressbucheinträgen](copying-address-book-entries.md).  <br/> |
|Entfernen von Messaging Benutzern  <br/> |Implementieren Sie die [IABContainer::D eleteentries](iabcontainer-deleteentries.md) -Methode. Weitere Informationen finden Sie unter [Entfernen von Adressbucheinträgen](removing-address-book-entries.md).  <br/> |
|Zusammenfassende Informationen zu Messaging Benutzern  <br/> |Unterstützung der Container-Eigenschaft **PR_CONTAINER_CONTENTS** ([pidtagcontainercontents (](pidtagcontainercontents-canonical-property.md)). For more information, see [Inhalt von Tabellen](contents-tables.md).  <br/> |
|Bereitstellen detaillierter Informationen zu Messaging Benutzern  <br/> |Unterstützung der **PR_DETAILS_TABLE** ([pidtagdetailstable (](pidtagdetailstable-canonical-property.md))-Eigenschaft für Messagingbenutzer und Verteilerlisten. Weitere Informationen finden Sie unter [Anzeigen von Empfängerinformationen](displaying-recipient-information.md) und [Anzeige Tabellen](display-tables.md).  <br/> |
|Bereitstellen detaillierter Informationen zu einem Container  <br/> |Unterstützen Sie die **PR_DETAILS_TABLE** -Eigenschaft des Containers. Weitere Informationen finden Sie unter [Anzeigen von Empfängerinformationen](displaying-recipient-information.md) und [Anzeige Tabellen](display-tables.md).  <br/> |
|Bereitstelleneiner hierarchischen Liste von Containern  <br/> |Unterstützung der Container-Eigenschaft **PR_CONTAINER_HIERARCHY** ([pidtagcontainerhierarchy (](pidtagcontainerhierarchy-canonical-property.md)). Weitere Informationen finden Sie unter [Hierarchietabellen](hierarchy-tables.md).  <br/> |
|Unterstützung für Messaging-Benutzereigenschaften  <br/> |Implementieren Sie die [IMailUser: IMAPIProp](imailuserimapiprop.md) -Schnittstelle.  <br/> |
|AufLösen von mehrdeutigen Namen  <br/> | Unterstützung der **PR_ANR** ([pidtaganr (](pidtaganr-canonical-property.md))-Eigenschaftseinschränkung.  <br/>  Implementieren Sie optional die [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) -Methode. For more information, see [Implementieren der Namensaufl�sung](implementing-name-resolution.md).  <br/> |
   

